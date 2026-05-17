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
| Envios      | Instancia_1:8081      | EnviosDB      | CRUD de Envios |
| Catalogo    | Instancia_2:8080    | CatalogoDB    | CRUD de Producto | https://github.com/CHermosilla12/catalogoservice |
| Tienda      | Instancia_2:8081      | TiendaDB      | CRUD de Tienda | https://github.com/CHermosilla12/tiendaservice |
| Proveedores | Instancia_2:8082 | ProveedoresDB | CRUD de Proveedores | https://github.com/CHermosilla12/proveedorservice |
| Carrito     | Instancia_2:8083     | CarritoDB     | CRUD de Carrito | https://github.com/CHermosilla12/carritoservice |
| Carta       | Instancia_2:8084       | CartaDB   | CRUD de Carta |
| Torneos     | Instancia_3:8080     | TorneoDB   | CRUD de Torneo |
| Subasta     | Instancia_3:8081     | SubastaDB | CRUD de Subasta |
| Venta   | Instancia_3:8082       | VentaDB | CRUD de Venta  |

### Despliegue Técnico
- **Instancias** 3 instancias de AWS EC2 t3.large (Ubuntu 24.04)
- **Comando de inicio:** `docker compose up -d` en cada carpeta de modulo
### Extra
-antes de inciar nuevamente los docker realizar un `docker compose down -v` en cada parte de modulo para que no quede con datos antiguos que pueden afectar 
al levantamiento 

