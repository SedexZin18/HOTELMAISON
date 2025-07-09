# Hotel Maison Étoile - Sistema MVC

Sistema de gestión hotelera desarrollado con arquitectura **MVC (Model-View-Controller)** y patrón **DAO (Data Access Object)** para el Hotel Maison Étoile.

## 🏗️ Arquitectura

### Patrón MVC
- **Model**: Manejo de datos y lógica de negocio
- **View**: Interfaz de usuario (HTML/CSS/JS)
- **Controller**: Lógica de control y coordinación

### Patrón DAO
- **Data Access Object**: Abstracción de acceso a datos
- Separación clara entre lógica de negocio y acceso a datos
- Facilita mantenimiento y testing

## 📁 Estructura del Proyecto

\`\`\`
hotel-maison-mvc/
├── config/
│   └── database.js          # Configuración de BD
├── models/
│   ├── BaseModel.js         # Modelo base
│   ├── Habitacion.js        # Modelo de habitaciones
│   ├── TipoHabitacion.js    # Modelo de tipos
│   ├── Contacto.js          # Modelo de contactos
│   └── Reclamacion.js       # Modelo de reclamaciones
├── dao/
│   ├── HabitacionDAO.js     # DAO de habitaciones
│   ├── ContactoDAO.js       # DAO de contactos
│   └── ReclamacionDAO.js    # DAO de reclamaciones
├── controllers/
│   ├── HabitacionController.js
│   ├── ContactoController.js
│   └── ReclamacionController.js
├── routes/
│   └── api.js               # Rutas de la API
├── public/
│   ├── index.html
│   ├── habitaciones.html
│   ├── contacto.html
│   ├── faqs.html
│   ├── reclamaciones.html
│   ├── styles/
│   │   └── main.css
│   └── js/
│       ├── api-client.js
│       ├── contacto-mvc.js
│       ├── reclamaciones-mvc.js
│       └── habitaciones-mvc.js
├── scripts/
│   ├── 01-create-database.sql
│   └── 02-seed-data.sql
├── app.js                   # Aplicación principal
└── package.json
\`\`\`

## 🚀 Instalación y Configuración

### 1. Clonar el repositorio
\`\`\`bash
git clone <repository-url>
cd hotel-maison-mvc
\`\`\`

### 2. Instalar dependencias
\`\`\`bash
npm install
\`\`\`

### 3. Configurar base de datos Neon
1. Crear cuenta en [neon.tech](https://neon.tech)
2. Crear nuevo proyecto "hotel-maison"
3. Ejecutar scripts SQL en orden:
   - `scripts/01-create-database.sql`
   - `scripts/02-seed-data.sql`

### 4. Configurar variables de entorno
\`\`\`bash
# Crear archivo .env
DATABASE_URL=postgresql://user:pass@host/db
PORT=3000
\`\`\`

### 5. Ejecutar la aplicación
\`\`\`bash
# Desarrollo
npm run dev

# Producción
npm start
\`\`\`

## 📊 API Endpoints

### Habitaciones
- `GET /api/habitaciones` - Obtener todas las habitaciones
- `GET /api/habitaciones/disponibles` - Habitaciones disponibles
- `GET /api/habitaciones/tipos` - Tipos de habitación
- `GET /api/habitaciones/:id` - Habitación por ID
- `POST /api/habitaciones` - Crear habitación
- `PUT /api/habitaciones/:id` - Actualizar habitación
- `PATCH /api/habitaciones/:id/estado` - Cambiar estado
- `DELETE /api/habitaciones/:id` - Eliminar habitación

### Contactos
- `POST /api/contactos` - Crear contacto
- `GET /api/contactos` - Obtener contactos
- `GET /api/contactos/:id` - Contacto por ID
- `PATCH /api/contactos/:id/leido` - Marcar como leído
- `PATCH /api/contactos/:id/respondido` - Marcar como respondido

### Reclamaciones
- `POST /api/reclamaciones` - Crear reclamación
- `GET /api/reclamaciones/seguimiento/:code` - Buscar por código
- `GET /api/reclamaciones` - Obtener reclamaciones
- `GET /api/reclamaciones/:id` - Reclamación por ID
- `PATCH /api/reclamaciones/:id/estado` - Actualizar estado

## 🎯 Características Principales

### Funcionalidades del Sistema
- ✅ Gestión de habitaciones y tipos
- ✅ Sistema de contactos
- ✅ Libro de reclamaciones oficial
- ✅ Panel administrativo
- ✅ Reportes y estadísticas
- ✅ API RESTful completa

### Tecnologías Utilizadas
- **Backend**: Node.js + Express
- **Base de datos**: PostgreSQL (Neon)
- **Frontend**: HTML5 + CSS3 + Bootstrap 5
- **Arquitectura**: MVC + DAO
- **ORM**: Neon Serverless

### Características Técnicas
- 🏗️ Arquitectura MVC bien estructurada
- 🔄 Patrón DAO para acceso a datos
- 🛡️ Validaciones en múltiples capas
- 📱 Diseño responsive
- 🔍 Sistema de búsqueda
- 📊 Reportes y estadísticas
- 🔐 Autenticación y autorización

## 🧪 Testing

\`\`\`bash
# Ejecutar tests
npm test

# Coverage
npm run test:coverage
\`\`\`

## 📈 Despliegue

### Vercel
1. Conectar repositorio a Vercel
2. Configurar variables de entorno
3. Desplegar automáticamente

### Variables de entorno requeridas:
- `DATABASE_URL`: String de conexión a Neon
- `PORT`: Puerto del servidor (opcional)

## 🤝 Contribución

1. Fork el proyecto
2. Crear rama feature (`git checkout -b feature/nueva-funcionalidad`)
3. Commit cambios (`git commit -am 'Agregar nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/nueva-funcionalidad`)
5. Crear Pull Request

## 📝 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para detalles.

## 👥 Equipo de Desarrollo

- **Piero Jefferson Anticona Honores**
- **Luis Gustavo Leiva Jesus**
- **Luis Armando Terán Saucedo**
- **James Bryan Quispe Torres**

---

**Hotel Maison Étoile** - Sistema de gestión hotelera con arquitectura MVC y DAO
