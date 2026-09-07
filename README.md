# Hola, soy Osel Nicolás 👋

Desarrollador web full-stack formado en JavaScript y TypeScript, buscando mi
primera oportunidad en el sector. Actualmente trabajo como fontanero y estoy
realizando una transición profesional hacia el desarrollo web. He completado una
formación de 6 meses basada en la creación de proyectos prácticos y, actualmente,
continúo formándome de manera autodidacta mediante el desarrollo de proyectos
propios, con el objetivo de seguir mejorando mis conocimientos, adquirir
experiencia práctica y avanzar constantemente como desarrollador.

Del oficio me traigo lo que creo que importa aquí: diagnosticar antes de tocar,
trabajar con método y no dar algo por terminado hasta que funciona de verdad.

## Proyectos destacados

### Gestión de proveedores · Angular + Node.js + MySQL

[Frontend](https://github.com/OselkoNico/gestion-proveedores) · [API](https://github.com/OselkoNico/Angular-NodeJS-Backend)

Aplicación completa para la gestión de un catálogo de proveedores, repartida en
dos repositorios: frontend en Angular y API REST en Express sobre MySQL. Es el
proyecto que he llevado más lejos, y el que más he reescrito a medida que
aprendía. El README del frontend incluye capturas de la aplicación.

**API**

- Persistencia en MySQL con `mysql2`, pool de conexiones y consultas
  parametrizadas en todo dato de entrada. Las restricciones de integridad
  —clave primaria, índice único, `NOT NULL`— viven en la base de datos, y el
  controlador se limita a traducir el error de MySQL al código HTTP
  correspondiente.
- Autenticación con JSON Web Tokens y contraseñas hasheadas con bcrypt, y
  control de acceso por rol: cualquier usuario identificado consulta el
  catálogo, solo un administrador puede modificarlo. Se distingue el `401`
  —no sé quién eres— del `403` —sé quién eres y no te dejo—.
- Listado paginado y con búsqueda en servidor, con los parámetros de entrada
  validados y acotados para que una petición manipulada no pueda devolver la
  tabla completa.
- Pruebas con Vitest y Supertest que **no requieren MySQL en marcha**: la capa
  de datos se sustituye por un doble. Se verifica además que una petición sin
  permisos no llega a consultar la base de datos. GitHub Actions las ejecuta en
  cada push y cada pull request.

**Cliente**

- Angular 21 en modo zoneless: el estado asíncrono vive en signals, porque una
  propiedad asignada dentro de un `subscribe` ya no provoca repintado.
- Interceptor HTTP que adjunta el token a todas las peticiones y centraliza la
  expiración de sesión, más guards de sesión y de rol sobre las rutas privadas.
- Buscador con antirrebote de 300 ms: sin él, cada pulsación genera una
  petición y las respuestas pueden llegar desordenadas, dejando en pantalla un
  resultado que no corresponde al texto introducido.
- Los controles de administración no se muestran a quien no puede usarlos. Es
  una decisión de experiencia de usuario, no de seguridad: el rol vive en el
  navegador y es manipulable; quien autoriza de verdad es el servidor.

`Angular 21 · TypeScript · RxJS · Node.js · Express 5 · MySQL · JWT · bcrypt · Vitest · Supertest · GitHub Actions`

### gestion-pacientes · React + Express

Aplicación full-stack para la gestión de pacientes, con validación tanto en
servidor como en cliente.

- **Backend:** API REST con Express 5 y ES Modules. Validación de todos los
  campos (formato de DNI, código postal y teléfono), control de duplicados con
  `409 Conflict` y códigos de estado HTTP correctos en cada respuesta.
- **Frontend:** React 19 con TypeScript y Vite. Estado y operaciones CRUD
  encapsulados en un hook propio (`usePacientes`), capa de servicios con Axios
  y una clase `ApiError` para que los errores del backend lleguen tipados a la
  interfaz.
- **Tests:** 28 en total. La API se prueba con Vitest y Supertest cubriendo los
  cinco endpoints; el frontend con Testing Library, incluyendo dos tests de
  regresión sobre el bloqueo del DNI durante la edición.
- **Arquitectura:** la aplicación Express está separada de su arranque
  (`app.js` / `server.js`) para poder importarla desde los tests sin levantar un
  puerto real.

`React 19 · TypeScript · Vite · Express 5 · Vitest · Testing Library · Supertest`

### gestion-suministros-api · Node.js + MongoDB

API REST para un catálogo de artículos de suministro industrial, identificados
por SKU. Proyecto centrado en hacer bien la capa de servidor.

- Persistencia real con MongoDB y Mongoose, frente al almacenamiento en memoria
  de los proyectos anteriores.
- Manejo centralizado de errores: una clase `AppError` que lleva asociado su
  código HTTP y un middleware `errorHandler` que traduce cualquier fallo a una
  respuesta JSON coherente, en lugar de repartir `try/catch` por los
  controladores.
- Estructura por capas: rutas, controladores, modelos, middlewares y
  configuración en carpetas separadas.
- Configuración por entorno con dotenv y un `.env.example` versionado.

`Node.js · Express 5 · MongoDB · Mongoose · dotenv`

## Con qué trabajo

**Lenguajes** JavaScript (ES6+) · TypeScript · HTML5 · CSS3

**Frontend** Angular 21 (standalone components, signals, Reactive Forms, Router
con guards, HttpClient con interceptores) · React 19 (hooks propios, componentes
controlados) · RxJS · Vite · Axios · consumo de APIs REST con manejo de estados
de carga y error

**Backend** Node.js con ES Modules · Express 5 · diseño de APIs REST ·
autenticación con JWT y hashing con bcrypt · validación de datos de entrada ·
códigos de estado HTTP · middlewares de error · CORS

**Bases de datos** MySQL · MongoDB · Mongoose

**Testing** Vitest · Supertest (integración de API) · React Testing Library ·
jsdom

**Herramientas** Git y GitHub (ramas por funcionalidad, pull requests, GitHub
Actions) · npm · Angular CLI · ESLint/Oxlint · Prettier · nodemon · dotenv

## Formación

**Desarrollo Web Full Stack — Deusto Formación · 750 horas (online)**

| Área | Contenidos |
| --- | --- |
| Control de versiones | Git · GitHub · GitHub Actions |
| Lenguajes | JavaScript (ECMAScript) · TypeScript |
| Maquetación | HTML5 · CSS3 · Sass con patrón 7-1 · Bootstrap · Tailwind |
| Frontend | React · React Router · Redux · Angular · RxJS y programación reactiva |
| Backend | Node.js · npm · Express · Postman |
| APIs | Diseño y consumo de APIs REST / RESTful |
| Bases de datos | MySQL · MongoDB · Mongoose · Compass |
| Testing | Jest · Vitest · Cypress |
| Herramientas y despliegue | Transpilado con Babel · Docker · Docker Compose · CI/CD |
| Buenas prácticas | Clean code · Arquitectura hexagonal |

Los tres proyectos de arriba son los que he llevado más lejos por mi cuenta, más
allá de los ejercicios del temario.

Sigo formándome: despliegue y configuración por entornos, bases de datos
relacionales y lectura de código ajeno son ahora mismo mis tres focos.

## Cómo trabajo

Estoy progresando en que mis repositorios se lean como los de un equipo, no como
los de un alumno:

- Commits con convención (`feat:`, `fix:`, `docs:`, `test:`, `refactor:`) y
  mensajes que explican el porqué, no solo el qué.
- Una rama por funcionalidad y merge mediante pull request, también cuando
  trabajo solo.
- Integración continua en cada push y cada pull request: las pruebas y la
  compilación tienen que pasar antes de fusionar.
- Tests antes de dar algo por cerrado, incluidos casos de regresión de los
  errores que ya he cometido una vez.
- README en cada proyecto, con instalación, endpoints y las decisiones de diseño
  que no se deducen del código.

## Contacto

Estoy buscando activamente mi primer puesto como desarrollador, en remoto o
presencial, y disponible para incorporación inmediata.

- **LinkedIn:** [osel-f-nicolás-benitez](https://www.linkedin.com/in/osel-f-nicol%C3%A1s-benitez/)
- **Correo:** [oselfrancisco.nb@gmail.com](mailto:oselfrancisco.nb@gmail.com)
