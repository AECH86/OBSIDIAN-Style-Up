---
Semana:
---

> [!NOTE] PROCESO DE PLANEACION SEMANAL
> 1. Revisa el calendario de la proxima semana e identifica los temas relevantes de cada tematica.
> 	1. TITULO (FECHA)
> 2. Enlista los temas identificados en su respectiva seccion
> 3. Define y enlista  las tareas generales que se deben realizar para cada tema identificado
> 4. Calendariza en Outlook el periodo que le dedicaras a resolver el tema 

<%*
// Get the current date
const today = new Date();

// Calculate the difference between today and the next Monday
const toMonday = today.getDay() === 0 ? -6 : 1 - today.getDay();

// Calculate the difference between today and the next Friday
const toFriday = 5 - today.getDay();

// Calculate the date of the current week's Monday
const monday = new Date(today);
monday.setDate(today.getDate() + toMonday);

// Calculate the date of the current week's Friday
const friday = new Date(today);
friday.setDate(today.getDate() + toFriday);

// Calculate the date of next week's Monday
const nextMonday = new Date(monday);
nextMonday.setDate(monday.getDate() + 7);

// Calculate the date of next week's Friday
const nextFriday = new Date(friday);
nextFriday.setDate(friday.getDate() + 7);

// Format the dates as DD-MM-YY
const format = (date) => {
  let day = date.getDate().toString().padStart(2, '0');
  let month = (date.getMonth() + 1).toString().padStart(2, '0');
  let year = date.getFullYear().toString().substr(-2);
  return `${year}-${month}-${day}`;
};

// Output the formatted date ranges
tR += `Current Week: ${format(monday)} a ${format(friday)}\n`;
tR += `Next Week: ${format(nextMonday)} a ${format(nextFriday)}`;
%>

# REUNIONES
1. 

# TAREAS GENERALES
1. 

# RELACION CON SOCIOS COMERCIALES
1. 

# TEMAS CONCURSOS EN PROCESO 
1. 

# PROSPECCION Y POSICIONAMIENTO
1. 
