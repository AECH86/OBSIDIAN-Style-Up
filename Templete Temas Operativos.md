**Temática**:
# DATA
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
	OR contains(file.lists.outlinks, this.file.link)
SORT file.mtime DESCENDING
```
## Reuniones
```dataview
TABLE without id Titulo as Reunion, Fecha
WHERE contains(file.link, this.file.link) And (Titulo or Fecha)
```
# GENERAL
## Notas Generales

## Reuniones

- Titulo::
	- Fecha:: 
	- PARTICIPANTES
	- NOTAS
	- ACCIONES
		- [ ]
