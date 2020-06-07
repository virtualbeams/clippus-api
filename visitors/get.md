# Obtener lista de visitantes

Obtiene la lista de lista de visitantes a tu establecimiento.

**URL** : `/api/public/visitors`

**Método** : `GET`

**Autenticación requerida** : YES

**Tipo de atenticación** : Authorization: Bearer <token>

**Restricciones de datos**

```json
{
    "point_id": "[Opcional | ID del punto | Númerico]",
    "visit_from": "[Opcional | formato: aaaa-mm-dd hh:mm:ss]",
    "visit_to": "[Opcional | formato: aaaa-mm-dd hh:mm:ss]"
}
```

**Datos de petición de ejemplo**

```json
{
    "point_id": "4",
    "visit_from": "2020-06-03 10:04:05",
    "visit_to": "2020-06-06 10:04:05"
}
```


## Respuesta exitosa

**Código** : `200 OK`

**Contenido de ejemplo**

Acá se muestra la estructura de la respuesta:

```json
{
    "message": "Successfully get visitors",
    "list": [
        {
            "id": 2,
            "uuid": "939303331",
            "document_type": 1,
            "document": "1214534232",
            "in_out": "in",
            "name": "Martin",
            "lastname": "Rodriguez",
            "birthday": "1997-02-11",
            "blood_type": "O+",
            "gender": "M",
            "phone": "3206783412",
            "email": "martin@gmail.com",
            "has_app": 0,
            "temperature": 35.5,
            "address": null,
            "accept_terms": 1,
            "latitude": "",
            "longitude": "",
            "comments": "Viene de zona sur",
            "visit_date": "2020-06-04 10:04:05",
            "account_id": 1,
            "point_id": 4,
            "created_at": "2020-06-01T20:06:50.000000Z",
            "updated_at": "2020-06-01T20:06:50.000000Z",
            "point": {
                "id": 4,
                "point_name": "Principal",
                "point_code": "P001",
                "name": "Entrada Principal",
                "username": "punto1",
                "email": "okk8YnsUYDXfot8B0tPo@clippus.info",
                "role": 1,
                "account_id": 1,
                "created_at": "2020-05-29T04:54:08.000000Z",
                "updated_at": "2020-06-02T01:11:22.000000Z"
            }
        }
    ],
    "totalPages": 0,
    "currentPage": 1,
    "totalRows": 1,
    "rowsPerPage": 30
}
```

## Nota importante

* Solo está habilitado realizar 100 peticiones por hora, en caso de sobrepasar ese límite el servidor respondrá:

**Código** : `429 Too Many Requests`