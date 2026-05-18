# Master_Proyecto_Semestral
Repositorio Maestro del proyecto semestral de Desarrollo FullStack I con enlaces a otros repositorios y README

# Proyecto Semestral: NextCard

## Integrantes: Felipe Acuña, Constanza Carrasco, Cristóbal Hermosilla

### Estado del Sistema
| Microservicio | Puerto | DB Name | Funcionalidad | Link |
| :--- | :--- | :--- | :--- |  :--- |
| Usuario     | Instancia_1:8080     | UsuarioDB     | CRUD de Usuario | https://github.com/Felipex360x/ms-usuario |
| Comprador   | Instancia_1:8084   | CompradorDB   | CRUD de Comprador | https://github.com/Felipex360x/ms-comprador |
| Vendedor    | Instancia_1:8085    | VendedorDB    | CRUD de Vendedor| https://github.com/Felipex360x/ms-vendedor |
| Repartidor | Intancia_1:8083 | RepartidorDB | CRUD de Repartidor | https://github.com/Felipex360x/ms-repartidor |
| Vehiculo    | Instancia_1:8082    | VehiculoDB    | CRUD de Vehiculo | https://github.com/Felipex360x/ms-vehiculo |
| Envios      | Instancia_1:8081      | EnviosDB      | CRUD de Envios |https://github.com/Felipex360x/ms-envios |
| Catalogo    | Instancia_2:8080    | CatalogoDB    | CRUD de Producto | https://github.com/CHermosilla12/catalogoservice |
| Tienda      | Instancia_2:8081      | TiendaDB      | CRUD de Tienda | https://github.com/CHermosilla12/tiendaservice |
| Proveedores | Instancia_2:8082 | ProveedoresDB | CRUD de Proveedores | https://github.com/CHermosilla12/proveedorservice |
| Carrito     | Instancia_2:8083     | CarritoDB     | CRUD de Carrito | https://github.com/CHermosilla12/carritoservice |
| Torneos     | Instancia_3:8080     | TorneoDB   | CRUD de Torneo Torneos | https://github.com/Constanza05-ctrl/torneoservice |
| Subasta     | Instancia_3:8085     | SubastaDB | CRUD de Subasta Subasta |https://github.com/Constanza05-ctrl/subastaservice |
| Venta   | Instancia_3:8086       | VentaDB | CRUD de Venta  | https://github.com/Constanza05-ctrl/ventaservice |
### Despliegue Técnico
- **Instancias** 3 instancias de AWS EC2 t3.large (Ubuntu 24.04)
- **Comando de inicio:** `docker compose up -d` en cada carpeta de modulo
### Extra
-antes de inciar nuevamente los docker realizar un `docker compose down -v` en cada parte de modulo para que no quede con datos antiguos que pueden afectar 
al levantamiento 

### Diagrama de dependencias
<img width="5760" height="3240" alt="Mapa de microservicios" src="https://github.com/user-attachments/assets/497f2796-c98e-404e-b616-86d9f68e0df3" />
### Tabla de contratos
| Origen | Destino | Método | Endpoint | DTO |
|---|---|---|---|---|
| Producto | Carrito | GET | /api/productos/{id} | ProductoDTO |
| Tienda | Torneo | GET | /api/v2/tienda/{/id} | TiendaDTO |
| Comprador|Usuario|Get |/api/v2/compradores/{id}| CompradorDTO |
| Vendedor|Usuario|Get |/api/v2/vendedores/{id}| VendedorDTO |
| Repartidor|Usuario|Get |/api/v2/repartidores/{id}| RepartidorDTO |
| Vehiculo|Repartidor|Get |/api/v2/repartidores/{id}| RepartidorDTO |


### Tecnología utilizada
- Cliente REST: **Feign Client** (justificación: elimina el código repetitivo al permitirte declarar la comunicación HTTP mediante interfaces simples anotadas, abstrayéndote por completo de configurar URLs o serializaciones manuales.)
- Manejo de errores: `@RestControllerAdvice` + excepciones personalizadas
- Logs: SLF4J en cada llamada externa
- Pruebas de integración: colección Postman en `/postman/hito2-integracion.json`

### Escenario de despliegue
- [ ] Escenario A — Todos los servicios en una sola instancia EC2
- [X] Escenario B — Servicios distribuidos en múltiples instancias EC2
  - Security Groups configurados: sí

### Cómo probar la integración
1. Levantar todos los servicios: `docker compose up -d`
2. Importar `postman/hito2-integracion.json` en Postman
3. Ejecutar el flujo "Crear cita - caso éxito"
4. Para probar resiliencia: `docker stop catalogoservice` y reintentar
