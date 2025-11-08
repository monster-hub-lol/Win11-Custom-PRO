# 🪟 Win11 Custom PRO

A full guide to customizing your Windows 11 terminal and environment using modern, powerful, and lightweight tools.  
Make your Windows look clean, professional, and personalized.

## 🚀 1. Install Oh My Posh  
Oh My Posh adds colorful and informative themes to your PowerShell prompt.

📦 Installation (via Winget)
```powershell
winget install JanDeDobbeleer.OhMyPosh --source winget
```
## ⚡ 2. Install Fastfetch
Fastfetch displays beautiful system information directly in your terminal — similar to Neofetch but faster.

📦 Installation (via Winget)

```powershell
winget install fastfetch
```
## 🛠️ 3. PowerShell Profile Setup
Set up your PowerShell profile to automatically apply custom themes and commands each time you open the terminal.

Create a Profile File (if not exists)

```powershell
New-Item -Path $PROFILE.CurrentUserAllHosts -Type File -Force
```
Allow Custom Scripts

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser -Force
```
Open Your Profile

```powershell
notepad $PROFILE
```
Then add the following lines inside your profile file:

```powershell
oh-my-posh init pwsh | Invoke-Expression
```
fastfetch
Now, Oh My Posh and Fastfetch will run automatically every time you open PowerShell.

## 🎨 4. Choose Your Theme
You can preview all available Oh My Posh themes:

```powershell
Get-PoshThemes
```
To set a theme (example: paradox):

```powershell
oh-my-posh init pwsh --config ~/atomic.omp.json | Invoke-Expression
```
Once you find your favorite, add that command permanently inside your profile file.

✅ Done!
Restart PowerShell, and enjoy your modern Windows 11 setup ✨
Simple, fast, and beautiful — just how a pro system should be.
