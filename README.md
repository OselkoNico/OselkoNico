## Hola, soy Osel Nicolás 👋

Desarrollador web full-stack formado en JavaScript y TypeScript, buscando mi
primera oportunidad en el sector. Actualmente trabajo como fontanero y estoy en
plena transición hacia la programación: llevo meses construyendo proyectos por mi
cuenta, con la misma constancia con la que se aprende un oficio.

Del oficio me traigo lo que creo que importa aquí: diagnosticar antes de tocar,
trabajar con método y no dar algo por terminado hasta que funciona de verdad.

---

## Proyectos destacados

### [Gestión de proveedores](https://github.com/OselkoNico/Angular-NodeJS-Frontend) · Angular + Node.js

CRUD completo de proveedores repartido en dos repositorios:
[frontend en Angular](https://github.com/OselkoNico/Angular-NodeJS-Frontend) y
[API en Express](https://github.com/OselkoNico/Angular-NodeJS-Backend).

- **Angular 21 al día:** standalone components, `signals` para el estado local
  del formulario y el nuevo control de flujo `@if` / `@for` en las plantillas.
- **Reactive Forms** con validación de campos obligatorios y marcado de campos
  tocados al intentar enviar un formulario incompleto.
- **Servicio inyectable** (`ProveedoresService`) que centraliza las cinco
  llamadas HTTP, con interfaces TypeScript propias para cada forma de respuesta
  de la API.
- **Enrutado con parámetros:** `/crear` y `/modificar/:cif` comparten un único
  componente de formulario, que detecta el modo por la presencia del parámetro
  de ruta. Ruta comodín que redirige a Inicio.
- **Errores de la API a la vista del usuario** (CIF duplicado, proveedor
  inexistente, servidor caído) en lugar de fallar en silencio.

`Angular 21` · `TypeScript` · `RxJS` · `Reactive Forms` · `Node.js` · `Express 5` · `Vitest`

### [gestion-pacientes](https://github.com/OselkoNico/gestion-pacientes) · React + Express

Aplicación full-stack para la gestión de pacientes, con validación tanto en
servidor como en cliente.

- **Backend:** API REST con Express 5 y ES Modules. Validación de todos los
  campos (formato de DNI, código postal y teléfono), control de duplicados con
  `409 Conflict` y códigos de estado HTTP correctos en cada respuesta.
- **Frontend:** React 19 con TypeScript y Vite. Estado y operaciones CRUD
  encapsulados en un hook propio (`usePacientes`), capa de servicios con Axios y
  una clase `ApiError` para que los errores del backend lleguen tipados a la
  interfaz.
- **Tests:** 28 en total. La API se prueba con Vitest y Supertest cubriendo los
  cinco endpoints; el frontend con Testing Library, incluyendo dos tests de
  regresión sobre el bloqueo del DNI durante la edición.
- **Arquitectura:** la aplicación Express está separada de su arranque
  (`app.js` / `server.js`) para poder importarla desde los tests sin levantar un
  puerto real.

`React 19` · `TypeScript` · `Vite` · `Express 5` · `Vitest` · `Testing Library` · `Supertest`

### [gestion-suministros-api](https://github.com/OselkoNico/gestion-suministros-api) · Node.js + MongoDB

API REST para un catálogo de artículos de suministro industrial, identificados
por SKU. Proyecto centrado en hacer bien la capa de servidor.

- **Persistencia real** con MongoDB y Mongoose, frente al almacenamiento en
  memoria de los proyectos anteriores.
- **Manejo centralizado de errores:** una clase `AppError` que lleva asociado su
  código HTTP y un middleware `errorHandler` que traduce cualquier fallo a una
  respuesta JSON coherente, en lugar de repartir `try/catch` por los controladores.
- **Estructura por capas:** rutas, controladores, modelos, middlewares y
  configuración en carpetas separadas.
- **Configuración por entorno** con `dotenv` y un `.env.example` versionado.

`Node.js` · `Express 5` · `MongoDB` · `Mongoose` · `dotenv`

---

## Con qué trabajo

**Lenguajes**
JavaScript (ES6+) · TypeScript · HTML5 · CSS3

**Frontend**
Angular 21 (standalone components, signals, Reactive Forms, Router, HttpClient) ·
React 19 (hooks propios, componentes controlados) · RxJS · Vite · Axios ·
consumo de APIs REST con manejo de estados de carga y error

**Backend**
Node.js con ES Modules · Express 5 · diseño de APIs REST · validación de datos
de entrada · códigos de estado HTTP · middlewares de error · CORS

**Bases de datos**
MongoDB · Mongoose

**Testing**
Vitest · Supertest (integración de API) · React Testing Library · jsdom

**Herramientas**
Git y GitHub (ramas por funcionalidad, pull requests) · npm · Angular CLI ·
ESLint/Oxlint · Prettier · nodemon · dotenv

---

## Formación

**Desarrollo Web Full Stack — Deusto Formación** · 750 horas (online)

| Área | Contenidos |
| ---- | ---------- |
| **Control de versiones** | Git · GitHub · GitHub Actions |
| **Lenguajes** | JavaScript (ECMAScript) · TypeScript |
| **Maquetación** | HTML5 · CSS3 · Sass con patrón 7-1 · Bootstrap · Tailwind |
| **Frontend** | React · React Router · Redux · Angular · RxJS y programación reactiva |
| **Backend** | Node.js · npm · Express · Postman |
| **APIs** | Diseño y consumo de APIs REST / RESTful |
| **Bases de datos** | MySQL · MongoDB · Mongoose · Compass |
| **Testing** | Jest · Vitest · Cypress |
| **Herramientas y despliegue** | Transpilado con Babel · Docker · Docker Compose · CI/CD |
| **Buenas prácticas** | Clean code · Arquitectura hexagonal |

Los tres proyectos de arriba son los que he llevado más lejos por mi cuenta,
más allá de los ejercicios del temario.

Sigo formándome: testing automatizado, buenas prácticas de Git y lectura de
código ajeno son ahora mismo mis tres focos.

---

## Cómo trabajo

Estoy progresando en que mis repositorios se lean como los de un equipo, no como los de un
alumno:

- **Commits con convención** (`feat:`, `fix:`, `docs:`, `test:`, `refactor:`) y
  mensajes que explican el porqué, no solo el qué.
- **Una rama por funcionalidad** y merge mediante pull request, también cuando
  trabajo solo.
- **Tests antes de dar algo por cerrado**, incluidos casos de regresión de los
  errores que ya he cometido una vez.
- **README en cada proyecto**, con instalación, endpoints y las decisiones de
  diseño que no se deducen del código.

---

## Contacto

Estoy buscando activamente mi primer puesto como desarrollador, en remoto o
presencial, y disponible para incorporación inmediata.

- **LinkedIn:** [https://www.linkedin.com/in/osel-f-nicol%C3%A1s-benitez/]
- **Correo:** [oselfrancisco.nb@gmail.com]
