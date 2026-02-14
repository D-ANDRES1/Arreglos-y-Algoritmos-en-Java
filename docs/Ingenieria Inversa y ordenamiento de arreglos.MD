# Ingenieria Inversa del Archivo JAR

## 1. Clases existentes

- **App**
- **BubbleSort**  
- **MergeSortDemo**  
- **QuickSort**  
- **Sumarray

## Ejemplo del app.class

package umg.edu.gt.data_structure.introduction;

import java.util.Arrays;
import umg.edu.gt.data_structure.array.BubbleSort;
import umg.edu.gt.data_structure.array.MergeSortDemo;
import umg.edu.gt.data_structure.array.QuickSort;
import umg.edu.gt.data_structure.array.SumArray;

public class App {
  public static void main(String[] args) {
    int[] d1 = { 3, 5, 2, 9 };
    SumArray sumArray = new SumArray();
    System.out.println(sumArray.sum(d1));
    MergeSortDemo mergeSortDemo = new MergeSortDemo();
    int[] d2 = { 8, 3, 7, 4, 9, 2 };
    mergeSortDemo.mergeSort(d2);
    System.out.println(Arrays.toString(d2));
    BubbleSort blueSort = new BubbleSort();
    int[] arr = { 5, 1, 4, 2, 8 };
    blueSort.bubbleSort(arr);
    for (int n : arr)
      System.out.print(n + " "); 
    QuickSort quick = new QuickSort();
    int[] arr1 = { 10, 7, 8, 9, 1, 5 };
    quick.quickSort(arr1, 0, arr1.length - 1);
    for (int n : arr1)
      System.out.print(n + " "); 
    int[] arr2 = { 10, 7, 8, 9, 1, 5 };
    Arrays.sort(arr2);
    System.out.println("\nUse sort: " + Arrays.toString(arr2));
  }
}


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

