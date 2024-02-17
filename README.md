# ordenamiento-burbuja
#include <iostream>
using namespace std;

void bubbleSort(int arr[], int n) {
    bool isAscending = true;
    for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                // Intercambio de elementos si están en el orden incorrecto
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
                isAscending = false;
            }
        }
    }
    if (isAscending) {
        cout << "Array ordenado en forma ascendente." << endl;
    } else {
        cout << "Array ordenado en forma descendente." << endl;
    }
}

int main() {
    const int n = 10;
    int arr[n];

    cout << "Ingrese 10 números separados por espacios: ";
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }

    bubbleSort(arr, n);

    cout << "Array ordenado: ";
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;

    return 0;
}
