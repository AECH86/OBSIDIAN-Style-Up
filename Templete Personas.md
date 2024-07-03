---
Empresa: 
Base: 
Tipo: 
Puesto: 
Correo: 
Cel: 
Linkedin: 
Cumpleaños: 
tags:
---
# DATA
## Reuniones
```dataview
TABLE without id 
	file.link as "Link",
	join(regexreplace(Titulo, "^", "  -"), "<br>") as "Titulo", 
	join(fecha, "<br>") as Fecha
WHERE file.name = this.file.name
```
## Proyectos
```dataview
TABLE WITHOUT ID
	file.link as "Proyecto",
	Empresa,
	Estatus,
	Estado,
	AreaM2,
	ArranqueConc,
	LiderDN,
	Broker,
	Gerencia,
	Diseñador
FROM "USER/Oportunidades"
WHERE contains(Empresa,this.file.link) 
	OR contains(Broker,this.file.link) 
	OR contains(Gerencia,this.file.link) 
	OR contains(Diseñador,this.file.link) 
	OR contains(LiderDN,this.file.link)
	OR contains(LiderCyC, this.file.link)
```
## Pendientes
```dataview
TASK
WHERE contains(resp,this.file.link)
WHERE !completed
GROUP BY file.link
```
## Menciones
```dataview
TABLE WITHOUT ID 
	file.link as "Link", 
	regexreplace(file.folder, ".*\/([^\/]+\/[^\/]+\/[^\/]+)$", "$1") as "Folder",
	file.mday as "Modified"
FROM [[]]
WHERE !contains(Empresa, this.file.link) 
	AND !contains(Gerencia, this.file.link) 
	AND !contains(Broker, this.file.link) 
	AND !contains(Diseñador, this.file.link)
	AND !contains(LiderDN, this.file.link)
	AND !contains(LiderCyC, this.file.link)
	OR contains(file.lists.outlinks, this.file.link)
SORT file.mtime DESCENDING
```
# GENERAL
## Notas Generales
- 
## Reuniones

- **Titulo**:: 
	- **Fecha**:: 
	- **PARTICIPANTES**
	- **NOTAS**
	- **ACCIONES**
		- 
