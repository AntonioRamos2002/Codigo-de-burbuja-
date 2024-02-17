#include <iostream>

using namespace std;

// Función para ordenar un arreglo utilizando el algoritmo de burbuja
void bubbleSort(int arreglo[], int n) {
    for (int i = 0; i < n - 1; ++i) {
        for (int j = 0; j < n - i - 1; ++j) {
            if (arreglo[j] > arreglo[j + 1]) {
                // Intercambiar elementos si están en el orden incorrecto
                int temp = arreglo[j];
                arreglo[j] = arreglo[j + 1];
                arreglo[j + 1] = temp;
            }
        }
    }
}

int main() {
    int arreglo[] = {64, 34, 25, 12, 22, 11, 90};
    int n = sizeof(arreglo) / sizeof(arreglo[0]);

    cout << "Arreglo original:\n";
    for (int i = 0; i < n; ++i) {
        cout << arreglo[i] << " ";
    }
    cout << endl;

    bubbleSort(arreglo, n);

    cout << "Arreglo ordenado:\n";
    for (int i = 0; i < n; ++i) {
        cout << arreglo[i] << " ";
    }
    cout << endl;

    return 0;
}
