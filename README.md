# API de Google Calendar con Python

Este proyecto utiliza la API de Google Calendar para obtener eventos del calendario.

## Configuración

Antes de poder ejecutar el script, deberás configurar las credenciales de OAuth 2.0 y descargar el token para la API de Google Calendar. Sigue estos pasos:

### Paso 1: Habilitar la API de Google Calendar

1. Ve a [Google Cloud Platform Console](https://console.cloud.google.com/).

2. Desde la lista de proyectos, selecciona un proyecto o crea uno nuevo.

3. Si la página de APIs & servicios no está ya abierta, abre el menú del lado izquierdo de la consola y selecciona **APIs & servicios**.

4. En el lado izquierdo, haz clic en **Biblioteca**.

5. En la Biblioteca de API, busca "API de Google Calendar".

6. Haz clic en la API para crear credenciales.

### Paso 2: Crear Credenciales

1. Ve a **Credenciales** en el menú del lado izquierdo.

2. Haz clic en **CREAR CREDENCIALES** y selecciona **ID de cliente de OAuth**.

3. Si aún no has configurado la pantalla de consentimiento de OAuth, se te pedirá que lo hagas.

4. Para el tipo de aplicación, elige **Aplicación de escritorio**.

5. Haz clic en **Crear**. Se mostrarán tu nuevo ID de cliente de OAuth y el secreto.

6. Descarga las credenciales haciendo clic en el icono de descarga en el lado derecho (es un archivo JSON).

### Paso 3: Instalar las Librerías Requeridas

Este proyecto requiere Python y la Google Client Library. Puedes instalar la Google Client Library usando pip:

```bash
python3 -m venv env
source env/bin/activate
pip install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib
```

### Paso 4: Configura Tu Script en Python

1. Cambia el nombre del archivo JSON descargado a `credentials.json` y colócalo en el mismo directorio que tu script de Python.

2. Cuando ejecutes el script por primera vez, te pedirá que autorices el acceso a tu Google Calendar.

3. Haz clic en el enlace proporcionado, elige tu cuenta de Google y haz clic en **Permitir**.

4. Serás redirigido a una página que proporciona un código. Copia este código, regresa a tu aplicación y pégalo en el símbolo del sistema.

5. El archivo `token.pickle` se creará automáticamente. Este token se utiliza para acceder a tus eventos de calendario.

Ahora puedes ejecutar el script tantas veces como quieras sin tener que autorizar la aplicación cada vez.

## Ejecución del Script

Para ejecutar el script, utiliza el comando:

```bash
python3 calendar.py
```
