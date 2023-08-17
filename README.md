# ios-android-permission


## IOS

go to ios/<project.name>/Info.plist, copy below code.

<?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
    <plist version="1.0">
    <dict>     
      <!-- 🚨 Keep only the permissions used in your app 🚨 -->
      <key>NSAppleMusicUsageDescription</key>
      <string>YOUR TEXT</string>
      <key>NSBluetoothAlwaysUsageDescription</key>
      <string>YOUR TEXT</string>
      <key>NSBluetoothPeripheralUsageDescription</key>
      <string>YOUR TEXT</string>
      <key>NSCalendarsUsageDescription</key>
      <string>YOUR TEXT</string>
      <key>NSCameraUsageDescription</key>
      <string>YOUR TEXT</string>
      <key>NSContactsUsageDescription</key>
      <string>YOUR TEXT</string>
      <key>NSFaceIDUsageDescription</key>
      <string>YOUR TEXT</string>
      <key>NSLocationAlwaysAndWhenInUseUsageDescription</key>
      <string>YOUR TEXT</string>
      <key>NSLocationAlwaysUsageDescription</key>
      <string>YOUR TEXT</string>
      <key>NSLocationTemporaryUsageDescriptionDictionary</key>
      <dict>
        <key>YOUR-PURPOSE-KEY</key>
        <string>YOUR TEXT</string>
      </dict>
      <key>NSLocationWhenInUseUsageDescription</key>
      <string>YOUR TEXT</string>
      <key>NSMicrophoneUsageDescription</key>
      <string>YOUR TEXT</string>
      <key>NSMotionUsageDescription</key>
      <string>YOUR TEXT</string>
      <key>NSPhotoLibraryUsageDescription</key>
      <string>YOUR TEXT</string>
      <key>NSPhotoLibraryAddUsageDescription</key>
      <string>YOUR TEXT</string>
      <key>NSRemindersUsageDescription</key>
      <string>YOUR TEXT</string>
      <key>NSSpeechRecognitionUsageDescription</key>
      <string>YOUR TEXT</string>
      <key>NSSiriUsageDescription</key>
      <string>YOUR TEXT</string>
      <key>NSUserTrackingUsageDescription</key>
      <string>YOUR TEXT</string>

      <!-- … -->
    </dict>
    </plist>

## Android

go to android/app/src/main/AndroidManifest.xml and copy the code 

<manifest xmlns:android="http://schemas.android.com/apk/res/android"
      package="com.myawesomeapp">
      <!-- 🚨 Keep only the permissions used in your app 🚨 -->
      <uses-permission android:name="android.permission.ACCEPT_HANDOVER" />
      <uses-permission android:name="android.permission.ACCESS_BACKGROUND_LOCATION" />
      <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
      <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
      <uses-permission android:name="android.permission.ACTIVITY_RECOGNITION" />
      <uses-permission android:name="android.permission.ANSWER_PHONE_CALLS" />
      <uses-permission android:name="android.permission.BODY_SENSORS" />
      <uses-permission android:name="android.permission.CALL_PHONE" />
      <uses-permission android:name="android.permission.CAMERA" />
      <uses-permission android:name="android.permission.GET_ACCOUNTS" />
      <uses-permission android:name="android.permission.PROCESS_OUTGOING_CALLS" />
      <uses-permission android:name="android.permission.READ_CALENDAR" />
      <uses-permission android:name="android.permission.READ_CALL_LOG" />
      <uses-permission android:name="android.permission.READ_CONTACTS" />
      <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
      <uses-permission android:name="android.permission.READ_PHONE_NUMBERS" />
      <uses-permission android:name="android.permission.READ_PHONE_STATE" />
      <uses-permission android:name="android.permission.READ_SMS" />
      <uses-permission android:name="android.permission.RECEIVE_MMS" />
      <uses-permission android:name="android.permission.RECEIVE_SMS" />
      <uses-permission android:name="android.permission.RECEIVE_WAP_PUSH" />
      <uses-permission android:name="android.permission.RECORD_AUDIO" />
      <uses-permission android:name="android.permission.SEND_SMS" />
      <uses-permission android:name="android.permission.USE_SIP" />
      <uses-permission android:name="android.permission.WRITE_CALENDAR" />
      <uses-permission android:name="android.permission.WRITE_CALL_LOG" />
      <uses-permission android:name="android.permission.WRITE_CONTACTS" />
      <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
      <uses-permission android:name="com.android.voicemail.permission.ADD_VOICEMAIL" />
   
      <!-- … -->

</manifest>


### request permission

request(Platform.OS === 'ios' ? PERMISSIONS.IOS.CAMERA : PERMISSIONS.ANDROID.CAMERA).then((result) => {
        setPermissionResult(result)
        console.log(result)
      });

return type and meaning:
![image](https://github.com/Ernestanior/ios-android-permission/assets/36638557/3fd851b4-889c-4d74-8680-69d5ba227a7c)



