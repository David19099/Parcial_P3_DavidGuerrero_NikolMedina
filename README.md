# Parcial_P3_DavidGuerrero_NikolMedina
Sistema de Inventario Forestal Nacional (IFN) - IDEAMSoftware desarrollado en Python para brindar soporte a la ejecución y gestión de la información del Inventario Forestal Nacional (IFN) del IDEAM, implementado bajo los principios de Programación Estructurada.   
Descripción del ProyectoEl programa permite registrar, consultar y procesar inspecciones de conglomerados forestales evaluados por las brigadas de campo, gestionando el conteo de árboles por diámetros (fustales, latizales, brinzales) y la toma de muestras botánicas.   
Arquitectura del Software (3 Capas)El proyecto está dividido en módulos independientes para cumplir con los estándares técnicos solicitados:Capa de Presentación: Interacción con el usuario mediante un menú en consola y captura de datos de entrada.   Capa de Lógica de Negocio: Procesamiento, validación, filtrado por ID y cálculo de indicadores (como la densidad de cobertura vegetal).   Capa de Datos: Gestión exclusiva de la lectura y escritura de la información en un archivo de texto plano (inspecciones_ifn.txt).  
Funcionalidades del Menú 
1. Registrar nueva inspección: Solicita el ID del conglomerado, geolocalización, brigada asignada, conteo de árboles (fustales, latizales, brinzales), nombre común de la especie, uso y código de muestra.
2. Consultar inspección por ID: Busca dentro del archivo plano y despliega de forma estructurada toda la información asociada a un conglomerado.
3. Generar informes e indicadores: Calcula automáticamente la densidad de cobertura vegetal y lista las especies y usos registrados.
4. Salir: Cierra la ejecución del sistema.
Persistencia de DatosEl sistema implementa persistencia en archivos de texto plano. Cada registro se almacena de forma estructurada en un archivo llamado inspecciones_ifn.txt, lo que garantiza que los datos no se pierdan al cerrar el programa.   🚀 Instrucciones de Ejecución
