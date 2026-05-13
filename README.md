# Master_Proyecto_Semestral
Repositorio Maestro del proyecto semestral de Desarrollo FullStack I con enlaces a otros repositorios y README

# Proyecto Semestral: NextCard
## Integrantes: Felipe Acuña, Constanza Carrasco, Cristóbal Hermosilla

### Estado del Sistema (Hito 1.5)
| Microservicio | Puerto | DB Name | Funcionalidad |
| :--- | :--- | :--- | :--- |
| Usuario     | Instancia_1:8080     | UsuarioDB     | CRUD de Usuario |
| Comprador   | Instancia_1:8083   | CompradorDB   | CRUD de Comprador |
| Vendedor    | Instancia_1:8084    | VendedorDB    | CRUD de Vendedor|
| Vehiculo    | Instancia_1:8082    | VehiculoDB    | CRUD de Vehiculo |
| Envios      | Instancia_1:8081      | EnviosDB      | CRUD de Envios |
| Catalogo    | Instancia_2:8080    | CatalogoDB    | CRUD de Producto |
| Tienda      | Instancia_2:8081      | TiendaDB      | CRUD de Tienda |
| Proveedores | Instancia_2:8082 | ProveedoresDB | CRUD de Proveedores |
| Carrito     | Instancia_2:8083     | CarritoDB     | CRUD de Proveedores |
| Carta       | Instancia_2:8084       | CartaDB       | CRUD de Carta |
| Torneos     | Instancia_3:8080     | TorneoDB      | CRUD de  |
| Subasta     | Instancia_3:8081     | DB | CRUD de  |
| Venta   | Instancia_3:8082       | DB | CRUD de  |

### Despliegue Técnico
- **Instancias** 3 instancias de AWS EC2 t3.large (Ubuntu 24.04)
- **Comando de inicio:** `docker compose up -d` en cada carpeta de modulo

