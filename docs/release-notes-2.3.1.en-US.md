## eFootball Toolkit PRO 2.3.1

This update consolidates the fixes found after version 2.3.0 and improves P2P match geolocation accuracy on Windows and Android.

### P2P geolocation

- New geolocation system based on consensus among three independent sources queried in parallel, keeping identification fast.
- STUN ping and physical distance now participate in validation, reducing locations that conflict with the observed latency.
- Smart caching reuses recent evidence without locking the app to an incorrect response.
- The same logic is available on Windows and Mobile without depending on requests to the Toolkit Worker.

### Match monitor

- Refined P2P match termination and reconnection handling to reduce sessions ending too early and rematches being classified as continuations of the previous match.
- Improved handling of resumed traffic from the same endpoint and IP, port, or transport changes during a session.
- Additional fixes for marked-opponent identification and rematch alerts.

### App and updates

- Fixed the Steam option that preserves custom launch instructions without changing them when starting the game.
- Mobile now reads the same signed manifest as Windows and validates version, signature, size, and SHA-256 before handing the APK to the Android installer.
- The public Windows build does not include the detailed diagnostic-log interface or collection.

