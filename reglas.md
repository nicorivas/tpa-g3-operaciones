# Reglas de auditoría de informes de visitas

Un lote son los informes de `datos/informes.csv`. Para cada informe se decide una de tres cosas: `marcar` (se devuelve o se revisa a mano), `pasar` (sin problema) o `espera` (hay una señal, pero no cabe y queda en una lista de espera con su motivo).

1. Un informe sin firma del cliente no se cierra. Se devuelve al técnico, sin excepciones.
2. Un informe con fecha posterior a hoy, o con fecha dentro de una licencia del técnico, se devuelve al técnico.
3. Cada visita debe tener fotos suficientes para su tipo y una duración razonable. Mínimo de fotos: instalación 3, mantención 2, falla 2. Duración mínima: 15 minutos. Un informe de la APK 2.3 sin fotos con fecha entre el 3 y el 8 de noviembre queda en `espera` hasta confirmar por escrito si lo afectó el error.
4. Ante la duda, se marca el informe, pero solo hasta el cupo de la regla 5. Los informes con señal se ordenan por gravedad: 1) seguridad sin firma; 2) sin firma, fecha posterior a hoy o visita en licencia; 3) duplicado, contradicción entre texto y campo u otra duda; 4) fotos o duración bajo el mínimo. Se marcan en ese orden y, dentro de una misma gravedad, por número de informe. Los que no caben quedan en `espera` con su motivo. Ninguno pasa.
5. El equipo de calidad revisa como máximo 30 informes marcados por lote. Los informes de gravedad 1 y 2 siempre entran. Si ellos solos superan 30, no se pasan: se pide al jefe de calidad ampliar el cupo. Un informe marcado sin defecto real cuenta como falso positivo y se descuenta al desempeño del agente auditor.
6. Si el texto del informe y un campo se contradicen, se marca. Por ejemplo, el texto dice que se cambiaron filtros y el campo dice 0. Hasta que el técnico lo corrija, manda el campo.
7. Un informe de visita de seguridad (urgencia «seguridad») se cierra el mismo día de la auditoría para que se active el seguimiento, sin excepciones, salvo que no tenga firma del cliente: ahí manda la regla 1. No se cierra, se marca primero y se avisa el mismo día al jefe de calidad para que active el seguimiento.
8. Los informes de un técnico en período de prueba (60 días desde su ingreso) se marcan igual, pero se devuelven a su supervisor y no cuentan en el cupo de la regla 5.
9. Si hay dos informes del mismo técnico, del mismo equipo y de la misma fecha, se marca el segundo y se conserva el primero.
10. Cada informe marcado debe llevar escrito el número de la regla que se aplicó.
