# Documentación Damaged Tags

Uso de endpoints para damaged tags

## Endpoints

### 1. Descargar Image Resource 

**Method:** GET  
**Endpoint:** `/api/damaged-tags/download-resource?id=:id`  

Descarga un recurso basado en el `id` proporcionado.

**Example Request:**
```http
GET {url}/api/damaged-tags/download-resource?id=12345
Authorization: Bearer <token>
```

### 2. Change status masivo e individual

**Method:** POST  
**Endpoint:** `/api/damaged-tags/change-status`  
**Body:** `{
    "ids" : [:id1, :id2, ... :idn]
}`  

Cambia el estado de los `damaged-tags` indicados en el body por ids. Para actualización individual usar un solo `id`.

**Example Request:**
```http
POST {url}/api/damaged-tags/change-status
body: {
    "ids" : [1, 21, 23]
}
Authorization: Bearer <token>
```
