# Cuaca Kalteng

Aplikasi Flutter sederhana untuk melihat cuaca saat ini di beberapa kabupaten/kota di Kalimantan Tengah. Data diambil dari [Open-Meteo API](https://open-meteo.com/) (gratis, tanpa API key).

## Fitur

- Memilih kabupaten/kota lewat dropdown
- Menampilkan suhu (°C), kecepatan angin (km/h), dan kode cuaca (weather code)
- Indikator loading dan pesan error saat koneksi atau server bermasalah

## Daftar Kota

- Palangkaraya
- Sampit (Kotim)
- Pangkalan Bun (Kobar)
- Muara Teweh (Barito Utara)
- Kuala Kapuas (Kapuas)
- Buntok (Barito Selatan)
- Puruk Cahu (Murung Raya)

## Struktur Proyek

```
lib/
├── main.dart            # UI dan logika pengambilan data cuaca
└── weather_model.dart   # Model KaltengCity dan CurrentWeather
```

## Teknologi

- Flutter & Dart
- Package [`http`](https://pub.dev/packages/http)
- Open-Meteo API

## Cara Menjalankan

1. Pastikan [Flutter SDK](https://docs.flutter.dev/get-started/install) sudah terpasang.
2. Tambahkan dependensi `http` di `pubspec.yaml`:

   ```yaml
   dependencies:
     http: ^1.2.0
   ```

3. Pasang dependensi:

   ```bash
   flutter pub get
   ```

4. Jalankan aplikasi (pastikan perangkat/emulator terhubung internet):

   ```bash
   flutter run
   ```

## Contoh Request API

```
https://api.open-meteo.com/v1/forecast?latitude=-2.2106&longitude=113.9139&current_weather=true
```

## Catatan Weather Code

Kode cuaca mengikuti standar WMO, misalnya `0` = cerah, `1–3` = berawan sebagian, `61–65` = hujan, `95` = badai petir.
