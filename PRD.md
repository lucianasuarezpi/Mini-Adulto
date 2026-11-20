# PRD — Mini Adulto

> Documento de requerimientos de producto. Fuente única de verdad para construir la app.
> Pensado para pasárselo a Claude Code y para sustentar en el curso.
> Versión 3.0 — 2026-11-12 (incluye las decisiones del prototipo round 1, §20).
> Curso: Diseño en Ingeniería Industrial, Uniandes, 2026-20, Grupo 1. Fase del doble diamante: **Desarrollar**.

---

## 0. Cómo leer este documento

- Lo **no negociable** son la definición de producto (§2), los tres principios de diseño (§4) y los 11 requerimientos del Taller 7 (§14). Toda decisión se evalúa contra ellos.
- **Norte de construcción:** esto se construye como **demo navegable / prototipo de alta fidelidad**, no como app de producción (§5). Lo caro o riesgoso (conexión bancaria, foro, sincronización de calendario, IA del menú) **se simula** con datos sembrados. No se corta una función por ser cara de construir; se corta solo si confunde o no le sirve al usuario.
- La **frontera** (§2.2) decide qué entra y qué no. Si algo no es parte del "segundo turno" de sostener la vida diaria, no va.

---

## 1. Objetivo

### 1.1 Problema (HMW vigente)
¿Cómo podríamos **redistribuir la carga cotidiana** que los estudiantes foráneos que se independizan por primera vez asumen solos al quedar lejos del soporte de su hogar, para que tengan tiempo y energía para sus prioridades y su bienestar, sin aprenderla por prueba y error ni vivirla como una falla personal?

### 1.2 Insight base
El bienestar del foráneo no cae por la dificultad de las materias, sino por el **agotamiento de sostener solo la vida diaria** (la "carga invisible" o "segundo turno"). Como nadie se lo enseñó, lo vive como falla personal ("no me organizo") y no como la jornada extra que es.

### 1.3 Causa raíz
Quedar lejos del soporte del hogar. Por eso la palabra clave del HMW es **redistribuir**: la app no ayuda a *aguantar* la carga, se la *quita* o la *reparte*.

---

## 2. Definición de producto (el corazón)

Esta sección es la que evita que la app sea "una suma de todo". Un hub es coherente cuando tiene **un trabajo, una frontera y una columna**.

### 2.1 El trabajo, en una frase
**Mini Adulto carga el segundo turno del foráneo:** todo lo de sostener la vida diaria solo —comer, la plata, el oficio, lo que se daña— en un solo lugar, para que no lo aprenda ni lo cargue solo.

Un solo trabajo: cargar la carga invisible. Al presentarlo, se empieza por el trabajo, no por la lista de funciones.

### 2.2 La frontera (qué entra y qué NO)
Regla de admisión: *¿esto es parte del segundo turno de sostener tu vida diaria?* Si sí, entra; si no, fuera.

- **Entra:** comida, plata, oficio, lo que se daña, las vueltas (EPS, arriendo, servicios), la red que responde (técnicos, pares, institución).
- **NO entra:** planeador académico / notas / tareas de la U (eso es rendimiento, no vida diaria); red social general; ser domiciliario o marketplace propio; coaching de salud mental (ahí la app es solo **puente**, no terapeuta); fitness o gym.

### 2.3 La columna (para que no sea plano)
La columna vertebral es el **bucle diario**: el usuario abre la app y ve *lo de hoy, ya resuelto* (el mensaje nocturno + el día armado). Todo lo demás **alimenta ese bucle o lo rescata cuando se rompe**:

- **Comida** le pone el menú del día.
- **Plata** le pone la línea de cuánto le queda.
- **Mi semana / Horario** le pone los tiempos.
- **Resolver, Directorio, Comunidad, Red** están para cuando algo se sale del plan.

### 2.4 Las dos direcciones de "redistribuir"
- **Hacia la app:** el bucle diario automatiza y decide para que el usuario no tenga que hacerlo (referentes: débito automático, caddie de golf).
- **Hacia otros:** Resolver + Directorio + Comunidad + Red reparten la carga a técnicos, pares ("familias sustitutas") e institución (FOPRE, Consejería).

---

## 3. Usuario

### 3.1 Usuario de diseño
**Estudiante foráneo:** de otra ciudad de Colombia, con familia lejos, que se independiza por primera vez para estudiar en Bogotá. La app sirve a cualquiera que se independiza por primera vez, pero el usuario de diseño es el foráneo.

### 3.2 Persona — Mariano Casas
19 años, Derecho en Uniandes, de Pereira, vive solo en Bogotá. Le desmotiva llegar a casa con tareas pendientes y sentir que el día no le alcanza. Quiere recuperar tiempo y energía, comer bien sin gastar mucho y sentir su vida bajo control. Habla con su familia a diario; cada cosa que resuelve solo le confirma que está aprendiendo a valerse. Necesita: comida rápida/barata/sana; acomodar mercado y oficio entre clases y trabajo; saber cuánto puede gastar por semana.

### 3.3 Investigación propia (resumen)
Encuesta N=61 (51 foráneos) + 20 entrevistas + mapa de contexto (7 dimensiones) + mapa de stakeholders (3 anillos).
- ~59 % vive sin familiares · 57 % estrés alto (≥7/10) · 68,9 % afectado por estar lejos de su red.
- Recursos: amigos 88,5 %, familia 75,4 %, actividad física 54,1 %, ayuda psicológica 16,4 %.
- 85 % conoce el apoyo psicológico de la U; 80 % nunca lo ha usado. 100 % tiene contacto diario con su familia.

### 3.4 Hallazgos que la app debe tomar en serio
1. **Alimentación = carga #1, casi universal.** Comen menos/peor o se saltan comidas; cansados piden domicilio y eso pega en la plata.
2. **Plata = estresor transversal.** Presupuesto fijo + gastos hormiga; algunos trabajan y baja el rendimiento. "La plata es una ilusión: todo cuesta."
3. **Tareas pequeñas pesan** (loza, ropa, cuarto).
4. **Todo se aprende por prueba y error.**
5. **Momentos críticos de estar solo:** enfermarse sin a quién acudir; miedo de que pase algo y la familia no se entere.
6. **El apoyo institucional existe pero no se usa.** Barrera #1: falta de info operativa ("sé que existe, pero no sé cómo se llama ni cómo se llega"). Confusión de marca. Pesan la pena, la autoexigencia y la desconfianza.
7. **Lo que los sostiene es el apoyo social**, no el institucional. → sustenta la función **Comunidad**.

---

## 4. Principios de diseño (no negociables)

1. **Ligereza** — quitar peso, no añadirlo. La app resuelve *por* el usuario. **Regla dura: si una función pide más trabajo del que quita, está mal.** Onboarding y uso diario con fricción casi cero.
2. **Cercanía** — fácil de encontrar, entender y confiar. Hecha para él, con su lenguaje (español de Colombia, tono de alguien que ya vivió esto).
3. **Respeto** — sin que se sienta juzgado, expuesto ni presionado. **Nunca culpa. Nada de rachas, puntajes ni vergüenza.** Si no hizo algo, la app lo reacomoda sin regañar.

**Referentes:** IKEA (un paso a la vez, qué NO hacer, qué necesitas antes de empezar) para Resolver y Aprender; débito automático (se decide una vez y corre solo) para la organización y los pagos; caddie de golf (carga la logística, el usuario decide) para todo.

**Estilo visual:** editorial y serio. Sin emojis. Sin tipografías juguetonas. Poco texto en pantalla.

> **Pendiente (§19):** la **personalidad y dirección de UI** (incluido el porqué de pedir el nombre) la define la diseñadora; este PRD fija la funcionalidad y deja el tono visual para esa definición.

---

## 5. Alcance: demo navegable, no producción

**Decisión de alcance.** El objetivo no es una app de producción con bases de datos de todos los usuarios, login y seguridad completa. Es una **web app para mostrar** (demo de alta fidelidad) que permita **testear deseabilidad y comprensión** con foráneos. Por tanto:

- Las integraciones caras o riesgosas **se simulan** con datos sembrados y creíbles: conexión bancaria/billeteras, sincronización de calendario, IA del menú, foro.
- No se construyen backend multiusuario, autenticación real ni moderación en esta etapa.
- Cada función deja **documentada la ruta real** (cómo se haría de verdad) aunque en la demo esté simulada, para que la decisión técnica quede clara.

**Fases**
- **Fase 0 — Prototipo en papel** (entrega inmediata del curso): pantallas + flujo imprimibles para testear el concepto. Archivo `prototipo.html`. *Su rediseño visual espera la dirección de UI (§19).*
- **Fase 1 — Demo navegable:** el bucle diario + Comida (bundles) + Plata (conexión simulada + forecast) + Resolver/Directorio + Red en Bogotá, con datos sembrados.
- **Fase 2 — Capas de la demo:** Aprender, Preguntar (IA real con modelo barato), Comunidad (sembrada), Horario conectable.
- **Fase 3 (hipotética, fuera del curso):** producto real — backend, integraciones reales, verificación del directorio, kiosco.

---

## 6. Mapa de funciones

| Función | Qué hace | En la demo |
|---|---|---|
| **Inicio** | El bucle diario: "lo de hoy, ya resuelto" + plata que queda + accesos. | Real (datos sembrados). |
| **Comida** | Bundles de mercado + menú + personalización en dos niveles. | Bundles y menús precalculados. |
| **Mi semana** | Comida/mercado/oficio encajados en el horario; pagos. | Horario conectable (simulado) o manual. |
| **Plata** | Conexión a cuentas/billeteras + forecast por sobres. | Cuenta conectada simulada. |
| **Resolver** | Qué hacer / a quién llamar / quién arregla (urgente). | Fichas + directorio curado. |
| **Directorio** | Técnicos, lavanderías, tiendas verificadas cerca. | Pocos, cargados a mano. |
| **Aprender** | Tutoriales cortos estilo IKEA (no urgente). | Pocos tutoriales de ejemplo. |
| **Preguntar** | Chat IA + opción de preguntar a la comunidad. | IA con modelo barato; o respuestas sembradas. |
| **Comunidad** | Foro asíncrono entre foráneos. | Hilos sembrados. |
| **Red en Bogotá** | Puente a FOPRE, Consejería y líneas de crisis. | Fichas reales verificadas. |

---

## 7. Funciones en detalle

### 7.1 Inicio (la columna)
Abre con la tarjeta **"Hoy/Mañana"** (resumen del mensaje nocturno), el indicador de **plata que queda esta semana**, los accesos a las funciones y el acceso a Red en Bogotá. Nunca pide "llenar" nada. Es la primera pantalla después del onboarding y sale ya personalizada con el nombre, la ciudad y "qué se te complica más".

### 7.2 Comida (lo más fuerte)
- **Dos niveles de personalización:** con solo el onboarding, da **ideas generales**; si el usuario entra a Comida y pone sus preferencias, se **personaliza**.
- **Bundles de mercado (centro de la función):** el usuario compra *una* lista de ingredientes versátiles y de ahí salen **varios platos combinables** para la semana. Pega en las tres cosas: quita carga (una compra, come toda la semana), cuida la plata (menos desperdicio y domicilio) y resuelve la alimentación (req 8).
- **Variables de preferencia (viven en la sección Comida, no en el onboarding):** qué no come (alergias/disgustos), dieta (veg, etc.), cuánto cocina / cuánto tiempo tiene, qué tiene para cocinar (estufa, microondas), cuántas comidas al día resuelve.
- **Demo:** 2–3 bundles precalculados (p. ej. "Económico", "Sin cocinar mucho") con sus menús y listas. Se ve inteligente sin IA real.

### 7.3 Mi semana (horario + pagos)
- **Horario opcional y conectable.** No va en el onboarding (fricción). Se ofrece desde Mi semana: *"Conecta tu horario y te armo la semana en los huecos reales."*
  - **Opción A — conectar calendario:** Google Calendar o los calendarios disponibles; se logean solos los compromisos y las cosas que tenga la persona.
  - **Opción B — manual:** si la persona prefiere, mete el horario a mano.
  - Sin horario, la app igual sirve (ideas de comida, Resolver, Red); con horario, se vuelve organizadora. Ruta real: importar Google Calendar o un `.ics` (Bloque Neón no tiene API pública, pero exporta). En la demo, se simula la conexión con un horario de ejemplo.
- **Recordatorios de pago:** **opcionales pero recomendados**. Se meten **una vez y se repiten solos cada mes** (arriendo, servicios): no es logeo constante. La app los sugiere/recomienda activar.
- **Reacomodo sin culpa:** si el usuario no hizo algo, la app lo reubica sola, sin regañar ni marcar fallos.

### 7.4 Plata (conexión + forecast + sobres)
**Mecanismo decidido: conexión, no logeo manual.** El usuario conecta cuentas/billeteras y la app lee los movimientos sola. Esto resuelve el trilema (preciso + sin fricción exige conexión; sin conexión solo da estimados borrosos; logeo manual se abandona).

- **De dónde salen los datos:** un agregador de *open finance* (p. ej. **Belvo**, Finerio) devuelve **saldos reales** de las cuentas y **movimientos ya categorizados** (reconoce que un cargo es domicilio, mercado, etc.).
  - **Sí conectan (según cobertura del agregador):** bancos, **Nequi**, **Daviplata**.
  - **No es posible:** **Apple Wallet / Apple Pay** no expone los movimientos a terceros (datos privados de Apple y del banco). Un iPhone igual queda cubierto conectando el banco o Nequi.
- **Cómo devuelve "cuánto me queda" (forecast):** `disponible = saldo real − pagos fijos pendientes antes del próximo ingreso − lo ya comprometido`. No es un presupuesto imaginario; es aritmética sobre datos reales. El usuario ve cuánto puede gastar, no una lista de gastos.
- **Rubros / sobres:** **el usuario configura sus propios rubros; si no, la app se los recomienda** (reparto por defecto tipo 50/30/20 adaptado al estudiante). 3–5 sobres máximo (p. ej. Mercado, Transporte, Gustos, Fijos, Ahorro) para que se lea de un vistazo. Los movimientos categorizados se descuentan solos de cada sobre: *"Te quedan $34.000 en gustos esta semana"*.
- **Lo que el usuario provee, una sola vez:** conectar cuentas, confirmar/ajustar el reparto de sobres (ya viene sugerido), los pagos fijos. De ahí en adelante corre con el stream de movimientos.
- **Demo:** cuenta conectada **simulada** con saldo + movimientos categorizados + sobres, para que el "cuánto me queda" muestre matemática real y creíble.

### 7.5 Resolver + Directorio
- **Resolver = urgente, está pasando ahora.** Categorías en lenguaje del usuario (se dañó algo / me siento mal / un recibo que no entiendo / una vuelta). Detalle estilo **IKEA**: qué hacer ya, qué **NO** hacer, a quién llamar. Termina en el **directorio** o en una **línea**.
- **Directorio verificado:** técnicos, lavanderías, tiendas cerca, con sello "Verificado" y acción de llamar. En la demo, **pocos, curados a mano**. Verificación real = Fase 3.

### 7.6 Aprender
- **Aprender = tranquilo, quiero saber hacerlo yo** (sin emergencia). Tutoriales cortos estilo IKEA: qué necesitas antes de empezar, pasos con imagen, qué **NO** hacer.
- **Relación con Resolver:** se complementan y se enlazan. Un Resolver puede mandar a un Aprender ("para la próxima, aprende a destaparlo"); un Aprender puede mandar a Resolver si algo se complica. **Regla de separación: ¿está pasando ahora y necesitas que alguien responda? → Resolver. ¿Quieres aprenderlo para hacerlo tú? → Aprender.**

### 7.7 Preguntar
- Chat con IA: se le pregunta como se le preguntaría a la mamá ("¿cuánto dura el pollo en la nevera?", "¿qué hago si se fue la luz?").
- **Gancho con Comunidad:** en cada pregunta, opción de **"pregúntale a la IA o pregúntale a la comunidad"**.
- **Caso salud (núcleo de seguridad):** la IA **no diagnostica**. Ante malestar/intoxicación/crisis, orienta con lo básico y **deriva a información real**: Línea 106 (24/7, WhatsApp 300 754 8933), Línea 123 (emergencias), Centro de Consejería, EPS/urgencias. Esto va aunque el chat sea capa; puede vivir como ficha fija sin IA.
- **Técnico:** modelo barato (DeepSeek u otro de bajo costo) llamado desde una ruta de servidor para no exponer la API key, con system prompt de guardarraíles (tono colombiano, no diagnosticar, no pedir datos personales).

### 7.8 Comunidad (foro)
- **Foro asíncrono** (posts e hilos), no chat en vivo: más barato, más seguro y más útil para "preguntarle a los que ya pasaron por esto". Sustentado por el hallazgo #7 (lo que sostiene es el apoyo social).
- **Demo:** hilos **sembrados** que se ven vivos ("¿Dónde mercar barato cerca de la 45?", "Me enfermé y no sabía a qué EPS ir"). Sin backend ni moderación.
- **Nota para producto real:** un foro en una app de tema sensible necesita **moderación** (riesgo); se documenta, pero en demo no aplica.

### 7.9 Red en Bogotá (puente institucional)
Fichas de **FOPRE** y **Consejería / No estás sol@**: qué ofrece, **nombre real**, requisitos básicos, cómo se llega (kiosco en campus). **Líneas 106 y 123 siempre visibles.** No duplica los servicios: los conecta (req 11). Datos reales, con fecha de verificación.

---

## 8. Onboarding (setup casi cero)

Cuatro o cinco toques; solo lo mínimo para que el **Inicio salga personalizado**. El detalle se difiere a cada sección.

1. **Nombre** — para el saludo y para personalizar el tono (se conecta con la personalidad/UI, §19).
2. **¿De dónde llegaste?** (ciudad) — ancla emocional de foráneo.
3. **¿Solo estudias o estudias y trabajas?** — calibra qué tan apretada es la semana.
4. **¿Qué es lo que más se te complica de vivir solo?** (comer bien / la plata / el oficio / sentirme solo) — personaliza el Inicio y viene directo del insight de la carga invisible.
5. **¿En qué zona vives?** — para el directorio ("cerca de ti").

Lo que **no** va en el onboarding: presupuesto (va en Plata, con la conexión), qué no come (va en Comida), horario (opcional, en Mi semana).

---

## 9. Historias de usuario

Prioridad: P0 (demo Fase 1), P1 (demo Fase 2), P2 (producto real).

- (P0) Como Mariano, quiero contar en pocas preguntas de dónde vengo, si trabajo, qué se me complica y dónde vivo, para que el Inicio ya salga hecho para mí sin configurar nada más.
- (P0) …ver al abrir la app lo de hoy ya resuelto y cuánta plata me queda, para no cargar la planeación en la cabeza.
- (P0) …recibir ideas de menú y un **bundle de mercado** del que salgan varios platos combinables, para comprar una vez y comer toda la semana sin pensar.
- (P1) …entrar a Comida y poner mis gustos para que el menú sea más mío.
- (P0) …**conectar mi cuenta/Nequi** y que la app me diga cuánto puedo gastar por sobre, sin que yo registre cada gasto.
- (P1) …**configurar mis rubros** o que la app me los recomiende si no quiero pensarlo.
- (P1) …**conectar mi calendario** (o meter el horario a mano) para que la app me arme la semana en mis huecos reales.
- (P1) …que me recuerde los pagos que se repiten cada mes, metiéndolos una sola vez.
- (P1) …que si un día no hice algo, la app lo reacomode sin regañarme.
- (P0) …cuando se me dañe algo o me enferme, saber en un paso qué hacer, a quién llamar y quién lo arregla.
- (P1) …encontrar técnicos/lavanderías **verificados** cerca.
- (P1) …preguntarle a la app como a mi mamá, o preguntarle a la **comunidad** de foráneos.
- (P0, seguridad) …que si digo que me siento mal, la app no me diagnostique pero me pase el número real al que llamar.
- (P0) …saber qué ofrece FOPRE y Consejería, cómo se llaman de verdad y cómo llego.

---

## 10. Pantallas

Prefijo = grupo. (El set final y su look dependen de la dirección de UI, §19.)

- **A. Entrada:** A1 Portada · A2 Onboarding (nombre, ciudad, estudia/trabaja, qué se complica, zona).
- **B. Inicio:** B1 Inicio (bucle diario) · B2 Mensaje nocturno.
- **C. Comida:** C1 Comida (ideas/bundles) · C2 Bundle de mercado (platos combinables) · C3 Menú de la semana · C4 Preferencias.
- **D. Mi semana:** D1 Mi semana · D2 Conectar horario / manual · D3 Pagos (recordatorios).
- **E. Plata:** E1 Plata (forecast + sobres) · E2 Conectar cuenta · E3 Configurar/recomendar rubros.
- **F. Resolver:** F1 Resolver (categorías) · F2 Detalle (un paso, IKEA) · F3 Directorio verificado.
- **G. Aprender:** G1 Lista de tutoriales · G2 Tutorial detalle (IKEA).
- **H. Preguntar:** H1 Preguntar (IA / comunidad) · H2 Caso salud (derivación).
- **I. Comunidad:** I1 Foro (hilos) · I2 Hilo.
- **J. Red en Bogotá:** J1 Red (FOPRE, Consejería, líneas).

---

## 11. Flujos principales

1. **Primer uso:** A1 → A2 (onboarding) → **B1 Inicio** ya poblado. No configura nada más.
2. **Bucle diario (columna):** B1 muestra lo de hoy; cada noche llega **B2 Mensaje nocturno**.
3. **Comida:** B1 → C1 → C2 Bundle → C3 Menú → (opcional) C4 Preferencias para personalizar.
4. **Plata:** B1 → E1 → E2 Conectar (simulado) → E3 Rubros (configura o recomienda) → forecast en E1.
5. **Organización:** B1 → D1 → D2 Conectar horario/manual → semana armada; D3 Pagos.
6. **Algo se dañó / me enfermé:** B1 → F1 → F2 detalle → F3 directorio o, en salud, H2 / J1 (líneas).
7. **No sé algo:** B1 → H1 → IA **o** comunidad (I1); si es salud/riesgo → H2.
8. **Puente:** B1 → J1 → ficha FOPRE/Consejería.

---

## 12. Modelo de datos

Minimalista por diseño. Entidades principales:

- **Usuario:** `id`, `nombre`, `ciudad_origen`, `trabaja` (bool), `zona`, `reto_principal` (comida|plata|oficio|soledad), `restricciones_comida`, `preferencias_comida`, `eps` (opcional).
- **ConexionFinanciera** (simulada en demo): `usuario_id`, `proveedor` (banco|nequi|daviplata), `saldo`, `movimientos[]` (`{monto, fecha, rubro_auto, descripcion}`).
- **Sobre:** `id`, `usuario_id`, `nombre`, `monto_asignado`, `gastado` (derivado de movimientos). Configurable por el usuario o recomendado por la app.
- **Pago:** `id`, `usuario_id`, `concepto`, `monto`, `dia_del_mes`, `recordar` (bool). Se repite mensual.
- **Horario** (conectado o manual): `usuario_id`, `fuente` (gcal|ics|manual), `bloques[]` (`{dia, inicio, fin, tipo}`).
- **Bundle:** `id`, `nombre`, `ingredientes[]`, `costo_estimado`, `platos[]` (combinaciones), `etiquetas`.
- **PlanSemana:** `id`, `usuario_id`, `bloques[]` (comida/mercado/oficio encajados), `estado` (sin culpa, se reacomoda).
- **DirectorioLugar:** `id`, `tipo`, `nombre`, `telefono`, `ubicacion`, `verificado`, `fecha_verificacion`.
- **Tutorial:** `id`, `titulo`, `pasos[]` (`{texto, imagen, es_advertencia}`), `requisitos[]`.
- **HiloComunidad** (sembrado en demo): `id`, `titulo`, `cuerpo`, `respuestas[]`, `zona`/`tema`.
- **ServicioInstitucional:** `id`, `nombre_real`, `alias`, `que_ofrece`, `requisitos`, `como_llegar`, `contacto`.
- **ConsultaIA:** efímera; no persistir contenido sensible.

---

## 13. Privacidad y datos personales

- **Minimización:** pedir solo lo necesario; sin login pesado en la demo.
- **Demo sin datos reales sensibles:** como las conexiones (banco, calendario) están **simuladas**, no se recoge información financiera ni de terceros real en esta etapa.
- **Ruta real (documentada para Fase 3):** la conexión de open finance implica consentimiento explícito, cifrado y cumplimiento de **Habeas Data (Ley 1581 de 2012)**; los datos financieros y de salud son sensibles y exigen el mayor cuidado. Preferir que el perfil y los cálculos vivan del lado del usuario cuando sea posible.
- **IA (Preguntar):** no enviar nombre ni datos identificables al modelo; no guardar historial sensible; aviso de que orienta y no reemplaza a un profesional.
- **Salud / salud mental (riesgo del curso):** la IA no diagnostica; deriva a líneas reales y actualizadas (§7.7).
- **Comunidad:** en producto real, moderación y reglas de convivencia.
- **Fuentes:** FOPRE/Consejería/directorio con fecha de verificación; no publicar requisitos de FOPRE sin confirmar la convocatoria vigente.

---

## 14. Requerimientos (Taller 7) y cómo se cumplen

| # | Requerimiento | Cómo lo cumple |
|---|---|---|
| 1 | No agregar tareas ni tiempo | Setup de 4–5 preguntas; bucle diario y mensaje nocturno; plata por conexión (no logeo); pagos una sola vez. |
| 2 | Costo compatible / gratis | Gratis para el estudiante; IA con modelo barato. |
| 3 | Sin experiencia previa | Tutoriales IKEA, Resolver en un paso, menú/sobres propuestos. |
| 4 | Repartir la carga entre más actores | Directorio + Comunidad + puente FOPRE/Consejería. |
| 5 | Sirve al que solo estudia y al que estudia+trabaja | Onboarding pregunta si trabaja; semana en huecos reales. |
| 6 | No exponer ni hacer sentir que falla | Sin culpa, rachas ni puntajes; reacomodo silencioso. |
| 7 | Fácil de encontrar, entender, confiar | Lenguaje cercano, directorio verificado, diseño editorial. |
| 8 | Atender la alimentación | **Centro del producto:** bundles + menú + lista. |
| 9 | Proteger datos personales | §13: minimización; demo simulada; ruta real con Habeas Data. |
| 10 | Efecto medible (tiempo/dinero) | §16 métricas. |
| 11 | Articularse con FOPRE y Consejería | Red en Bogotá (J1): nombre real, qué ofrece, cómo llegar. |

---

## 15. Stack / enfoque técnico

**Norte: demo navegable primero.** Construir una web app de alta fidelidad con datos sembrados; simular integraciones.

- **Front:** Next.js (React) + TypeScript + Tailwind. Mobile-first. Tipografía editorial (la paleta/tono final espera §19).
- **Estado/datos (demo):** local (localStorage/IndexedDB) y JSON sembrado para bundles, directorio, hilos, cuenta financiera simulada. Sin backend multiusuario.
- **IA (Preguntar):** modelo barato (DeepSeek u otro) vía ruta de servidor; guardarraíles de salud.
- **Integraciones — rutas reales documentadas (simuladas en demo):**
  - Plata: agregador de open finance (Belvo/Finerio) para saldos + movimientos categorizados; Nequi/Daviplata según cobertura. Apple Wallet no es fuente de datos.
  - Horario: Google Calendar API o import `.ics`.
  - Comunidad: backend + moderación (fuera de alcance de la demo).
- **Deploy:** Vercel. **PWA** (manifest + service worker) para "instalar" y el mensaje nocturno.

---

## 16. Criterios de aceptación y métricas

### 16.1 Criterios de aceptación (demo Fase 1)
- Del onboarding al **Inicio poblado** en **≤ 5 toques y < 2 min**, sin configurar nada más.
- Comida entrega un **bundle con sus platos combinables** y la lista con costo en **≤ 2 toques**.
- Plata muestra "cuánto puedes gastar" **por sobre**, calculado sobre la cuenta (simulada), sin registrar gastos a mano.
- El usuario puede **configurar rubros** o aceptar los **recomendados**.
- Mensaje nocturno de ≤ 4 líneas con lo de mañana + plata restante.
- Resolver llega a un detalle "un paso" en **≤ 2 toques**.
- En toda la app: ningún mensaje de culpa, racha, puntaje ni comparación.
- Caso salud: muestra derivación real (106/123/Consejería/EPS) y **no** diagnostica.

### 16.2 Métricas de efecto (req 10)
- **Lo que la demo puede testear ahora (deseabilidad/comprensión):** ¿entendió el "trabajo" en una frase? ¿qué función le quita más peso? ¿la volvería a abrir? carga percibida antes/después (escala 1–7). Comprensión del puente (¿supo cómo llegar a FOPRE/Consejería tras ver J1?).
- **Lo que mediría un piloto funcional (fuera del curso):** minutos/semana en planear comida/mercado; gasto semanal en domicilios y hormiga; nº de comidas saltadas; % del presupuesto que llega a fin de mes.

---

## 17. Riesgos y mitigaciones

| Riesgo | Mitigación |
|---|---|
| **"Suma de todo"** | Definición de producto (§2): un trabajo, una frontera, una columna. Presentar por el trabajo, no por las funciones. |
| **Plata vaga o con fricción** | Conexión como fuente de verdad (saldos + movimientos categorizados) + forecast por sobres; nada de logeo manual. |
| **Salud mental (usuario en crisis)** | IA no diagnostica; deriva a líneas reales (§7.7, §13). |
| **Directorio (datos reales + mantenimiento)** | Demo con pocos, curados a mano, con fecha de verificación. |
| **Confusión de marca institucional** | J1 usa el nombre real y aclara alias. |
| **Foro (moderación/seguridad)** | En demo, sembrado; moderación documentada para producto real. |
| **Depender de integraciones** | En demo todo simulado; rutas reales documentadas para no vender humo. |

---

## 18. Fuentes verificadas (datos del mundo real que la app cita)

- **FOPRE** — cubre alimentación, transporte, fotocopias y materiales por semestre; se pide/renueva cada semestre en Apoyo Financiero. Requisitos y convocatoria vigente: verificar en apoyofinanciero.uniandes.edu.co/fopre.
- **Centro de Consejería / "No estás sol@"** — app institucional de bienestar operada por Uniandes, acceso con correo institucional; recursos abiertos sin login. Mini Adulto es el **puente**, no la reemplaza.
- **Línea 106** (Secretaría de Salud de Bogotá) — escucha/orientación psicológica, gratuita, 24/7. Marcar 106 o WhatsApp **300 754 8933**.
- **Línea 123** — emergencias, incluida crisis de salud mental con riesgo inmediato.

*(Verificar vigencia de números y requisitos antes de cada entrega; marcar fecha de verificación en el directorio.)*

---

## 19. Pendientes / decisiones abiertas

- **Personalidad y dirección de UI** (incluido el porqué de pedir el nombre): la define la diseñadora. Afecta el rediseño del prototipo de pantallas.
- Semilla de **bundles** de mercado: cuántos, de qué tipo, con qué costos de referencia en Bogotá.
- Modelo de IA definitivo y costo por consulta con uso real.
- Verificar en campus los datos operativos de FOPRE y Consejería para J1.
- Set final de pantallas y su jerarquía visual, una vez fijada la UI.

---

## 20. Prototipo round 1 — decisiones de diseño (2026-11-12)

Cierre del primer round de diseño del prototipo navegable. Todo esto queda fijado; se itera después.

### 20.1 Mascota: Tinto
- **Tinto** es una **capibara pixel**. Se eligió sobre búho/otros porque encarna el producto: calma (anti-estrés), comunal (apoyo social, hallazgo #7), compañera de igual a igual (no autoridad, evita el aire "Duolingo"), y es de la región (capibara/chigüiro). A Gen Z le gusta sin ser infantil.
- **Nombre:** la app sigue siendo "Mini Adulto"; la mascota es **Tinto** (el ritual diario, cálido, humilde; y su marrón = color de tinto). El producto se presenta por el trabajo (§2), no por la mascota.
- **Brote en la cabeza:** identidad fija (crecer = aprender a sostener tu vida). **No es un medidor** (nada de que se marchite = culpa).
- **Sprite:** `assets/tinto-idle.png` (pose idle sentada, fondo transparente y recortada con Pillow).
- **Globo de Tinto:** estilo pixel (fuente Pixelify Sans), aparece al tocarlo.

### 20.2 Identidad visual
- **UI editorial y seria, Tinto el único con carácter.** Ese contraste la hace adulta y cercana a la vez. Nada infantil en la UI; el pixel vive solo en Tinto.
- **Tipografía:** Source Serif 4 (titulares) + Inter (UI). Pixelify Sans **solo** para el globo de Tinto.
- **Paleta** tomada del mundo de Tinto: marrón cálido (acento) + verde del brote, sobre neutros. **Claro y oscuro** (el oscuro se ve mejor; es el usado para impresión).
- **Respeto:** sin rachas, sin puntajes, sin regaños. Tinto acompaña, nunca juzga.

### 20.3 Navegación
- **Celular tamaño real** (proporción 390×844).
- **Menú flotante abajo, solo iconos:** Inicio · Chat · Red.
- **Inicio = feed carrusel tipo widget:** una tarjeta grande a la vez, deslizando de lado con snap (de a una, no scroll continuo) y puntos de posición. Orden: **Mi semana → Plata → Comida → Resolver → Aprender.**
- **Tocar una tarjeta** abre su pantalla. **Back** = botón cuadrado-redondeado con chevron; vuelve a su pantalla padre.
- **Engranaje de ajustes** (arriba derecha) en Mi semana, Plata y Comida: las pantallas se ven "ya conectadas/logueadas" y las conexiones/preferencias viven en el engranaje. (Resolver/Aprender aún sin engranaje; pendiente opcional.)

### 20.4 Inventario de pantallas (prototipo)
Inicio (día) · Inicio (noche) · Comida · Comida/Bundles · Plata · Mi semana · Resolver · Resolver/Se dañó algo · Aprender · Chat/Tinto · Chat/Foro · Red en Bogotá · Ajustes (ejemplo, un engranaje abierto).

- **Inicio noche:** toggle Día/Noche. En noche cambia el saludo ("Buenas noches"), el mensaje pasa al **nocturno** ("Mañana… Descansa") y Tinto **duerme** (se inclina, respira y le salen Zzz pixel). Es el mockup del mensaje nocturno.
- **Chat:** toggle **Tinto / Foro**. Tinto = chat IA (Tinto parado en la barra de escribir); mensajes arriba, input abajo. Foro = hilos sembrados de otros foráneos.
- **Comida → Bundles:** ideas de mercado ("Económico", "Sin cocinar mucho") con sus platos y la **lista de mercado** con precios y total. Menú mostrado como **mini-calendario** (día arriba, comida abajo, en grid).
- **Resolver → Se dañó algo:** pasos estilo IKEA (qué hacer + qué NO), **directorio verificado** (plomeros, "Llamar") y un **tutorial** ("mientras llega").
- **Tags de las tarjetas** = acciones o **lo que falta** (p. ej. "Conectar horario", "Agregar banco"), no descripciones obvias.

### 20.5 Motions de Tinto (uno por pantalla)
Técnica de Noodle (proyecto previo de la estudiante), **sin dibujar sprites nuevos**: mismo sprite idle + **prop pixel hecho con CSS** + un bob; se reproduce al entrar a la pantalla y al tocar a Tinto.
- Plata = billetes · Comida = manzana · Mi semana = calendario · Resolver = cruz de primeros auxilios · Aprender = librito.
- Pose de noche = inclinación + respiración + Zzz (tampoco necesita sprite nuevo). Opción futura: derivar poses con Pillow (rotar/recolorear), como el "sleep" de Noodle.

### 20.6 Archivos y build
- **`mini-adulto.html`** — prototipo interactivo autónomo (Tinto embebido como data URI). Se abre con doble clic y se **reenvía como un solo archivo**. No es artifact publicado (decisión de la estudiante).
- **`pantallas-impresion.html`** — pliego imprimible: todas las pantallas como mockups de celular en **oscuro sobre hoja blanca**, A4, **3 celulares por hoja**. *Al imprimir, activar "Gráficos de fondo" en el diálogo para que salgan los fondos oscuros.*
- **`assets/tinto-idle.png`** — sprite de Tinto.
- **Flujo de edición:** se edita el cuerpo en el scratchpad (`inicio.html`) y se reconstruye con un script Python que embebe la imagen y envuelve con doctype. (El mismo script arma el pliego de impresión.)

### 20.7 Alcance confirmado
**Demo navegable, no producción.** Lo caro/riesgoso se simula (conexión bancaria, calendario, IA, foro) con datos sembrados; cada función deja documentada su ruta real. No se construyen backend multiusuario, login ni moderación en esta etapa.
