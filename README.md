# Sitio Web de Presentación Profesional - Joseph Medina

## 1. Objetivo del Proyecto
Desarrollar y desplegar un sitio web de presentación profesional aplicando estándares modernos de **HTML5 semántico** y hojas de estilo en cascada (**CSS3 externo**) bajo una estética minimalista y responsiva, empaquetando la aplicación estática en un contenedor **Docker** servido mediante **Nginx** para garantizar portabilidad y despliegue rápido.

## 2. Tecnologías Utilizadas
* **HTML5:** Estructura semántica (`header`, `nav`, `section`, `table`, listas ordenadas/anidadas y enlaces).
* **CSS3 Externo:** Diseño responsivo con *CSS Grid*, *Flexbox*, variables personalizadas (`:root`) y *Media Queries*.
* **Google Fonts & Font Awesome:** Tipografías (`Source Sans Pro`, `Source Code Pro`) e iconografía vectorial.
* **Nginx (Alpine):** Servidor web HTTP ligero de alto rendimiento.
* **Docker & Docker Hub:** Contenedorización y publicación de la imagen oficial del proyecto.
* **Git & GitHub:** Control de versiones del código fuente.

## 3. Estructura del Proyecto
```text
potafolio-Joseph/
├── src/
│   ├── css/
│   │   └── styles.css      # Hoja de estilos CSS3 externa
│   └── img/                # Recursos gráficos e imágenes del portafolio
│       ├── ESPE.png
│       ├── fotoPerfil.jpeg
│       ├── gitHub.jpg
│       ├── icono.jpg
│       ├── LinkedIn.png
│       └── Riot.jpg
├── index.html              # Estructura principal HTML5 del sitio
├── Dockerfile              # Configuración para construir la imagen con Nginx
├── .dockerignore           # Archivos excluidos del contenedor Docker
├── .gitignore              # Archivos excluidos del control de versiones Git
└── README.md               # Documentación técnica del proyecto
```

## 4. Instrucciones para Construir y Ejecutar la Imagen Docker

### Opción A: Construir y ejecutar localmente desde el repositorio
1. Clonar el repositorio:
   ```bash
   git clone [https://github.com/Joseph-Benjamin-Medina-Sanchez/Perfil-Profesional.git](https://github.com/Joseph-Benjamin-Medina-Sanchez/Perfil-Profesional.git)
   cd Perfil-Profesional
   ```
2. Construir la imagen Docker:
   ```bash
   docker build -t joseph323123/perfil-profesional:latest .
   ```
3. Ejecutar el contenedor en el puerto `8080`:
   ```bash
   docker run -d -p 8080:80 --name mi-portafolio joseph323123/perfil-profesional:latest
   ```
4. Abrir en el navegador: `http://localhost:8080`

### Opción B: Descargar y ejecutar directamente desde Docker Hub
```bash
docker pull joseph323123/perfil-profesional:latest
docker run -d -p 8080:80 --name mi-portafolio joseph323123/perfil-profesional:latest
```

## 5. Enlace a Docker Hub
* **Repositorio en Docker Hub:** [https://hub.docker.com/r/joseph323123/perfil-profesional](https://hub.docker.com/r/joseph323123/perfil-profesional)