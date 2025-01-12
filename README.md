# Mi primer proyecto UNITY

<a href="https://github.com/mendozalz"><img src="https://img.shields.io/badge/.NET-512BD4.svg?style=for-the-badge&logo=dotnet&logoColor=512BD4&labelColor=ffffff" alt="dotnet"></a> 
<a href="https://github.com/mendozalz"><img src="https://img.shields.io/badge/C%23-239120.svg?style=for-the-badge&logo=c-sharp&logoColor=239120&labelColor=ffffff" alt="csharp"></a> 

## Proyecto BolaRodante 

<img src="https://github.com/menzDev/BolaRodante/blob/main/Mi_primer_proyecto_UNITY.gif?raw=true" alt="Video demostrativo de mi proyecto" />

## Configuración en local

1. Haz un `Fork` del repositorio.

2. Clona ese repositorio en tu máquina local.

   ```bash
   git clone https://github.com/<USERNAME>/Potfolio-Python.git <EL_NOMBRE_DE_MI_CARPETA>
   ```

3. Navega al directorio del proyecto.

   ```bash
   cd <EL_NOMBRE_DE_MI_CARPETA>
   ```

4. Crea un entorno virtual.

   ```bash
   python3 -m venv venv
   ```

5. Activa el entorno virtual.

   ```bash
   source venv/bin/activate
   ```

6. Instala las dependencias.

   ```bash
   python -m pip install -r requirements.txt
   ```

7. Inicializa el proyecto de Reflex.

   ```bash
   reflex init
   ```

8. Ejecuta el proyecto en local.

   ```bash
   reflex run
   ```

   _Podrás acceder a él entrando en la url `http://localhost:3000/` desde el navegador._

> Tienes más la información sobre [Reflex](https://reflex.dev/) en su [documentación oficial](https://reflex.dev/docs).

## Despliegue

Para realizar el despliegue del proyecto se ha creado un archivo `build.sh` que se encarga de ejecutar el flujo necesario para generar el directorio `public` con todos los recursos estáticos que necesita el servidor web.

Todo el proceso de empaquetado para producción podría ser delegado en el servidor, pero el repositorio cuenta siempre con el directorio `public` para que así puedas revisar el contenido estático de la web sin necesidad de ejecutar el script `build.sh`.

```bash
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
reflex init
reflex export --frontend-only
rm -fr public
unzip frontend.zip -d public
rm -f frontend.zip
deactivate
```

_Básicamente, prepera el entorno, instala dependencias, inicializa el proyecto, crea la construcción de producción, y la descomprime._

> El proyecto se puede desplegar en cualquier proveedor o servidor que soporte recursos estáticos.

Configuración en Vercel:

- Se ha asociado el repositorio de GitHub al proyecto (para que cada `push` en la rama `main` desencadene un nuevo despliegue)
- Build & Development Settings: Other
- Root Directory: `public` (que contiene el empaquetado estático para producción)

## Recursos utilizados

![Python](https://img.shields.io/github/stars/python/cpython?label=Python&style=social)
![Reflex](https://img.shields.io/github/stars/reflex-dev/reflex?label=Reflex&style=social)
![NES.css](https://img.shields.io/github/stars/nostalgic-css/NES.css?label=NES.css&style=social)
![Vercel](https://img.shields.io/github/stars/vercel/vercel?label=Vercel&style=social)

- Lenguaje: [Python](https://www.python.org/)
- Framework: [Reflex](https://reflex.dev/)
- CSS: [NES.css](https://nostalgic-css.github.io/NES.css/)
- GSAP: [GSAP](https://gsap.com/)
- Lenis: [Lenis](https://github.com/studio-freight/lenis)
- Fuente: [Press Start 2P](https://fonts.google.com/specimen/Press+Start+2P)
- Hosting: [Vercel](https://vercel.com/)
