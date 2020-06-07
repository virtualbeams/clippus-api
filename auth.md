# Auth / Login

Usada para obtener el Token válido para las peticiones.

**URL** : `/api/public/auth/`

**Método** : `POST`

**Autenticación requerida** : NO

**Restricciones de datos**

```json
{
    "email": "[valid email address]",
    "password": "[password in plain text]"
}
```

**Datos de petición de ejemplo**

```json
{
    "email": "email@example.com",
    "password": "abcd1234"
}
```

## Respuesta exitosa

**Código** : `200 OK`

**Contenido ejemplo de respuesta**

```json
{
    "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJhdWQiOiIxIiwianRpIjoiZmQ1Mzhh....",
    "token_type": "Bearer",
    "expires_at": "2021-06-07 01:17:01",
    "role": 1
}
```

## Respuesta de error

**Condición** : Si 'email' o 'password' son incorrectas.

**Código** : `401 UNAUTHOTIZED`

**Contenido** :

```json
{
    "message": [
        "Unauthorized"
    ]
}
```