# arbi-full-node

```
mkdir -p ~/data/arbitrum
chmod -fR 777 ~/data/arbitrum
sudo apt install docker.io -y
docker run -d -v ~/data/arbitrum:/home/user/.arbitrum -p 0.0.0.0:8547:8547 -p 0.0.0.0:8548:8548 offchainlabs/nitro-node:v2.0.11-8e786ec --l1.url <l1-url> --l2.chain-id=42161 --http.api=net,web3,eth,debug --http.corsdomain=* --http.addr=0.0.0.0 --http.vhosts=* --init.url="https://snapshot.arbitrum.io/mainnet/nitro.tar"
docker ps -a
docker logs --tail 100 <container-i>
```

**Komutları, <> sembolleri ve arasındaki yazı ile ilgili değerleri değiştirerek kullabilirsiniz.**
Örnek:
```
docker run -d -v ~/data/arbitrum:/home/user/.arbitrum -p 0.0.0.0:8547:8547 -p 0.0.0.0:8548:8548 offchainlabs/nitro-node:v2.0.11-8e786ec --l1.url https://eth-mainnet.g.alchemy.com/v2/Mq9JNICpSyC5NGC --l2.chain-id=42161 --http.api=net,web3,eth,debug --http.corsdomain=* --http.addr=0.0.0.0 --http.vhosts=* --init.url="https://snapshot.arbitrum.io/mainnet/nitro.tar"
```

```
docker logs --tail 100 a6aea82506c8
```

6 Cpu
8 Gb RAM
1200 Gb SSD Hafızaya sahip bir makina yeterli olacaktır.
