<div align="center">

# ⛏ TemkaMiner-pearl-gpu-miner (PRL)

**High-performance GPU miner for Pearl (PRL)**

![Version](https://img.shields.io/badge/version-1.0-informational)
![Coin](https://img.shields.io/badge/coin-Pearl%20%28PRL%29-8A2BE2)
![Platform](https://img.shields.io/badge/platform-Windows%20x64-0078D6)
![NVIDIA](https://img.shields.io/badge/NVIDIA-RTX%2030%2F40%2F50-76B900)
![Dev fee](https://img.shields.io/badge/dev%20fee-1%25-2ea44f)

</div>

```
  █████ █████ █   █ █   █  ███    █   █ █████ █   █ █████ ████
    █   █     ██ ██ █  █  █   █   ██ ██   █   ██  █ █     █   █
    █   ████  █ █ █ ███   █████   █ █ █   █   █ █ █ ████  ████
    █   █     █   █ █  █  █   █   █   █   █   █  ██ █     █  █
    █   █████ █   █ █   █ █   █   █   █ █████ █   █ █████ █   █
```

TemkaMiner is a fast, self-contained miner for **Pearl (PRL)**. It is heavily tuned for
the **RTX 5080** (~185–190 TH/s) and runs on modern **NVIDIA RTX** cards (30, 40 and 50
series and newer). One small `.exe`, no installer, no dependencies beyond your GPU driver.

---

## ✨ Features

- 🚀 **~185–190 TH/s** on an RTX 5080 — at the silicon ceiling
- 📊 **Live dashboard** — per-GPU hashrate with rolling **1h / 3h / 24h** averages, plus temp, fan, power, clocks and VRAM (NVML)
- 🧩 **Multi-GPU from one process** — `--all-gpus`, nonce-striped so cards never duplicate work
- 🌐 **Multi-pool** — BaikalMine, HeroMiners and other LuckyPool-protocol pools
- 📦 **One portable binary** — runs RTX 30/40/50-series and data-center GPUs
- 🔌 **Zero install** — the CUDA runtime is built in; you only need your NVIDIA driver

## 🖥 Dashboard

```
  TemkaMiner v1.0  · Pearl (PRL) NoisyGEMM PoW
  ──────────────────────────────────────────────────────────────
  Pool    pearl.baikalmine.com:2010
  Miner   prl1pz6u…djftxy.rig1
  Driver  596.49 · batch 8
  GPUs    1 detected
    [0] NVIDIA GeForce RTX 5080 · 16 GB  ⛏ mining
  ──────────────────────────────────────────────────────────────

[09:14:07] JOB    93b5590f_1572864  ·  height 67597  ·  batch 8
[09:14:31] ★ HIT  nonce 115  ·  proof 143840B  ·  submitting…
[09:14:31] ✓ SHARE ACCEPTED  312 / 0
[09:14:37] GPU0  192.92 TH/s  │ 1h 193 · 3h 193 · 24h 193 TH/s │ 67°C 100% 360W 2722 MHz 99% │ ⬆ 312
[09:14:37] ── up 9:42:11 · 1 GPU · total 192.92 TH/s · ✓312 ✗0 ──
```

## 🖥 Supported GPUs

| GPU | Status |
|---|---|
| RTX 5070 / 5080 / 5090 | ✅ supported — tuned |
| RTX 4060 … 4090 | ✅ supported |
| RTX 3060 … 3090 | ✅ supported |
| A100 / H100 (data-center) | ✅ supported |
| GTX 16xx, RTX 20xx and older | ❌ not supported |

> Performance is tuned for the RTX 5080. Other cards mine correctly but may not reach their individual peak.

## 🚀 Quick start (Windows)

1. **Download** the latest release and unzip it anywhere.
2. **Edit `start.bat`** — set your Pearl wallet in `WALLET=` (and the pool/worker if you like).
3. **Double-click `start.bat`**.

To use every GPU in the rig, run **`start-all-gpus.bat`** instead.

## 🐧 Linux

> The file attached to this release is the **Windows** build. The Linux build is a
> separate native binary named `TemkaMiner` (no `.exe`) — the Windows executable does
> not run on Linux.

Run it from a terminal:

```bash
chmod +x TemkaMiner
./TemkaMiner --pool pearl.baikalmine.com:2010 --wallet YOUR_PRL_WALLET --worker rig1
# add  --all-gpus  to mine on every GPU in the rig
```

…or put your wallet into a `start.sh` and run `bash start.sh`:

```bash
#!/usr/bin/env bash
cd "$(dirname "$0")"
WALLET="PUT_YOUR_PRL_WALLET_HERE"
./TemkaMiner --pool pearl.baikalmine.com:2010 --wallet "$WALLET" --worker rig1 --batch 8 "$@"
```

**Requirements:** an up-to-date NVIDIA driver only — the CUDA runtime is built in, so
there is no CUDA toolkit to install.

## 🌐 Pools

Set `POOL=` in the `.bat` to any of these (or any LuckyPool-protocol Pearl pool):

| Pool | Endpoint |
|---|---|
| BaikalMine | `pearl.baikalmine.com:2010` |
| HeroMiners | `pearl.herominers.com:1200`  (also `de.` / `ru.` / `us.`) |

## ⚙ Command-line options

| Option | Default | Description |
|---|---|---|
| `--wallet <addr>` | — | Your PRL wallet **(required)** |
| `--worker <name>` | `rig1` | Worker name shown on the pool |
| `--pool <host:port>` | BaikalMine | Mining pool |
| `--batch <n>` | `8` | Nonces per GPU launch |
| `--all-gpus` | off | Mine on every detected GPU |
| `--devices 0,1,2` | — | Mine on specific GPUs only |
| `--stats <sec>` | `30` | Dashboard refresh interval |
| `--version` | — | Print the version and exit |

## 💸 Developer fee

TemkaMiner charges a transparent **1% developer fee**. It is **time-based** — roughly one
minute out of every ~100 is mined to the developer, the rest is 100% yours. The fee is
announced in the console at startup. There are no hidden fees.

## 🛡 Antivirus

GPU miners are **routinely flagged as false positives** by antivirus software — this is
true of *every* miner, not just this one. If your AV quarantines the file, add a folder
exclusion. The binary is **not** packed or obfuscated.

## 📄 License

See [`LICENSE.txt`](LICENSE.txt). Distributed as a binary only; reverse engineering and
modification are not permitted.

<div align="center">
<sub>Made for the Pearl community ⛏</sub>
</div>
