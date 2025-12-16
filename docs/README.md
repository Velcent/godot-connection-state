<p align="center">
	<img width="256" height="256" src="https://raw.githubusercontent.com/godot-sdk-integrations/godot-connection-state/main/demo/assets/connection-state-android.png">
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
	<img width="256" height="256" src="https://raw.githubusercontent.com/godot-sdk-integrations/godot-connection-state/main/demo/assets/connection-state-ios.png">
</p>

---

# <img src="https://raw.githubusercontent.com/godot-sdk-integrations/godot-connection-state/main/addon/icon.png" width="24"> Godot Connection State Plugin

A Godot plugin that provides a unified GDScript interface for getting information on mobile device connections on **Android** and **iOS**.

**Key Features:**
- Get information about all available connections on mobile device
- Know when a new connection is established (signal)
- Know when a connection is lost (signal)

---

## <img src="https://raw.githubusercontent.com/godot-sdk-integrations/godot-connection-state/main/addon/icon.png" width="20"> Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Signals](#signals)
- [Methods](#methods)
- [Classes](#classes)
- [Platform-Specific Notes](#platform-specific-notes)
- [Links](#links)
- [All Plugins](#all-plugins)
- [Credits](#credits)
- [Contributing](#contributing)

---

<a name="installation"></a>

## <img src="https://raw.githubusercontent.com/godot-sdk-integrations/godot-connection-state/main/addon/icon.png" width="20"> Installation
_Before installing this plugin, make sure to uninstall any previous versions of the same plugin._

_If installing both Android and iOS versions of the plugin in the same project, then make sure that both versions use the same addon interface version._

There are 2 ways to install the `ConnectionState` plugin into your project:
- Through the Godot Editor's AssetLib
- Manually by downloading archives from Github

### <img src="https://raw.githubusercontent.com/godot-sdk-integrations/godot-connection-state/main/addon/icon.png" width="18"> Installing via AssetLib
Steps:
- search for and select the `ConnectionState` plugin in Godot Editor
- click `Download` button
- on the installation dialog...
	- keep `Change Install Folder` setting pointing to your project's root directory
	- keep `Ignore asset root` checkbox checked
	- click `Install` button
- enable the plugin via the `Plugins` tab of `Project->Project Settings...` menu, in the Godot Editor

#### <img src="https://raw.githubusercontent.com/godot-sdk-integrations/godot-connection-state/main/addon/icon.png" width="16"> Installing both Android and iOS versions of the plugin in the same project
When installing via AssetLib, the installer may display a warning that states "_[x number of]_ files conflict with your project and won't be installed." You can ignore this warning since both versions use the same addon code.

### <img src="https://raw.githubusercontent.com/godot-sdk-integrations/godot-connection-state/main/addon/icon.png" width="18"> Installing manually
Steps:
- download release archive from Github
- unzip the release archive
- copy to your Godot project's root directory
- enable the plugin via the `Plugins` tab of `Project->Project Settings...` menu, in the Godot Editor

---

<a name="usage"></a>


## <img src="https://raw.githubusercontent.com/godot-sdk-integrations/godot-connection-state/main/addon/icon.png" width="20"> Usage
- Add `ConnectionState` node to your main scene or an autoload global scene.

### <img src="https://raw.githubusercontent.com/godot-sdk-integrations/godot-connection-state/main/addon/icon.png" width="18"> Loading and displaying ads
- use the `ConnectionState` node's `get_connection_state()` method to get information on all available connections
- connect `ConnectionState` node signals
	- `connection_established(a_connection_info: ConnectionInfo)`
	- `connection_lost(a_connection_info: ConnectionInfo)`

---

<a name="signals"></a>

## <img src="https://raw.githubusercontent.com/godot-sdk-integrations/godot-connection-state/main/addon/icon.png" width="20"> Signals
- register listeners to the following signals of the `ConnectionState` node:
	- `connection_established(a_connection_info: ConnectionInfo)`
	- `connection_lost(a_connection_info: ConnectionInfo)`

---

<a name="methods"></a>

## <img src="https://raw.githubusercontent.com/godot-sdk-integrations/godot-connection-state/main/addon/icon.png" width="20"> Methods
- `get_connection_state()` - retuns an array of `ConnectionInfo` objects

---

<a name="classes"></a>

## <img src="https://raw.githubusercontent.com/godot-sdk-integrations/godot-connection-state/main/addon/icon.png" width="20"> Classes

### <img src="https://raw.githubusercontent.com/godot-sdk-integrations/godot-connection-state/main/addon/icon.png" width="16"> ConnectionInfo
- Encapsulates adapter response data that is returned by the SDK for an ad request.
- Properties: `connection_type`, `is_active`, `is_metered`

---

<a name="platform-specific-notes"></a>

## <img src="https://raw.githubusercontent.com/godot-sdk-integrations/godot-connection-state/main/addon/icon.png" width="20"> Platform-Specific Notes

### Android
- Download Android export template and enable gradle build from export settings
- **Troubleshooting:**
- Logs: `adb logcat | grep 'godot'` (Linux), `adb.exe logcat | select-string "godot"` (Windows)
- You may find the following resources helpful:
	- https://docs.godotengine.org/en/stable/tutorials/export/exporting_for_android.html
	- https://developer.android.com/tools/adb
	- https://developer.android.com/studio/debug
	- https://developer.android.com/courses

### iOS
- Follow instructions on [Exporting for iOS](https://docs.godotengine.org/en/stable/tutorials/export/exporting_for_ios.html)
- View XCode logs while running the game for troubleshooting.
- See [Godot iOS Export Troubleshooting](https://docs.godotengine.org/en/stable/tutorials/export/exporting_for_ios.html#troubleshooting).

---

<a name="links"></a>

# <img src="https://raw.githubusercontent.com/godot-sdk-integrations/godot-connection-state/main/addon/icon.png" width="24"> Links

- [AssetLib Entry Android](https://godotengine.org/asset-library/asset/2548)
- [AssetLib Entry iOS](https://godotengine.org/asset-library/asset/3178)

---

# <img src="https://raw.githubusercontent.com/godot-sdk-integrations/godot-connection-state/main/addon/icon.png" width="24"> All Plugins

| Plugin | Android | iOS | Free | Open Source | License |
| :--- | :---: | :---: | :---: | :---: | :---: |
| [Notification Scheduler](https://github.com/godot-sdk-integrations/godot-notification-scheduler) | ✅ | ✅ | ✅ | ✅ | MIT |
| [Admob](https://github.com/godot-sdk-integrations/godot-connection-state) | ✅ | ✅ | ✅ | ✅ | MIT |
| [Deeplink](https://github.com/godot-sdk-integrations/godot-deeplink) | ✅ | ✅ | ✅ | ✅ | MIT |
| [Share](https://github.com/godot-sdk-integrations/godot-share) | ✅ | ✅ | ✅ | ✅ | MIT |
| [In-App Review](https://github.com/godot-sdk-integrations/godot-inapp-review) | ✅ | ✅ | ✅ | ✅ | MIT |
| [Connection State](https://github.com/godot-sdk-integrations/godot-connection-state) | ✅ | ✅ | ✅ | ✅ | MIT |

---

<a name="credits"></a>

# <img src="https://raw.githubusercontent.com/godot-sdk-integrations/godot-connection-state/main/addon/icon.png" width="24"> Credits

Developed by [Cengiz](https://github.com/cengiz-pz)

Original repository: [Godot Connection State Plugin](https://github.com/godot-sdk-integrations/godot-connection-state)

---

<a name="contributing"></a>

# <img src="https://raw.githubusercontent.com/godot-sdk-integrations/godot-connection-state/main/addon/icon.png" width="24"> Contributing

See [our guide](https://github.com/godot-sdk-integrations/godot-connection-state?tab=contributing-ov-file) if you would like to contribute to this project.
