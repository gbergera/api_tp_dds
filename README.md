# api_tp_dds

## Descripcion
Service a presentar para el tp de dds, permite obtener las recomendaciones de puntos de donacion cercanos a una ubicacion en base a su latitud y longitud

**CURSO**: martes maniana grupo 13

## Endpoints

### Obtener Recomendacion de puntos de donacion

**Método:** `GET`

**URL:** `/recommendations/?lat=&long=&limit=`

**Parámetros:**

- `lat` (float): Latitud de la ubicación actual (entre -90 y 90).
- `lon` (float): Longitud de la ubicación actual (entre -180 y 180).
- `limit` (int, opcional): limite de respuestas.

**Respuesta:**
- `200 OK` con una lista de puntos de donación cercanos.


### Cargar punto de donacion

**Método:** `POST`

**URL** `/punto/`


**JSON:**

```
[
  {
    "nombre": "string",
    "lat": 0,
    "long": 0,
    "direccion": "string"
  }
]
```

**Respuesta:**
- `200 OK` 

## Levantar la api de forma local

### Pasos
- Utiliza base de datos MySql, se recomienda crear un `.env` con un `DB_CONNECTION` y la ruta.
- Utilizar comando `uvicorn main:app --reload --port (puerto)` en la consola del proyecto, en caso de no incluir el flag de port por default se asignara `http://127.0.0.1:8000`

### Dependencias 
- `fastapi`
- `sqlalchemy`
-  `geopy`
-  `pydantic`




