
## **# Install-portable-programs**  
A guide on how to install a portable program on Linux and make it available system-wide, including in the application menu.

---

### **## Step 1: Download and Extract the Program**

Download the `.tar.gz` file, then extract it to `/opt/`:

```bash
tar -xzf file.tar.gz -C /opt/
```

---

### **## Step 2: Create a Symbolic Link for Terminal Access**

Create a symbolic link in `/usr/local/bin/` to allow execution from the terminal:

```bash
sudo ln -s /opt/program-directory/program /usr/local/bin/program
```

---

### **## Step 3: Create a `.desktop` File for the Application Menu**

Create a `.desktop` file in `~/.local/share/applications/` with the program's name.

Open your text editor and add the following content to the `.desktop` file:

```ini
[Desktop Entry]
Name=Program Name
Exec=/opt/program-directory/program
Icon=/opt/program-directory/program.png
Type=Application
Categories=Utility;
Terminal=false
```

---
