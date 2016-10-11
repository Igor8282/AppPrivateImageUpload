# AppPrivateImageUpload
App to demonstrate giving Permission to Camera App to Write in App Private External Storage space.

## When do you need this
When you want to upload Full Quality images from your Android app using the Camera App but **don't** want to put the **WRITE_EXTERNAL_STORAGE** permission for any reason.

## How does it work.

1. Introduce a File Provider using the AndroidManifest.xml and point it to the filePath allowed to be shared with other apps.
2. Create a file in the External Storage Private app space and give its Content URI to the Camera app intent via the extras
3. Give temporary permission to write to the file
4. onActivityResult, read the image from the file path you already knew, also revokePermissions for safety ( havent coded that yet)

## References
https://developer.android.com/training/camera/photobasics.html#TaskPath

http://stackoverflow.com/questions/18249007/how-to-use-support-fileprovider-for-sharing-content-to-other-apps

http://stackoverflow.com/questions/17674634/saving-and-reading-bitmaps-images-from-internal-memory-in-android

http://stackoverflow.com/questions/29185631/take-pictures-with-camera-and-store-in-internal-instead-of-external-storage

https://developer.android.com/guide/topics/data/data-storage.html#filesExternal

