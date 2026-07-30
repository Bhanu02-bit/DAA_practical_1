#include <iostream>
#include <vector>
using namespace std;

int partition(vector<int>& arr, int low, int high) {
    int pivot = arr[high]; // Last element chosen as pivot
    int i = low - 1;

    for (int j = low; j < high; j++) {
        if (arr[j] < pivot) {
            i++;
            swap(arr[i], arr[j]);
        }
    }
    swap(arr[i + 1], arr[high]); // Place pivot in right location
    return i + 1;
}

void quickSort(vector<int>& arr, int low, int high) {
    if (low < high) {
        int pi = partition(arr, low, high); // Partition index
        quickSort(arr, low, pi - 1);       // Sort left partition
        quickSort(arr, pi + 1, high);      // Sort right partition
    }
}

int main() {
    vector<int> arr = {10, 7, 8, 9, 1, 5};

    cout << "Unsorted array: ";
    for (int x : arr) cout << x << " ";
    cout << "\n";

    quickSort(arr, 0, arr.size() - 1);

    cout << "Sorted array (Quick Sort): ";
    for (int x : arr) cout << x << " ";
    cout << "\n";

    return 0;
}
