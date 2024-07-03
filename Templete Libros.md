---
Autor: 
Fecha: 
tags:
---

```dataview
TABLE WITHOUT ID 
	file.link as "Menciones", 
	regexreplace(file.folder, ".*\/([^\/]+\/[^\/]+\/[^\/]+)$", "$1") as "Folder",
	file.cday as "Created", 
	file.mday as "Modified"
FROM [[]]
SORT file.mtime DESCENDING
```
# NOTAS
- 




