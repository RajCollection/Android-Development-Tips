# Android-Development-Tips

1. Allow google signin in android

    1. need to generate sha1 certificate from android playstore
          - keystore file path and password is required (generated while generating signed apk)
          - go to bin folder of java jdk
          C:\Program Files\Java\jdk1.8.0_111\bin>
          - then run keytool command
          keytool -list -v -keystore "C:\Users\raj\Desktop\hubnrKeystore.jks"
          - it will ask the password (password of keystore file while generated signed apk)
          - it will generate sha1 certificate if everything is correct
          37:66:62:FA:B2:03:C6:62:39:AA:4E:4A:CB:17:04:58:5B:79:67:D3


     2. go to https://developers.google.com/identity/sign-in/android/start-integrating
          - Click on CONFIGURE A PROJECT
          - select your project, which shold be created in google cloud console
          - select Android in "where are you calling from" dropdown
          - add your project package
          - Add sha1 key which you generated in previous step
          - Then click on CREATE button, copy generated cliend ID
          - Paste it in in your android studio project -> app -> res -> values -> strings.xml
     <string name="google_server_client_id">paste here</string>

	3. generate apk. thats it
