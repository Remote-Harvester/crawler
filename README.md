# RemoteHarvester — Crawler

This Python module implements the core crawling logic for **RemoteHarvester**.

The goal of this package is to fetch remote-friendly job postings from supported
sources and write normalized records into a PostgreSQL database.

> ⚠️ At this stage, the module is still under active development and the public
> API may change.

## 📦 Installation (local development)

Clone the repository:

```bash
git clone https://github.com/Remote-Harvester/crawler.git
cd crawler
```

Create and activate a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## 🧩 Usage (local)

To run the crawler locally and execute all available sources, use:

```bash
python -m src.main
```

## 🐋 Docker

This module is designed to run inside a Docker container so it can execute
consistently across environments (local, CI, or Kubernetes).

### 1️⃣ Build the image

From the repository root:

```bash
docker build -t crawler:latest .
```

### 2️⃣ Run the container

```bash
 docker run --rm crawler:latest
```

## 📜 License

This repository is open-source and distributed under the MIT License.
See the [`LICENSE`](LICENSE) file for details.