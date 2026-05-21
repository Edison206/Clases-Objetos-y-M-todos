# APE-04: Clases, Objetos y Métodos

**Universidad Técnica de Ambato**  
Facultad de Ingeniería en Sistemas, Electrónica e Industrial  
Carrera de Software · Nivel Primero · Enero 2026 – Julio 2026

---

**Asignatura:** Algoritmos y Lógica de Programación  
**Docente:** Ing. M.Sc. José Rubén Caiza Caizabuano  
**Estudiante:** Edison Landeta  

---

## Descripción

Este repositorio contiene el código fuente de la guía práctica **APE-04**, cuyo objetivo es desarrollar programas en **C++** y **Java** aplicando el paradigma de **Programación Orientada a Objetos (POO)**: clases, objetos, constructores, encapsulamiento y métodos.

---

## Estructura del Repositorio

```
APE04-ClasesObjetos/
│
├── Ejercicio1_Estudiante/
│   ├── cpp/
│   │   └── Estudiante.cpp        ← Clase + Main en un solo archivo C++
│   └── java/
│       ├── Estudiante.java       ← Definición de la clase
│       └── MainEstudiante.java   ← Programa principal
│
├── Ejercicio2_Producto/
│   ├── cpp/
│   │   └── Producto.cpp          ← Clase + Main en un solo archivo C++
│   └── java/
│       ├── Producto.java         ← Definición de la clase
│       └── MainProducto.java     ← Programa principal
│
└── README.md
```

---

## Ejercicio 1 – Clase Estudiante

### Descripción
Modela un estudiante universitario con sus datos académicos.

### Atributos (privados)
| Atributo   | Tipo   | Descripción                      |
|------------|--------|----------------------------------|
| `nombre`   | string | Nombre completo del estudiante   |
| `edad`     | int    | Edad en años                     |
| `carrera`  | string | Carrera universitaria            |
| `promedio` | double | Promedio académico (0.0 – 10.0)  |

### Métodos (públicos)
| Método              | Retorno | Descripción                            |
|---------------------|---------|----------------------------------------|
| `getNombre()`       | string  | Retorna el nombre                      |
| `getEdad()`         | int     | Retorna la edad                        |
| `getCarrera()`      | string  | Retorna la carrera                     |
| `getPromedio()`     | double  | Retorna el promedio                    |
| `setNombre(n)`      | void    | Actualiza el nombre                    |
| `setEdad(e)`        | void    | Actualiza la edad                      |
| `setCarrera(c)`     | void    | Actualiza la carrera                   |
| `setPromedio(p)`    | void    | Actualiza el promedio                  |
| `estaAprobado()`    | bool    | `true` si promedio >= 7                |
| `mostrar()`         | void    | Imprime todos los datos + estado       |

### Datos de prueba
```
Edison Landeta  →  Promedio: 8.5  →  Aprobado
Maria Torres    →  Promedio: 5.8  →  Reprobado
Carlos Vega     →  Promedio: 7.3  →  Aprobado
```

### Compilación y Ejecución

**C++**
```bash
cd Ejercicio1_Estudiante/cpp
g++ -o estudiante Estudiante.cpp
./estudiante
```

**Java**
```bash
cd Ejercicio1_Estudiante/java
javac Estudiante.java MainEstudiante.java
java MainEstudiante
```

### Salida esperada
```
===== SISTEMA DE NOTAS - ESTUDIANTES =====
================================
Nombre  : Edison Landeta
Edad    : 19
Carrera : Software
Promedio: 8.50
Estado  : Aprobado
================================
Nombre  : Maria Torres
Edad    : 21
Carrera : Industrial
Promedio: 5.80
Estado  : Reprobado
================================
Nombre  : Carlos Vega
Edad    : 20
Carrera : Sistemas
Promedio: 7.30
Estado  : Aprobado
================================
Total estudiantes : 3
Total aprobados   : 2
```

---

## Ejercicio 2 – Clase Producto

### Descripción
Modela un producto de inventario con su información comercial.

### Atributos (privados)
| Atributo    | Tipo   | Descripción                         |
|-------------|--------|-------------------------------------|
| `nombre`    | string | Nombre del producto                 |
| `precio`    | double | Precio unitario                     |
| `cantidad`  | int    | Cantidad de unidades en stock       |
| `categoria` | string | Categoría del producto              |

### Métodos (públicos)
| Método                    | Retorno | Descripción                              |
|---------------------------|---------|------------------------------------------|
| `getNombre()`             | string  | Retorna el nombre                        |
| `getPrecio()`             | double  | Retorna el precio                        |
| `getCantidad()`           | int     | Retorna la cantidad                      |
| `getCategoria()`          | string  | Retorna la categoría                     |
| `setNombre(n)`            | void    | Actualiza el nombre                      |
| `setPrecio(p)`            | void    | Actualiza el precio                      |
| `setCantidad(c)`          | void    | Actualiza la cantidad                    |
| `setCategoria(c)`         | void    | Actualiza la categoría                   |
| `calcularSubtotal()`      | double  | Retorna `precio × cantidad`              |
| `aplicarDescuento(pct)`   | void    | Reduce el precio en `pct%`               |
| `mostrar()`               | void    | Imprime todos los datos + subtotal       |

### Datos de prueba
```
Laptop   →  $850.00 × 2 = $1700.00
Mouse    →   $15.00 × 5 =   $75.00
Teclado  →   $30.00 × 3 =   $90.00
```

### Compilación y Ejecución

**C++**
```bash
cd Ejercicio2_Producto/cpp
g++ -o producto Producto.cpp
./producto
```

**Java**
```bash
cd Ejercicio2_Producto/java
javac Producto.java MainProducto.java
java MainProducto
```

### Salida esperada
```
===== SISTEMA DE INVENTARIO - PRODUCTOS =====
================================
Nombre    : Laptop
Categoria : Tecnologia
Precio    : $850.00
Cantidad  : 2
Subtotal  : $1700.00
================================
Nombre    : Mouse
Categoria : Periferico
Precio    : $15.00
Cantidad  : 5
Subtotal  : $75.00
================================
Nombre    : Teclado
Categoria : Periferico
Precio    : $30.00
Cantidad  : 3
Subtotal  : $90.00

-- Aplicando 10% de descuento a Laptop --
Nuevo precio Laptop: $765.00
================================
Total general       : $1865.00
Producto mayor valor: Laptop ($1700.00)
```

---

## Requisitos

| Herramienta        | Versión mínima | Uso                         |
|--------------------|----------------|-----------------------------|
| g++ / MinGW        | C++11 o mayor  | Compilar archivos `.cpp`    |
| Java JDK           | 17+            | Compilar y ejecutar Java    |
| Visual Studio Code | Cualquiera     | Editor recomendado          |

---

## Conceptos Aplicados

- ✅ **Encapsulamiento** — atributos `private`, métodos `public`
- ✅ **Constructor parametrizado** — inicialización de objetos con datos
- ✅ **Métodos getter y setter** — acceso controlado a atributos
- ✅ **Instanciación de objetos** — uso del operador `new` (Java) y objetos locales (C++)
- ✅ **Métodos de comportamiento** — `mostrar()`, `estaAprobado()`, `calcularSubtotal()`, `aplicarDescuento()`
- ✅ **Arreglo de objetos** — iteración con `for` sobre una colección de instancias

---

*Ciclo académico: Enero 2026 – Julio 2026*
