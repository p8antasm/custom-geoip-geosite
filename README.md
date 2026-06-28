# Daily Automated GeoIP/Geosite Builder

This repository automatically compiles and publishes custom `.dat` (GeoIP/not Geosite) database files for applications on a daily schedule.

## 🚀 How It Works
1. **Schedule Execution:** GitHub Actions triggers the workflow every day at 02:00 UTC.
3. **Data Fetching:** The script downloads the latest official database files from upstream repositories.
4. **Compilation:** The `v2fly/geoip` compiler merges, filters, and packages the data into a single custom `.dat` file.
5. **Release Update:** The finalized file and its SHA256 checksum are pushed to the GitHub Releases section under the `latest` tag, overwriting previous versions.

## 📥 Download Links
Your client can fetch the daily updated files using these permanent URLs:
* **Custom GeoIP:** `https://github.com/p8antasm/custom-geoip-geosite/releases/geoip.dat`
* **SHA256 Checksum:** `https://github.com/p8antasm/custom-geoip-geosite/releases/geoip.dat.sha256sum`

## 🛠 Project Structure
* `config.json` — Configuration file for the compiler. Defines data sources and custom country/routing rules.
* `.github/workflows/daily-build.yml` — GitHub Actions workflow automation script.
