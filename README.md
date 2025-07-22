# Modal Drawer Sheet Example - Jetpack Compose

Contoh penggunaan **`ModalNavigationDrawer`** di Jetpack Compose dengan integrasi navigasi dan drawer menu.

## 🚀 Fitur

- Menggunakan `ModalDrawerSheet` dari Material3
- Navigasi antar layar menggunakan `NavHost` + `NavController`
- Drawer menu yang bisa dibuka/tutup secara dinamis
- Ikon dan label untuk setiap item menu

## 📱 Tampilan UI

- Top app bar dengan ikon menu
- Modal drawer yang muncul dari kiri saat ikon ditekan
- Menu drawer berisi:
  - Home
  - Profile
  - Settings
  - Help
- Konten layar yang berubah sesuai navigasi

## 🧩 Komponen Utama

- `ModalNavigationDrawer` – komponen drawer dari Material 3
- `NavHost` – navigasi antar composable
- `DrawerState` dan `CoroutineScope` – kontrol buka/tutup drawer
- `TopAppBar` – header aplikasi

## 🧪 Cara Menggunakan

1. Tambahkan dependensi Jetpack Compose dan Material 3 di `build.gradle`
2. Siapkan daftar item drawer (`drawerItems`)
3. Pastikan `HomeScreen`, `ProfileScreen`, dll., sudah didefinisikan
4. Panggil `ExampleWithModalDrawer()` dari `setContent {}` atau composable utama

## 🧱 Contoh Struktur Item Menu

```kotlin
val drawerItems = listOf(
    DrawerItem("Home", Icons.Default.Home, "home"),
    DrawerItem("Profile", Icons.Default.Person, "profile"),
    DrawerItem("Settings", Icons.Default.Settings, "settings"),
    DrawerItem("Help", Icons.Default.Help, "help")
)

data class DrawerItem(
    val label: String,
    val icon: ImageVector,
    val route: String
)
