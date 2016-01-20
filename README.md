This is an attempt to find the minimal requirements for building FlexJS from source repositories on Windows.
* Install Ant for Windows and add the Ant bin folder to your PATH variable (example: C:\Program Files\apache-ant-1.9.6\bin)
* FlashPlayerDebugger.exe can be found in an older Adobe Flex SDK distribution (not sure where else...) such as http://fpdownload.adobe.com/pub/flex/sdk/builds/flex4.5/flex_sdk_4.5.1.21328A.zip
* Download ${env.PLAYERGLOBAL_HOME}/11.1/player-global.swc from https://fpdownload.macromedia.com/get/flashplayer/updaters/11/playerglobal11_1.swc
* Set environment variables AIR_HOME, ANT_HOME, FLASHPLAYER_DEBUGGER, PLAYERGLOBAL_HOME
* Make sure *.swf has a registered file association to open with a browser or FlexUnit4 tests will time out and fail (because they use url.dll,FileProtocolHandler).
* Run ./init to initialize the local repositories and ./binary-release to build.