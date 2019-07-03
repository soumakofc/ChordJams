# ChordJams

This music player is an **AI Music Player** which you can operate through *Voice Enabled Commands*. I am developing this app using ***Android Studio Speech to Text Recognition Api*** in android.


**Permission Dependencies and Packages:** https://github.com/Karumi/Dexter


### Dependency
Include the library in your build.gradle

'''
dependencies{
    implementation 'com.karumi:dexter:5.0.0'
}
'''


### Single permission
In this App I used Single permission. For each permission, register a PermissionListener implementation to receive the state of the request:

'''
Dexter.withActivity(this)
	.withPermission(Manifest.permission.CAMERA)
	.withListener(new PermissionListener() {
		@Override public void onPermissionGranted(PermissionGrantedResponse response) {/* ... */}
		@Override public void onPermissionDenied(PermissionDeniedResponse response) {/* ... */}
		@Override public void onPermissionRationaleShouldBeShown(PermissionRequest permission, PermissionToken token) {/* ... */}
	}).check();
'''

