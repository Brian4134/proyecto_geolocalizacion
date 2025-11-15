# Sistema de Geolocalización de Bus Institucional

Sistema completo de tracking GPS para buses institucionales con panel administrativo, módulo de conductor y seguimiento para pasajeros.

## 🚀 Características

- **Panel Administrativo**: Gestión de usuarios, buses, alertas y métricas
- **Módulo Conductor**: Control de recorridos, GPS en tiempo real y alertas de emergencia
- **Módulo Pasajero**: Seguimiento en tiempo real del bus
- **Autenticación**: Login con email/password y Google Auth
- **Base de datos**: Firebase Firestore + Realtime Database
- **Mapas**: Leaflet con OpenStreetMap
- **UI/UX**: Tailwind CSS + Framer Motion

## 🛠️ Tecnologías

- **Frontend**: React + Vite
- **Styling**: Tailwind CSS
- **Animaciones**: Framer Motion
- **Mapas**: React Leaflet
- **Backend**: Firebase (Auth, Firestore, Realtime DB)
- **Despliegue**: Netlify

## 📦 Instalación

```bash
cd frontend
npm install
npm run dev
```

## 🌐 Despliegue en Netlify

1. **Build del proyecto**:
```bash
npm run build
```

2. **Conectar con Netlify**:
   - Sube el proyecto a GitHub
   - Conecta el repositorio en Netlify
   - Configuración automática con `netlify.toml`

3. **Variables de entorno** (si es necesario):
   - Las credenciales de Firebase están en el código (público)
   - Para producción, considera usar variables de entorno

## 🔧 Configuración Firebase

El proyecto usa Firebase con la siguiente estructura:

### Firestore Collections:
- `usuarios`: Datos de usuarios (nombre, email, rol, busAsignado)
- `buses`: Información de buses (placa, modelo, capacidad, conductor)

### Realtime Database:
- `buses/{busId}/ubicacion`: Coordenadas GPS en tiempo real
- `recorridos/{recorridoId}`: Historial de recorridos con coordenadas
- `alertas`: Alertas de emergencia
- `usuariosConectados`: Usuarios activos en tiempo real

## 👥 Roles de Usuario

- **Admin**: Acceso completo al panel administrativo
- **Conductor**: Control de recorridos y alertas
- **Pasajero**: Visualización del bus en tiempo real

## 🗺️ Funcionalidades del Mapa

- Seguimiento GPS en tiempo real
- Guardado inteligente de coordenadas (cada 10s o 10m)
- Visualización de rutas históricas
- Cálculo de distancias recorridas

## 📱 Responsive Design

- Diseño adaptativo para móviles y desktop
- Interfaz optimizada para conductores en dispositivos móviles
- Panel administrativo optimizado para desktop

## 🔒 Seguridad

- Autenticación Firebase
- Roles y permisos por usuario
- Validación de datos en frontend
- Reglas de seguridad en Firebase

## 📊 Métricas y Analytics

- Usuarios conectados en tiempo real
- Alertas activas
- Recorridos diarios y totales
- Gráficos visuales con CSS/SVG

## 🚨 Sistema de Alertas

5 tipos de alertas de emergencia:
- Accidente
- Emergencia médica
- Retraso en ruta
- Falla mecánica
- Comportamiento de pasajeros