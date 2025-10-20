#  vetkeys-motoko DApp

![Internet Computer](https://img.shields.io/badge/Internet_Computer-ICP-blue?style=for-the-badge&logo=internetcomputer)
![Motoko](https://img.shields.io/badge/Motoko-orange?style=for-the-badge&logo=motoko)
![DFX](https://img.shields.io/badge/DFX-grey?style=for-the-badge)
![ICP Ninja](https://img.shields.io/badge/Made%20with-ICP%20Ninja-green?style=for-the-badge)

## 1. Project Definition

### What is this project?
Ini adalah DApp (Aplikasi Terdesentralisasi) *full-stack* yang berjalan di platform **Internet Computer (ICP)**. Proyek ini dibuat menggunakan *template* dari **ICP Ninja**.

Fokus dari *template* ini kemungkinan adalah untuk mendemonstrasikan penggunaan **vetKeys** (Verifiable-Encrypted Threshold Keys), sebuah fitur kriptografi canggih di ICP, yang ditulis dalam bahasa **Motoko**.

### Konteks: Migrasi dari ICP Ninja
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

### Struktur Direktori
Struktur proyek ini mengikuti standar DApp ICP:
