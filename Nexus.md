
### Nexus Testnet II CLI Node Setup Guide

#### Prerequisites
- Ensure you have a 64-bit Linux operating system.
- Install necessary dependencies:
  ```bash
  sudo apt-get update
  sudo apt-get install build-essential libssl-dev libdb++-dev libboost-all-dev
  ```
Quick run
  ```bash
curl https://cli.nexus.xyz/ | sh
  ```
#### Installation Steps

1. **Clone the Nexus Repository:**
   ```bash
   git clone https://github.com/Nexusoft/Nexus.git
   cd Nexus
   ```

2. **Build the Nexus Node:**
   ```bash
   make -f makefile.cli -j1 AMD64=1 NO_WALLET=1
   ```

3. **Run the Nexus Node:**
   ```bash
   ./nexus -daemon
   ```

#### Configuration

1. **Create Configuration File:**
   Create a file named `nexus.conf` in the `~/.nexus` directory with the following content:
   ```conf
   rpcuser=your_rpc_username
   rpcpassword=your_rpc_password
   ```

2. **Start the Node with Configuration:**
   ```bash
   ./nexus -daemon -conf=~/.nexus/nexus.conf
   ```

3. **Check Node Status:**
   ```bash
   ./nexus getinfo
   ```

#### Additional Commands

- **Stop the Node:**
  ```bash
  ./nexus stop
  ```

- **View Node Logs:**
  ```bash
  tail -f ~/.nexus/debug.log
  ```

---
