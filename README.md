# Melody Music

Reproductor de música local + YouTube + sincronización con Google Drive.

## Características actuales

- Reproducción real con **Media3 (ExoPlayer)**
- Escaneo de toda la música del dispositivo (carpetas y subcarpetas)
- Portadas de álbum
- Playlists y favoritos
- Interfaz oscura con acentos neón
- Base preparada para Google Sign-In y Google Drive
- Servicio en segundo plano + notificación de reproducción

## Cómo abrir el proyecto

1. Abre **Android Studio**
2. Elige **Open** y selecciona esta carpeta (`melody_project`)
3. Espera a que Gradle sincronice
4. Conecta un móvil o emulador (API 26+)
5. Pulsa **Run**

La primera vez la app pedirá permiso de acceso a archivos de audio. Después ve a **Inicio** y pulsa el botón de escanear.

## Estructura principal

```
app/src/main/java/com/example/
├── MainActivity.kt
├── playback/
│   ├── MelodyPlaybackService.kt   ← Servicio Media3
│   └── PlayerManager.kt           ← Control del reproductor
├── data/
│   ├── local/                     ← Room (canciones + playlists)
│   ├── repository/
│   └── scanner/LocalMusicScanner.kt
├── ui/
│   ├── MelodyApp.kt
│   ├── screens/
│   ├── components/
│   └── viewmodel/
└── util/GoogleDriveSyncManager.kt
```

## Próximas mejoras

- Google Sign-In real
- Sincronización multilateral con Google Drive
- Integración YouTube (búsqueda + descarga)
- Equalizador real
- Mejor organización por carpetas
