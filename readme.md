# Clippus Rest-API

Esta es la documentación de API pública de la aplicación
[Clippus](https://clippus.info/), si aún no tienes una cuenta te invitamos a crearla.

La URL base para cualquier petición es 'https://api.clippus.info/'.

## Endpoints abiertos

Los endpoints abiertos no requieren token de autorización

### Obtener Token de autorización

Para obtener el token de autorización y ser utilizado en los endpoints cerrados:

* [Auth](auth.md) : `POST /api/public/auth`

## Endpoints que requieren token de autorización

Para endpoints cerrados es requerido un **Token** válido con el que se pueden realizar peticiones de manera segura. Este Token debe ser incluido en el **encabezado de la petición**. Este Token deberá ser obtenido mediante el endpoint de [Auth](auth.md) descrito anteriormente.

### Obtener visitantes

Para obtener la lista de los visitantes a tu establecimiento debes utilizar el siguiente endpoint:

* [Obtener visitantes](visitors/get.md) : `GET /api/public/visitors`

## Política y protección  de datos
Para conocer nuestra [política de protección de datos personales](https://clippus.info/politica-tratamiento-datos.html) y [nuestros términos y condiciones](https://clippus.info/terminos.html)

