## using in-game keybinds

you can for Example use the in-game keybinds for the blinkers.
to use the in-game keybinds you need to add the cInput.dll as a reference!

here's an example of how to use the in-game keybinds: 

!> this example code won't work for axes!

```csharp
using UnityEngine;
using MSCLoader;

ExampleClass : MonoBehaviour
{
    void Update()
    {
        if(cInput.GetKeyDown("IndicatorLeft"))
        {
            //left blinking Logic here.
            ModConsole.Log("IndicatorLeft key pressed.");
        }
        else if(cInput.GetKeyDown("IndicatorRight"))
        {
            //right blinking Logic here.
            ModConsole.Log("IndicatorRight key pressed.");
        }
    }
}
```

# using in-game axes

here's an example of how to use the in-game axes: 

!> this example code won't work for keybinds!

```csharp
using UnityEngine;
using MSCLoader;

ExampleClass : MonoBehaviour
{
    public float steeringInput;

    void Update()
    {
        steeringInput = cInput.GetAxis("Horizontal"); //gets steering Input
    }
}
```

# configured keybinds

Driving Keys:

ID | Default Key | Extra Notes
-- | ----------- | -----------
Left | A | (Not sure if used)
Right | D | (Not sure if used)
Up | W | (Not sure if used)
Down | S | (Not sure if used)
Throttle | W
Brake | S
Clutch | X
Throttle1 | None
Brake1 | None
Clutch1 | None
StartEngine | None
ShiftUp | G
ShiftDown | B
reverse | None
neutral | None
first | None
second | None
third | None
fourth | None
fifth | None
sixth | None
Handbrake | Z
Handbrake1 | None
IndicatorLeft | Semicolon
IndicatorRight | Colon
Range | R
HighBeam | L
Wipers | K
Boost | T

Player Controls:

ID | Default Key
-- | -----------
PlayerLeft | A
PlayerRight | D
PlayerUp | W
PlayerDown | S
Jump | Space
Zoom | LeftControl
Use | F
Crouch | C
ReachLeft | Q
ReachRight | E
Hitchhike | O
Swear | N
Hit | H
Push | J
Finger | M
Urinate | P
Drunk | K
DrivingMode | Return
Smoking | I
Watch | U

# configured axes

ID | Extra Notes
-- | -----------
PlayerVertical |
PlayerHorizontal |
Horizontal | Steering axis
Vertical |
Throttle |
Brake |
Clutch |
Handbrake |