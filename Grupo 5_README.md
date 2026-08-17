Grupo 5
Integrantes:
Kevin Coello
Katherine Nieto
Elizabeth Agila

README – Diseñar un flujo analítico reproducible

1. Descripción del proyecto

El proyecto integra información proveniente de diferentes fuentes de datos para realizar un proceso reproducible de lectura, validación, transformación, integración y generación de resultados.



2. Fuentes de datos

•	empleados.xlsx
•	socioeconomico.csv
•	educacion.json



3. Estructura del proyecto

El proyecto organiza la información en carpetas para mantener las fuentes originales, las versiones de respaldo, los datos procesados y los resultados.
tarea_educacion/
├── README.md
└── data/
    ├── raw/
    ├── raw_versions/
    ├── processed/
    └── outputs/


4. Proceso realizado

1.	Creación de las carpetas del proyecto.
2.	Generación de una copia versionada de las bases originales.
3.	Lectura controlada de las fuentes de información.
4.	Validación de las variables requeridas y de las claves de unión.
5.	Homogeneización de la variable cod_provincia.
6.	Integración de las diferentes fuentes mediante cod_provincia.
7.	Auditoría de las coincidencias obtenidas en las uniones.
8.	Tratamiento de valores faltantes.
9.	Cálculo de la tasa de docentes por cada 100 estudiantes.
10.	Generación y auditoría de los archivos finales.


5. Clave de integración

La variable cod_provincia se utiliza como clave común para integrar las diferentes fuentes. El código se estandariza a dos dígitos mediante zfill(2).



6. Variable derivada

Se calcula la variable tasa_docente_estu, que representa la cantidad de docentes por cada 100 estudiantes:
tasa_docente_estu = (Total_Docentes / Total_Estudiantes) × 100


7. Resultados generados

•	consolidado_provincial_informacion_202601.csv
•	tablero_indicadores_informacion_202601.xlsx
•	manifiesto_ejecucion.json


8. Trazabilidad

El proceso genera versiones de las fuentes originales y calcula el hash SHA-256 de los archivos finales para facilitar la trazabilidad y verificar su integridad.



9. Reglas de trabajo del equipo

Commits: registrar cambios con mensajes claros que indiquen qué se modificó.
Ramas: trabajar los cambios o funcionalidades en ramas separadas antes de incorporarlos a la rama principal.
Revisión de cambios: revisar el código antes de incorporarlo a la rama principal.
README: mantener actualizada la documentación cuando cambien la estructura, ejecución o resultados del proyecto.

==========================================================================

10. Consideraciones

Las fuentes originales deben conservarse sin modificaciones. Los cambios y transformaciones se realizan durante el procesamiento, manteniendo la trazabilidad de los archivos generados.
