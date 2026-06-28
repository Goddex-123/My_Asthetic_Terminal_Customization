# 🚀 Pimp My Terminal (Windows Edition) 🚀

Tired of your Windows Terminal looking like a boring 1990s hacker movie? Want it to look so incredibly clean and aesthetic that it makes your friends jealous? You've come to the right place, young padawan! 

This guide is **dummy-proof**. If you can click buttons and copy-paste, you can do this. Let’s turn that crusty terminal into a glass-like, auto-completing, system-flexing masterpiece! 😎

---

## 🛠️ Ground Zero (The Basics)

1. **Windows Terminal**: Don't have it? Go to the Microsoft Store and download it. Seriously, why don't you have it yet?
2. **Nerd Font**: You need a special font so those cool little icons show up instead of weird boxes. 
   - Go to [Nerd Fonts](https://www.nerdfonts.com/font-downloads) and download **JetBrainsMono Nerd Font**.
   - Unzip the folder, select all the font files inside, right-click -> **Install**. Boom. Font installed.

---

## 🧊 Step 1: The Sexy Glass Effect (Windhawk)

We want that transparent, frosty glass look. We'll use a magic app called Windhawk for this.

1. Download **Windhawk** from [windhawk.net](https://windhawk.net/) and install it. Just click next, next, next. You know the drill.
2. Open Windhawk and click on **Explore**.
3. Search for **"Windows Terminal Acrylic"** (or Mica).
4. Slap that **Install** button.
5. Close your terminal and open it again. *Voila!* You can now see through it! 👻

---

## 🎨 Step 2: Make it Look Good

Now we inject the drip.

1. Open **Windows Terminal**.
2. Click that little arrow `v` at the very top (next to your tabs) and click **Settings**.
3. Look at the bottom left corner for **Open JSON file** (it’s a gear icon ⚙️). Click it!
4. Delete literally everything in that file and paste the contents of `settings.json` from this repository.
   *(This gives you the cool colors, the right font, and enables the acrylic effect).*
5. Save and close. Looking better already, right?

---

## 🐧 Step 3: Fastfetch (The Big Flex)

You know how Linux users always have that cool system info pop up when they open their terminal? We’re stealing that.

1. Open PowerShell and type this exactly:
   ```powershell
   winget install fastfetch
   ```
2. Press Enter. Let it do its thing. 
3. Now, open File Explorer and go to: `C:\Users\YOUR_USERNAME\.config\fastfetch` 
   *(If the folders aren't there, just create them! No panicking!)*
4. Grab `config.jsonc` and `ascii.txt` from this repo and dump them into that folder. 
   *(This gives you that sick Arch logo and custom colors).*

---

## 🧠 Step 4: Mind-Reading Autocomplete

Typing full commands is for peasants. Let’s make the terminal finish your sentences.

1. Right-click your Start button and open **Terminal (Admin)**. Gotta have those admin privileges!
2. Paste this bad boy in and hit Enter:
   ```powershell
   Install-Module -Name PSReadLine -AllowClobber -Force
   ```
   *(If it asks you some yes/no questions about trusting stuff, just type `Y` and Enter. Trust the process).*

---

## ⚡ Step 5: The Grand Finale (PowerShell Profile)

We need to tell PowerShell to run our fancy Fastfetch every time we open it.

1. Open PowerShell (regular one is fine) and run:
   ```powershell
   echo $PROFILE
   ```
   *(It will spit out a path, usually `C:\Users\YOUR_USERNAME\Documents\WindowsPowerShell\profile.ps1`)*
2. Go to that path in File Explorer. If the folder doesn't exist, make it! 
3. Create a text file, name it exactly `profile.ps1` (watch out for `.ps1.txt`, turn on file extensions if you're blind to them).
4. Copy everything from `profile.ps1` in this repo and paste it into your new file. Save it.

---

### 🎉 YOU DID IT! 🎉
Close all your terminals. Open a fresh one. 
Bask in the glory of your transparent, auto-completing, system-fetching masterpiece. Go show off to your mom, she'll be very proud.
