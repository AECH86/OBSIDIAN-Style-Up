---
Programa_Curso: 
Tematica_Curso: 
URL_Curso: 
Fecha_Curso: 
Instructor: 
tags:
---
# DATA
## Menciones
```dataview
TABLE WITHOUT ID file.link as "Menciones", regexreplace(file.folder, ".*\/([^\/]+)$", "$1") as "Folder", file.cday as "Created", file.mday as "Modified"
FROM [[]]
SORT file.mtime DESCENDING
```
## Reuniones
```dataview
TABLE without id Titulo as Reunion, Fecha
WHERE contains(file.link, this.file.link) And (Titulo or Fecha)
```
***
# GENERAL

## Notas Generales
- 
## Reuniones

- Titulo:: 
	- Fecha:: 
	- PARTICIPANTES
	- NOTAS
	- ACCIONES
		- 
