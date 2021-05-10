# Changelog

## 1.0.7 (07.05.2021)

- Bolt components can now operate independently from a BoltMagnet component.
- Added OnScrew event to Bolt component, executed each screw, as well as events OnMaxTightness and OnMinTightness executed when the bolt reach max and min tightness respectively.
- Fixed SettingSlider value text not working properly when the value went into negatives.
- Adjusted UI text and shadows.
- Fixed NexusMods login failing, if user didn't have profile picture set.
- Changed how NexusMods login is being handled, if CoolUpdater couldn't start a web browser
- Removed resources from template, instead adding a guide on the website on how to add resources to your project.
- Addressed an issue related with objects using PartMagnet being not detacheable, if the object has been disabled
- Fixed music not playing after quitting from game to the main menu (issue #5)
- CoolUpdater: Added info page, if CoolUpdater is open by the user
- Uninstaller: Added support for launching the Uninstaller via "Add or remove programs"

## 1.0.6 (02.05.2021)

- Fixed UI scaling on ultrawide resolutions.
- Fixed Nexus out of range exception.
- Fixed user avatar when using Gravatar.

## 1.0.5 (01.05.2021)

- CoolUpdater: Added "Start Game (No Steam)" button.
- Fixed keybinds with None as a modifier.

## 1.0.4 (30.04.2021)

- CoolUpdater: Fixed "Start Game" button not starting the game with Mod Loader Pro.
- Mod Auto Updater should now prioritze archives with .pro.zip extension as intended.

## 1.0.3 (30.04.2021)

- Added "ExecuteCommand" method.
- Fixed update status permanently staying on the main menu, if no mods are installed.
- Fixed compatibility with Cassette mod.

## 1.0.2 (30.04.2021)

- Fixed missing null checks.
- Fixed legacy sliders not updating as they should.

## 1.0.1 (30.04.2021)

- Removed game freezing bug with NexusMods login.

## 1.0 (30.04.2021)

- Initial release.

## 1.0-RC13 (29.04.2021)

- Updated CoolUpdater version to 1.0.
- Fixed hidden settings (SettingString, SettingBoolean, SettingNumber) not loading right away.

## 1.0-RC12 (28.04.2021)

- NexusMods: Mod Loader will now check if Nexus login save data is corrupted.
- Added missing websocket-sharp.dll.
