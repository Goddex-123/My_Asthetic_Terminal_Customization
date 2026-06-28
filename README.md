# My Aesthetic Terminal Customization Guide

Welcome to the ultimate guide for making your Windows Terminal look stunning, complete with a glass-like transparent effect, customized system information via fastfetch, and smart autocompletion!

Follow these simple, layman-friendly steps to achieve this setup.

## 🛠 Prerequisites

1. **Windows Terminal**: If you don't have it, download it from the Microsoft Store.
2. **A Nerd Font**: You need a font that supports icons (like the ones you see in the terminal). 
   - Download **JetBrainsMono Nerd Font** from [Nerd Fonts](https://www.nerdfonts.com/font-downloads).
   - Extract the downloaded ZIP file, select all the font files inside, right-click, and choose **Install**.

---

## 🎨 Step 1: Transparent Glass Effect (Windhawk)

To get that beautiful blurry glass effect, we'll use a tool called Windhawk.

1. Download and install **Windhawk** from [windhawk.net](https://windhawk.net/).
2. Open Windhawk and click on **Explore** to find mods.
3. Search for **"Windows Terminal Acrylic"** (or Mica/Glass mod).
4. Click on the mod and hit **Install**. 
5. Restart your Windows Terminal to see the transparency take effect!

---

## 🚀 Step 2: Customizing the Terminal Look

We're going to apply our custom settings to the terminal.

1. Open **Windows Terminal**.
2. Click the small down arrow `v` at the top next to your tabs, and select **Settings**.
3. In the bottom left of the settings sidebar, click on **Open JSON file** (it usually looks like a small gear icon or text).
4. Replace the contents of that file with the contents from the `settings.json` file in this repository.
   *(This enables the acrylic effect, sets the font to JetBrainsMono Nerd Font, and applies the colors.)*
5. Save the file and close it.

---

## 📊 Step 3: Installing & Setting up Fastfetch

Fastfetch is what shows the system information and the cool Arch Linux logo when you open the terminal.

1. **Install Fastfetch**: 
   Open PowerShell and run the following command (you may need `winget` installed):
   ```powershell
   winget install fastfetch
   ```
2. **Set up the Configuration**:
   - Open your File Explorer and go to `C:\Users\YOUR_USERNAME\.config\fastfetch` (create these folders if they don't exist).
   - Copy the `config.jsonc` and `ascii.txt` from this repository into that folder.

---

## 🧠 Step 4: Adding Smart Autocomplete (PSReadLine)

PSReadLine provides awesome suggestions as you type commands based on your history.

1. Right-click on your start menu and open **Terminal (Admin)**.
2. Run the following command exactly as it is:
   ```powershell
   Install-Module -Name PSReadLine -AllowClobber -Force
   ```
   *(If it asks you to trust the repository or install NuGet, type `Y` and hit Enter).*

---

## ⚙️ Step 5: Applying the PowerShell Profile

The profile is a script that runs every time you open PowerShell. It makes sure Fastfetch runs automatically!

1. Open PowerShell and run this command to find exactly where your profile should go:
   ```powershell
   echo $PROFILE
   ```
   *(Usually, it's `C:\Users\YOUR_USERNAME\Documents\WindowsPowerShell\profile.ps1`)*
2. Go to that path in your File Explorer. If the folder doesn't exist, create it.
3. Create a new text file and name it `profile.ps1` (make sure it's not `.ps1.txt`).
4. Copy the contents of the `profile.ps1` file from this repository and paste it in there.
5. Save the file.

---

### 🎉 You're Done!
Close your terminal and open it again. You should now be greeted with a beautiful transparent window, the Arch logo system fetch, and smart autocompletion! Enjoy your aesthetic setup!
