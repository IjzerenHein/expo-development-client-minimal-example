These instructions link to specific commits that show the diff for that step. The steps showing "Resulting auto-generated changes" just show the results of running a command (such as `npx pod-install`) that edits files automatically.

- Start with a bare expo project
    - This project was initialized with `expo init DevClientMinimalExample` (that was the name of this project, feel free to use your own!)
- Install expo-development-client
  - package.json dependencies
    - yarn add expo-development-client expo-dev-menu-interface@next expo-barcode-scanner
      [Resulting auto-generated package.json changes](https://github.com/nikki93/expo-development-client-minimal-example/commit/2428aca062f2725d36c9c06139715f50d74e09b8)
      [Resulting auto-generated yarn.lock changes](https://github.com/nikki93/expo-development-client-minimal-example/commit/cc86a874eee559214fe371d9f2d3bc20afaa502c)
  - iOS
    - Run `npx pod-install` from the root of the project
      [Resulting auto-generated Podfile.lock changes](https://github.com/nikki93/expo-development-client-minimal-example/commit/b86f767da63508bf91b158e47d795f0f050b3ca8)
    - [Edit AppDelegate.h, AppDelegate.m](https://github.com/nikki93/expo-development-client-minimal-example/commit/782b38364e3fbcd3512ab1b3a7e88fd7c97c9d5d)
    - Enable camera and microphone permissions (for the QR code scanner):
      [Edit Info.plist](https://github.com/nikki93/expo-development-client-minimal-example/commit/a1f11a1aed26629530a9b264bc5721501227e1c4)
    - Run from Xcode, follow the instructions you see in the development client launcher screen that now appears.
  - Android
    - [Edit MainActivit.java, MainApplication.java](https://github.com/nikki93/expo-development-client-minimal-example/commit/1fa4504373ae4541ee7027b60ed00848848732c4)
    - Enable camera permissions
      - Run the app once to get it on your device.
      - On the device, manually go to the app's 'App Info' (eg. long-press app icon in Android menu), go to permissions and enable Camera permissions, then restart the app. You can now follow the instructions in the development client launcher that appears.
- Install expo-dev-menu
  - package.json dependencies
    - yarn add expo-dev-menu
      [Resulting auto-generated package.json changes](https://github.com/nikki93/expo-development-client-minimal-example/commit/88858ca8aa3d5885f8dbe01ab7194e2af53dff7a)
      [Resulting auto-generated yarn.lock changes](https://github.com/nikki93/expo-development-client-minimal-example/commit/3dbcbe93810e364b2e4ee184951184d2abd810d3)
  - iOS
    - [Edit Podfile](https://github.com/nikki93/expo-development-client-minimal-example/commit/70cf83b766741e95837cf9b2075968684846bf98)
    - Run `npx pod-install` from the root of the project
      [Resulting auto-generated changes](https://github.com/nikki93/expo-development-client-minimal-example/commit/51adbc675ac530f287fb37ab9041c465bdfb0959)
    - [Edit AppDelegate.m](https://github.com/nikki93/expo-development-client-minimal-example/commit/84aef7bb920fa728fb7e472d89a9fc99aa492c69)
    - Run the app again, you should now be able to shake your device when viewing your app to go back to the launch screen.
  - Android
    - [Edit settings.gradle, app/build.gradle](https://github.com/nikki93/expo-development-client-minimal-example/commit/ace92be22a5b1c03ca4db93ff0a10adb5d8a7d53)
    - [Edit MainActivity.java](https://github.com/nikki93/expo-development-client-minimal-example/commit/bc2038bcf9d3e54f76aa04d18a40248c1de79bea)
    - Run the app again, you should now be able to shake your device when viewing your app to go back to the launch screen.
