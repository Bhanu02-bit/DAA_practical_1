#include <iostream>
#include <vector>
using namespace std;

void insertionSort(vector<int>& arr) {
    int n = arr.size();
    for (int i = 1; i < n; i++) {
        int key = arr[i]; // Value to place in sorted sequence
        int j = i - 1;

        
}

int main() {
    vector<int> arr = {12, 11, 13, 5, 6};

    cout << "Unsorted array: ";
    for (int x : arr) cout << x << " ";
    cout << "\n";

    insertionSort(arr);

    cout << "Sorted array (Insertion Sort): ";
    for (int x : arr) cout << x << " ";
    cout << "\n";

    return 0;
}
