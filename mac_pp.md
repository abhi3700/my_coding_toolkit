# Password-Protected Folder on macOS

macOS does not password-protect an ordinary Finder folder directly. Use an encrypted disk image instead. When it is unlocked, it behaves like a normal drive; ejecting it locks the files again.

## Create the encrypted folder

1. Open **Disk Utility** with Spotlight.
2. Select **File → New Image → Image from Folder**.
3. Choose the folder to protect.
4. Choose **256-bit AES encryption** and enter a strong password.
5. Disable **Remember password in my keychain** if the password must be requested each time.
6. For **Image Format**, choose **Sparse Bundle Image (UDSB)**. It supports read/write access and grows as files are added.
7. Save the image. It will have a name such as `foo.sparsebundle`.
8. Confirm that the encrypted image opens and contains every file before removing the original unencrypted folder.

## Open and use it

1. Try double-clicking the `.sparsebundle` in Finder and enter the password.
2. If it does not open from Finder, open **Disk Utility**, find the image in the sidebar, right-click it, and choose **Mount** or **Open**.
3. Open the mounted drive under **Finder → Locations**.
4. Add, edit, rename, or delete files normally. Save and close any open files when finished.

## Lock it again

1. Close every file stored inside the encrypted drive.
2. In Finder, click the **Eject ⏏** button beside the drive under **Locations**. You can also eject it from Disk Utility.
3. After it disappears from Finder, the contents are locked and require the password to mount again.

## Important precautions

- While the image is mounted, its contents are unlocked. Eject it whenever it is not being used.
- Do not open the `.sparsebundle` with **Show Package Contents** or manually change files inside its `bands` folder.
- Back up the entire `.sparsebundle` only while it is ejected.
- If it is stored in iCloud or another sync service, wait for syncing to finish before opening it on another Mac.
- Keep the password somewhere secure. The files usually cannot be recovered if the password is forgotten.
- Do not delete the original folder until the encrypted copy has been opened and checked successfully.

## If it will not open

1. Ensure the image is fully downloaded and stored locally.
2. Open it from Disk Utility using the right-click method above.
3. If needed, run the following in Terminal, then enter the password when prompted:

   ```bash
   hdiutil attach "/full/path/to/foo.sparsebundle"
   ```

   Do not put the password in the command.
