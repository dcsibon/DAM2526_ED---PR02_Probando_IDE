# 📘 Práctica ED02 – Del código fuente al ejecutable (con IDE) - versión Windows

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
   gcc bucle2.c -o bucle2.exe
   ```

3. Anota el **mensaje de error** que aparece.

---

### Parte 2. Uso de un IDE

1. **Instala Visual Studio Code**

   * Descarga el instalador desde 👉 [https://code.visualstudio.com/Download](https://code.visualstudio.com/Download).
   * Ejecuta el archivo `.exe` y durante la instalación marca la opción **“Add to PATH”**.

2. **Abre Visual Studio Code** y entra en la sección de **Extensiones** (icono de bloques en la barra lateral izquierda o `Ctrl+Shift+X`).

3. **Instala las siguientes extensiones de Microsoft** (como se ven en la captura):

   * **C/C++** → soporte para IntelliSense, resaltado de errores y depuración.
   * **C/C++ Extension Pack** → incluye configuraciones útiles adicionales.
   * *(Opcional)* **C/C++ Themes** → cambia solo la apariencia de la extensión *(lo habitual es que se instale solo al instalar el Extension Pack)*.

4. **Selecciona el compilador por defecto (solo la primera vez):**

   * Al abrir un archivo `.c`, la extensión C/C++ puede mostrar una notificación preguntando qué compilador usar.
   * Selecciona **GCC (MinGW-w64/WinLibs)** en la ruta donde lo instalaste (por ejemplo `C:\mingw64\bin\gcc.exe`).
   * Si no aparece el aviso, puedes configurarlo desde:

     * Menú **View > Command Palette…** (`Ctrl+Shift+P`).
     * Busca **C/C++: Edit Configurations (UI)**.
     * En **Compiler path** selecciona tu `gcc.exe`.

5. **Abre el archivo `bucle2.c`** en VS Code.

6. **Corrige los 2 errores de sintaxis**. El propio VS Code te marcará con subrayado rojo dónde están los fallos. Al posicionarse encima con el ratón muestra el mensaje de error de sintaxis.

7. **Compila y ejecuta desde el mismo IDE con `Ctrl+F5`**. Aunque también, desde la pestaña inferior `Terminal` que tiene integrada, podéis lanzar, una vez compilado, directamente el programa escribiendo el comando `.\bucle2`.

8. Haz una **captura de pantalla** mostrando la ejecución correcta, con la suma final y el tiempo medido.

---

### Parte 3. Reflexión

Responde:

1. ¿Qué diferencias notaste entre compilar en **CMD** y compilar en el **IDE**?
2. ¿Qué ventajas tiene el IDE a la hora de detectar errores de sintaxis?
3. ¿Qué aporta el IDE frente a un editor simple como Notepad++?
4. ¿En qué casos crees que puede seguir siendo útil un editor simple?
