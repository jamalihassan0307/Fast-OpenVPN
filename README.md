<div align="center">
  <h1>
    <img src="assets/images/logo-removebg.png" width="80px"><br/>
    Fast VPN - Secure & Free VPN App
  </h1>
  <h3>A Modern VPN Application with Beautiful UI and Multiple Server Locations</h3>
</div>

<p align="center">
    <a href="https://github.com/jamalihassan0307/" target="_blank">
        <img alt="" src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" />
    </a>
    <a href="https://www.linkedin.com/in/jamalihassan0307/" target="_blank">
        <img alt="" src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" />
    </a>
</p>

## 📌 Overview

A beautifully designed Flutter VPN application with an elegant UI, smooth animations, and multiple free server locations. The app features a modern design, real-time network statistics, and comprehensive VPN functionality.

## 🚀 Tech Stack

- **Flutter** (UI Framework)
- **GetX** (State Management)
- **Hive** (Local Storage)
- **Custom Animations**
- **Material Design**
- **VPN Engine Integration**

## 🔑 Key Features

- ✅ **Multiple Server Locations**: Free servers across various countries
- ✅ **Real-time Network Stats**: Monitor your connection details
- ✅ **Dark/Light Theme**: Customizable app appearance
- ✅ **Network Testing**: Check connection speed and details
- ✅ **Location Selection**: Choose from various VPN servers
- ✅ **Connection Timer**: Track connection duration
- ✅ **Modern UI**: Elegant and responsive interface
- ✅ **Onboarding Screens**: Smooth introduction to the app

## 📸 Banner

<img src="screenshots/VPN_banner.png" alt="Fast VPN App Banner" />

## 📸 Screenshots

### Main Features

<table border="1">
  <tr>
    <td align="center">
      <img src="screenshots/home (light theme).png" alt="Home Light" width="250"/>
      <p><b>Home Screen (Light)</b></p>
    </td>
    <td align="center">
      <img src="screenshots/home (dark theme).png" alt="Home Dark" width="250"/>
      <p><b>Home Screen (Dark)</b></p>
    </td>
    <td align="center">
      <img src="screenshots/vpn_location(light theme).png" alt="Locations" width="250"/>
      <p><b>VPN Locations</b></p>
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="screenshots/network_info(light theme).png" alt="Network Light" width="250"/>
      <p><b>Network Info (Light)</b></p>
    </td>
    <td align="center">
      <img src="screenshots/network_info(dark theme).png" alt="Network Dark" width="250"/>
      <p><b>Network Info (Dark)</b></p>
    </td>
    <td align="center">
      <img src="screenshots/toast.png" alt="Toast" width="250"/>
      <p><b>Status Updates</b></p>
    </td>
  </tr>
</table>

### Onboarding Experience

<table border="1">
  <tr>
    <td align="center">
      <img src="screenshots/splash.png" alt="Splash" width="250"/>
      <p><b>Splash Screen</b></p>
    </td>
    <td align="center">
      <img src="screenshots/walk1(light theme).png" alt="Walkthrough 1" width="250"/>
      <p><b>Walkthrough 1</b></p>
    </td>
    <td align="center">
      <img src="screenshots/walk2(light theme).png" alt="Walkthrough 2" width="250"/>
      <p><b>Walkthrough 2</b></p>
    </td>
  </tr>
</table>

## 🌍 Available Server Locations

<table>
  <tr>
    <td>
      <img src="assets/flags/us.png" width="20" style="vertical-align: middle"> United States
    </td>
    <td>
      <img src="assets/flags/japan.png" width="20" style="vertical-align: middle"> Japan
    </td>
    <td>
      <img src="assets/flags/kr.png" width="20" style="vertical-align: middle"> South Korea
    </td>
  </tr>
  <tr>
    <td>
      <img src="assets/flags/id.png" width="20" style="vertical-align: middle"> Indonesia
    </td>
    <td>
      <img src="assets/flags/ec.png" width="20" style="vertical-align: middle"> Ecuador
    </td>
    <td>
      <img src="assets/flags/ro.png" width="20" style="vertical-align: middle"> Romania
    </td>
  </tr>
  <tr>
    <td>
      <img src="assets/flags/ru.png" width="20" style="vertical-align: middle"> Russia
    </td>
    <td>
      <img src="assets/flags/tw.png" width="20" style="vertical-align: middle"> Taiwan
    </td>
    <td>
      <img src="assets/flags/vn.png" width="20" style="vertical-align: middle"> Vietnam
    </td>
  </tr>
</table>

## 📁 Project Structure

```
lib/
├── apis/
│   └── apis.dart
├── controllers/
│   ├── home_controller.dart
│   └── location_controller.dart
├── core/
│   └── vpn_engine.dart
├── helpers/
│   ├── pref.dart
│   └── my_dialogs.dart
├── models/
│   ├── ip_details.dart
│   ├── network_data.dart
│   └── vpn.dart
├── screens/
│   ├── home_screen.dart
│   ├── location_screen.dart
│   ├── network_test_screen.dart
│   ├── splash_screen.dart
│   └── walkthrough_screen.dart
├── widgets/
│   ├── count_down_timer.dart
│   ├── network_card.dart
│   └── vpn_card.dart
└── main.dart
```

## 📱 Download APK

You can download the latest version of the app from:
[APK/app-armeabi-v7a-release.apk](APK/app-armeabi-v7a-release.apk)

## 👨‍💻 Developer

Developed by [Jam Ali Hassan](https://github.com/jamalihassan0307)

---

## Do this to Connect / Disconnect

Connect or Disconnect vpn with single line of code!

```dart
    ...
        _vpnStage = AliVpn.vpnDisconnected;
        _selectedVpn = VpnConfig(
            config: "OVPN CONFIG IS HERE",
            name: "Japan",
            username: "VPN Username",
            password:"VPN Password"
        );
    ...

    ...
        if (_selectedVpn == null) return; //Stop right here if user not select a vpn
        if (_vpnStage == AliVpn.vpnDisconnected) {
            //Start if stage is disconnected
            AliVpn.startVpn(_selectedVpn);
        } else {
            //Stop if stage is "not" disconnected
            AliVpn.stopVpn();
        }
    ...
```

## Listen to VPN Stage & Status

Don't forget to listen your vpn stage and status, you can simply show them with this.

```dart
    ...
        //Add listener to update vpnStage
        AliVpn.vpnStageSnapshot().listen((event) {
            setState(() {
                _vpnStage = event; //Look at stages detail below
            });
        });
    ...
    ...
        //Add listener to update vpnStatus
        AliVpn.vpnStatusSnapshot().listen((event){
            setState((){
                _vpnStatus = event;
            });
        })
    ...
```

### VPN Stages

Let me be clearer, VPN Stage shows the connection indicator when connecting the VPN

```dart
static const String vpnConnected = "connected";
static const String vpnDisconnected = "disconnected";
static const String vpnWaitConnection = "wait_connection";
static const String vpnAuthenticating = "authenticating";
static const String vpnReconnect = "reconnect";
static const String vpnNoConnection = "no_connection";
static const String vpnConnecting = "connecting";
static const String vpnPrepare = "prepare";
static const String vpnDenied = "denied";
```

Note : To change notification's icon, you can go to `vpnLib/main/res/drawable` and replace ic_notification.png from there!
