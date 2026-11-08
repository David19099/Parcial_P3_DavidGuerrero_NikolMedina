# Parcial_P3_DavidGuerrero_NikolMedina
# Inventario Forestal Nacional (IFN) – IDEAM

DAVID SANTIAGO GUERRERO GARCIA 012501371065
NIKOL FERNANDA MEDINA MONTERREY 012501371052

## Descripción
El **Inventario Forestal Nacional (IFN) – IDEAM** es un proyecto desarrollado en Python que tiene como propósito brindar soporte al registro, gestión y consulta de información relacionada con las inspecciones de conglomerados forestales en campo.
El programa permite registrar y administrar información sobre los conglomerados, las brigadas de trabajo, la geolocalización, el conteo y clasificación de árboles según su diámetro (fustales, latizales y brinzales), así como los datos correspondientes al muestreo botánico.
Además, permite consultar los registros almacenados, generar informes consolidados y calcular indicadores relacionados con la cobertura vegetal mediante un menú interactivo ejecutado desde la consola.
El sistema está desarrollado bajo una **arquitectura de tres capas** (Presentación, Lógica de Negocio y Datos) y utiliza archivos de texto plano para garantizar la persistencia de la información.
## 🎯 Objetivo general
Desarrollar un programa en Python que facilite el registro, almacenamiento, consulta y procesamiento de información del Inventario Forestal Nacional (IFN), permitiendo gestionar los datos de las inspecciones forestales y generar indicadores relevantes para el análisis de la información recopilada.
### Objetivos específicos
- Registrar información de las inspecciones de conglomerados forestales.
- Gestionar los datos de las brigadas de trabajo y la geolocalización.
- Realizar el conteo y clasificación de árboles en tres categorías: fustales, latizales y brinzales.
- Registrar información del muestreo botánico, incluyendo nombre común, uso y código de identificación de las especies.
- Implementar persistencia de datos mediante archivos de texto plano, evitando la pérdida de información al cerrar el programa.
- Permitir la consulta estructurada de los registros mediante el ID del conglomerado.
- Generar informes e indicadores relacionados con la cantidad de árboles, la densidad de cobertura vegetal, las especies identificadas y sus respectivos usos.
Funcionamiento del programa
El sistema cuenta con un menú interactivo en consola que permite acceder a las diferentes funcionalidades.
### 1. Inicialización
Al iniciar el programa, se cargan las estructuras necesarias para su funcionamiento y se verifica la existencia del archivo de persistencia `inspecciones_ifn.txt`. Si el archivo no existe, se prepara para almacenar los nuevos registros.
### 2. Menú interactivo
Se presenta un menú en consola con las opciones disponibles para:
- Registrar nuevas inspecciones.
- Consultar inspecciones por ID de conglomerado.
- Generar informes e indicadores.
- Salir del sistema.
### 3. Registro de inspecciones
El programa solicita al usuario los datos correspondientes a cada inspección, incluyendo:
- Identificación del conglomerado.
- Información de la brigada.
- Datos de geolocalización.
- Cantidad de árboles por categoría.
- Información de las muestras botánicas.
### 4. Persistencia de datos
Los datos ingresados se organizan mediante una estructura delimitada y se almacenan en el archivo `inspecciones_ifn.txt`, utilizando operaciones de escritura en modo de adición (`append`).
Esto permite conservar los registros y recuperarlos en futuras ejecuciones del programa.
### 5. Consulta por ID
El sistema realiza una búsqueda secuencial en el archivo de texto plano para localizar el conglomerado solicitado. Si encuentra coincidencias, presenta la información correspondiente de manera organizada.
### 6. Generación de informes
El programa procesa los registros almacenados para generar un informe consolidado con los principales indicadores forestales, incluyendo el total de conglomerados, la cantidad de árboles, la densidad promedio, las especies identificadas y sus usos.
Cálculos realizados
El sistema implementa los siguientes cálculos:
**1. Total de conglomerados**
Corresponde a la cantidad de inspecciones registradas en el sistema.
**2. Total de árboles**
Se calcula sumando las tres categorías de árboles registradas en cada conglomerado:
`Total de árboles = Fustales + Latizales + Brinzales`
**3. Densidad promedio de cobertura vegetal**
Se obtiene dividiendo el total de árboles registrados entre el número total de conglomerados evaluados:
`Densidad = Total de árboles / Total de conglomerados`
Este indicador representa el promedio de árboles registrados por conglomerado.
Validación de datos y manejo de excepciones
El programa incorpora mecanismos de validación para garantizar la integridad de la información ingresada y evitar errores durante su ejecución.

Entre las medidas implementadas se encuentran:

- Validación de entradas numéricas.
- Control de cantidades inválidas de árboles.
- Uso de estructuras condicionales para verificar los datos ingresados.
- Implementación de bloques `try/except` para gestionar excepciones.
- Manejo de errores relacionados con la lectura y escritura de archivos.
- Verificación de la disponibilidad del archivo de persistencia.

Estas medidas permiten mejorar la estabilidad y confiabilidad del sistema.
Reportes y salidas generadas
El programa proporciona diferentes resultados a través de la consola:

- Mensajes de confirmación o error durante el registro de información.
- Visualización detallada de las inspecciones consultadas mediante su ID.
- Informe consolidado del total de conglomerados evaluados.
- Cantidad total de árboles registrados.
- Densidad promedio de árboles por conglomerado.
- Listado de especies botánicas identificadas.
- Relación de los usos registrados para las especies.
- Archivo de texto plano con los registros almacenados.

Arquitectura del sistema
El proyecto utiliza una **arquitectura de tres capas**, que permite organizar el código y separar las responsabilidades de cada componente.
| Capa | Responsabilidad |
|---|---|
| Presentación | Interacción con el usuario mediante el menú de consola y visualización de resultados. |
| Lógica de Negocio | Procesamiento de datos, validaciones, cálculos e indicadores forestales. |
| Datos | Almacenamiento, lectura y consulta de información mediante archivos de texto plano. |
Esta organización facilita el mantenimiento, la comprensión y la ampliación del programa.

Autores
- **Nikol Fernanda Medina Monterrey**
- **David Santiago Guerrero García**
