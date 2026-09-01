## eFootball Toolkit PRO 2.3.0

This release delivers an extensive reengineering of the match detection and tracking engine, focused on accuracy, continuity, and compatibility across Steam, Xbox PC, and OpenWrt.

### Match monitoring

- The match engine was extensively restructured with new classification and lifecycle stages to identify P2P and PSP connections more reliably.
- IP, port, and TCP/UDP transport transitions are now tracked without incorrectly splitting a single match.
- Fixed Xbox PC matches that could remain stuck in the monitor or be replaced without a proper match-end event.
- Rematches and marked opponents now distinguish a same-match reconnection from a new session more accurately, with more consistent visual alerts and blocking.

### Modes and networking

- New smart COOP mode with country selection, fast geolocation, and controlled blocking only after the match is identified; blocked attempts are not saved to match history.
- P2P Experimental and COOP now also work through OpenWrt in the Windows app while preserving the validated local Npcap capture flow.
- Expanded regional catalog with additional countries, cities, and international endpoints.

### Mobile

- PSP and P2P match alerts now use clearly distinct sounds, making the connection type easy to identify without looking at the screen.

### DirectX and app experience

- DirectX detection was revised for both Steam and Xbox PC.
- Right-clicking the eFootball button can launch the Steam version with DX11 or DX12, or preserve all user-defined launch options unchanged.
- First launch now begins with language selection before activation and includes a guided dashboard tour.
- Firewall, Server Center, and Network & Overlay screens were reorganized with general responsiveness and readability improvements.
- App shutdown and capture-component cleanup are now faster and more reliable.
