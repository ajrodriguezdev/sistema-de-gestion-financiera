# 💰 Sistema de Gestión Financiera

<img src="https://img.shields.io/badge/Java-17%2B-orange?style=for-the-badge&logo=openjdk&logoColor=white"/>
  <img src="https://img.shields.io/badge/Spring_Boot-Backend-6DB33F?style=for-the-badge&logo=springboot&logoColor=white"/>
  <img src="https://img.shields.io/badge/SQL-Database-4479A1?style=for-the-badge&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Maven-Build-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white"/>
</p>

<p align="center">
&#x20; Aplicación backend para el registro, administración y seguimiento de ingresos, egresos y movimientos financieros.
</p>

---

## 📌 Descripción del proyecto

El Sistema de Gestión Financiera es una aplicación orientada a la administración y control de operaciones financieras.

Permitirá registrar ingresos y egresos, organizar movimientos por categorías, consultar historiales y generar resúmenes que faciliten el análisis de la información financiera.

El sistema estará desarrollado con Java y Spring Boot, aplicando principios de arquitectura por capas, persistencia de datos y reglas de negocio para garantizar la consistencia de las operaciones.

## 🎯 Objetivos

- Gestionar ingresos y egresos.
- Clasificar movimientos financieros.
- Consultar historiales de operaciones.
- Calcular balances y saldos.
- Generar resúmenes financieros.
- Implementar validaciones para evitar inconsistencias.
- Aplicar transacciones para proteger la integridad de los datos.

## ⚙️ Funcionalidades

| Funcionalidad           | Descripción                                   | Estado       |
| ----------------------- | --------------------------------------------- | ------------ |
| Registro de ingresos    | Registrar entradas de dinero                  | 📋 Pendiente |
| Registro de egresos     | Registrar salidas de dinero                   | 📋 Pendiente |
| Categorías              | Clasificar movimientos financieros            | 📋 Pendiente |
| Consulta de movimientos | Consultar historial de operaciones            | 📋 Pendiente |
| Balance financiero      | Calcular ingresos, egresos y saldo disponible | 📋 Pendiente |
| Filtros                 | Buscar movimientos por fecha o categoría      | 📋 Pendiente |
| Resúmenes               | Generar reportes de comportamiento financiero | 📋 Pendiente |
| Validaciones            | Controlar montos y datos de las operaciones   | 📋 Pendiente |

## 🛠️ Tecnologías utilizadas

**Backend**

- Java
- Spring Boot
- Spring Web
- Spring Data JPA
- Hibernate

**Base de datos**

- SQL
- PostgreSQL o MySQL (motor por definir)

**Herramientas**

- Maven
- Git y GitHub
- Postman
- IntelliJ IDEA o Visual Studio Code

## 🏗️ Arquitectura del proyecto

```text
src/
└── main/
    ├── java/com/finanzas/
    │   ├── controller/
    │   ├── service/
    │   ├── repository/
    │   ├── entity/
    │   ├── dto/
    │   ├── exception/
    │   └── FinanzasApplication.java
    └── resources/
        └── application.properties
```

### Responsabilidad de las capas

| Capa       | Responsabilidad                        |
| ---------- | -------------------------------------- |
| Controller | Recibir y responder solicitudes HTTP   |
| Service    | Ejecutar cálculos y reglas financieras |
| Repository | Consultar y persistir información      |
| Entity     | Representar movimientos y categorías   |
| DTO        | Transportar información de la API      |
| Exception  | Gestionar errores y validaciones       |

## 🗄️ Modelo de datos

Se contempla inicialmente el siguiente modelo:

- **Transaction:** representa un ingreso o egreso.
- **Category:** clasifica los movimientos financieros.
- **Account:** representa una cuenta o fuente de dinero.
- **TransactionType:** identifica el tipo de movimiento.

El modelo definitivo se establecerá durante el diseño de la base de datos.

## 🔗 Endpoints proyectados

| Método | Endpoint                     | Descripción                  |
| ------ | ---------------------------- | ---------------------------- |
| POST   | `/api/transactions`          | Registrar movimiento         |
| GET    | `/api/transactions`          | Consultar movimientos        |
| GET    | `/api/transactions/{id}`     | Consultar movimiento         |
| PUT    | `/api/transactions/{id}`     | Actualizar movimiento        |
| DELETE | `/api/transactions/{id}`     | Eliminar movimiento          |
| GET    | `/api/transactions/income`   | Consultar ingresos           |
| GET    | `/api/transactions/expenses` | Consultar egresos            |
| GET    | `/api/finance/balance`       | Consultar balance            |
| GET    | `/api/finance/summary`       | Consultar resumen financiero |

*Los endpoints son una propuesta inicial.*

## 📊 Lógica financiera

El sistema contemplará cálculos básicos para consultar el estado financiero:

**Balance disponible**

```text
Balance = Total de ingresos - Total de egresos
```

**Total de ingresos**

```text
Total ingresos = Suma de movimientos de tipo ingreso
```

**Total de egresos**

```text
Total egresos = Suma de movimientos de tipo egreso
```

Los cálculos se realizarán utilizando tipos de datos adecuados para valores monetarios y reglas que eviten errores de precisión.

## 🚀 Instalación y ejecución

### Requisitos previos

- Java 17 o superior.
- Maven.
- Motor de base de datos SQL.
- Git.

### 1. Clonar el repositorio

```bash
git clone https://github.com/ajrodriguezdev/sistema-gestion-financiera.git
```

### 2. Ingresar al proyecto

```bash
cd sistema-gestion-financiera
```

### 3. Configurar la conexión

La configuración definitiva dependerá del motor de base de datos seleccionado.

```properties
spring.datasource.url=${DB_URL}
spring.datasource.username=${DB_USERNAME}
spring.datasource.password=${DB_PASSWORD}
```

### 4. Ejecutar la aplicación

```bash
mvn spring-boot:run
```

## 🧪 Pruebas

Se utilizará Postman para validar el registro y consulta de operaciones, los cálculos de balances y el comportamiento de las reglas financieras.

También se contemplan pruebas automatizadas para los servicios y operaciones críticas.

## 🗺️ Roadmap

- [ ] Configuración inicial de Spring Boot.
- [ ] Selección y configuración de la base de datos.
- [ ] Diseño del modelo de datos.
- [ ] Implementación de entidades y repositorios.
- [ ] Desarrollo del registro de ingresos y egresos.
- [ ] Implementación de categorías.
- [ ] Cálculo de balances.
- [ ] Filtros por fecha y categoría.
- [ ] Generación de resúmenes financieros.
- [ ] Manejo de transacciones y excepciones.
- [ ] Pruebas automatizadas y con Postman.
- [ ] Documentación de la API.

## 👩‍💻 Autora

**Andrea Rodriguez**
Ingeniera de Sistemas | Backend Developer

- GitHub: [@ajrodriguezdev](https://github.com/ajrodriguezdev)
- LinkedIn: [Perfil profesional](https://www.linkedin.com/in/aj-rodriguez-g)

---

\<p align="center">
&#x20; Desarrollado con Java y Spring Boot.
&#x20; \<br/>
&#x20; \<b>Transformando operaciones en información financiera. 💻\</b>
\</p>
