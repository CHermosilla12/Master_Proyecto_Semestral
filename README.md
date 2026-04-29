# Master_Proyecto_Semestral
Repositorio Maestro del proyecto semestral de Desarrollo FullStack I con enlaces a otros repositorios y README

# Proyecto Semestral: NextCard
## Integrantes: Felipe Acuña, Constanza Carrasco, Cristóbal Hermosilla

### Estado del Sistema (Hito 1.5)
| Microservicio | Puerto | DB Name | Funcionalidad |
| :--- | :--- | :--- | :--- |
| Usuario | Instancia_1:8080 | UsuarioDB | CRUD de Usuario |
| Envios | Instancia_1:8081 | EnviosDB | CRUD de Envios |
| Catalogo | Instancia_2:8080 | CatalogoDB | CRUD de Producto |
| Tienda | Instancia_2:8081 | TiendaDB | CRUD de Tienda |
| Proveedores | Instancia_2:8082 | ProveedoresDB | CRUD de Proveedores |

### Despliegue Técnico
- **Instancias** 3 instancias de AWS EC2 t3.large (Ubuntu 24.04)
- **Comando de inicio:** `docker compose up -d` en cada carpeta de modulo
