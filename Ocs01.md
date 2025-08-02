
![image](https://github.com/user-attachments/assets/0d8ec782-edf6-4ce2-a75b-4ee08589afe7)

## 1. Update Server and Dependencies

```bash
sudo apt update -y && sudo apt upgrade -y
```
---

## 2. Download Neccessary Packages

```bash
sudo apt install htop ca-certificates zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev tmux iptables curl nvme-cli git wget make jq libleveldb-dev build-essential pkg-config ncdu tar clang bsdmainutils lsb-release libssl-dev libreadline-dev libffi-dev jq gcc screen file nano btop unzip lz4 -y
```
---

## 3. Install Rust

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
---

<img width="1098" height="537" alt="Screenshot 2025-08-02 123200" src="https://github.com/user-attachments/assets/3b590eeb-7584-404d-bf05-6379fe6c1dc5" />

> When propmpted with this page (in the image above), just hit Enter.

- When the installation is complete, load the environment variables into the current shell session using the code below: 
```bash
source $HOME/.cargo/env
```
---

## 4. Clone Repo and Build 

```bash
git clone https://github.com/octra-labs/ocs01-test.git
cd ocs01-test
cargo build --release
```
<img width="599" height="184" alt="image" src="https://github.com/user-attachments/assets/1e8cf79a-b9ab-4f5a-a34e-81cf383ef2a6" />

---

## 5. Copy Code to Target file 
```bash
cp EI/exec_interface.json .
```

<img width="497" height="147" alt="image" src="https://github.com/user-attachments/assets/1dc46574-f2f7-4c2e-af99-aa5512ff42cc" />

---

## Import wallet to the Shell 

```bash
nano wallet.json
```

- Copy the code below and replace "your_B64_Private_Key" with your Octra B64 Private Key and "Octra_Wallet_Address" with your Octa Wallet Address. Keep the quotes(" ") by the way. 

```bash
{
  "priv": "your_B64_Private_Key",
  "addr": "octilebaslayancuzdanadresiniz",
  "rpc": "https://octra.network"
}
```

- CTRL + X and then Y, then hit Enter to save the file.
---

## Execute the Script

```bash
./target/release/ocs01-test
```

<img width="538" height="380" alt="image" src="https://github.com/user-attachments/assets/aa2bb395-6240-4e18-8a92-5191474fffce" />

---

**From here, you can chose from options 1 - 14 if you're good with math - but in this guide, we will be doing just 1 and 3 as these two seem like the most important ones.**

- 1 ; 

<img width="626" height="434" alt="Gw4_7lcWAAAZ34o" src="https://github.com/user-attachments/assets/b0710c41-7c92-4142-ac6e-721b0e4a45bb" />

- 3 ; 

<img width="551" height="508" alt="image" src="https://github.com/user-attachments/assets/2ebfbf1f-d364-4b86-b93d-74ada0a06f87" />


- Afer entering your prefereed choice, just hit ENTER to execute.
---

## HAVE FUN TESTING!
