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
sudo apt install docker.io
```
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

```
```
sudo chmod +x /usr/local/bin/docker-compose
```
```
docker-compose --version
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
## Initialize a new app chain. Select Sovereign as Settlement and Avail as DA also fund the DA account
### To use faucet follow these instructions: 
https://docs.availproject.org/about/faucet/

```
./target/release/madara init
```
## Run your app chain:

```
screen -S run
cd madara-cli
```
```
./target/release/madara run
```
#### After finished your logs will appear on the console

![image](https://github.com/Alping0/Clash-of-Nodes-Madara---Karnot-Appchains-Challenge/assets/105454859/ada11cd4-ed1d-47a2-ab44-52a2f0459e17)

#### CTRL + A + D to exit

## Let's match the data with explorer to view

```
./madara-cli/target/release/madara explorer --host=$(wget -qO- eth0.me)
```
#### Optionally, explore the StarkCompass explorer. Accessible at http://localhost:4000.
That's it, your madara app is running

## Let's generate app id from Avail for the leaderboard
https://app-id-gen.vercel.app/

![image](https://github.com/Alping0/Clash-of-Nodes-Madara---Karnot-Appchains-Challenge/assets/105454859/d69c9fb9-ac53-4816-a86f-be36052fd072)

#### You can import your Avail wallet to Polkadot.js or Talisman extension wallet to continue.
##### After connect your wallet write your appname and wait for getting appid.

![image](https://github.com/Alping0/Clash-of-Nodes-Madara---Karnot-Appchains-Challenge/assets/105454859/7b8003c5-9831-4ff3-96eb-2244bb0f277e)

##### Copy your app id to notepad we'll need to write it on da-config file

## Change your appid on config file

```
appname="Your appname goes here"
nano /root/.madara/app-chains/$appname/da-config.json
```
##### Delete quoation marks after you wrote your app id.

#### Change your app id 0 to what you get from previous step

#### Create a PR to Register Your Appchain: For your appchain to be recognized in the Clash of Nodes campaign, you must register it by submitting a pull request in the avail-campaign-listing repository. The PR should include a JSON configuration file named "your uid".json with the following structure:

##### Generate a random uid from here first: (This id is only for pr different than Avail app id)
https://www.uuidgenerator.net/

### You need to add "Your uid".json file in this format:
```
{
  "name": "my_app_chain",
  "logo": "https://placehold.co/400x400",
  "rpc_url": "http://ipv4:9944",
  "explorer_url": "http://ipv4:4000",
  "metrics_endpoint": "http://ipv4:9615/metrics",
  "id": "942ff35e-f048-4d10-ae61-6cb970cad2f0"
}
```
To create a json "Your id".json file run:
```
sudo touch "Your uid"
```
##### After created, add your app infos and download it on your desktop.

### Details

name: The name of your app chain.

logo: A image link for the logo of your app chain

rpc_url: A public endpoint for your app chain to make RPC calls (port 9944 by default)

explorer_url: A public endpoint where your app chain explorer is visible

metrics_endpoint: A public endpoint for your prometheus metrics (port 9615 by default)

id: Your node id

##### logo: You can use this website to get png url:
https://im.ge/upload
##### rpc-url format: "http://ipv4:9944"
##### explorer_url: "http://ipv4:4000"
##### metrics_endpoint: "http://ipv4:9615/metrics"
##### id: The id is a randomly generated uuid.


### To create a Pull Request follow these steps:
##### Fork this repository:
https://github.com/karnotxyz/avail-campaign-listing

![image](https://github.com/Alping0/Clash-of-Nodes-Madara---Karnot-Appchains-Challenge/assets/105454859/6d858141-b9cf-474e-9f66-dc0893b3ea9a)

##### Click on app_chains

![image](https://github.com/Alping0/Clash-of-Nodes-Madara---Karnot-Appchains-Challenge/assets/105454859/7ac719eb-9a5e-4ad5-b08e-b2ac27b85b78)

##### Upload "your uid".json file

![image](https://github.com/Alping0/Clash-of-Nodes-Madara---Karnot-Appchains-Challenge/assets/105454859/a416dc34-c92d-4400-854b-bd07d3f5db06)


##### After upload create new pull request

![image](https://github.com/Alping0/Clash-of-Nodes-Madara---Karnot-Appchains-Challenge/assets/105454859/64b38ae0-fd99-48ad-9339-1b6ef7c047b7)

##### This configuration file includes essential details about your appchain, such as its name, logo URL, RPC endpoint, explorer URL, metrics endpoint, and a unique identifier. Ensure all information is accurate and up-to-date to facilitate smooth registration and participation in the campaign. Once the PR is merged, the appchain will appear on the Clash of Nodes Leaderboard.

![image](https://github.com/Alping0/Clash-of-Nodes-Madara---Karnot-Appchains-Challenge/assets/105454859/18f2404d-7c77-43e7-a61c-39f7bb951412)

#### You may have trouble with the prettier, if you deal with the thats kind of issue:

![image](https://github.com/Alping0/Clash-of-Nodes-Madara---Karnot-Appchains-Challenge/assets/105454859/a39d80da-63bb-42cd-9d7a-82af09c9d332)

##### Try to copy with CTRL + A and paste it, check unnecessary spaces and delete all.





                                                                                                                                                                                          



                                                                                                                                                                             







