# Sixgpt

# About
SixGPT, Vana ağı üzerine inşa edilmiş merkezi olmayan bir sentetik veri üretim platformudur. Kullanıcılara verilerinin sahipliğini vererek ve bundan kazanç elde etmelerini sağlayarak onları güçlendiriyoruz. SixGPT Miner, kullanıcıların wikipedia soru-cevap tabanlı görevler için ürettikleri verileri ödüller karşılığında ağa katkıda bulunmalarını sağlayan bir yazılım paketidir. Gelecekte, sohbet robotu konuşmaları, resim altyazısı vb. gibi diğer görevleri de destekleyeceğiz,

# Prerequisites
- Cüzdanınıza en az 0,1 $VANA ile para yatırın
- Bu cüzdan ile buraya giriş yapın sixgpt.xyz

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
Aşağıdaki kodları nano .env dosyasına girelim

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
- Madenciyi çalıştırmadan önce sixgpt.xyz'e cüzdanınızla giriş yapmış olmalısınız
- Vana özel anahtarınızla ilişkili cüzdanınızda yeterli $VANA bakiyesine sahip olduğundan emin olun (mainnet'te en az 0,1)

