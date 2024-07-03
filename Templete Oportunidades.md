---
Empresa: 
LiderDN: 
LiderCyC: 
Estado: 
Localidad: 
Nue/Rep: 
ArranqueConc: 
AreaM2: 
ValorMMXN: 
Segmento: 
Broker: 
Gerencia: 
Diseñador: 
Competencia: 
Estatus: 
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
	