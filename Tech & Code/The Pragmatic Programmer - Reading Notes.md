# The Pragmatic Programmer: 20th Anniversary Edition
## Reading Notes & Opinions

---

## Chapter 1: A Pragmatic Philosophy
**Topics:** Career ownership, software entropy, and knowledge portfolios

### My Thoughts & Opinions:
- Habla sobre como comportarse tanto con uno mismo como con los demas
- Recomienda no dejar ventanas rotas sin atender, si no se puede resolver se anota
- Involve your users in the Trade-Off: Preguntar si prefieren algo rapido con algunos errores o algo perfecto que demore
- Generalmente ningun software es perfecto, centrarse en que sea usañe
- Portfoliio: Invest, buy low sell high
- Estudiar sobre Critical Thinking
- Escribir que es lo que queremos comunicar antes de planear que decir
- Restrict your nonAPI commeting to discuting why somehting is donde,its purpose and its goal. the code alrwad shows how its done
- Know what you want to say, know your audience, choose your moment, choose a style, make it look good, involve your audience, be a listener, get back to people

---

## Chapter 2: A Pragmatic Approach
**Topics:** Good design, the DRY principle, and orthogonality

### My Thoughts & Opinions:
- ETC: Easier to change. did the thing i just did make the overall system easier or ahrder to change?
- Idea: Resumen semana por semana del codigo funciones (esto es una idea mia no algo que dice el libro)
- DRY: Dont Repeat Yourself. No tener cosas repetidas porque quedaran desactualizadas.
- All services offered by a module should be avialable through a uniform notation
- Orthogonality: Two or more things are orthogonal if changes in one do not affect any of the others
- In a well-designed system, the DB code will be orthogonal to the user interface.
- Diseniar software en capas con distintas abstracciones
- Also ask yourself how decoupled your design is from changes in real world (Cambios de numeros de celular, ids ,etc)
- Hacer el codigo lo mas reversible posible para poder cambiar de BD; de Web a Mobile;
- Mantener la arquitecutra Flexible
- Prototyping generates disposable code. Tracer code is lean but complete, and forms par of the skeleton of the final system
- Un prototipo puede ser de cualquier cosa que implique riesgo. Algo que no fue probado o que es critico o dudoso.
- Al final menciono como estimar recursos y tiempo

---

## Chapter 3: The Basic Tools
**Topics:** Plain text, shell games, and version control

### My Thoughts & Opinions:
- You need to be comfortable beyond the limits imposed by an IDE. (Esto no lo sabian en la universidad(?)
- Crear alias en Shell para comandos que normalmente usamos por ejemplo update and upgrade
- Al uso de Tab lo podemos configurar para que cambie segun contexto
- Preguntarse siempre que hacemos algo repetitivo si hay alguna mejor forma de hacerlo
- Centrarse en resolver un Bug no en de quien fue la culpa y apagar las defensas del ego
- 

---

## Chapter 4: Pragmatic Paranoia
**Topics:** Design by contract and assertive programming

### My Thoughts & Opinions:
- Hacer un contrato sobre que hara y que no hara el Software.  Aclarando Preconditions, Postcondition, Classs invariants
- Dont eclipse the aplicattion with error handling
- Planificar solo lo que podemos ver no pensar tanto en el futuro sino en el presente
- The more you have to predict what the future will look like, the more risk you incur
- Hacer codigo reemplazable, en caso de que no sirva más se va

---

## Chapter 5: Bend, or Break
**Topics:** Decoupling and configuration

### My Thoughts & Opinions:
- Mantener bajo acoplamiento en el codigo, suena muy a fundamentos pero es algo que no tengo tan presente al programar
- Un chatbot es eventdriven? Deberiamos hacer graficos como en sistemas 3?
- Ver mas sobre finite state machines
  
---

## Chapter 6: Concurrency
**Topics:** Breaking temporal coupling and shared state

### My Thoughts & Opinions:
- La herencia es acoplamiento ya sea usarla para no escribir codigo o tener tipos de cosa esta mal
- Alternativas
  * Interfaces and protocols
  * Delegation
  * Mixins and traits
- You can use activity disgramas to maximize parallelism by identifying activtitirs that could be performef in parallel but arent
---

## Chapter 7: While You Are Coding
**Topics:** Refactoring and programming by coincidence

### My Thoughts & Opinions:
- Cuando nos trabamos en codigo tomarnos una pausa. Si luego de eso no encontramos las solucion consultar por fuera
- Capaz que contando el problema nos viene la solución
- No escribir codigo sobre cosas que asumimos, probarlo
- No solo testear codigo, testear lo que asumimos también
- Para estimar recursos usar big O notation

Notas reescritas por claude:

**Configuración externa**
- Sacá del código todo lo que sabés que va a cambiar: reglas de validación por entorno, valores impuestos desde afuera (alícuotas de impuestos), detalles de formato por sitio, claves de licencia. Todo eso va a un "balde" de configuración.
- Si cambia un valor de configuración, no debería hacer falta recompilar.
- Código dodo: sin configuración externa el código no se adapta, y lo que no se adapta se extingue.
- Muchas apps cargan la configuración en una estructura global al arrancar. Los autores prefieren envolverla en una API fina, para que el código no dependa de cómo está representada.
- Configuración como servicio: externa, pero detrás de una API de servicio en vez de un archivo plano o una base. Ventajas: varias apps la comparten con autenticación y control de acceso, los cambios son globales, se mantiene desde una interfaz dedicada y pasa a ser dinámica.
- Lo dinámico importa en sistemas de alta disponibilidad. Tener que reiniciar para cambiar un parámetro está fuera de época. Con un servicio, los componentes se suscriben a cambios y reciben los valores nuevos.

**Notación Big‑O**
- O() aproxima cómo crece el costo (tiempo, memoria) con el tamaño n. O(n²) significa que duplicar la entrada cuadruplica el tiempo. Leé la O como "del orden de". Es una cota superior.
- Un bucle O(n²) simple puede ganarle a un algoritmo O(n log n) complejo con n chico, sobre todo si el segundo tiene un bucle interno caro.
- Advertencias prácticas: puede parecer lineal con pocos datos y desplomarse con millones de registros cuando el sistema empieza a paginar. Un sort probado solo con claves aleatorias te puede sorprender con entrada ya ordenada. Cubrí esos casos.
- Si tenés O(n²), buscá una variante divide y vencerás que te lleve a O(n log n).
- Si no sabés cómo escala, corré el código variando el tamaño de entrada y graficá. Con tres o cuatro puntos ves la forma de la curva.

**Concurrencia (diagrama de actividad)**
Pasos escritos en serie muchas veces se pueden paralelizar. En el ejemplo del trago: abrir la mezcla, abrir la licuadora y medir el ron son independientes; se sincronizan (barras gruesas) antes de poner la mezcla, el hielo y el ron; después cerrar, licuar, abrir; en paralelo se buscan vasos y sombrillitas; todo converge en "servir".

---

## Chapter 8: Before the Project 
**Topics:** Requirements and solving impossible puzzles

### My Thoughts & Opinions:
_[Space for your notes as you read...]_

---

## Chapter 9: Pragmatic Projects
**Topics:** Pragmatic teams and delighting users

### My Thoughts & Opinions:
_[Space for your notes as you read...]_

---

## References
- [Pearson - The Pragmatic Programmer](https://www.pearson.com/en-us/subject-catalog/p/Thomas-The-Pragmatic-Programmer-your-journey-to-mastery-20th-Anniversary-Edition-2nd-Edition/P200000000337?view=educator&srsltid=AfmBOooj08HZfKTKcM1AnUCEUh-gecStyQyda6Kk7A2enhzcgnPCAcBe)
- [Pragmatic Programmers - Official Site](https://pragprog.com/titles/tpp20/the-pragmatic-programmer-20th-anniversary-edition/)
