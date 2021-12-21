Julius is available on [Google Play](https://play.google.com/store/apps/details?id=com.github.bvschaik.julius).

## Transferring Caesar 3 files to your device
Julius requires the original Caesar 3 files to be able to run. You can either move the files from your computer, or use the GOG version and extract that on your Android device (no computer needed).

### Transferring from a computer

1. Install Caesar 3 on your computer if it's not yet installed
2. Copy the whole install folder (containing `c3.eng`, among others) and any subfolders to your Android device, for example using [Android File Transfer](https://www.android.com/filetransfer/), or the utility that your device manufacturer provides for such purpose.
3. Start Julius and point it to the folder where you transfered the files to.

### Using the GOG installer
If you have purchased Caesar 3 on [GOG](https://www.gog.com/game/caesar_3), you can download and extract the files directly on your device.

1. Download the "offline backup game installer" file from GOG. It should be about 366 MB and have a name like `setup_caesar3_2.0.0.9.exe`. Do **not** download the "GOG Galaxy" version.
2. Install [Inno Setup Extractor](https://play.google.com/store/apps/details?id=uk.co.armedpineapple.innoextract) on your Android device.
3. Extract the setup_caesar3.exe file using this app to a folder of your choice. This will result in two subfolders: `app` and `tmp`. Feel free to remove the `tmp` folder: it's not needed.
4. Start Julius and point it to the `app` folder that was extracted.

## Running Julius
The first time you run Julius, the game will notify you that you need to point it to the game folder
location, which should contain the file `c3.eng`, among others. If you used Inno Setup Extractor, that would be the `app` folder, otherwise point the game to
wherever you downloaded the files to. After setting up the folder for the first time, Julius remembers it and you will not be
asked to do so again.

Julius has full touch support. For detailed touch usage, please check the
[Touch Support](Touch-Support) page.

Julius for Android has limited mouse support. Right mouse button clicks are notoriously flaky.
However, if you have a recent Samsung smartphone, Julius is fully compatibly with Samsung DeX.