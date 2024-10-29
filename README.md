# Proyek Java: Simulasi Transaksi Pembelian Gundam

Proyek ini adalah aplikasi untuk mensimulasikan transaksi pembelian Gundam. Aplikasi ini memungkinkan pelanggan untuk menambahkan produk Gundam ke keranjang belanja dan memproses transaksi dengan fitur diskon.

## Fitur
- Tambah produk Gundam ke keranjang belanja
- Proses transaksi dengan rincian harga
- Fitur diskon pada transaksi

## Cara Menjalankan
1. Clone repository: `git clone https://github.com/username/repository-name.git`
2. Buka proyek di IntelliJ IDEA atau editor pilihan Anda
3. Jalankan file `Main.java`

## Informasi Tambahan
- Pastikan Anda memiliki Java Development Kit (JDK) terinstal di sistem Anda.
- Untuk menambahkan diskon, gunakan metode `setDiskon` di kelas `Transaksi`.

## Kelas dan Metode Utama
- **Gundam**: Kelas yang merepresentasikan produk Gundam.
  - `Gundam(String nama, double harga, int stok)`
  - `getNama()`
  - `getHarga()`
  - `getStok()`
  
- **Pelanggan**: Kelas yang merepresentasikan pelanggan.
  - `Pelanggan(String nama)`
  - `tambahKeKeranjang(Gundam gundam)`
  - `getNama()`
  - `getKeranjang()`
  
- **Transaksi**: Kelas yang mengelola proses transaksi.
  - `Transaksi(Pelanggan pelanggan)`
  - `setDiskon(double diskon)`
  - `prosesTransaksi()`
  - `cetakInfoPelanggan()`
  - `cetakDaftarBelanja()`
  - `hitungTotalHarga()`
  
- **Main**: Kelas utama yang menjalankan program.
  - `main(String[] args)`

## Contoh Penggunaan
```java
// Daftar produk
Gundam gundam1 = new Gundam("Gundam RX-78-2", 500000, 10);
Gundam gundam2 = new Gundam("Gundam Barbatos", 750000, 5);

// Membuat pelanggan
Pelanggan pelanggan1 = new Pelanggan("Andi");

// Pelanggan membeli gundam
pelanggan1.tambahKeKeranjang(gundam1);
pelanggan1.tambahKeKeranjang(gundam2);

// Proses transaksi
Transaksi transaksi1 = new Transaksi(pelanggan1);
transaksi1.setDiskon(10); // Misalkan ada diskon 10%
transaksi1.prosesTransaksi();
