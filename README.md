# Sixgpt

# About
SixGPT is a decentralized synthetic data generation platform built on the Vana network. We empower users by giving them ownership of their data and enabling them to earn from it.
The SixGPT Miner is a software package which allows users to contribute data they generate for wikipedia question-answer based tasks to the network for rewards. In the future, we will support other tasks such as chatbot conversations, image captioning, etc.

# Prerequisites
- Fund your wallet with at least 0.1 $VANA
- Login with this wallet on sixgpt.xyz

# Run the miner
```yaml
sudo apt-get update && \
sudo apt-get install -y ca-certificates curl && \
sudo install -m 0755 -d /etc/apt/keyrings && \
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc && \
sudo chmod a+r /etc/apt/keyrings/docker.asc && \
echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null && \
sudo apt-get update && \
sudo apt-get install -y docker-ce docker-ce-cli containerd.io
```
```yaml
git clone https://github.com/sixgpt/miner.git
cd miner
```
```yaml
nano .env
```
Let's enter the following codes into nano .env

```yaml
VANA_PRIVATE_KEY=abcdefabcef
VANA_NETWORK=mainnet
OLLAMA_API_URL=http://ollama:11434/api
```
# Run the miner:
```yaml
docker-compose up -d
```
# Check miner logs:
```yaml
docker-compose logs -f
```
# Notes
- You must have logged into sixgpt.xyz with your wallet before running the miner
- Make sure the wallet associated with your vana private key has enough $VANA balance on the desired network (at least 0.1)

