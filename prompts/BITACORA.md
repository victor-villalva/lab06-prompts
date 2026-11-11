# Bitacora de prompts

Laboratorio 06: Fundamentos de Ingenieria de Prompts.

Herramienta de IA usada: ChatGPT

## Ejercicio 2: Tokens y ventana de contexto

| Texto | Caracteres | Tokens |
|---|---:|---:|
| Los estudiantes programan en Java. | 34 | 7 |
| The students program in Java. | 29 | 6 |
| desafortunadamente | 18 | 4 |

En la primera conversación, ChatGPT recordó correctamente el nombre de la aplicación y la tecnología después de recibir esa información.

En una conversación nueva también recordó los datos. Esto puede deberse a la función de memoria de ChatGPT, que permite conservar información de conversaciones anteriores.

## Ejercicio 3: Temperatura

| Temperatura | BiblioTec (%) | Nombres obtenidos en los 5 intentos |
|---|---:|---|
| 0 | 100.0% | BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 0.5 | 65.3% | BiblioTec, LibroYa, BiblioTec, BiblioTec, BiblioTec |
| 1 | 44.5% | BiblioTec, LibroYa, LectoGo, BiblioTec, LibroYa |
| 1.8 (intento 1) | 32.2% | PaginaLibre, PrestaLibro, LectoGo, LibroYa, BiblioTec |
| 1.8 (intento 2) | 32.2% | LibroYa, BiblioTec, NubeDeTinta, BiblioTec, PrestaLibro |

Al aumentar la temperatura, disminuye la probabilidad de elegir BiblioTec y aparecen otros nombres con mayor frecuencia.

Los nombres no cambian porque el simulador utiliza una lista de seis opciones previamente definida en el código.

## Ejercicio 4: Prompt vago vs estructurado

| Criterio | Prompt vago | Prompt estructurado |
|---|---|---|
| Menciona objetivo del sistema | Sí | Sí |
| Menciona usuarios principales | No | Sí |
| Tiene exactamente 3 funcionalidades | No | Sí |
| Está en 3 párrafos | No | Sí |
| Lo usaría en un informe real | No | Sí |

El prompt vago generó una descripción general con varias funcionalidades y sin una estructura definida.

El prompt estructurado obtuvo una respuesta más precisa, indicando el objetivo, los usuarios principales y exactamente tres funcionalidades en tres párrafos.

## Ejercicio 5: Anatomia de un prompt

| Componente | Texto del prompt final |
|---|---|
| Rol | Actua como desarrollador Java. |
| Instruccion | Crea un programa en Java para gestionar los productos de una tienda. |
| Contexto | Usando una clase Producto con los atributos codigo, nombre, precio y stock. |
| Ejemplo | Usa este estilo para los metodos: getPrecio(), setPrecio(double precio). |
| Formato | Explica primero la estructura de la clase y luego presenta el codigo Java. |

**Cambios observados por nivel:**

- Nivel 1: La respuesta fue general porque solo se pidió crear un programa.
- Nivel 2: La respuesta incluyó el rol de desarrollador Java.
- Nivel 3: Se especificó que el programa debía gestionar productos de una tienda.
- Nivel 4: Se indicaron los atributos de la clase Producto.
- Nivel 5: Se solicitó explicar primero la estructura y después presentar el código.
