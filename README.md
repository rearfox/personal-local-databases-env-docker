## How to Use 

## 📂 Directory Structure

```
~/
├── personal-local-databases-env-docker/
│   ├── mysql-phpmyadmin/
│   │   └── docker-compose.yml
│   └── mongo-express/
│       └── docker-compose.yml
└── .mysql/
    └── docker-compose.yml  <-- the selected config to run
```

---

## ⚙️ Usage Options

### ✅ Option A: Clone from Repository

#### 1. Clone the Repository

```bash
git clone git@github.com:rearfox/personal-local-env-docker
```

#### 2. Create the `.mysql` Directory

```bash
mkdir ~/.mysql
```

#### 3. Copy the Desired Docker Compose File

Choose between MySQL or MongoDB:

**For MySQL + phpMyAdmin:**

```bash
cp personal-local-env-docker/mysql-phpmyadmin/docker-compose.yml ~/.mysql/
```

**For MongoDB + Mongo Express:**

```bash
cp personal-local-env-docker/mongo-express/docker-compose.yml ~/.mysql/
```

### ✅ Option B: Download `docker-compose.yml` Directly

#### 1. Create `.mysql` Folder

```bash
mkdir ~/.mysql
```

#### 2. Download Compose File or Copy and paste 


---

### 4. Set File Permissions

```bash
chmod 755 ~/.mysql
```

> If needed for full:

```bash
chmod 777 ~/.mysql
```

### 5. Run Docker Compose

```bash
cd ~/.mysql
docker compose up -d
```

---

## 🐬 Accessing the Services

Depending on which configuration you use: you can always change the ports and everything

### For MySQL + phpMyAdmin: 

* **phpMyAdmin:** [http://localhost:9090](http://localhost:9090)
* **MySQL:** Accessible from database clients or apps

### For MongoDB + Mongo Express:

* **Mongo Express:** [http://localhost:9191](http://localhost:9191)
* **MongoDB:** Accessible from MongoDB clients or drivers

#### Default Credentials:

| Service       | Username                | Password |
| ------------- | ----------------------- | -------- |
| MySQL Server  | `root`                  | `root`   |
| phpMyAdmin    | Use MySQL credentials   |          |
| MongoDB       | `admin`                 | `admin`  |
| Mongo Express | Use MongoDB credentials |          |
 
---

## 🧼 Shutdown

To stop the containers:

```bash
$ ~/.mysql
docker compose down
```

---

## 🗘️ Note for WSL (Windows Subsystem for Linux) Users

1. Make sure **Docker Desktop** is installed and running on Windows.
2. Open **Docker Desktop > Settings > Resources > WSL Integration**.
3. Enable integration for your WSL distro (e.g. Ubuntu).
4. Restart the terminal or run `wsl --shutdown`.
5. Check if Docker is accessible from WSL:

   ```bash
   docker info
   ```

---

