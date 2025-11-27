
+ Crear fechas
	+ Mes / Día  / Año 
+ Para measure: Aconcagua
	+ Crear: Numero * unit
	+ Convertir: `aMeasure convertTo: baseUnit`

1) January/10/2019 crea la fecha 10 de Enero de 2019
2) 10:00 crea la hora 10:00
3) January/10/2019 at: 10:00 crea el día/hora del 10 de Enero de 2019 a las 10:00
4) (January/10/2019 at: 10:00) to: (January/10/2019 at: 11:00) crea un intervalo de tiempo que va desde el 10 de Enero de 2019 a las 10:00 a las 11:00 del mismo día. De la misma manera se puede crear intervalos solo de fechas como January/10/2019 to: January/11/2019 o de horas 10:00 to: 15:30.
5) Los día se semana son Sunday (para domingo), Monday (para lunes), etc.
6) Se pueden crear medidas de tiempo multiplicando una cantidad por su unidad, por ejemplo: 1*hour o 10*day o 5*week, etc.
7)  January/10/2019 to: January/15/2019 by: 2*day crea un intervalo de fechas que va desde el 10 al 15 de Enero cada 2 dias, o sea que incluye el 10, 12 y 14 de Enero.
8) January/10/2019 to: FixedGregorianDate theEndOfTime crea un intervalo de fecha que empieza el 10 de Enero de 2019 y no termina.
