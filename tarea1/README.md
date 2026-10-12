# Administración de Proyectos de Software - Tarea 1

**Clave:** 1151055  
**Alumno:** Erick Alan Briones Sánchez  
**Carrera:** Ingeniería en Computación  
**Matrícula:** 2223037252  
**Docente:** Gabriel Hurtado Avilés  
**Fecha:** 11 de octubre de 2024

---

## Ejercicio 2. Investigación

### ¿Qué es un proyecto de software?

Un proyecto de software es un esfuerzo delimitado en el tiempo cuyo objetivo es diseñar, desarrollar e implementar una solución digital orientada a resolver un problema específico (Arcus AI, s. f.). A diferencia de los artefactos físicos de otras ingenierías, el software opera como un conjunto de instrucciones lógicas ejecutadas por hardware (IBM, s. f.).


---

### ¿Cómo se administra?

La gestión de proyectos consiste en guiar una iniciativa de principio a fin mediante un enfoque estructurado que permita a los equipos cumplir objetivos específicos dentro de parámetros delimitados (Atlassian, s. f.). 

Para llevar a cabo esta administración existen distintos enfoques:

* Los enfoques **predictivos** requieren una planificación detallada desde el principio y siguen una secuencia fija de pasos. Dan mejores resultados cuando los requisitos del proyecto son claros y es poco probable que sufran cambios.
* Los enfoques **adaptativos** gozan de un carácter flexible y permiten a los equipos ajustar los planes conforme avanza el proyecto. Son la mejor alternativa cuando los requisitos están sujetos a cambios o no se han esclarecido del todo al principio.
* Los enfoques **híbridos** combinan elementos de los métodos predictivos y adaptativos. Los equipos pueden recurrir a la planificación predictiva para unas fases y a los métodos adaptativos para otras, lo que permite mantener un equilibrio entre estructura y flexibilidad.

**Elección para el proyecto del curso**: 
Para un proyecto académico, el enfoque más conveniente es el **ágil / iterativo** (Scrum). A diferencia de un modelo predictivo que exige definir toda la arquitectura y requisitos sin margen de error, un esquema iterativo permite avanzar por entregas funcionales cortas, probar herramientas (como Docker y Git) y ajustar configuraciones de inmediato ante cualquier falla técnica sin tener que rehacer una planificación extensa.

---


### ¿Con qué herramientas?

Para planificar, ejecutar y supervisar proyectos de software, los equipos se apoyan en diversas herramientas de gestión y desarrollo (Atlassian, s. f.):

* **Control de versiones:** Registra el historial de cambios en el código fuente, permite trabajar en ramas paralelas y coordina los aportes del equipo sin sobreescribir el trabajo ajeno.
* **Tableros de trabajo:** Herramientas visuales de seguimiento. Según Atlassian (s. f.), «los equipos ágiles utilizan tableros de scrum para gestionar los sprints y los backlogs de los productos y los tableros de kanban para gestionar los flujos de trabajo y limitar el trabajo en progreso».
* **Contenedores:** Entornos aislados y ligeros que contienen todo lo necesario para ejecutar una aplicación sin depender de lo que esté instalado en el host, lo que permite que cualquier colaborador obtenga exactamente el mismo comportamiento (Docker, s. f.).
* **Integración continua (CI):** Práctica que automatiza la compilación y ejecución de pruebas con cada cambio en el repositorio, detectando errores de integración de forma temprana.

---

### ¿Bajo qué licencia se distribuye el software?

#### a) Los dos grandes tipos de licencias

El software de código abierto y libre se distribuye principalmente bajo dos filosofías legales:

* **Licencias permisivas (MIT, BSD, Apache 2.0):** Otorgan libertad prácticamente irrestricta sobre el código. Permiten a terceros usar, modificar, redistribuir, comercializar e incluso cerrar el software derivado para convertirlo en un producto propietario. Su única exigencia sustancial es conservar el aviso de derechos de autor (*copyright*) original y la renuncia explícita de garantías (Open Source Initiative [OSI], s. f.).
* **Licencias copyleft (GPL, LGPL, AGPL):** Emplean el marco legal de derechos de autor no para restringir, sino para garantizar la reciprocidad y libertad perpetua del software. Permiten modificar y distribuir el código, pero imponen la condición estricta de que cualquier obra derivada que sea distribuida debe publicarse bajo la misma licencia y con su código fuente accesible (Free Software Foundation [FSF], 2007).
  * *GPL:* Copyleft fuerte a nivel de aplicación completa.
  * *LGPL:* Permite el enlace dinámico con componentes propietarios sin exigir la liberación de todo el proyecto.
  * *AGPL:* Extiende las obligaciones de la GPL a servicios consumidos a través de una red o infraestructura en la nube (*SaaS*).

**Comparativa de permisos y obligaciones**

| Licencia | Categoría | Permite uso comercial | Permite modificar y distribuir | Exige liberar código derivado (*Copyleft*) | Requisitos clave |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **MIT** | Permisiva | Sí | Sí | **No** | Incluir la nota de *copyright* y la exención de responsabilidad en todas las copias. |
| **Apache 2.0** | Permisiva | Sí | Sí | **No** | Incluir *copyright*, documentar cambios y concede licencias expresas de patentes. |
| **GNU GPLv3** | Copyleft fuerte | Sí | Sí | **Sí (obligatorio)** | Distribuir el código fuente bajo GPLv3, documentar modificaciones y prohibir candados DRM. |
| **GNU AGPLv3** | Copyleft de red | Sí | Sí | **Sí (obligatorio)** | Mismas condiciones de GPLv3, sumando la obligación de entrega de código si se ejecuta como servicio web. |

---

##### b) Elección de licencia para el repositorio

* **¿Por qué usar MIT?:**  
  La licencia MIT es idónea para proyectos de aprendizaje, utilitarios o de portafolio debido a su mínima fricción administrativa y legal. Permite que cualquier desarrollador o empresa use, integre, modifique o bifurque el código sin temor a incompatibilidades de licenciamiento y sin restricciones comerciales (OSI, s. f.).
* **Ventajas principales:**
  * **Máxima adopción:** Facilita la reutilización del código en entornos tanto comunitarios como corporativos.
  * **Simplicidad:** El texto legal es breve, comprensible y no exige auditorías complejas sobre cómo se compilan o enlazan las dependencias.
* **¿Qué cambiaría si se hubiera elegido GPL?:**  
  Bajo una licencia GNU GPLv3, el código quedaría blindado contra la privatización. Cualquier persona u organización que tome el código, lo modifique y distribuya la solución resultante estaría legalmente obligada a liberar todo el código fuente del proyecto bajo la misma licencia GPLv3 (FSF, 2007). Esto impediría que una empresa incorpore el código dentro de un producto de software privativo o cerrado.

---

#### c) Caso real: Red Hat, CentOS y el surgimiento de Rocky Linux / AlmaLinux

**Qué ocurrió y cuándo**

Durante casi dos décadas, **CentOS** operó como una reconstrucción comunitaria, abierta y gratuita de **Red Hat Enterprise Linux (RHEL)**, compilada a nivel binario idéntico al sistema de pago de Red Hat. 

En **diciembre de 2020**, Red Hat (subsidiaria de IBM) anunció que descontinuaría CentOS 8 de forma anticipada para sustituirlo por **CentOS Stream**, una distribución que ya no serviría como clon posterior y estable de RHEL, sino como una rama intermedia de desarrollo continuo situada antes de cada lanzamiento corporativo (Red Hat, 2020). Este cambio dejó desamparadas a miles de organizaciones y servidores en producción que dependían de la estabilidad de CentOS sin pagar licencias de soporte empresarial.

**La reacción comunitaria**

Ante esta decisión, la comunidad de código abierto y figuras históricas como Gregory Kurtzer (cofundador original de CentOS) iniciaron proyectos independientes de reconstrucción limpia: **Rocky Linux** y **AlmaLinux**.

**Por qué la licencia permitió que la alternativa existiera sin pedir permiso**

La base del sistema operativo RHEL está compuesta por miles de paquetes de software libre, principalmente el núcleo Linux y las herramientas del proyecto GNU, distribuidos bajo la licencia **GNU General Public License (GPL)** (FSF, 2007). 

Por los términos vinculantes de la GPL, Red Hat está legalmente obligada a entregar y publicar el código fuente completo de todos los paquetes de software cubiertos por esta licencia a quien reciba los binarios. Ni Red Hat ni IBM tenían el derecho de revocar esas libertades.

La comunidad ejerció el derecho conferido por la GPL: tomó el código fuente público liberado por Red Hat, eliminó las marcas registradas, nombres comerciales y logotipos protegidos por copyright de la empresa, y recompiló el sistema operativo desde cero. De este modo, nacieron Rocky Linux y AlmaLinux como sistemas operativos 100% compatibles con RHEL, de forma legal e independiente, **sin requerir autorización ni consentimiento de Red Hat** (Vaughan-Nichols, 2020).

---

## Ejercicio 3. De PostgreSQL 17 a 18


### 1. Diferencias entre los dos contenedores

| Elemento | Qué decía (`1-postgres17`) | Qué dice (`2-postgres18`) | Por qué cambió |
| :--- | :--- | :--- | :--- |
| **Nombre del archivo** | `docker-compose.yml` | `compose.yaml` | Sigue la recomendación oficial de la Compose Specification. La convención con guion proviene de cuando Compose era una herramienta independiente en Python. |
| **Clave `version:`** | `version: '3.8'` | Omitida | Compose V2 ignora esta clave y avisa que es obsoleta al levantar el entorno. |
| **Nombre del proyecto (`name:`)** | No definido | `name: apsw-1151055-contenedor` | Evita usar el nombre de la carpeta base, el cual cambia entre máquinas y puede producir contenedores duplicados. |
| **Origen y construcción de la imagen** | `image: postgres:17` | `build: .`<br>`image: postgres-1151055:26o` | Ahora se compila localmente con el `Dockerfile` del directorio para incluir utilidades (`nano`, `less`), fijar el idioma (`C.UTF-8`), la zona horaria (`America/Mexico_City`) y el directorio de trabajo; `image:` define el nombre que tendrá la imagen construida. |
| **Versión base de PostgreSQL** | `postgres:17` (descarga la última menor disponible) | `postgres:18.6` (en el `Dockerfile`) | Fija la versión exacta para asegurar reproducibilidad y evitar diferencias por actualizaciones imprevistas de imagen. |
| **Nombres de contenedores** | `postgres173CV231AGO2026` | `apsw_db`<br>`apsw_adminer` | Estandariza los identificadores de los contenedores para el curso y añade el gestor web Adminer. |
| **Variables de entorno** | Fijas en texto plano (`postgres` / `postgres`) | Parametrizadas con valores por defecto: `${VAR:-defecto}` | Permite sobreescribir valores mediante un archivo `.env` sin exponer credenciales directamente en el archivo versionado. |
| **Codificación y ordenamiento** | No configuradas | `POSTGRES_INITDB_ARGS: "--encoding=UTF8 --locale=C"` | Garantiza que dos entornos ordenen y procesen cadenas exactamente de la misma manera. |
| **Mapeo de puertos** | `"5432:5432"` (expuesto a toda la red `0.0.0.0`) | `"127.0.0.1:${POSTGRES_PORT:-5434}:5432"` | Aísla la base a la interfaz de loopback local (`127.0.0.1`) por seguridad y mapea hacia el puerto 5434 (configurable) para no colisionar con instalaciones locales en el puerto estándar. |
| **Volumen de datos** | `./data:/var/lib/postgresql/data` (bind mount) | `datos_db:/var/lib/postgresql` (volumen administrado con nombre) | PostgreSQL 18 cambió la ruta interna del clúster (`PGDATA=/var/lib/postgresql/18/docker`). Montar `/var/lib/postgresql/data` con la imagen 18 impide el arranque del servicio. Además, el volumen nombrado persiste independientemente del árbol de archivos del sistema anfitrión. |
| **Puntos de montaje adicionales** | Ninguno | `./initdb` en `/docker-entrypoint-initdb.d:ro`<br>`./` en `/trabajo` | Permite ejecutar scripts de inicialización SQL/Bash en el primer arranque y montar la carpeta del proyecto dentro del contenedor. |
| **Directorio de trabajo (`working_dir`)** | Por defecto (`/`) | `/trabajo` | Ubica la sesión de trabajo directamente en la carpeta del proyecto al entrar por consola. |
| **Comprobación de estado (`healthcheck`)** | Ninguno | Configurado con `pg_isready` | Monitorea si el motor de la base de datos realmente responde antes de permitir la interacción con otros servicios. |
| **Servicios auxiliares** | Únicamente la base de datos | Servicio `adminer` (`adminer:5.5.1`) | Integra una interfaz web en el puerto 8080 para administrar y consultar la base sin instalar software adicional en el host. |

---

### 2. ¿Se usaba el Dockerfile viejo? Justificación técnica

**No, no se usaba.**

En el archivo `docker-compose.yml`, el servicio estaba definido exclusivamente con:

```yaml
services:
  postgres:
    image: postgres:17
```

Docker Compose únicamente invoca o construye un archivo Dockerfile cuando se especifica la directiva build: (por ejemplo, build: .). Al colocar únicamente image: postgres:17, Compose descarga directamente la imagen pública oficial desde Docker Hub y la ejecuta, ignorando por completo el Dockerfile ubicado en la carpeta.

En contraste, el archivo nuevo incluye build: . en el servicio db, lo que fuerza la construcción de la imagen a partir de su propio Dockerfile.

---

### 3. Versionado semántico y el cambio de la versión 17 a la 18

¿Qué es el versionado semántico?
El versionado semántico es una convención formal de nomenclatura para versiones de software estructurada en tres números: MAYOR.MENOR.PARCHE (por ejemplo, 18.6.0):

PARCHE (Patch): Incorpora correcciones de errores (bug fixes) manteniendo compatibilidad hacia atrás.

MENOR (Minor): Añade nueva funcionalidad preservando la compatibilidad con versiones previas.

MAYOR (Major): Introduce modificaciones sustanciales o incompatibles que rompen la compatibilidad hacia atrás (breaking changes).

¿Por qué pasar de la 17 a la 18 es un cambio mayor?
A partir de PostgreSQL 10, el esquema de versiones toma el primer número como la versión mayor del sistema (17, 18, etc.):

1. Incompatibilidad del almacenamiento físico del clúster: Los formatos de almacenamiento en disco de los datos y catálogos internos de PostgreSQL cambian entre versiones mayores. Un clúster de datos inicializado con los binarios de la versión 17 no puede ser leído ni iniciado de forma directa por el motor de la versión 18 sin una migración explícita (usando `pg_upgrade` o respaldo y restauración con `pg_dump`).
1. Ruptura en la estructura de rutas de la imagen Docker: En la imagen oficial de PostgreSQL 18, el directorio base interno cambió a `/var/lib/postgresql` (con `PGDATA=/var/lib/postgresql/18/docker`). Si se intenta reutilizar la ruta o volumen de la versión 17 (`/var/lib/postgresql/data`), el contenedor falla al iniciar con código de error.
1. Cambios en sintaxis, extensiones y parámetros: Las versiones mayores deprecian o retiran parámetros de configuración en `postgresql.conf`, modifican vistas de catálogos y alteran comportamientos internos del planificador de consultas.

## Ejercicio 4. MySQL + phpMyAdmin

### 1. Tabla comparativa: PostgreSQL + Adminer frente a MySQL + phpMyAdmin

| Criterio | PostgreSQL + Adminer | MySQL + phpMyAdmin |
| :--- | :--- | :--- |
| **Enfoque del motor de BD** | Objeto-relacional (ORDBMS). Destaca por su estricto apego al estándar SQL, soporte avanzado para tipos complejos (JSONB, arrays, GIS con PostGIS) y alta extensibilidad. | Puramente relacional (RDBMS). Muy popular en la web tradicional (pila LAMP), optimizado históricamente para lecturas rápidas y configuraciones sencillas. |
| **Peso y consumo del gestor web** | **Adminer** es extremadamente ligero; consta técnicamente de un único archivo PHP. Su imagen oficial en Docker suele pesar menos de 50 MB y consume muy poca memoria RAM. | **phpMyAdmin** es una suite completa con múltiples dependencias y módulos. Su imagen de contenedor es considerablemente más pesada (cientos de MB) y demanda más memoria. |
| **Soporte de múltiples motores en la UI** | Adminer es multigestor de forma nativa: una misma interfaz permite conectarse a PostgreSQL, MySQL, SQLite, Oracle, MS SQL, entre otros. | phpMyAdmin está diseñado exclusivamente para interactuar con MySQL y sus derivados directos (como MariaDB). |
| **Interfaz y curva de uso** | Minimalista, compacta y directa. Prioriza la rapidez de carga y la visualización tabular sin adornos. | Interfaz gráfica madura, rica en opciones visuales, asistentes y menús contextuales, aunque con mayor sobrecarga visual. |
| **Uso en laboratorios y contenedores** | Ideal para microservicios y prácticas locales por su despliegue instantáneo y casi nulo impacto en recursos del sistema anfitrión. | Muy extendido en entornos tradicionales de hospedaje web (cPanel), aunque más pesado para orquestaciones locales efímeras. |

---

### 2. Versiones LTS frente a Innovation y el uso de etiquetas fijas en Docker

**¿Qué es una versión LTS y una Innovation?**

A partir de la serie MySQL 8.4 y MySQL 9, Oracle adoptó un modelo de ciclo de vida dividido en dos líneas de distribución (Oracle Corporation, 2024):

- **Versión LTS (*Long-Term Support*):**
  * Diseñada para entornos de producción corporativos donde la estabilidad y la predictibilidad son críticas (Oracle Corporation, 2024).
  * Mantiene el comportamiento del motor sin introducir cambios incompatibles ni nuevas funciones que rompan el sistema (Oracle Corporation, 2024).
  * Recibe parches de seguridad y correcciones de errores (*bug fixes*) durante un periodo extendido de soporte de hasta 8 años (Oracle Corporation, 2024).
- **Versión Innovation:**
  * Diseñada para entornos de desarrollo y adopción temprana donde se busca probar las últimas características técnicas (Oracle Corporation, 2024).
  * Su ciclo de vida es corto (meses) y es sustituida rápidamente por la siguiente versión de la serie (Oracle Corporation, 2024).
  * Puede introducir cambios sustanciales, deprecaciones o funciones experimentales que no garantizan compatibilidad a largo plazo (Oracle Corporation, 2024).

---

### ¿Por qué se usa `mysql:9.7.2` y no `mysql:latest`?

En entornos de contenedores e ingeniería de software, utilizar una etiqueta explícita como `mysql:9.7.2` en lugar de `mysql:latest` responde a principios fundamentales de diseño y reproducibilidad:

1. **`latest` no significa "estable", significa "lo último que se subió":**  
   La etiqueta `latest` es simplemente un puntero mutable que apunta a la imagen construida más recientemente en el registro. No garantiza estabilidad ni una versión aprobada.
2. **Rompe la reproducibilidad (*idempotencia*):**  
   Si dos colaboradores o entornos de CI/CD ejecutan `docker compose up -d` usando `latest` en momentos distintos, uno podría descargar una versión y otro una posterior completamente distinta, provocando fallas difíciles de depurar del tipo «en mi máquina sí funciona».
3. **Incompatibilidad del almacenamiento de datos:**  
   Los motores de bases de datos relacionales cambian sus formatos de almacenamiento interno y catálogos entre versiones. Si se usa `latest`, una actualización automática e imprevista de la imagen puede intentar arrancar sobre un volumen de datos creado por una versión anterior, impidiendo el arranque del contenedor y corrompiendo el clúster.
4. **Fijar la versión (`9.7.2`) congela el entorno:**  
   Especificar el tag completo garantiza que cada miembro del equipo y cada servidor descarguen exactamente los mismos binarios con el mismo comportamiento esperado en cada ejecución.

   
## Declaración sobre el uso de inteligencia artificial:

En la elaboración de este documento se utilizó Gemini (Google, 2026) como herramienta de asistencia para la estructuración de respuestas en formato Markdown, la síntesis técnica de conceptos y la normalización de referencias bibliográficas bajo el estándar APA 7.ª edición. Todo el contenido generado fue revisado, validado técnicamente y verificado con las fuentes documentales oficiales y el material de la UEA por el autor.

## Referencias

- IBM. (s. f.). *¿Qué es el desarrollo de software?* Recuperado el 11 de octubre de 2026, de https://www.ibm.com/mx-es/think/topics/software-development
- Arcus AI. (s. f.). Guía de tipos de proyectos de software y cómo desarrollarlos. *Blog de Arcus Way*. Recuperado el 11 de octubre de 2026, de https://www.arcusway.com/post/guia-de-tipos-de-proyectos-de-software-y-como-desarrollarlos
- Atlassian. (s. f.). *¿Qué es la Gestión de proyectos de TI?* The Workstream. Recuperado el 11 de octubre de 2026, de https://www.atlassian.com/es/work-management/project-management
- Docker. (s. f.). *What is Docker?*. Docker Docs. Recuperado el 11 de octubre de 2026, de https://docs.docker.com/get-started/overview/
- Free Software Foundation. (2007). *GNU General Public License* (versión 3). Free Software Foundation. https://www.gnu.org/licenses/gpl-3.0.html
- Open Source Initiative. (s. f.). *The MIT License*. Open Source Initiative. Recuperado el 11 de octubre de 2026, de https://opensource.org/license/mit
- Red Hat. (2020, 8 de diciembre). *CentOS Stream: Building an innovative future for enterprise Linux*. Red Hat Blog. https://www.redhat.com/en/blog/centos-stream-building-innovative-future-enterprise-linux
- Vaughan-Nichols, S. J. (2020, 10 de diciembre). *Goodbye CentOS, hello Rocky Linux*. ZDNet. https://www.zdnet.com/article/goodbye-centos-hello-rocky-linux/
- Oracle Corporation. (2024). *Introducing MySQL Innovation and Long-Term Support (LTS) versions*. MySQL Server Blog. https://dev.mysql.com/blog-archive/introducing-mysql-innovation-and-long-term-support-lts-versions/
- Google. (2026). *Gemini* (Versión octubre 2026) [Modelo de lenguaje de gran escala]. https://gemini.google.com/