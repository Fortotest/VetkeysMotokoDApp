#  vetkeys-motoko DApp

![Internet Computer](https://img.shields.io/badge/Internet_Computer-ICP-blue?style=for-the-badge&logo=internetcomputer)
![Motoko](https://img.shields.io/badge/Motoko-orange?style=for-the-badge&logo=motoko)
![DFX](https://img.shields.io/badge/DFX-grey?style=for-the-badge)
![ICP Ninja](https://img.shields.io/badge/Made%20with-ICP%20Ninja-green?style=for-the-badge)

## 1. Project Definition

### What is this project?
Ini adalah DApp (Aplikasi Terdesentralisasi) *full-stack* yang berjalan di platform **Internet Computer (ICP)**. Proyek ini dibuat menggunakan *template* dari **ICP Ninja**.

Fokus dari *template* ini kemungkinan adalah untuk mendemonstrasikan penggunaan **vetKeys** (Verifiable-Encrypted Threshold Keys), sebuah fitur kriptografi canggih di ICP, yang ditulis dalam bahasa **Motoko**.

### Context: Migration from ICP Ninja
Proyek yang di-deploy melalui ICP Ninja bersifat sementara (biasanya 20 menit). Repositori ini berisi kode sumber yang telah diunduh agar dapat dilanjutkan pengembangannya secara lokal dan di-deploy secara permanen.

Dokumentasi ini akan memandu Anda melalui proses instalasi dan deployment lokal.

---

## 2. Tech Stack 🛠️

* **Blockchain:** [Internet Computer (ICP)](https://internetcomputer.org/)
* **Backend Canister:**
    * **Bahasa:** [Motoko](https://internetcomputer.org/docs/current/motoko/main/motoko)
    * **Package Manager:** [Mops](https://mops.one/) (diindikasikan oleh `BUILD.md`)
* **Frontend Canister:** HTML, CSS, JavaScript
* **Development Tooling:**
    * **SDK:** [DFINITY Canister SDK (DFX)](https://internetcomputer.org/docs/current/developer-docs/getting-started/install/)
    * **Lingkungan:** [Node.js](https://nodejs.org/en)

---

## 3. Project Structure

### Directory Structure
Struktur proyek ini mengikuti standar DApp ICP:

---

## 4. Local Setup & Installation 🚀

### Initial Installation
Untuk menjalankan dan melanjutkan pengembangan proyek ini di komputer Anda, ikuti langkah-langkah berikut.

1.  **Clone Repositori**
    ```bash
    git clone [https://github.com/Fortotest/vetkeys-motoko.git](https://github.com/Fortotest/vetkeys-motoko.git)
    cd vetkeys-motoko
    ```

2.  **Install DFX SDK**
    Jika Anda belum memilikinya, install DFINITY Canister SDK (DFX).
    ```bash
    sh -ci "$(curl -fsSL [https://internetcomputer.org/install.sh](https://internetcomputer.org/install.sh))"
    ```
    *Catatan: Di Windows, disarankan menggunakan [WSL2](https://learn.microsoft.com/en-us/windows/wsl/install).*

3.  **Install Node.js**
    Pastikan Anda memiliki [Node.js](https://nodejs.org/en) (versi LTS direkomendasikan) terinstal, karena DFX membutuhkannya.

4.  **Install Mops (Motoko Package Manager)**
    Proyek ini mungkin memerlukan dependensi Motoko. Install Mops untuk mengelolanya.
    ```bash
    npm install -g ic-mops
    ```

---

## 5. Running the DApp Locally

### Local Environment Setup
Langkah-langkah ini akan menjalankan aplikasi di komputer Anda.

1.  **Buat Identitas Lokal (Sangat Direkomendasikan)**
    Daripada menggunakan identitas `default`, buat identitas pengembangan baru yang aman.
    ```bash
    # Mulai replika lokal jika belum berjalan
    dfx start --background
    
    # Buat identitas baru (ganti NAMA_ANDA)
    dfx identity new NAMA_ANDA
    
    # Gunakan identitas baru tersebut
    dfx identity use NAMA_ANDA
    ```
    ***PENTING:*** *Simpan *seed phrase* yang muncul di tempat yang aman!*

2.  **Install Dependensi Node.js**
    Jika Anda belum melakukannya, jalankan:
    ```bash
    npm install
    ```

3.  **Deploy Canister Secara Lokal**
    Perintah ini akan membangun dan men-deploy semua canister (backend & frontend) ke replika lokal Anda.
    ```bash
    dfx deploy
    ```

4.  **Akses Frontend**
    Setelah deploy berhasil, DFX akan memberikan URL untuk canister frontend Anda. Buka URL tersebut (biasanya `http://127.0.0.1:4943/?canisterId=...`) di browser Anda.

---

## 6. Mainnet Deployment

### Acquiring Cycles
Deploy ke mainnet (jaringan publik ICP) membutuhkan "Cycles" untuk membayar komputasi dan penyimpanan.
* Anda bisa mendapatkan cycles gratis dari [ICP Faucet](https://faucet.dfinity.org/) untuk developer.
* Atau, Anda dapat mengonversi token ICP menjadi Cycles.

### Deploying to 'ic' (Mainnet)
Setelah Anda memiliki Cycles di *principal identity* Anda, jalankan:
```bash
dfx deploy --network ic
