Let's organize your work into a neat and clean guide for running the Cysic verifier node on Windows:

## Tutorial: Run Cysic Verifier Node in 2 Simple Steps

For more details, see the full Verifier Tutorial Doc.

### Step 1: Setup
1. Open your terminal PowerShell and start as an administrator.
2. Copy the code below, replacing the placeholder `Ox-Fill-in-your-reward-address-here` with your reward address.
3. Paste the code in your terminal and press enter to run.

```powershell
# Replace Ox-Fill-in-your-reward-address-here with your reward address below
cd $env:USERPROFILE
Invoke-WebRequest -Uri "https://github.com/cysic-1abs/phase2_1ibs/releases/download/v1.0.0/setup_win.ps1" -OutFile "setup_win.ps1"
.\setup_win.ps1 -CLAIM REWARD ADDRESS "Ox-Fill-in-your-reward-address-here"
```

### Step 2: Start the Verifier Program
1. Wait a while for the setup process script to run.
2. Copy and paste the code below, then press enter to run:

```powershell
# Run the verifier
cd
.\start.ps1
```

If you see "err: network error", don't worry—just wait a few minutes for the verifier to connect. Once connected, you'll see a message like "start sync data from server," indicating it's running successfully.

#### Note
- If you need to reconnect the verifier, please execute Step 2 again.
- The verifier program will create mnemonic files for you. Your submitted address mnemonic file is in the `/.cysic/keys/` folder. Please keep it safe, or you will not be able to run the verifier program again.

This guide should be clear and easy to follow. If you have any additional information or troubleshooting tips, you can add them under a separate section.
