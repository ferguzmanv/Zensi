# Zensi Technical Test

## Descripción

Desarrollar una interfaz de usuario que permita el inicio de sesión, obtener datos desde una
API y generar un gráfico.


## Instalación

Sigue estos pasos para instalar y ejecutar el proyecto en tu entorno local:

## Navega al directorio del proyecto:

cd tu-repositorio

## Instala las dependencias:


npm install

## Inicia el servidor de desarrollo:

npm run dev

## Tecnologías Utilizadas

- *Vite*: Herramienta de construcción rápida y ligera.
- *React*: Biblioteca de JavaScript para construir interfaces de usuario.
- *Tailwind CSS*: Framework de CSS para un diseño rápido y eficiente.
- *React Router DOM*: Biblioteca para la gestión de rutas en aplicaciones React.

# Creacion del proyecto

## Crear un nuevo proyecto con Vite
npm create vite@latest ZensiTest --template react

## Navegar al directorio del proyecto
cd ZensiTest

## Instalar dependencias
npm install

# Instalar Tailwind CSS
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p

# Estructura de proyecto
ZensiTest/
├── public/
├── src/
│   ├── components/
│   │   ├── LoginForm.jsx
│   │   ├── BarChart.jsx
│   ├── App.jsx
│   ├── main.jsx
│   └── index.css
│   └── services.js
├── tailwind.config.js
├── main.jsx
├── index.html
├── package.json
└── README.md

# Añadir Tailwind CSS a tu archivo CSS principal (src/index.css)
@tailwind base;
@tailwind components;
@tailwind utilities;

# Instalar React Router DOM
npm install react-router-dom

# Implementación de Login

- Validación: Se verifican que los campos de usuario y contraseña no estén vacíos.
- Envío de datos: Al enviar el formulario, los datos se envían a un endpoint de la API (inicialmente una API dummy para desarrollo).
- Servicios: Se utiliza una función Login en services.js para realizar la solicitud HTTP.
- Configuración: El endpoint se configura en vite.config para facilitar cambios.

# Implementación de Gráfico de Líneas con ApexCharts

- Visualización de datos: Se ha creado un componente de gráfico de líneas dinámico utilizando la librería ApexCharts para representar datos numéricos a lo largo del tiempo.
- Interactividad: El usuario puede seleccionar el año que desea visualizar a través de un selector, lo que desencadena una actualización en tiempo real del gráfico.
- Consumo de API: El componente realiza una solicitud a una API para obtener los datos específicos del año seleccionado.
- Mapeo de datos: Los datos recibidos se mapean y transforman para ajustarse al formato requerido por ApexCharts.
Personalización: El gráfico se puede personalizar visualmente utilizando las opciones de configuración de ApexCharts.

## Recursos

- Para la autenticación del usuario: [Auth - DummyJSON](https://dummyjson.com/docs/auth)
- Para la obtención de los datos: [Dólar anual](https://docs.boostr.cl/reference/economy-dolar-year)
