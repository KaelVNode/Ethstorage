# Ethstorage

Tutorial ETH Storage BLOB Storage Race (Use VPS Ubuntu 22)  😎😊

1️⃣ Install Docker

````
sudo apt-get update && \
sudo apt-get install -y apt-transpo# Ethstorage

Tutorial ETH Storage BLOB Storage Race (Use VPS Ubuntu 22)  😎😊

1️⃣ Install Docker

````
sudo apt-get update && \
sudo apt-get install -y apt-transport-https ca-certificates curl software-properties-common gnupg && \
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg && \
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null && \
sudo apt-get update && \
sudo apt-get install -y docker-ce docker-ce-cli containerd.io

```

2️⃣ OPEN PORT

````
sudo ufw allow 22
sudo ufw allow 9545
sudo ufw allow 9222
sudo ufw allow 30305/udp
sudo ufw enable
```
3️⃣ SIAPIN BAHAN BAHAN DI BAWAH

<miner> = Isi Address 0x Kita
<private_key> = Ganti Dengan Private Key Wallet kalian

➡️ Create Api Untuk Ganti <el_rpc>

➖ Create Account and Login : https://dashboard.blockpi.io/workbench/dashboard
➖ Get Started > Free Package Gift
➖ Klik Generate API Key
➖ Pilih Ethereum Sepolia
➖ Copy Link Http
➖ Taruh di <el_rpc> (Tanpa <>)

➡️ Create Endpoints Untuk Ganti  <cl_rpc>

➖ Create Endpoint : https://dashboard.quicknode.com/endpoints/new
➖ Pilih Ethereum Sepolia
➖ Pilih Compile Safety
➖ Pilih Endpoints Armor
➖ Select Plan $0 > Individual
➖ Isi Data
➖ Payment Menthod (Isi Kredit Card Bank Jago)
➖ Create Endpoints
➖ Copy Link Http Provider
➖ Taruh di <cl_rpc> (Tanpa <>)

4️⃣Run Docker Edit Semua Data Yang di Minta, Jalankan di Vps  :

docker run --name es  -d  \
          -v ./es-data:/es-node/es-data \
          -e ES_NODE_STORAGE_MINER=<miner> \
          -e ES_NODE_SIGNER_PRIVATE_KEY=<private_key> \
          -p 9545:9545 \
          -p 9222:9222 \
          -p 30305:30305/udp \
          --entrypoint /es-node/run.sh \
          ghcr.io/ethstorage/es-node:v0.1.9 \
          --l1.rpc <el_rpc> \
          --l1.beacon <cl_rpc>

5️⃣ CHECK LOG 

docker logs -f es 

😂 PERHATIKAN OUPUT YANG KELUAR (BIARKAN SAJA JALAN SAMPAI 3 TAHAP / COMMAND DI BAWAH GAK PERLU DI PASTE DI TERMINAL VPS0

➡️ Data sync phase (Ouputnya)

INFO [01-18|09:13:32.564] Storage sync in progress progress=85.50% peerCount=2 syncTasksRemain=1@0 blobsSynced=1@128.00KiB blobsToSync=0 fillTasksRemain=30 emptyFilled=3,586,176@437.77GiB emptyToFill=608,127   timeUsed=1h48m7.556s  eta=18m20.127s

➡️ Sampling phase (Ouputnya)

INFO [01-19|05:02:23.210] Mining info retrieved                    shard=0 LastMineTime=1,705,634,628 Difficulty=4,718,592,000 proofsSubmitted=6
INFO [01-19|05:02:23.210] Mining tasks assigned                    shard=0 threads=64 block=10,397,712 nonces=1,048,576
INFO [01-19|05:02:26.050] The nonces are exhausted in this slot, waiting for the next block samplingTime=2.8s shard=0 block=10,397,712

➡️ Proof submission phase (Ouputnya)

INFO [01-19|05:02:23.210] Calculated a valid hash                  shard=0 thread=3 block=5,437,371 nonce=58101
INFO [01-19|05:05:23.210] Mining transaction confirmed"            txHash=0x7afa13e5211c403a7024bdf0a6880203d54698355679be9aab1aa0ecef78eecd
INFO [01-19|05:05:23.210] Mining transaction success! √            miner=0xBB9D13efa21c0a053eCFE622e2AbfAF0D7573f50

6️⃣Kalo udah Sampe 3 Tap di Atas Check Your Address di : https://grafana.ethstorage.io/
rt-https ca-certifi# Ethstorage

Tutorial ETH Storage BLOB Storage Race (Use VPS Ubuntu 22)  😎😊

1️⃣ Install Docker

````
sudo apt-get update && \
sudo apt-get install -y apt-transpo# Ethstorage

Tutorial ETH Storage BLOB Storage Race (Use VPS Ubuntu 22)  😎😊

1️⃣ Install Docker

````
sudo apt-get update && \
sudo apt-get install -y apt-transport-https ca-certificates curl software-properties-common gnupg && \
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg && \
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null && \
sudo apt-get update && \
sudo apt-get install -y docker-ce docker-ce-cli containerd.io

```

2️⃣ OPEN PORT

````
sudo ufw allow 22
sudo ufw allow 9545
sudo ufw allow 9222
sudo ufw allow 30305/udp
sudo ufw enable
```
3️⃣ SIAPIN BAHAN BAHAN DI BAWAH

<miner> = Isi Address 0x Kita
<private_key> = Ganti Dengan Private Key Wallet kalian

➡️ Create Api Untuk Ganti <el_rpc>

➖ Create Account and Login : https://dashboard.blockpi.io/workbench/dashboard
➖ Get Started > Free Package Gift
➖ Klik Generate API Key
➖ Pilih Ethereum Sepolia
➖ Copy Link Http
➖ Taruh di <el_rpc> (Tanpa <>)

➡️ Create Endpoints Untuk Ganti  <cl_rpc>

➖ Create Endpoint : https://dashboard.quicknode.com/endpoints/new
➖ Pilih Ethereum Sepolia
➖ Pilih Compile Safety
➖ Pilih Endpoints Armor
➖ Select Plan $0 > Individual
➖ Isi Data
➖ Payment Menthod (Isi Kredit Card Bank Jago)
➖ Create Endpoints
➖ Copy Link Http Provider
➖ Taruh di <cl_rpc> (Tanpa <>)

4️⃣Run Docker Edit Semua Data Yang di Minta, Jalankan di Vps  :

docker run --name es  -d  \
          -v ./es-data:/es-node/es-data \
          -e ES_NODE_STORAGE_MINER=<miner> \
          -e ES_NODE_SIGNER_PRIVATE_KEY=<private_key> \
          -p 9545:9545 \
          -p 9222:9222 \
          -p 30305:30305/udp \
          --entrypoint /es-node/run.sh \
          ghcr.io/ethstorage/es-node:v0.1.9 \
          --l1.rpc <el_rpc> \
          --l1.beacon <cl_rpc>

5️⃣ CHECK LOG 

docker logs -f es 

😂 PERHATIKAN OUPUT YANG KELUAR (BIARKAN SAJA JALAN SAMPAI 3 TAHAP / COMMAND DI BAWAH GAK PERLU DI PASTE DI TERMINAL VPS0

➡️ Data sync phase (Ouputnya)

INFO [01-18|09:13:32.564] Storage sync in progress progress=85.50% peerCount=2 syncTasksRemain=1@0 blobsSynced=1@128.00KiB blobsToSync=0 fillTasksRemain=30 emptyFilled=3,586,176@437.77GiB emptyToFill=608,127   timeUsed=1h48m7.556s  eta=18m20.127s

➡️ Sampling phase (Ouputnya)

INFO [01-19|05:02:23.210] Mining info retrieved                    shard=0 LastMineTime=1,705,634,628 Difficulty=4,718,592,000 proofsSubmitted=6
INFO [01-19|05:02:23.210] Mining tasks assigned                    shard=0 threads=64 block=10,397,712 nonces=1,048,576
INFO [01-19|05:02:26.050] The nonces are exhausted in this slot, waiting for the next block samplingTime=2.8s shard=0 block=10,397,712

➡️ Proof submission phase (Ouputnya)

INFO [01-19|05:02:23.210] Calculated a valid hash                  shard=0 thread=3 block=5,437,371 nonce=58101
INFO [01-19|05:05:23.210] Mining transaction confirmed"            txHash=0x7afa13e5211c403a7024bdf0a6880203d54698355679be9aab1aa0ecef78eecd
INFO [01-19|05:05:23.210] Mining transaction success! √            miner=0xBB9D13efa21c0a053eCFE622e2AbfAF0D7573f50

6️⃣Kalo udah Sampe 3 Tap di Atas Check Your Address di : https://grafana.ethstorage.io/
rt-https ca-certificates curl software-properties-common gnupg && \
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg && \
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null && \
sudo apt-get update && \
sudo apt-get install -y docker-ce docker-ce-cli containerd.io

```

2️⃣ OPEN PORT

````
sudo ufw allow 22
sudo ufw allow 9545
sudo ufw allow 9222
sudo ufw allow 30305/udp
sudo ufw enable
```
3️⃣ SIAPIN BAHAN BAHAN DI BAWAH

<miner> = Isi Address 0x Kita
<private_key> = Ganti Dengan Private Key Wallet kalian

➡️ Create Api Untuk Ganti <el_rpc>

➖ Create Account and Login : https://dashboard.blockpi.io/workbench/dashboard
➖ Get Started > Free Package Gift
➖ Klik Generate API Key
➖ Pilih Ethereum Sepolia
➖ Copy Link Http
➖ Taruh di <el_rpc> (Tanpa <>)

➡️ Create Endpoints Untuk Ganti  <cl_rpc>

➖ Create Endpoint : https://dashboard.quicknode.com/endpoints/new
➖ Pilih Ethereum Sepolia
➖ Pilih Compile Safety
➖ Pilih Endpoints Armor
➖ Select Plan $0 > Individual
➖ Isi Data
➖ Payment Menthod (Isi Kredit Card Bank Jago)
➖ Create Endpoints
➖ Copy Link Http Provider
➖ Taruh di <cl_rpc> (Tanpa <>)

4️⃣Run Docker Edit Semua Data Yang di Minta, Jalankan di Vps  :

docker run --name es  -d  \
          -v ./es-data:/es-node/es-data \
          -e ES_NODE_STORAGE_MINER=<miner> \
          -e ES_NODE_SIGNER_PRIVATE_KEY=<private_key> \
          -p 9545:9545 \
          -p 9222:9222 \
          -p 30305:30305/udp \
          --entrypoint /es-node/run.sh \
          ghcr.io/ethstorage/es-node:v0.1.9 \
          --l1.rpc <el_rpc> \
          --l1.beacon <cl_rpc>

5️⃣ CHECK LOG 

docker logs -f es 

😂 PERHATIKAN OUPUT YANG KELUAR (BIARKAN SAJA JALAN SAMPAI 3 TAHAP / COMMAND DI BAWAH GAK PERLU DI PASTE DI TERMINAL VPS0

➡️ Data sync phase (Ouputnya)

INFO [01-18|09:13:32.564] Storage sync in progress progress=85.50% peerCount=2 syncTasksRemain=1@0 blobsSynced=1@128.00KiB blobsToSync=0 fillTasksRemain=30 emptyFilled=3,586,176@437.77GiB emptyToFill=608,127   timeUsed=1h48m7.556s  eta=18m20.127s

➡️ Sampling phase (Ouputnya)

INFO [01-19|05:02:23.210] Mining info retrieved                    shard=0 LastMineTime=1,705,634,628 Difficulty=4,718,592,000 proofsSubmitted=6
INFO [01-19|05:02:23.210] Mining tasks assigned                    shard=0 threads=64 block=10,397,712 nonces=1,048,576
INFO [01-19|05:02:26.050] The nonces are exhausted in this slot, waiting for the next block samplingTime=2.8s shard=0 block=10,397,712

➡️ Proof submission phase (Ouputnya)

INFO [01-19|05:02:23.210] Calculated a valid hash                  shard=0 thread=3 block=5,437,371 nonce=58101
INFO [01-19|05:05:23.210] Mining transaction confirmed"            txHash=0x7afa13e5211c403a7024bdf0a6880203d54698355679be9aab1aa0ecef78eecd
INFO [01-19|05:05:23.210] Mining transaction success! √            miner=0xBB9D13efa21c0a053eCFE622e2AbfAF0D7573f50

6️⃣Kalo udah Sampe 3 Tap di Atas Check Your Address di : https://grafana.ethstorage.io/
cates curl software-properties-common gnupg && \
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg && \
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null && \
sudo apt-get update && \
sudo apt-get install -y docker-ce docker-ce-cli containerd.io

```

2️⃣ OPEN PORT

````
sudo ufw allow 22
sudo ufw allow 9545
sudo ufw allow 9222
sudo ufw allow 30305/udp
sudo ufw enable
```
3️⃣ SIAPIN BAHAN BAHAN DI BAWAH

<miner> = Isi Address 0x Kita
<private_key> = Ganti Dengan Private Key Wallet kalian

➡️ Create Api Untuk Ganti <el_rpc>

➖ Create Account and Login : https://dashboard.blockpi.io/workbench/dashboard
➖ Get Started > Free Package Gift
➖ Klik Generate API Key
➖ Pilih Ethereum Sepolia
➖ Copy Link Http
➖ Taruh di <el_rpc> (Tanpa <>)

➡️ Create Endpoints Untuk Ganti  <cl_rpc>

➖ Create Endpoint : https://dashboard.quicknode.com/endpoints/new
➖ Pilih Ethereum Sepolia
➖ Pilih Compile Safety
➖ Pilih Endpoints Armor
➖ Select Plan $0 > Individual
➖ Isi Data
➖ Payment Menthod (Isi Kredit Card Bank Jago)
➖ Create Endpoints
➖ Copy Link Http Provider
➖ Taruh di <cl_rpc> (Tanpa <>)

4️⃣Run Docker Edit Semua Data Yang di Minta, Jalankan di Vps  :

docker run --name es  -d  \
          -v ./es-data:/es-node/es-data \
          -e ES_NODE_STORAGE_MINER=<miner> \
          -e ES_NODE_SIGNER_PRIVATE_KEY=<private_key> \
          -p 9545:9545 \
          -p 9222:9222 \
          -p 30305:30305/udp \
          --entrypoint /es-node/run.sh \
          ghcr.io/ethstorage/es-node:v0.1.9 \
          --l1.rpc <el_rpc> \
          --l1.beacon <cl_rpc>

5️⃣ CHECK LOG 

docker logs -f es 

😂 PERHATIKAN OUPUT YANG KELUAR (BIARKAN SAJA JALAN SAMPAI 3 TAHAP / COMMAND DI BAWAH GAK PERLU DI PASTE DI TERMINAL VPS0

➡️ Data sync phase (Ouputnya)

INFO [01-18|09:13:32.564] Storage sync in progress progress=85.50% peerCount=2 syncTasksRemain=1@0 blobsSynced=1@128.00KiB blobsToSync=0 fillTasksRemain=30 emptyFilled=3,586,176@437.77GiB emptyToFill=608,127   timeUsed=1h48m7.556s  eta=18m20.127s

➡️ Sampling phase (Ouputnya)

INFO [01-19|05:02:23.210] Mining info retrieved                    shard=0 LastMineTime=1,705,634,628 Difficulty=4,718,592,000 proofsSubmitted=6
INFO [01-19|05:02:23.210] Mining tasks assigned                    shard=0 threads=64 block=10,397,712 nonces=1,048,576
INFO [01-19|05:02:26.050] The nonces are exhausted in this slot, waiting for the next block samplingTime=2.8s shard=0 block=10,397,712

➡️ Proof submission phase (Ouputnya)

INFO [01-19|05:02:23.210] Calculated a valid hash                  shard=0 thread=3 block=5,437,371 nonce=58101
INFO [01-19|05:05:23.210] Mining transaction confirmed"            txHash=0x7afa13e5211c403a7024bdf0a6880203d54698355679be9aab1aa0ecef78eecd
INFO [01-19|05:05:23.210] Mining transaction success! √            miner=0xBB9D13efa21c0a053eCFE622e2AbfAF0D7573f50

6️⃣Kalo udah Sampe 3 Tap di Atas Check Your Address di : https://grafana.ethstorage.io/
