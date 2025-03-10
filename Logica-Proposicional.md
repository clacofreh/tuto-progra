# **📌 Lógica Proposicional**

La **lógica proposicional** es una herramienta para razonar usando frases que pueden ser **verdaderas** o **falsas**. Nos permite combinar estas frases para crear reglas y llegar a conclusiones lógicas.

---

## 📖 **Índice**
1. [**Introducción a la Lógica Proposicional**](#1️⃣-introducción-a-la-lógica-proposicional)
2. [**Proposiciones y Valores de Verdad**](#2️⃣-proposiciones-y-valores-de-verdad)
3. [**Conectores Lógicos**](#3️⃣-conectores-lógicos)
   - Negación (NO, ¬)
   - Conjunción (Y, ∧)
   - Disyunción (O, ∨)
   - Implicación (Si... entonces, →)
   - Bicondicional (Si y solo si, ↔)
4. [**Tablas de Verdad**](#4️⃣-tablas-de-verdad)
5. [**Leyes y Reglas de Inferencia**](#5️⃣-leyes-y-reglas-de-inferencia)
6. [**Aplicaciones de la Lógica Proposicional**](#6️⃣-aplicaciones-de-la-lógica-proposicional)
7. [**Ejemplo Práctico**](#7️⃣-ejemplo-práctico)
8. [**Resumen Final**](#-resumen-final)

---

## 1️⃣ **Introducción a la Lógica Proposicional**

Imagina que tienes una caja mágica que solo responde con **"Sí" (Verdadero)** o **"No" (Falso)** a cualquier pregunta.

📌 **Ejemplo:**
- "¿El cielo es azul?" → ✅ **Sí (Verdadero)**
- "¿Los gatos vuelan?" → ❌ **No (Falso)**

A estas frases que pueden ser **Sí o No**, las llamamos **proposiciones**.

---

## 2️⃣ **Proposiciones y Valores de Verdad**

Una **proposición** es una afirmación que puede ser **Verdadera (V)** o **Falsa (F)**.

📌 **Ejemplo:**
- "2 + 2 = 4" → ✅ **Verdadero**
- "El agua hierve a 50°C" → ❌ **Falso**

Las proposiciones se representan con letras como **p, q, r**.

---

## 3️⃣ **Conectores Lógicos**

Podemos combinar proposiciones usando **conectores lógicos**.

| **Símbolo** | **Nombre** | **Ejemplo** |
|---------|--------|---------|
| **¬**   | No (Negación) | "No es de día" |
| **∧**   | Y (AND) | "Tengo helado **y** galletas" |
| **∨**   | O (OR) | "Tengo helado **o** galletas" |
| **→**   | Si... entonces (Implicación) | "Si llueve, entonces uso paraguas" |
| **↔**   | Si y solo si (Equivalencia) | "Voy al cine **si y solo si** tengo dinero" |

---

## 4️⃣ **Tablas de Verdad**

Las **tablas de verdad** nos ayudan a ver todas las combinaciones de valores de verdad para una proposición.

### Negación (¬)
| p | ¬p |
|---|---|
| ✅ V | ❌ F |
| ❌ F | ✅ V |

### Conjunción (∧)
| p | q | p ∧ q |
|---|---|-------|
| ✅ V | ✅ V | ✅ V |
| ✅ V | ❌ F | ❌ F |
| ❌ F | ✅ V | ❌ F |
| ❌ F | ❌ F | ❌ F |

### Disyunción (∨)
| p | q | p ∨ q |
|---|---|-------|
| ✅ V | ✅ V | ✅ V |
| ✅ V | ❌ F | ✅ V |
| ❌ F | ✅ V | ✅ V |
| ❌ F | ❌ F | ❌ F |

### Implicación (→)
| p | q | p → q |
|---|---|-------|
| ✅ V | ✅ V | ✅ V |
| ✅ V | ❌ F | ❌ F |
| ❌ F | ✅ V | ✅ V |
| ❌ F | ❌ F | ✅ V |

### Bicondicional (↔)
| p | q | p ↔ q |
|---|---|-------|
| ✅ V | ✅ V | ✅ V |
| ✅ V | ❌ F | ❌ F |
| ❌ F | ✅ V | ❌ F |
| ❌ F | ❌ F | ✅ V |

📌 **Reglas importantes:**
- **Negación (¬)**: Invierte el valor de verdad
- **Conjunción (∧)**: Verdadera solo si ambas son verdaderas
- **Disyunción (∨)**: Falsa solo si ambas son falsas
- **Implicación (→)**: Falsa solo si p es verdadera y q es falsa
- **Bicondicional (↔)**: Verdadera si ambas son iguales

## 5️⃣ **Leyes y Reglas de Inferencia**

### 📐 **Leyes Fundamentales de la Lógica**

Estas leyes son como las "reglas matemáticas" de la lógica que siempre se cumplen:

#### **Ley de identidad:** 
- **p ∧ V = p**: Si combinamos una proposición con algo que siempre es verdadero (usando AND), el resultado es la proposición original.
  - *Ejemplo:* "Está lloviendo Y es verdad que existo" = "Está lloviendo"
- **p ∨ F = p**: Si combinamos una proposición con algo que siempre es falso (usando OR), el resultado es la proposición original.
  - *Ejemplo:* "Está lloviendo O los peces viven en Marte" = "Está lloviendo"

#### **Ley del complemento:**
- **p ∨ ¬p = V**: Una proposición O su negación siempre es verdadero (no hay otra opción).
  - *Ejemplo:* "Está lloviendo O NO está lloviendo" = Siempre verdadero
- **p ∧ ¬p = F**: Una proposición Y su negación siempre es falso (es imposible).
  - *Ejemplo:* "Está lloviendo Y NO está lloviendo" = Siempre falso

#### **Ley de distributiva:**
- **p ∧ (q ∨ r) = (p ∧ q) ∨ (p ∧ r)**: Podemos "distribuir" una proposición sobre un paréntesis.
  - *Ejemplo:* "Tengo hambre Y (tengo pizza O tengo pasta)" = "(Tengo hambre Y tengo pizza) O (Tengo hambre Y tengo pasta)"

### 🔍 **Reglas de Inferencia**

Estas reglas nos permiten llegar a conclusiones lógicas a partir de premisas:

#### **Modus Ponens (Afirmación del antecedente):**
- Si sabemos que "p → q" (Si p, entonces q) y también sabemos que "p" es verdadero, podemos concluir que "q" es verdadero.
- *Ejemplo práctico:* 
  - Premisa 1: "Si llueve, entonces las calles se mojan"
  - Premisa 2: "Está lloviendo"
  - Conclusión: "Las calles están mojadas"

#### **Modus Tollens (Negación del consecuente):**
- Si sabemos que "p → q" (Si p, entonces q) y también sabemos que "q" es falso, podemos concluir que "p" es falso.
- *Ejemplo práctico:* 
  - Premisa 1: "Si Juan está en casa, entonces su auto está en el garaje"
  - Premisa 2: "El auto de Juan NO está en el garaje"
  - Conclusión: "Juan NO está en casa"

#### **Silogismo Hipotético:**
- Si "p → q" y "q → r", entonces "p → r"
- *Ejemplo:* 
  - "Si llueve, entonces uso paraguas"
  - "Si uso paraguas, entonces no me mojo"
  - Por lo tanto: "Si llueve, entonces no me mojo"

#### **Silogismo Disyuntivo:**
- Si "p ∨ q" y "¬p", entonces "q"
- *Ejemplo:* 
  - "O estudio o repruebo"
  - "No estoy estudiando"
  - Por lo tanto: "Voy a reprobar"
## 6️⃣ **Aplicaciones de la Lógica Proposicional**

✅ **Tomar decisiones lógicas:** "Si estudio, entonces apruebo".  
✅ **Resolver problemas de verdad o mentira:** "Si un sospechoso miente, podemos saber quién es culpable".  
✅ **Usar en computadoras:** Los circuitos electrónicos siguen reglas de lógica para hacer cálculos.

---

## 7️⃣ **Ejemplo Práctico**

Imagina que eres un **detective** y tienes estas pistas:
1️⃣ "Si Juan está en casa, entonces el perro ladra".  
2️⃣ "El perro no ladró".  

🔍 **Pregunta:** ¿Juan está en casa?  
💡 **Respuesta usando lógica:**
- Si el perro **no** ladró, entonces **Juan no puede estar en casa**.
- Usamos la regla de **Si... entonces (→)** para resolverlo.

---

## 🔥 **Resumen Final**

- **Lógica Proposicional** = Juego de **verdadero o falso** con frases.  
- Usamos **conectores** para unir frases y crear reglas.  
- Las **tablas de verdad** nos ayudan a analizar combinaciones.  
- Se usa en la vida diaria, en matemáticas y en computadoras.

