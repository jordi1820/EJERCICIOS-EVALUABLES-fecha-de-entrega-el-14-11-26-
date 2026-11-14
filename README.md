# EJERCICIOS-EVALUABLES-fecha-de-entrega-el-14-11-26-
Ejercicio 3.11
****
++++++++
****
++++++++
****
++++++++
****
++++++++
****
++++++++


Ejercicio 3.12
>>>>>>>>>>
<<<<<<<<<<
>>>>>>>>>>
<<<<<<<<<<
>>>>>>>>>>
<<<<<<<<<<
>>>>>>>>>>
<<<<<<<<<<
>>>>>>>>>>
<<<<<<<<<<


Ejercicio 3.25
#include <iostream>
using namespace std;

int main() {
    int n;
    cout << "Introduce un entero no negativo: ";
    cin >> n;

    long long factorial = 1;
    int i = 1;

    while (i <= n) {
        factorial = factorial * i;
        i++;
    }

    cout << "El factorial es: " << factorial << endl;
    return 0;
}



Ejercicio 3.26
#include <iostream>
using namespace std;

int main() {
    int numero;
    cout << "Introduce un entero de 4 cifras: ";
    cin >> numero;

    int d1 = numero / 1000;
    int d2 = (numero / 100) % 10;
    int d3 = (numero / 10) % 10
    int d4 = numero % 10;

    d1 = (d1 + 7) % 10;
    d2 = (d2 + 7) % 10;
    d3 = (d3 + 7) % 10;
    d4 = (d4 + 7) % 10;

    Intercambiar 1º con 3º, y 2º con 4º
    int temp = d1; d1 = d3; d3 = temp;
    temp = d2; d2 = d4; d4 = temp;

    cout << "Número cifrado: " << d1 << d2 << d3 << d4 << endl;
    return 0;
}



Ejercicio 4.15
#include <iostream>
#include <iomanip>
using namespace std;

int main() {
 double pi = 0.0;
    int terminos = 200000;

    cout <<(10) << "term" << " | " << "pi" << endl;

    for (int i = 1; i <= terminos; ++i) {
        if (i % 2 == 1) {
            pi += 4.0 / (2 * i - 1);
        } else {
            pi -= 4.0 / (2 * i - 1);
        }

        if (i <= 5) {
            cout << setw(10) << i << " | " << fixed << setprecision(8) << pi << endl;
        }
    }
    return 0;
}



Ejercicio 4.6
El programa utiliza dos bucles for. El bucle exterior se ejecuta 9 veces y el interior pone 5 @ por cada fila, seguido de un salto de línea. Por lo tanto, dibuja en la pantalla un rectángulo de caracteres de @ de 9 filas de alto i 5 columnas de ancho.


Ejercicio 4.8
#include <iostream>
using namespace std;

int main() {
    long long producto = 1;

    for (int i = 1; i <= 15; i += 2) {
        producto *= i;
    }

    cout << "El producto de los enteros impares del 1 al 15 es: " << producto << endl;
    return 0;
}



Ejercicio 5.1
Valores de x después de cada instrucción:
a) x = fabs(7.5); →→ 7.5
b) x = floor(7.5); →→ 7.0
c) x = fabs(0.0); →→ 0.0
d) x = ceil(0.0); →→ 0.0
e) x = fabs(-6.4); →→ 6.4
f) x = ceil(-6.4); →→ -6.0
g) x = ceil(-fabs(-8 + floor(-5.5))); →→ -14.0


Ejercicio 5.6
Instrucciones para asignar enteros aleatorios a n:
a) 1≤n≤21≤n≤2: n = rand() % 2 + 1;
b) 1≤n≤1001≤n≤100: n = rand() % 100 + 1;
c) 0≤n≤90≤n≤9: n = rand() % 10;
d) 1000≤n≤11121000≤n≤1112: n = rand() % 113 + 1000;
e) −1≤n≤1−1≤n≤1: n = rand() % 3 - 1;
f) −3≤n≤11−3≤n≤11: n = rand() % 15 - 3;



Ejercicio 5.18 
#include <iostream>
using namespace std;

(int numero) {
    int invertido = 0;
    while (numero > 0) {
        int cifra = numero % 10;
        invertido = invertido * 10 + cifra;
        numero /= 10;
    }
    return invertido;
}

int main() {
    int num = 7631;
    cout << "Original: " << num << " | Invertido: " << invertirCifras(num) << endl;
    return 0;
}



Ejercicio 5.21
#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int flip() {
    return rand() % 2; // 0 para cruz (tails), 1 para cara (heads)
}

int main() {
    srand(time(0));
    int caras = 0, cruces = 0;

    for (int i = 0; i < 100; i++) {
        if (flip() == 1) {
            cout << "Heads" << endl;
            caras++;
        } else {
            cout << "Tails" << endl;
            cruces++;
        }
    }

    cout << "\nCaras: " << caras << " | Cruces: " << cruces << endl;
    return 0;
}



Ejercicio 5.26 
#include <iostream>
using namespace std;

(int n, int origen, int destino, int temporal) {
    if (n == 1) {
        cout << origen << "->" << destino << endl;
        return;
    }
   (n - 1, origen, temporal, destino);
    cout << origen << "->" << destino << endl;
   (n - 1, temporal, destino, origen);
}

int main() {
    int discos = 3; // O el número deseado
    cout << "Movimientos:" << endl;
    (discos, 1, 3, 2);
    return 0;
}
