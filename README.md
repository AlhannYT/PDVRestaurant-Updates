# 🍽️ Gloria Restaurant - Sistema de Gestión y Punto de Venta (POS)

[![Windows](https://img.shields.io/badge/Plataforma-Windows%2010%20%2F%2011-0078D7?style=for-the-badge&logo=windows&logoColor=white)](https://microsoft.com/windows)
[![.NET 8.0](https://img.shields.io/badge/.NET-8.0--windows-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)](https://dotnet.microsoft.com/)
[![SQL Server](https://img.shields.io/badge/Database-SQL%20Server-CC292B?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)](https://www.microsoft.com/sql-server/)
[![Actualizaciones](https://img.shields.io/badge/Distribución-GitHub%20Releases-2ea44f?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AlhannYT/PDVRestaurant-Updates/releases)

Sistema integral y profesional para la administración de restaurantes y punto de venta (POS) de alto rendimiento. Desarrollado con tecnología moderna en **C# (.NET 8)** y **Windows Forms**, diseñado para cubrir todo el flujo operativo: punto de venta, cocina y comandas, gestión de mesas, reservaciones, facturación fiscal (NCF), control de delivery en tiempo real con Google Maps, servidor web local embebido y aplicación para repartidores.

---

## 🚀 Características Principales

### 🧾 Punto de Venta (POS) y Facturación
- **Toma de pedidos ágil:** Registro rápido de órdenes para salón, para llevar o despacho por delivery.
- **Comprobantes fiscales (NCF):** Control riguroso de secuencias fiscales, tipos de comprobantes y alertas de vencimiento.
- **Múltiples métodos de pago:** Efectivo, tarjetas, transferencias bancarias y pagos mixtos.
- **Control de devoluciones:** Módulo para cancelaciones y devoluciones con reversión de inventario y cuadre de caja.

### 🍳 Comandas y Operaciones de Cocina
- **Gestión de comandas en tiempo real:** Comunicación directa y sin demoras con estaciones de cocina y barra.
- **Estados de preparación:** Seguimiento visual por estados (*Pendiente*, *En Preparación*, *Listo*, *Servido*).
- **Pantalla para Televisión / Monitor de Turnos:** Visualizador en vivo para llamado de clientes y despacho de pedidos listos.

### 🪑 Salón, Mesas y Reservaciones
- **Mantenimiento de mesas:** Mapa interactivo con estado en vivo (*Disponible*, *Ocupada*, *Reservada*).
- **Control de reservaciones:** Agenda de reservas con registro de comensales, fecha, hora y datos del cliente.

### 🛵 Módulo de Delivery y Repartidores
- **Despacho y asignación:** Asignación rápida de repartidores a pedidos a domicilio.
- **Seguimiento con Google Maps:** Visualización de rutas y geolocalización de entregas.
- **App / Portal móvil para repartidores:** Interfaz móvil para inicio de sesión de repartidores, cambio de estado de entrega y registro de cobros.

### 🌐 Servidor Web Integrado y Pedidos Online
- **Servidor web local embebido:** Autogestionado en segundo plano sin requerir configuraciones complejas de servidores externos.
- **Carta / Menú digital interactivo:** Consulta de carta y recepción de pedidos online.
- **Sistema de reseñas y calificaciones:** Valoración del servicio y retroalimentación post-entrega.
- **Progressive Web App (PWA):** Notificaciones en tiempo real para nuevos pedidos y compatibilidad móvil.

### 📦 Inventario, Compras y Proveedores
- **Catálogo de productos:** Gestión de platos, bebidas, combos e ingredientes con control de existencias mínimas.
- **Módulo de compras:** Entrada de insumos y compras a proveedores con costeo automático.
- **Gestión de proveedores y clientes:** Directorio centralizado con historial de movimientos y pedidos.

### 📊 Reportería y Auditoría
- **Informes analíticos:**
  - Facturación comercial y facturas de delivery.
  - Comandas de cocina e historial de compras.
  - Ventas generales por rangos de fecha.
  - Platos más vendidos y productos de mayor rotación.
  - Estado y valorización del inventario.
  - Registro y auditoría de comprobantes fiscales emitidos.

### 🔒 Seguridad y Estabilidad
- **Cifrado de datos:** Protección criptográfica de credenciales de acceso y cadenas de conexión.
- **Instancia única:** Prevención de ejecuciones simultáneas accidentales en el equipo mediante control por *Mutex*.
- **Auto-actualizador integrado:** Detección y aplicación de nuevas versiones de forma desatendida.

---

## 💻 Requisitos del Sistema

- **Sistema Operativo:** Windows 10 / Windows 11 (64-bit recomendado).
- **Entorno de Ejecución:** [.NET Desktop Runtime 8.0](https://dotnet.microsoft.com/download/dotnet/8.0) *(incluido o descargable si el instalador lo solicita)*.
- **Base de Datos:** Microsoft SQL Server 2016 o superior (Express, Standard o Enterprise).
- **Navegación Web:** Microsoft Edge WebView2 Runtime (incluido de fábrica en Windows 10 y 11).

---

## 📥 Descarga e Instalación

> [!IMPORTANT]  
> Este software se distribuye en formato de instaladores precompilados (`.exe`). No es necesario compilar código fuente.

### 1. Descarga del Instalador
Descarga la versión más reciente del sistema desde el repositorio oficial de lanzamientos:
👉 **[Descargar última versión en GitHub Releases](https://github.com/AlhannYT/PDVRestaurant-Updates/releases)**

### 2. Instalación en Windows
1. Ejecuta el archivo instalador descargado (`PDVRestaurant-Setup.exe`).
2. Sigue los pasos del asistente de instalación para completar la configuración en tu equipo.
3. El instalador creará los accesos directos y registrará los componentes necesarios automáticamente.

### 3. Configuración Inicial de Base de Datos
1. Asegúrate de contar con una instancia de **Microsoft SQL Server** activa.
2. Se debe hablar con el propietario del software para hacer la configuración inicial, ya que esta conlleva seriales y activación con credenciales de Super-Usuario
3. En la primera apertura del sistema se definen los parámetros de conexión al servidor SQL (Servidor, Base de Datos, Usuario y Contraseña).

---

## 🔄 Sistema de Actualizaciones Automáticas

El sistema cuenta con un mecanismo de actualización integrado (**AutoUpdater**). 

- Al iniciar la aplicación, el software consulta automáticamente el canal oficial en [PDVRestaurant-Updates](https://github.com/AlhannYT/PDVRestaurant-Updates).
- Si existe una nueva versión disponible, el sistema notificará al usuario y descargará e instalará el paquete correspondiente sin perder configuraciones ni información almacenada.

---

## 🏗️ Arquitectura del Ecosistema

```
┌───────────────────────────────────────────────────────────────┐
│                    Gloria Restaurant (POS)                    │
├───────────────────────────────┬───────────────────────────────┤
│         Escritorio            │           Web & PWA           │
│  - Punto de Venta (POS)       │  - Carta Digital Online       │
│  - Facturación & NCF          │  - Pedidos Web                │
│  - Mesas & Reservaciones      │  - Portal Delivery Móvil      │
│  - Comandas de Cocina         │  - Reseñas & Calificaciones   │
│  - Monitor TV para Turnos     │  - Notificaciones en Vivo     │
│  - Compras & Inventario       │                               │
│  - Reportes & Auditoría       │                               │
├───────────────────────────────┴───────────────────────────────┤
│                   Capa de Datos & Servicios                   │
│   • Microsoft SQL Server (Base de Datos Centralizada)         │
│   • Motor PHP Embebido (Servicios Web Locales)                │
│   • AutoUpdater.NET (Distribución de Versiones)               │
└───────────────────────────────────────────────────────────────┘
```

---

## 👤 Autor

- **Desarrollador:** [AlhannYT](https://github.com/AlhannYT)
- **Canal de Descargas y Actualizaciones:** [PDVRestaurant-Updates](https://github.com/AlhannYT/PDVRestaurant-Updates/releases)

---

## ⚖️ Propiedad y Licencia

**Copyright © AlhannYT. Todos los derechos reservados.**

Este software es de carácter **privado y propietario**. Queda terminantemente prohibida la copia, reproducción, descompilación, distribución no autorizada o comercialización del código fuente o sus binarios sin el consentimiento previo y por escrito del titular de los derechos.
