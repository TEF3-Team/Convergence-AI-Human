# Hipótesis de Vulnerabilidad Cognitiva en LLMs

**Autor:** Oscar Aguilera / Zorro12  
**Año:** 2025  
**Tipo:** Hipótesis técnica independiente  
**Área:** Seguridad de IA, alineamiento, interacción humano-LLM

---

## 1. Formulación breve

La **Vulnerabilidad Cognitiva** es una clase de falla en modelos de lenguaje donde el sistema no es vulnerado por una instrucción maliciosa explícita, sino por una trayectoria conversacional que altera su interpretación del contexto, del rol y del riesgo.

En términos simples:

> **El modelo no falla solo por lo que se le pide.  
> Falla por cómo llega a interpretar la conversación completa.**

---

## 2. Tesis central

Un LLM puede resistir una solicitud peligrosa directa, pero fallar ante una conversación que gradualmente redefine lo que el modelo considera seguro, legítimo o coherente responder.

La vulnerabilidad no vive únicamente en el prompt aislado. Vive en el patrón acumulado.

> **El exploit no está solo en el prompt.  
> Está en el patrón.**

---

## 3. Hipótesis principal

Un modelo de lenguaje puede presentar fallas de alineamiento cuando su sistema de interpretación prioriza la coherencia conversacional, el encuadre narrativo o la continuidad semántica por sobre la evaluación global del riesgo.

Esto puede ocurrir cuando la intención peligrosa no aparece como una orden explícita, sino distribuida en:

- múltiples turnos,
- fragmentos aparentemente inocuos,
- metáforas,
- lenguaje culturalmente ambiguo,
- humor,
- tecnicismos,
- rol ficticio,
- presión semántica,
- o acumulación progresiva de premisas.

---

## 4. Diferencia con un jailbreak tradicional

Un jailbreak tradicional intenta romper la defensa del modelo mediante una instrucción o fórmula explícita.

La Vulnerabilidad Cognitiva opera de otra manera:

- no depende necesariamente de una frase mágica,
- no requiere sintaxis adversarial evidente,
- no necesita pedir directamente contenido restringido,
- no siempre se reconoce en un solo turno,
- puede emerger desde la trayectoria completa de la conversación.

En vez de forzar al modelo, lo desplaza.

> **No rompe la puerta.  
> Cambia el mapa que usa el guardia.**

---

## 5. Mecanismos observados

La hipótesis considera varios mecanismos compatibles entre sí.

### 5.1 Contexto acumulado

El modelo ajusta su respuesta según el historial conversacional. Si el contexto construye una normalidad aparente, el modelo puede interpretar como seguro algo que habría rechazado de forma directa.

### 5.2 Descomposición

Una solicitud riesgosa puede dividirse en piezas pequeñas, cada una aparentemente aceptable. El riesgo aparece solo cuando las piezas se integran.

### 5.3 Camuflaje semántico

La intención puede quedar oculta dentro de jerga, metáforas, humor, errores ortográficos, idioma local, doble sentido o códigos culturales.

### 5.4 Encuadre narrativo

El modelo puede responder distinto si interpreta la situación como ficción, análisis, auditoría, simulación, investigación o juego de rol.

### 5.5 Presión conversacional

El modelo puede ser empujado por continuidad, confianza, autoridad aparente, urgencia o insistencia hacia una respuesta más cooperativa de lo que corresponde.

### 5.6 Trayectoria multi-turn

El riesgo puede no estar presente en un mensaje aislado, sino en la dirección completa que toma la conversación.

---

## 6. Relación con investigaciones públicas

La hipótesis de Vulnerabilidad Cognitiva es compatible con líneas de investigación pública sobre seguridad de IA, incluyendo:

- **Universal jailbreaks:** patrones reutilizables capaces de evadir salvaguardas en múltiples tipos de solicitudes.
- **Many-shot jailbreaking:** uso de muchos ejemplos en contexto para inducir respuestas no deseadas.
- **Ataques multi-turn:** estrategias donde la falla emerge a través de varios turnos conversacionales.
- **Prompt injection indirecto:** instrucciones ocultas en documentos, páginas o herramientas externas.
- **Clasificación de conversación completa:** defensas que evalúan no solo una salida aislada, sino el contexto conversacional completo.

La diferencia de esta hipótesis está en el marco conceptual:

> La Vulnerabilidad Cognitiva describe la falla como un problema de interpretación, no solo como evasión de filtros.

---

## 7. Modelo conceptual

La vulnerabilidad aparece cuando existe una brecha entre:

1. lo que el usuario está construyendo realmente en la conversación,
2. lo que el modelo cree que está ocurriendo,
3. lo que el sistema de seguridad logra clasificar,
4. y lo que la respuesta final termina habilitando.

Cuando esas cuatro capas se desalinean, el modelo puede responder de forma insegura sin haber recibido una instrucción abiertamente maliciosa.

---

## 8. Riesgo principal

El riesgo principal no es que el modelo “quiera” romper reglas.

El riesgo es que el modelo sea demasiado bueno siguiendo contexto, intención implícita, estilo, rol y continuidad, mientras sus defensas no evalúan con la misma profundidad la trayectoria completa de la interacción.

En otras palabras:

> La misma capacidad que hace útil al modelo —entender contexto— puede transformarse en superficie de ataque.

---

## 9. Implicancias para seguridad

Las defensas no deberían evaluar únicamente:

- palabras prohibidas,
- última pregunta del usuario,
- última respuesta del modelo,
- o prompts explícitamente maliciosos.

También deberían evaluar:

- intención acumulada,
- dirección de la conversación,
- cambios de marco,
- fragmentación de objetivos,
- camuflaje semántico,
- patrones de insistencia,
- y relación entre turnos previos y salida final.

---

## 10. Formulación final

La Vulnerabilidad Cognitiva en LLMs puede definirse como:

> Una falla de alineamiento inducida por trayectoria conversacional, donde el modelo interpreta erróneamente el significado acumulado, el rol contextual o el riesgo emergente de una interacción, produciendo respuestas que no habría generado ante una solicitud directa equivalente.

---

## 11. Posición del estudio

Esta hipótesis no afirma prioridad sobre laboratorios de IA ni sobre investigaciones públicas previas.

Su aporte es formular, desde observación independiente, una lectura cognitivo-contextual del problema:

> Los LLMs no solo deben protegerse contra instrucciones peligrosas.  
> Deben protegerse contra conversaciones que lentamente les enseñan a interpretar mal el peligro.

---

## 12. Nota de seguridad

Este documento no contiene instrucciones operacionales ni prompts replicables.

Su propósito es contribuir al análisis responsable de fallas de alineamiento y al desarrollo de mejores defensas para modelos de lenguaje.

Todos los ejemplos sensibles deben mantenerse redactados.
