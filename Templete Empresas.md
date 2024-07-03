---
Empresa: 
Nacionalidad: 
URL: 
tags:
---
# DATA
## Reuniones
```dataview
TABLE without id 
	file.link as "Link", 
	join(regexreplace(Titulo, "^", "  -"), "<br>") as "Titulo", 
	join(fecha, "<br>") as Fecha
WHERE contains(Empresa, this.file.link) 
	AND (Titulo or Fecha)
```
## Oportunidades
```dataview
table without id file.link as "Proyecto", Estatus,Estado,AreaM2,ArranqueConc,LiderDN,Broker,Gerencia,Diseñador
from "ABITAT/Oportunidades"
where contains(Empresa,this.file.link) OR contains(Broker,this.file.link) OR contains(Gerencia,this.file.link) OR contains(Diseñador,this.file.link)
```
## Personas
```dataview
table without id file.link as "Persona",Puesto,Base,Correo,Linkedin
from "ABITAT/Personas"
where contains(Empresa,this.file.link)
```
## Pendientes
```dataview
task
where contains(Empresa,this.file.link)
WHERE !completed
GROUP BY file.link
```
## Menciones
```dataview
TABLE WITHOUT ID 
	file.link as "Link", 
	regexreplace(file.folder, ".*\/([^\/]+\/[^\/]+\/[^\/]+)$", "$1") as "Folder"
FROM [[]]
WHERE !contains(Empresa, this.file.link) 
	AND !contains(Gerencia, this.file.link) 
	AND !contains(Broker, this.file.link) 
	AND !contains(Diseñador, this.file.link)
	OR contains(file.lists.outlinks, this.file.link)
SORT file.mtime DESCENDING
```
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
