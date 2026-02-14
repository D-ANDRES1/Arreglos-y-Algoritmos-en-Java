# Ingenieria Inversa del Archivo JAR

## 1. Clases existentes

T
- **BubbleSort**  
- **MergeSortDemo**  
- **QuickSort**  
- **Sumarray

Estas clases corresponden a algoritmos de ordenamiento sobre arreglos enteros (`int[]`).

---

## 2. Operaciones sobre arreglos

### BubbleSort
- Itera sobre el arreglo comparando elementos adyacentes.
- Intercambia los valores si el de la izquierda es mayor que el de la derecha.
- Optimización: si no hay intercambios en una pasada, termina antes.
- Resultado: **orden ascendente**.

### MergeSortDemo
- Divide el arreglo en mitades recursivamente (`Arrays.copyOfRange`).
- Combina los subarreglos ordenándolos en un solo arreglo (`merge`).
- Uso de índices `i`, `j`, `k`:
  - `i` → índice de subarreglo izquierdo
  - `j` → índice de subarreglo derecho
  - `k` → índice del arreglo original donde se van colocando los elementos más pequeños
- Resultado: **orden ascendente**, estable.

### QuickSort
- Selecciona un **pivote** (último elemento del subarreglo).
- Reorganiza el arreglo colocando elementos menores a la izquierda y mayores a la derecha.
- Aplica recursión en las partes izquierda y derecha del pivote.
- Resultado: **orden ascendente**, in-place.

---


- **BubbleSort** es simple y útil para aprender, pero poco eficiente para arreglos grandes.
- **MergeSortDemo** utiliza memoria extra para los subarreglos, pero siempre garantiza orden correcto.
- **QuickSort** es muy rápido en promedio, pero puede ser ineficiente si el pivote no se selecciona bien.
- Todas las clases trabajan sobre **arreglos de enteros (`int[]`)**.
