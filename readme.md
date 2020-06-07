# Clippus Rest-API

Esta es la documentación de API pública de la aplicación
[Clippus](https://clippus.info/), si aún no tienes una cuenta te invitamos a crearla.

La URL base para cualquier petición es 'https://api.clippus.info/'.

## Endpoints abiertos

Endpoints públicos no requieren autenticación

* [Auth](auth.md) : `POST /api/pubic/auth`

## Endpoints que requieren autenticación

Endpoints cerrados requiren un token valido el cual debe ser uncluido en el encabezado de la petición. El token puede ser obtenido usando el endpoint de "Auth" descrito anteriormente.

### Obtener visitantes

Para obtener los visitantes a tu establecimiento debes utilizar el siguiente endpoint:

* [Obtener visitantes](visitors/get.md) : `GET /api/public/visitors`

## Política y protección  de datos
Para conocer nuestra [política de protección de datos personales](https://clippus.info/politica-tratamiento-datos.html) y [nuestros términos y condiciones](https://clippus.info/terminos.html)

