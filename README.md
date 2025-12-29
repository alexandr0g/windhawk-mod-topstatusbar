# Top Status Bar

![Preview](screenshots/screenshot%20(1).png)

![Settings](screenshots/screenshot%20(2).png)

---
# Top Status Bar

## [EN] Technical Specifications
- **Language:** C++ / Win32 API.
- **Rendering Engine:** Direct2D (migrated from GDI+) for hardware-accelerated drawing.
- **Text Engine:** DirectWrite for subpixel anti-aliasing.
- **Target OS:** Windows 10 / 11.

### Core Functionality
- **Resource Monitoring:** Real-time tracking of CPU load, RAM utilization, and C: drive activity using `GetSystemTimes` and `GlobalMemoryStatusEx`.
- **Battery Module:** Geometric path rendering. Detects `ACLineStatus` to toggle charging indicators.
- **Smart Auto-hide:** Hides when active windows are maximized or occupy the top screen region.
- **Survivor Logic:** Prevents hiding when interacting with `WorkerW` (Desktop), `#32768` (Context Menus), or system flyouts.
- **App Integration:** 
  - **Calendar:** Invokes `outlookcal:` or `ms-calendar:`. Fallback to Google Calendar URL if no local handler is detected.
  - **Clock:** Invokes `ms-clock:` with fallback to system time settings.

### Performance
- **Frame Rate:** Capped at 30 FPS to minimize CPU cycles.
- **Memory Footprint:** ~10-15 MB RAM.
- **Rendering:** Zero-allocation draw loop with cached Direct2D resources.

---

## [ES] Especificaciones Técnicas
- **Lenguaje:** C++ / Win32 API.
- **Motor de Renderizado:** Direct2D (migrado desde GDI+) para dibujo acelerado por hardware.
- **Motor de Texto:** DirectWrite para suavizado de subpíxeles.
- **SO Compatible:** Windows 10 / 11.

### Funcionalidad Principal
- **Monitoreo de Recursos:** Seguimiento en tiempo real de CPU, RAM y actividad de disco mediante `GetSystemTimes` y `GlobalMemoryStatusEx`.
- **Módulo de Batería:** Renderizado mediante rutas geométricas. Detecta `ACLineStatus` para indicadores de carga.
- **Ocultamiento Automático:** Se oculta cuando la ventana activa está maximizada o invade la zona superior de la pantalla.
- **Lógica de Supervivencia:** Evita el ocultamiento al interactuar con el Escritorio (`WorkerW`), Menús Contextuales (`#32768`) o elementos del sistema.
- **Integración de Aplicaciones:** 
  - **Calendario:** Invoca protocolos `outlookcal:` o `ms-calendar:`. Redirección a Google Calendar si no hay cliente local.
  - **Reloj:** Invoca `ms-clock:` con respaldo a la configuración de hora del sistema.

### Rendimiento
- **Tasa de Refresco:** Limitada a 30 FPS para reducir el uso de CPU.
- **Uso de Memoria:** ~10-15 MB RAM.
- **Renderizado:** Bucle de dibujo optimizado con recursos Direct2D en caché.

## Installation / Instalación
1. Install [Windhawk](https://windhawk.net/).
2. Create a new mod and paste the code from `topstatusbar.wh.cpp`.
3. Compile and enable.
