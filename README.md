# Android-Development-Tips

1. Allow google signin in android

    1. need to generate sha1 certificate from android playstore
          - keystore file path and password is required (generated while generating signed apk)
          - go to bin folder of java jdk
          C:\Program Files\Java\jdk1.8.0_111\bin>
          - then run keytool command
          keytool -list -v -keystore "C:\Users\username\Desktop\hubnrKeystore.jks"
          - it will ask the password (password of keystore file while generated signed apk)
          - it will generate sha1 certificate if everything is correct
          37:43:A1::D3....etc


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
	
----------------------------------------------------------------------------------------------------------------------------------
 2. How to generate signed APK
   
	   - go to build, select Generate Signed Bundle/APK
	   - Select APK
	   - Click on create new (if your don't have keystore generated)
	   - Select keystore path where you want to save that file
	   - Give password (remember the password)
	   - You can change alias name is required
	   - Same password you can give for key also
	   - Fill other details
	   - Click on OK
	   - It will take you previous page and details will be filled automatically
	   - Click on NEXT
	   - Check both check boxes and click finish. Thats it
-------------------------------------------------------------------------------------------------------------------------------------
3. Internet permission to your APP
	   - Add this line into your AndroidManifest.xml, outside of application tag
	    <uses-permission android:name="android.permission.INTERNET" />

4. External Storage read and write permission to your APP
	   - Add this line into your AndroidManifest.xml, outside of application tag
	    <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
	    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />

5. Camera permission to your APP
	   - Add this line into your AndroidManifest.xml, outside of application tag
	    <uses-permission android:name="android.permission.CAMERA" />
--------------------------------------------------------------------------------------------------------------------------------------

6. Change Android App version
   	Go to build.gradle (Module: app) file, edit your versionName "your App version"

