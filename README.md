# Gaianet Auto Bot

Gaianet Auto Bot adalah skrip Bash otomatis yang dirancang untuk mengirim permintaan HTTP POST ke API Gaianet setiap 30 detik menggunakan kata kunci acak dari file `keywords.txt` yang sudah disediakan.

## Fitur

- Membaca kata kunci dari file `keywords.txt` yang telah disertakan dalam repository.
- Mengirim permintaan POST ke endpoint API Gaianet.
- Menampilkan respons penting (konten pesan) dengan jelas di terminal.
- Konfigurasi endpoint (URL) yang mudah diubah.

## Prasyarat

Untuk menjalankan skrip ini di Ubuntu, Anda hanya perlu menjalankan satu perintah untuk menginstal semua dependensi yang diperlukan:

```bash
sudo apt update && sudo apt install git curl jq -y
```

Perintah ini akan menginstal:

- **Git** untuk meng-clone repository,
- **cURL** untuk mengirim permintaan HTTP,
- **jq** untuk memproses data JSON.

## Instalasi

1. **Clone Repository**  
   Clone proyek ini ke sistem Anda:

   ```bash
   git clone https://github.com/caraka15/gaianet-bot.git
   cd gaianet-bot
   ```

2. **Edit URL API**  
   Buka file `run.sh` dan ubah baris berikut sesuai dengan Node ID Anda:

   ```bash
   URL="https://NodeId.gaia.domains/v1/chat/completions"
   ```

   Ganti `NodeId` dengan ID node yang Anda miliki.

3. **Berikan Izin Eksekusi**  
   Berikan izin eksekusi pada file `run.sh`:

   ```bash
   chmod +x run.sh
   ```

4. **Jalankan Skrip**  
   Jalankan skrip dengan perintah berikut:
   ```bash
   ./run.sh
   ```

## Contoh Output

```
Mengirim request dengan kata kunci: where is Paris
Response diterima:
Paris is located in northern central France.
------------------------------------
Menunggu 30 detik sebelum request berikutnya...
```

## Konfigurasi Tambahan

- **Interval Waktu**: Anda dapat mengubah interval pengiriman request dengan mengedit variabel `INTERVAL` di file `run.sh`.  
  Contoh:
  ```bash
  INTERVAL=60  # Mengirim request setiap 60 detik
  ```

## File yang Disertakan

- `run.sh`: Skrip utama untuk mengirim permintaan.
- `keywords.txt`: File berisi daftar kata kunci yang akan digunakan.

## Catatan

- Pastikan URL API (`NodeId`) benar sebelum menjalankan skrip.
- Pastikan file `keywords.txt` tersedia dan berisi setidaknya satu kata kunci.

## Donasi

Jika Anda merasa terbantu dengan bot ini, Anda dapat memberikan dukungan melalui:

- Crypto: `0xede7fa099638d4f39931d2df549ac36c90dfbd26`
- Saweria: [https://saweria.co/crxanode](https://saweria.co/crxanode)
