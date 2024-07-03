---
tags: []
---
# REFLEXIONES
## AECH
```dataview

TABLE without id 
	file.link as "Link", 
	Ref.ReflexionAECH AS "Reflexiones Sobre AECH"
WHERE contains(file.tags,"#TAG")
FLATTEN file.lists as Ref
WHERE contains(Ref.ReflexionAECH,"#TAG")
SORT file.link asc
```
## USER
```dataview
TABLE without id 
	file.link as "Link", 
	Ref.ReflexionUSER AS "Reflexiones Sobre USER"
WHERE contains(file.tags,"#TAG")
FLATTEN file.lists as Ref
WHERE contains(Ref.ReflexionAbitat,"#TAG")
SORT file.link asc
```
## Atypical
```dataview
TABLE without id 
	file.link as "Link", 
	Ref.ReflexionAtypical AS "Reflexiones Sobre Atypical"
WHERE contains(file.tags,"#TAG")
FLATTEN file.lists as Ref
WHERE contains(Ref.ReflexionAtypical,"#TAG")
SORT file.link asc
```

# EXPANSION DEL CONCEPTO
> [!reflexion] Lorem Ipsum
> - Lorem Ipsum


# CONCLUSIONES

