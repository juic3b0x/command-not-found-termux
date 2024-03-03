# Adding Repo to Termux sources.list.d

To add this repository to your Termux setup, follow these steps:

1. Open Termux on your device.

2. Run the following command to edit the sources.list file:
   ```bash
   nano $PREFIX/etc/apt/sources.list.d/theworkjoy.list
   ```

3. Add the following line at the end of the file:
   ```bash
   deb [trusted=yes] https://repo.theworkjoy.com/ termux extras
   ```

4. Save the changes by pressing Ctrl + O, then press Enter. Exit the editor with Ctrl + X.

5. Update the package list by running:
   ```bash
   pkg update
   ```
 Now, you have successfully added the repository to your Termux sources.list.d/ directory.
