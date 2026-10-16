# FarmacoforIA

Aprende Química Farmacéutica practicando: receptores, metabolismo, QSAR, síntesis, examen y casos. Aplicación web de un solo fichero.

**Usar la app:** https://fborrasumh.github.io/farmacoforia/

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23416307.svg)](https://doi.org/10.5281/zenodo.23416307)

**Idiomas:** español (por defecto), inglés, portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

## Qué hace

Siete módulos, todos accesibles sin clave de IA salvo donde se indica:

- **Receptores.** Clasificar 16 receptores por tipo (canal iónico, acoplado a proteína G, ligado a cinasas, nuclear), localización y escala de tiempo de la respuesta. Corrige el código.
- **Metabolismo.** 22 transformaciones reales (fenacetina → paracetamol, paracetamol → NAPQI, codeína → morfina, prontosil → sulfanilamida, enalapril → enalaprilato…) con sustrato y metabolito dibujados a partir de su SMILES; se decide fase, tipo de reacción y enzima.
- **Tarjetas de repaso** con repetición espaciada (cajas de Leitner), 30 del temario más las que se generen de los apuntes propios.
- **Laboratorio numérico.** Ocho tipos de problema con datos distintos por estudiante a partir de su nombre o código: ecuación de Hansch y π óptimo, constante π y log P, Free-Wilson con la modificación de Fujita-Ban, ecuación de Hammett, antagonismo competitivo y Schild (DR y pA2), reparto octanol/agua, ionización por Henderson-Hasselbalch y rendimiento de una síntesis con reactivo limitante. La solución la calcula el código y, cuando la respuesta es incorrecta, se recalcula con los errores típicos declarados para explicar el fallo.
- **Prácticas de síntesis.** Las cinco de la guía (6-metil-2-tioxo-4-pirimidona, benzocaína, fenitoína, análogo de nifedipina y borneol): esquema de la reacción dibujado, y procedimiento y mecanismo para ordenar paso a paso.
- **Simulacro de examen.** 35 preguntas de teoría tipo test, repartidas por unidades y corregidas por el código con la clave, y preguntas de desarrollo sobre las prácticas. **No pone nota ni aplica penalización**: muestra aciertos, fallos, preguntas en blanco y la explicación de cada una; en el desarrollo, qué conceptos aparecen (sin IA) o un feedback detallado con IA.
- **Casos de diseño.** Seis casos (profármaco para absorción oral, profármaco hidrosoluble inyectable, liberación en el colon, fármaco blando de acción ultracorta, optimización de una serie con QSAR y bloqueo de un punto de metabolismo) con pistas graduadas y un tutor socrático.
- **Mis apuntes** (con IA): preguntar a los apuntes propios o generar tarjetas, siempre con cita literal comprobada contra el material.
- **Progreso**: aciertos recientes por unidad, exportación a Word, CSV y JSON, e importación para continuar en otro ordenador.

## Cómo se usa la IA

Con la propia clave de OpenAI, Google Gemini o Anthropic Claude. La clave se guarda solo en el navegador. No hace falta servidor.

## Privacidad

Todo se procesa y se guarda en el navegador (IndexedDB): progreso, respuestas, apuntes y la clave de IA. Las estructuras se dibujan localmente y los cálculos del laboratorio, la corrección del test y de los ordenamientos y la verificación de las citas los hace el código, sin red.

Solo salen datos hacia el proveedor de IA si se usan las funciones con IA: las respuestas de desarrollo, los mensajes al tutor o los apuntes, con correos, documentos de identidad y teléfonos enmascarados y tras un aviso previo con una muestra de lo que sale. El fichero JSON exportado no contiene la clave de API.

## Límites

- El contenido base (receptores, metabolismo, tarjetas, test, casos) es material de repaso elaborado a partir del temario de la guía docente: puede contener errores u omisiones. Mandan el profesorado, la guía docente y el guion de prácticas.
- Los procedimientos de las cinco síntesis son los generales de cada reacción, **no el guion de prácticas de la asignatura**: cantidades, tiempos y condiciones concretas hay que tomarlos del guion.
- Las estructuras son esquemas generados a partir del SMILES con smiles-drawer; no son imágenes oficiales del temario.
- El simulacro no pone nota ni reproduce la penalización del examen real, y no sustituye la corrección del profesorado. Si la IA cuela una calificación, el código la elimina.
- El feedback de la IA solo se muestra cuando su cita literal aparece de verdad en la respuesta del estudiante; lo que no se puede comprobar se marca como «sin cita verificada».
- El tutor de los casos no recibe la solución y el código filtra sus frases, pero el filtro es una lista de términos: puede dejar pasar una formulación inesperada.
- El progreso es una orientación para decidir qué repasar, no una calificación.

Probado con IA simulada de los tres proveedores (incluida una IA que inventa citas y cuela una nota), en español, inglés y portugués, en escritorio y móvil. No se ha probado con una clave de API real.

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche) y Nathalie Zink Lorre (Universidad Miguel Hernández de Elche).

Sigue el temario, las prácticas y el formato de examen de la guía docente 2026-2027 de Química Farmacéutica I (asignatura 1692, Grado en Farmacia, UMH), cuya responsable es Nathalie Zink Lorre. Diseño basado en VirologIA. Las estructuras se dibujan con [smiles-drawer](https://github.com/reymond-group/smilesDrawer) (licencia MIT), incluida en el fichero.

ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573) · Nathalie Zink Lorre [0000-0003-3081-995X](https://orcid.org/0000-0003-3081-995X)

## Cómo citar

Borrás Rocher, F. y Zink Lorre, N. (2026). *FarmacoforIA* (v1.0.0) [Software]. DOI: [10.5281/zenodo.23416307](https://doi.org/10.5281/zenodo.23416307)

## Licencia

MIT. Véase [LICENSE](LICENSE).
