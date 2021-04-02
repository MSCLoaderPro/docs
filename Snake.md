# Snake

<style>
.snake-window {
    box-sizing: border-box;
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
    border: 0px solid #969696;
    background: #d9dbda;
    margin: 10px;
    position: relative;
}

.square {
    box-sizing: border-box;
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
    width: 1em;
    height: 1em;
    background: #000;
    position: absolute;
}

.head {
    z-index: 10;
    background: yellow;
}

.apple {
    background: red;
}

.score-box {
    text-align: left;
}

.score-box p {
    display: inline;
}

.important {
    font-weight: bold;
}
</style>

<div class="score-box">
    <p class="important">Score:</p>
    <p id="score">0</p>
    <p class="important">Best:</p>
    <p id="best">0</p>
</div>

<div class="snake-window" id="snake-window">
    <div class="square head" id="player"></div>
    <div class="square apple" id="apple"></div>
</div>

<script>

    async function gameLoop() {
        class SnakeBody {
            constructor(block, destroyAfterTicks, isDestroyed, x, y) {
                this.block = block;
                this.destroyAfterTicks = destroyAfterTicks;
                this.x = x;
                this.y = y;
            }
        }
        var map = document.getElementById("snake-window");
        const mapWidth = 10;
        const mapHeight = 10;

        // Keys.
        const keyLeft = 37;
        const keyUp = 38;
        const keyRight = 39;
        const keyDown = 40;
        const keyReset = 82;
        // Directions
        const directions = {
            LEFT: 0,
            UP: 1,
            RIGHT: 2,
            DOWN: 3,
        };

        // Player movement
        var player = document.getElementById("player");
        var playerX = (mapWidth / 2) - 1;
        var playerY = (mapHeight / 2) - 1;
        var direction = directions.LEFT;
        var lastDirection = direction;
        var snakeBlocks = [];

        // Apples
        var apple = document.getElementById("apple");
        var ticks = 0;
        var appleX;
        var appleY;

        // HUD and Scores
        var score = 0;
        var best = 0;
        var scoreHUD = document.getElementById("score");
        var bestHUD = document.getElementById("best");

        // Key listener.
        document.addEventListener('keydown', function(event) {
            if(event.keyCode == keyLeft && lastDirection != directions.RIGHT) {
                direction = directions.LEFT;
            }
            else if(event.keyCode == keyUp && lastDirection != directions.DOWN) {
                direction = directions.UP;
            }
            else if(event.keyCode == keyRight && lastDirection != directions.LEFT) {
                direction = directions.RIGHT;
            }
            else if(event.keyCode == keyDown && lastDirection != directions.UP) {
                direction = directions.DOWN;
            }
            else if(event.keyCode == keyReset) {
                resetGame();
            }
        });

        function setPosition(theElement, x, y) {
            theElement.style.left = `${Math.floor(x)}em`;
            theElement.style.top = `${Math.floor(y)}em`;
        }

        // SETTING UP THE GAME.
        function resetGame() {
            map.style.width = mapWidth + `em`;
            map.style.height = mapHeight + `em`;

            playerX = (mapWidth / 2) - 1;
            playerY = (mapHeight / 2) - 1;
            direction = directions.LEFT;

            if (score > best) {
                best = score;
                bestHUD.innerHTML = best;
            }

            setPosition(player, playerX, playerY);
            createNewApple();
            score = 0;
            updateScoreText();

            for (let i = 0; i < snakeBlocks.length; i++) {
                if (!snakeBlocks[i].isDestroyed) {
                    map.removeChild(snakeBlocks[i].block);
                }
            }
            snakeBlocks = [];
        }

        function isOutOfBounds() {
            return (playerX < 0) || (playerY < 0) || (playerX >= mapWidth) || (playerY >= mapHeight);
        }

        function isCollidingWithSnakeBody(x, y) {
            for (let i = 0; i < snakeBlocks.length; i++) {
                if (snakeBlocks[i].isDestroyed) {
                    continue;
                }

                if (snakeBlocks[i].x == x && snakeBlocks[i].y == y) {
                    return true;
                }
            }

            return false;
        }

        function createNewApple() {
            var x = 0;
            var y = 0;

            do {
                x = Math.floor(Math.random() * (mapWidth - 1));
                y = Math.floor(Math.random() * (mapHeight - 1));
            } while ((x == playerX && y == playerY) || (x == appleX && y == appleY) || isCollidingWithSnakeBody(x, y));

            appleX = x;
            appleY = y;
            setPosition(apple, appleX, appleY);
        }

        function eatApple() {
            createNewApple();
            score++;
            updateScoreText();
        }

        function updateScoreText() {
            scoreHUD.innerHTML = score;
        }

        function leaveSnakeBody() {
            var bodyPart = document.createElement('div');
            bodyPart.className = `square`;
            map.appendChild(bodyPart);
            setPosition(bodyPart, playerX, playerY);
            var sb = new SnakeBody(bodyPart, score + 2, false, playerX, playerY);
            snakeBlocks.push(sb);
        }

        resetGame();

        while (true) {
            await new Promise(resolve => setTimeout(resolve, 500));
            // Update position of the game snake and all the logic.
            ticks++;

            // PLAYER.
            if (direction == directions.LEFT) {
                playerX--;
            }
            else if (direction == directions.UP) {
                playerY--;
            }
            else if (direction == directions.RIGHT) {
                playerX++;
            }
            else if (direction == directions.DOWN) {
                playerY++;
            }

            setPosition(player, playerX, playerY);
            lastDirection = direction;

            if (isCollidingWithSnakeBody(playerX, playerY)) {
                resetGame();
            }

            if (isOutOfBounds()) {
                resetGame();
            }

            // PLAYER x APPLE COLLISIONs.
            if (Math.floor(playerX) == Math.floor(appleX) && Math.floor(playerY) == Math.floor(appleY)) {
                eatApple();
            }

            if (score > 0)
            {
                leaveSnakeBody();
                if (snakeBlocks.length > 0) {
                    for (let i = 0; i < snakeBlocks.length; i++) {
                        snakeBlocks[i].destroyAfterTicks--;
                        if (snakeBlocks[i].destroyAfterTicks <= 0 && !snakeBlocks[i].isDestroyed) {
                            var sb = snakeBlocks[i].block;
                            map.removeChild(sb);
                            snakeBlocks[i].isDestroyed = true;
                        }
                    }
                }
            }
        }
    }

    gameLoop();
</script>