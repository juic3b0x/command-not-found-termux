## Table of Contents
1. [Adding Repo Source.list](#adding-repo-source-list)
2. [Installing Package](#installing-package)
3. [Editing .zshrc](#editing-zshrc)
4. [Updating commands.db](#updating-commands-db)
5. [Edit command_not_found_handler](#edit-command_not_found_handler)

---

## 1. Adding Repo Source.list

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

---

## 2. Installing Package

```bash
pkg install command-not-found-termux
```

---

## 3. Editing .zshrc

This is the minimal you need in a .zshrc file for this to work properly
```bash
export COMMAND_NOT_FOUND_INSTALL_PROMPT=1
source /data/data/com.termux/files/usr/etc/zsh_command_not_found
```

---

## 4. Edit command_not_found_handler

Next:
```bash
nano $PREFIX/etc/zshrc
```
Then comment out every line if you wanna keep this file or just:
```bash
rm -rf $PREFIX/etc/zshrc
```

---

## 5. Updating commands.db

Last but not least, run:
```bash
pkg update
```
This will update the commands.db with your packages commands.
