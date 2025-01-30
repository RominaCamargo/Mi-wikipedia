# Mi Wikipedia

**Mi Wikipedia** es una aplicación web que permite a los usuarios crear y ver contenido en formato Markdown, el cual es procesado y mostrado como HTML en una página web. El sistema permite ingresar y visualizar textos escritos en Markdown, facilitando la creación de contenido como artículos, guías o cualquier otro tipo de documentación.

## Características

- **Interfaz sencilla**: La aplicación tiene una interfaz fácil de usar, donde los usuarios pueden ingresar texto en formato Markdown.
- **Renderización de Markdown a HTML**: El contenido escrito en Markdown se convierte automáticamente a HTML para ser mostrado en la página.
- **Accesibilidad**: Los usuarios pueden ver los artículos creados sin necesidad de registros, solo mediante el enlace directo a la página.
- **Backend en Perl**: El sistema está construido con Perl y utiliza CGI para procesar las solicitudes del usuario.
  
## Tecnologías Utilizadas

- **HTML**: Estructura de la página web.
- **CSS**: Estilos visuales para la presentación de la página.
- **Perl (CGI)**: Backend para procesar y renderizar el contenido Markdown.
- **Markdown**: Lenguaje de marcado utilizado para la entrada de contenido.
- **Docker**: La aplicación está dockerizada para facilitar su instalación y ejecución.

## Instalación

Para ejecutar este proyecto en tu máquina local, sigue estos pasos:

1. **Clonar el repositorio**:

   ```bash
   git clone https://github.com/RominaCamargo/Mi-wikipedia.git
   cd Mi-wikipedia
   ```

2. **Construir la imagen de Docker**:

   Asegúrate de tener Docker instalado. Luego, construye la imagen con el siguiente comando:

   ```bash
   docker build -t mi-wikipedia .
   ```

3. **Ejecutar el contenedor Docker**:

   Una vez que la imagen se haya creado, ejecuta el contenedor:

   ```bash
   docker run -p 80:80 mi-wikipedia
   ```

   Esto hará que la aplicación esté disponible en tu navegador en `http://localhost`.

## Uso

1. Abre la página en tu navegador.
2. Ingresa tu contenido en el editor de Markdown.
3. Haz clic en el botón para ver el contenido renderizado como HTML.
4. Los resultados se mostrarán en la misma página.

## Estructura de Archivos

- **Dockerfile**: Contiene las instrucciones para construir la imagen de Docker.
- **cgi-bin/render.pl**: Script Perl que procesa el contenido Markdown y lo convierte en HTML.
- **css/styles.css**: Archivo de estilos CSS para la presentación de la página web.
- **index.html**: Página principal que contiene el editor de Markdown y muestra el HTML resultante.
