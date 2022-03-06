#include <stdio.h>

void bubbleSort(int arr[], int n){
  int i, j, tmp;
  for(i = 0; i < n; i++){
    for(j=0; j < n-i-1; j ++){
      if(arr[j] > arr[j+1]){
        tmp = arr[j];
        arr[j] = arr[j+1];
        arr[j+1] = tmp;
      }
    }
  }
}

int main() {
  int array[100], n, i, j;
  printf("Masukkan banyak elemen: ");
  scanf("%d", &n);
 
 printf("Masukkan nilai: \n");
  
  for(i = 0; i < n; i++){
    scanf("%d", &array[i]);
  }
  
  bubbleSort(array, n);
  
  printf("Hasil pengurutan sebagai berikut:\n");
  for(i = 0; i < n; i++){
    printf("%d ", array[i]);
  }
  printf("\n");
}

int selectionSort(int arr[], int n){
  int i, j, posisi, swap;
  for(i = 0; i < (n-1); i++){
    posisi = i;
    for (j = i + 1; j < n; j++){
      if(arr[posisi] > arr[j]){
        posisi = j;
      }
    }
    if(posisi != i){
      swap = arr[i];
      arr[i] = arr[posisi];
      arr[posisi] = swap;
    }
  }
}

int main(){
  int array[100], n, i, j;
  
  printf("Masukkan banyaknya jumlah data: ");
  scanf("%d", &n);
  
  printf("Masukkan data sebanyak %d :\n", n);
  for(i = 0; i < n; i++){
    scanf("%d", &array[i]);
  }
  selectionSort(array, n);
  
  printf("Hasil pengurutan sebagai berikut:\n");
  for(i = 0; i < n; i++){
    printf("%d ", array[i]);
  }
  printf("\n");
}

int main(){
  int n, array[100], i, j, tmp;
  
  printf("Masukkan jumlah banyaknya data: ");
  scanf("%d", &n);
  
  printf("Masukkan %d angka integer\n", n);
  
  for(i = 0; i < n; i++){
    scanf("%d", &array[i]);
  }
  
  for (i = 1; i <= n; i++){
    j = i;
    while(j > 0 && array[j-1] > array[j]){
      tmp = array[j];
      array[j] = array[j-1];
      array[j-1] = tmp;
      
      j--;
    }
  }
  
  printf("Hasil pengurutan sebagai berikut:\n");
  
  for (i = 0; i <= n-1; i++){
    printf("%d ", array[i]);
  }
  printf("\n");
  
  return 0;
}
