# 📘 Práctica ED02 – Del código fuente al ejecutable (con IDE)

📌 **Objetivo:** comprobar paso a paso el proceso **código fuente → código objeto → ejecutable** en C, trabajando con un programa algo más largo y usando un IDE para depurar errores de sintaxis.

---

### Parte 1. Código inicial con errores

1. Copia este programa en un archivo llamado `bucle2.c` (**contiene 2 errores de sintaxis intencionados**):

```c
#include <stdio.h>
#include <time.h>

int main() {
    clock_t inicio, fin
    inicio = clock();

    long long suma = 0
    for (long long i = 0; i < 100000000; i++) {
        suma += i;
    }

    fin = clock();
    double tiempo = (double)(fin - inicio) / CLOCKS_PER_SEC;

    printf("Suma final: %lld\n", suma);
    printf("Tiempo en segundos: %f\n", tiempo);
    return 0;
}
```

2. Intenta compilar desde **CMD**:

   ```bash
   gcc bucle.c -o bucle.exe
   ```
3. Anota el **mensaje de error** que aparece.

---

### Parte 2. Uso de un IDE

1. Instala un IDE para C:

   * **Code::Blocks** 👉 [http://www.codeblocks.org/downloads/](http://www.codeblocks.org/downloads/)
     *(elige la versión “mingw-setup.exe”, que ya incluye compilador)*
     
2. Abre el archivo `bucle2.c` en el IDE.
3. Usa las herramientas del IDE para encontrar y corregir los **2 errores de sintaxis**.
4. Compila (Build) y ejecuta (Run) el programa desde el IDE.
5. Haz una **captura de la ejecución correcta** mostrando la suma final y el tiempo medido.

---

### Parte 3. Reflexión

Responde:

1. ¿Qué diferencias notaste entre compilar en **CMD** y compilar en el **IDE**?
2. ¿Qué ventajas tiene el IDE a la hora de detectar errores de sintaxis?
3. ¿Qué aporta el IDE frente a un editor simple como Notepad++?
4. ¿En qué casos crees que puede seguir siendo útil un editor simple?

---

📌 **Entrega:**

* Capturas de pantalla de la ejecución con error en CMD, corrección en el IDE y resultado final.
* Respuestas a las preguntas de la reflexión.
