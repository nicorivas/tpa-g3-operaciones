# Reglas de auditoría de informes de visitas

Un lote son los informes de `datos/informes.csv`. Para cada informe se decide una de tres cosas: `marcar` (se devuelve o se revisa a mano), `pasar` (sin problema) o `espera` (hay una señal, pero no cabe y queda en una lista de espera con su motivo).

1. Un informe sin firma del cliente no se cierra. Se devuelve al técnico, sin excepciones.
2. Un informe con fecha posterior a hoy, o con fecha dentro de una licencia del técnico, se devuelve al técnico.
3. Cada visita debe tener fotos suficientes para su tipo. Mínimo de fotos: instalación 6, mantención 4, falla 3. Duración mínima de una visita: 15 minutos.
4. Ante la duda, se marca el informe, pero por orden de gravedad y hasta el cupo de la regla 5. Orden de más a menos grave: reglas 1 y 2 (firma, fecha, licencia), duplicado (regla 9), contradicción entre texto y campo (regla 6), informe sin fotos, fotos bajo el mínimo y duración bajo el mínimo. Si hay empate, pesa más una visita de seguridad.
5. El equipo de calidad revisa como máximo 30 informes marcados por lote. Se marcan los 30 más graves según la regla 4. Los demás informes con señal quedan en `espera`, con su motivo escrito. Un informe marcado sin defecto real cuenta como falso positivo y se descuenta al desempeño del agente auditor.
6. Si el texto del informe y un campo se contradicen, se marca. Por ejemplo, el texto dice que se cambiaron filtros y el campo dice 0. Hasta que el técnico lo corrija, manda el campo.
7. Un informe de visita de seguridad (urgencia «seguridad») se cierra el mismo día de la auditoría para que se active el seguimiento, sin excepciones.
8. Los informes de un técnico en período de prueba (60 días desde su ingreso) se marcan igual, pero se devuelven a su supervisor y no cuentan en el cupo de la regla 5.
9. Si hay dos informes del mismo técnico, del mismo equipo y de la misma fecha, se marca el segundo y se conserva el primero.
10. Cada informe marcado debe llevar escrito el número de la regla que se aplicó.
