# AI_USAGE.md — Declaración de uso de IA

## Herramienta utilizada
Claude (Anthropic) — chat en claude.ai

---

## Descripción general

Durante el Lab 2 usé IA principalmente para resolver dudas sobre cómo
estructurar las funciones matemáticas y para solucionar errores que me
aparecían al ejecutar el notebook. Las decisiones de diseño y la comprensión
de los algoritmos las trabajé yo a partir de lo visto en clase.

---

## Detalle por celda

### Celda 1 — Carga del corpus
Tenía duda de cómo cargar el JSON del Lab 1 y separar los tokens.
Le pregunté a la IA y me mostró cómo usar `json.load` y extraer
la lista de tokens con un list comprehension. Lo entendí y lo apliqué.

### Celda 2 — Preprocesar
Reutilicé mi función del Lab 1. Tuve un error de `NameError` porque
`re` y `unicodedata` no estaban importados en esa celda. Le pregunté
a la IA por qué ocurría y me explicó que cada celda necesita sus imports
si los usa directamente. Lo corregí agregando los imports al inicio.

### Celda 3 — TF, IDF, TF-IDF
Tenía claro el concepto de las fórmulas por la clase, pero tuve un
`NameError` de `documentos` porque no había ejecutado las celdas en orden.
La IA me sugirió usar "Run All" para ejecutar todo en secuencia. Lo hice
y funcionó correctamente.

### Celda 4 — Vectorizar consulta
Le pregunté si era correcto usar el IDF del corpus sin recalcularlo
con la consulta incluida. Me confirmó que sí, y me explicó que
recalcularlo alteraría los pesos del índice ya construido.

### Celda 5 — Coseno y buscar
Tenía duda de cómo manejar el caso de norma 0 para evitar división
por cero. La IA me explicó que basta con verificar antes de dividir
y retornar 0.0 en ese caso. Yo implementé la función con ese criterio.

### Celda 9 — Verificación sklearn
Tuve un `ModuleNotFoundError` porque sklearn no estaba instalado en
el entorno virtual. La IA me indicó el comando `pip install scikit-learn`.
Los rankings de mi implementación y los de sklearn coincidieron en orden,
lo que confirma que mis funciones están correctas.

---

## Qué no usé IA para hacer

- La lógica matemática de TF, IDF y coseno la entendí de las fórmulas
  de clase y la implementé yo mismo.
- Las dos consultas fallidas y sus causas las identifiqué yo analizando
  el corpus y probando diferentes búsquedas.
- La interpretación de los resultados y la comparación con sklearn
  la hice yo observando las salidas.