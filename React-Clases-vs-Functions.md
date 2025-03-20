## 🎯 Tema: ¿Cuándo realmente necesitamos clases en React Native?

### 📌 Objetivo:
Explicar cuándo el uso de clases en React Native es innecesario y cómo reemplazarlas con funciones y hooks, sin imponer una migración forzada.

---

## 🏁 1. Introducción (5-10 min)

### 👉 Pregunta para abrir el debate:
**"¿Qué problemas han tenido al usar clases en React Native?"**

Si nadie responde mucho, lanzar ejemplos:
- _"¿Alguna vez han tenido que hacer un `bind(this)` porque `this` se perdió?"_
- _"¿Han intentado compartir lógica entre clases y se volvió complicado?"_

🔍 **Meta:** Que el equipo detecte los problemas antes de la parte técnica.

---

## 🔥 2. Clases: ¿Cuándo son un problema? (15 min)

### 📌 1. Código más verboso y difícil de mantener

**Ejemplo con clase (innecesario)**:
```javascript
class Contador {
  constructor() {
    this.contador = 0;
  }

  aumentar() {
    this.contador++;
  }
}
```
**Alternativa con Hooks:**
```javascript
const [contador, setContador] = useState(0);
const aumentar = () => setContador(contador + 1);
```
💡 **Conclusión:** Hooks hacen lo mismo con menos código y sin `this`.

---

### 📌 2. React no detecta cambios en clases

**Ejemplo con clase (React no detecta cambios)**:
```javascript
class Store {
  data = { usuario: "Juan" };
  setUsuario(nombre) {
    this.data.usuario = nombre;
  }
}
```
🚨 React no sabe que `data.usuario` cambió.

**Solución con Hooks:**
```javascript
const [usuario, setUsuario] = useState("Juan");
```
💡 **Conclusión:** Hooks permiten reactividad sin hacks adicionales.

---

### 📌 3. Clases pueden generar problemas con Redux y AsyncStorage

**Ejemplo con problema al guardar en AsyncStorage:**
```javascript
class Usuario {
  constructor(nombre) {
    this.nombre = nombre;
  }
}
```
Si se guarda en Redux o AsyncStorage, **los métodos se pierden**.

💡 **Solución:** Usar objetos planos:
```javascript
const usuario = { nombre: "Juan" };
```

---

## 🛠️ 3. ¿Cuándo SÍ usar clases en React Native? (15 min)

### ✅ Casos donde las clases pueden ser útiles:

1. **Modelos de datos complejos** (si encapsulan lógica de negocio)
```javascript
class Usuario {
  constructor(nombre, edad) {
    this.nombre = nombre;
    this.edad = edad;
  }
  esMayor() {
    return this.edad >= 18;
  }
}
```

2. **Integraciones con librerías externas** (si una librería lo requiere)

3. **Patrón Singleton en servicios**
```javascript
class APIService {
  static instance;
  constructor(url) {
    if (!APIService.instance) {
      this.url = url;
      APIService.instance = this;
    }
    return APIService.instance;
  }
}
```

---

## 🎤 4. Conclusión + Plan de Acción (10 min)

### 📈 Pregunta para el equipo:
**"En qué partes de nuestro código usamos clases donde podríamos usar funciones?"**

### 💡 Plan de Acción:
1. No reemplazar clases de inmediato, pero en **nuevas funcionalidades**, **preferir hooks y funciones**.
2. Cuando haya código problemático con clases (estado, `this`, reusabilidad), **buscar una alternativa con hooks**.
3. Usar clases **solo en los casos justificados** que se discutieron.

---

## 🎮 Ejercicio rápido (opcional):
Pídeles que conviertan **un código con clases** a **hooks** en vivo. 🚀
