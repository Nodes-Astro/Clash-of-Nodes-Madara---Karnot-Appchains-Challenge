# ClashOfNodes Madara KarnotAppchains Challenge
## First install dependencies

```
sudo apt update
sudo apt upgrade
sudo apt install build-essential
```
```
sudo apt install pkg-config
sudo apt install libssl-dev
sudo apt install clang
sudo apt install protobuf-compiler
```
## Install Rust

```
curl https://sh.rustup.rs -sSf | sh
```
```
source $HOME/.cargo/env
```
## Install Git & Docker

```
sudo apt install git-all
sudo apt install docker

```
## Install CLI

```
git clone https://github.com/karnotxyz/madara-cli
```
```
cd madara-cli
```
```
cargo build --release
```
## Initialize a new app chain. Select Avail as DA and fund the DA account
### To use faucet follow these instructions: 
https://docs.availproject.org/about/faucet/

```
./target/release/madara init
```
## Run your app chain:

```
cd madara-cli
screen -S run
```
```
./target/release/madara run
```
#### CTRL + A + D to exit

```
./target/release/madara explorer
```
#### Optionally, explore the StarkCompass explorer. Accessible at http://localhost:4000.
That's it, your madara app is running

##### If Needed, Host Your Appchain with Karnot: Karnot provides comprehensive, ready-to-use services for appchains, including RPC, proof, cross-chain capabilities, and more. Fill out this form to request hosting services:
https://docs.google.com/forms/d/e/1FAIpQLSdxqFdvI4iGewNL_N-8q8gEdJdtCeBMl9QSHp-uxnbN0RtfKA/viewform
#### Create a PR to Register Your Appchain: For your appchain to be recognized in the Clash of Nodes campaign, you must register it by submitting a pull request in the avail-campaign-listing repository. The PR should include a JSON configuration file named "listing.json" with the following structure:

### You need to add listing.json file in this format:
```
{
  "name": "my_app_chain",
  "logo": "https://placehold.co/400x400",
  "rpc_url": "https://rpc.mychain.xyz",
  "explorer_url": "https://explorer.mychain.xyz",
  "metrics_endpoint": "https://metrics.mychain.xyz",
  "id": "942ff35e-f048-4d10-ae61-6cb970cad2f0"
}
```
To create a json listing.json file run:
```
sudo touch listing
```
##### After created add your app infos and download

### Details

name: The name of your app chain.

logo: A image link for the logo of your app chain

rpc_url: A public endpoint for your app chain to make RPC calls (port 9944 by default)

explorer_url: A public endpoint where your app chain explorer is visible

metrics_endpoint: A public endpoint for your prometheus metrics (port 9615 by default)

id: Your node id

##### logo: You can use this website to get png url:
https://im.ge/upload
##### rpc-url format: "http://ipv4:9944/"
##### explorer_url: "http://ipv4:4000/"
##### metrics_endpoint: "http://ipv4:9615/"
##### id:
![image](https://github.com/Alping0/Clash-of-Nodes-Madara---Karnot-Appchains-Challenge/assets/105454859/cff17ec7-b8cd-4f9b-bd8e-145b78d9ac94)

### To create a Pull Request follow these steps:
##### Fork this repository:
https://github.com/karnotxyz/avail-campaign-listing

![image](https://github.com/Alping0/Clash-of-Nodes-Madara---Karnot-Appchains-Challenge/assets/105454859/6d858141-b9cf-474e-9f66-dc0893b3ea9a)

##### Upload listing.json file

![image](https://github.com/Alping0/Clash-of-Nodes-Madara---Karnot-Appchains-Challenge/assets/105454859/645a6cd2-eb5e-4704-bae3-ee89694a0bc9)

##### After upload create new pull request

![image](https://github.com/Alping0/Clash-of-Nodes-Madara---Karnot-Appchains-Challenge/assets/105454859/64b38ae0-fd99-48ad-9339-1b6ef7c047b7)

##### This configuration file includes essential details about your appchain, such as its name, logo URL, RPC endpoint, explorer URL, metrics endpoint, and a unique identifier. Ensure all information is accurate and up-to-date to facilitate smooth registration and participation in the campaign. Once the PR is merged, the appchain will appear on the Clash of Nodes Leaderboard.

![image](https://github.com/Alping0/Clash-of-Nodes-Madara---Karnot-Appchains-Challenge/assets/105454859/18f2404d-7c77-43e7-a61c-39f7bb951412)





                                                                                                                                                                                          



                                                                                                                                                                             







