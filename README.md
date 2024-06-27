# Proyecto: Sprint 4

## Descripción del Proyecto

¡Felicidades! Has completado la sección de Análisis estadístico de datos. Es hora de aplicar el conocimiento y las habilidades que has adquirido en un proyecto: un estudio de caso analítico real que completarás por tu cuenta.

Trabajas como analista para el operador de telecomunicaciones Megaline. La empresa ofrece a sus clientes dos tarifas de prepago, Surf y Ultimate. El departamento comercial quiere saber cuál de los planes genera más ingresos para poder ajustar el presupuesto de publicidad.

Vas a realizar un análisis preliminar de las tarifas basado en una selección de clientes relativamente pequeña. Tendrás los datos de 500 clientes de Megaline: quiénes son los clientes, de dónde son, qué tarifa usan, así como la cantidad de llamadas que hicieron y los mensajes de texto que enviaron en 2018. Tu trabajo es analizar el comportamiento de los clientes y determinar qué tarifa de prepago genera más ingresos.

## Descripción de las Tarifas

### Surf

- Pago mensual: $20.
- 500 minutos al mes, 50 SMS y 15 GB de datos.
- Si se exceden los límites del paquete:
  - 1 minuto: 3 centavos.
  - 1 SMS: 3 centavos.
  - 1 GB de datos: $10.

### Ultimate

- Pago mensual: $70.
- 3000 minutos al mes, 1000 SMS y 30 GB de datos.
- Si se exceden los límites del paquete:
  - 1 minuto: 1 centavo.
  - 1 SMS: 1 centavo.
  - 1 GB de datos: $7.

## Diccionario de Datos

### Tabla users (datos sobre los usuarios):

- `user_id`: identificador único del usuario.
- `first_name`: nombre del usuario.
- `last_name`: apellido del usuario.
- `age`: edad del usuario (en años).
- `reg_date`: fecha de suscripción (dd, mm, aa).
- `churn_date`: fecha en la que el usuario dejó de usar el servicio.
- `city`: ciudad de residencia del usuario.
- `plan`: nombre de la tarifa.

### Tabla calls (datos sobre las llamadas):

- `id`: identificador único de la llamada.
- `call_date`: fecha de la llamada.
- `duration`: duración de la llamada (en minutos).
- `user_id`: identificador del usuario que realiza la llamada.

### Tabla messages (datos sobre los SMS):

- `id`: identificador único del SMS.
- `message_date`: fecha del SMS.
- `user_id`: identificador del usuario que envía el SMS.

### Tabla internet (datos sobre las sesiones web):

- `id`: identificador único de la sesión.
- `mb_used`: volumen de datos usados durante la sesión (en megabytes).
- `session_date`: fecha de la sesión web.
- `user_id`: identificador del usuario.

### Tabla plans (datos sobre las tarifas):

- `plan_name`: nombre de la tarifa.
- `usd_monthly_fee`: pago mensual en dólares.
- `minutes_included`: minutos incluidos al mes.
- `messages_included`: SMS incluidos al mes.
- `mb_per_month_included`: datos incluidos al mes (en megabytes).
- `usd_per_minute`: precio por minuto tras exceder los límites del paquete.
- `usd_per_message`: precio por SMS tras exceder los límites del paquete.
- `usd_per_gb`: precio por gigabyte de los datos extra tras exceder los límites del paquete.

## Instrucciones para Completar el Proyecto

### Paso 1: Abre el Archivo de Datos y Estudia la Información General

- Abre los archivos de datos (`/datasets/megaline_calls.csv`, `/datasets/megaline_internet.csv`, `/datasets/megaline_messages.csv`, `/datasets/megaline_plans.csv` y `/datasets/megaline_users.csv`) y echa un vistazo al contenido general de cada tabla.

### Paso 2: Prepara los Datos

- Convierte los datos en los tipos necesarios.
- Encuentra y elimina errores en los datos. Explica qué errores encontraste y cómo los eliminaste.
- Para cada usuario, busca:
  - El número de llamadas realizadas y minutos utilizados al mes.
  - La cantidad de SMS enviados por mes.
  - El volumen de datos usado por mes.
  - Los ingresos mensuales por cada usuario. 

### Paso 3: Analiza los Datos

- Describe el comportamiento de la clientela:
  - Encuentra los minutos, SMS y volumen de datos que requieren los usuarios de cada tarifa por mes.
  - Calcula la media, la varianza y la desviación estándar.
  - Traza histogramas. Describe las distribuciones.

### Paso 4: Prueba las Hipótesis

- El ingreso promedio de los usuarios de las tarifas Ultimate y Surf difiere.
- El ingreso promedio de los usuarios en el área de estados Nueva York-Nueva Jersey es diferente al de los usuarios de otras regiones.
- Explica cómo formulaste las hipótesis nula y alternativa.
- Explica qué criterio utilizaste para probar las hipótesis y por qué.

### Paso 5: Escribe una Conclusión General

- Completa todas las tareas en un Jupyter Notebook. Almacena todo el código en las celdas `code` y las explicaciones de texto en las celdas `markdown`. Añade títulos y el formato adecuado si es necesario.

## Contribución

Si deseas contribuir a este proyecto, por favor realiza un fork del repositorio y crea una pull request con tus mejoras. Asegúrate de que tu código sigue los lineamientos del proyecto y está bien comentado.

## Licencia

Este proyecto está bajo la licencia MIT. Para más detalles, consulta el archivo LICENSE.
