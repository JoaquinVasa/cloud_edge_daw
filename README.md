# # Tarea (a+b) · Cloud: niveles y funciones (DAW 1º)

## 🅰️ Tarea A — Niveles de cloud (IaaS/PaaS/SaaS)
Crea una tabla con 10 servicios reales. Incluye enlace oficial y justifica responsabilidades.

| **Servicio**                        | **Proveedor**      | **Nivel (IaaS/PaaS/SaaS)** | **Enlace oficial**                                                                                     | **¿Qué gestiona el proveedor?**                             | **¿Qué gestiona el equipo/usuario?**                       |
| ----------------------------------- | ------------------ | -------------------------- | ------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------- | ---------------------------------------------------------- |
| Amazon EC2                          | AWS                | IaaS                       | [https://aws.amazon.com/ec2/](https://aws.amazon.com/ec2/)                                             | Centros de datos, hardware, red, virtualización             | Sistema operativo, parches, aplicaciones, seguridad del SO |
| AWS Lambda                          | AWS                | PaaS (FaaS)                | [https://aws.amazon.com/lambda/](https://aws.amazon.com/lambda/)                                       | Infraestructura, escalado automático, runtime base          | Código, lógica de negocio, permisos y eventos              |
| Azure App Service                   | Microsoft Azure    | PaaS                       | [https://azure.microsoft.com/services/app-service/](https://azure.microsoft.com/services/app-service/) | Servidores, SO, runtime y balanceo                          | Código de la app, configuración, variables de entorno      |
| Salesforce CRM                      | Salesforce         | SaaS                       | [https://www.salesforce.com/](https://www.salesforce.com/)                                             | Aplicación completa, infraestructura, actualizaciones       | Configuración del CRM, usuarios, datos                     |
| Google Workspace                    | Google             | SaaS                       | [https://workspace.google.com/](https://workspace.google.com/)                                         | Aplicaciones, infraestructura, seguridad base               | Gestión de cuentas, políticas, contenido                   |
| Amazon S3                           | AWS                | PaaS (almacenamiento)      | [https://aws.amazon.com/s3/](https://aws.amazon.com/s3/)                                               | Infraestructura de almacenamiento, durabilidad, replicación | Organización de datos, permisos, ciclo de vida             |
| Microsoft OneDrive                  | Microsoft          | SaaS                       | [https://www.microsoft.com/onedrive/](https://www.microsoft.com/onedrive/)                             | Almacenamiento, sincronización, disponibilidad              | Gestión de archivos, accesos y carpetas                    |
| Firebase                            | Google             | PaaS                       | [https://firebase.google.com/](https://firebase.google.com/)                                           | Backend, base de datos, autenticación, hosting              | Lógica de la app, reglas de acceso, datos                  |
| GitHub                              | GitHub (Microsoft) | SaaS                       | [https://github.com/](https://github.com/)                                                             | Plataforma, repositorios, disponibilidad                    | Código, gestión de repos, permisos                         |
| Oracle Cloud Infrastructure Compute | Oracle             | IaaS                       | [https://www.oracle.com/cloud/compute/](https://www.oracle.com/cloud/compute/)                         | Infraestructura física, red, virtualización                 | SO, aplicaciones, seguridad del sistema                    |

## 🅱️ Tarea B — Funciones principales de cloud (arquitectura)
Incluye un diagrama (ASCII/Mermaid/imagen) y una explicación breve.
1. Usuarios
Son las personas o equipos que usan la nube desde un navegador o una app.

2. Aplicaciones
Son los programas que se ejecutan en la nube (webs, correos, sistemas).

3. Computación
Es la “fuerza” que hace funcionar las aplicaciones (servidores, funciones).

4. Almacenamiento
Es donde se guardan los datos (archivos, fotos, bases de datos).

5. Red
Permite que todo esté conectado y que los datos viajen por Internet.

6. Seguridad y gestión
Protege la información y controla quién puede acceder.
### Diagrama
(Pega aquí el diagrama)
┌──────────────┐
│   Usuarios   │
└──────┬───────┘
       │ Internet
┌──────▼───────┐
│ Frontend /   │  Acceso web, apps, APIs
│ Cliente      │
└──────┬───────┘
       │
┌──────▼───────┐
│ Aplicaciones │  Lógica de negocio
└──────┬───────┘
       │
┌──────▼───────────┐
│ Computación      │  VMs, contenedores, serverless
├──────────────────┤
│ Almacenamiento   │  Objetos, bases de datos, backups
├──────────────────┤
│ Red              │  VPC, balanceo, firewall
├──────────────────┤
│ Seguridad/Gestión│  IAM, monitoreo, logs
└──────────────────┘

### Explicación (8–12 líneas)
(Describe el flujo front → API → BBDD/storage y dónde entra la cloud)
El usuario accede a la aplicación desde un navegador o una app móvil (frontend).
El frontend envía las peticiones a través de Internet hacia una API alojada en la nube.
La API se ejecuta en servicios cloud de computación (máquinas virtuales, contenedores o funciones).
Esta API procesa la lógica del negocio y decide qué datos necesita.
Cuando es necesario, la API consulta o guarda información en la base de datos o en el almacenamiento cloud.
La base de datos y el storage también están gestionados dentro de la nube.
Una vez procesados los datos, la API devuelve la respuesta al frontend.
El frontend muestra la información final al usuario.
La nube proporciona escalado, seguridad y disponibilidad en todo el flujo.
### Mapeo de funciones cloud a componentes (mínimo 3)
- Procesamiento → Máquinas virtuales (VMs), contenedores (Docker), servicios de cómputo gestionado (AWS EC2, Azure VM, Google Compute Engine)
- Ejecución → Funciones serverless / FaaS (AWS Lambda, Azure Functions, Google Cloud Functions)
- Almacenamiento → Almacenamiento de objetos (Amazon S3, Azure Blob Storage, Google Cloud Storage)
- Intercambio → APIs, colas de mensajes, brokers de eventos

## 📚 Fuentes (enlaces oficiales)
(Enlaces oficiales usados en la tabla A y en la B)
A
[https://aws.amazon.com/ec2/](https://aws.amazon.com/ec2/) 
[https://aws.amazon.com/lambda/](https://aws.amazon.com/lambda/)
[https://azure.microsoft.com/services/app-service/]
(https://azure.microsoft.com/services/app-service/)
[https://www.salesforce.com/](https://www.salesforce.com/) 
[https://workspace.google.com/](https://workspace.google.com/)
[https://aws.amazon.com/s3/](https://aws.amazon.com/s3/)
[https://www.microsoft.com/onedrive/]
(https://www.microsoft.com/onedrive/)
[https://firebase.google.com/](https://firebase.google.com/)
[https://github.com/](https://github.com/)
[https://www.oracle.com/cloud/compute/]
(https://www.oracle.com/cloud/compute/)  
B
https://aws.amazon.com/what-is-cloud-computing/
 — AWS (Amazon Web Services)

https://cloud.google.com/learn/what-is-cloud-architecture
 — Google Cloud

https://docs.cloud.google.com/architecture
 — Google Cloud

https://aws.amazon.com/products/compute/
 — AWS (Amazon Web Services)

https://cloud.google.com/storage
 — Google Cloud

https://cloud.google.com/learn/what-is-cloud-security
 — Google Cloud

https://aws.amazon.com/getting-started/aws-security-essentials/
 — AWS (Amazon Web Services)
