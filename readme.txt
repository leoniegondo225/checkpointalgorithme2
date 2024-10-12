function insertionSort(arr) {
  for (let i = 1; i < arr.length; i++) {
    let key = arr[i];
    let j = i - 1;
    
    // Déplacer les éléments de arr[0..i-1], qui sont plus grands que key,
    // d'une position vers la droite pour créer de la place pour key
    while (j >= 0 && arr[j] > key) {
      arr[j + 1] = arr[j];
      j = j - 1;
    }
    arr[j + 1] = key; // Insérer key dans la bonne position
  }
  return arr;
}

// Exemple d'utilisation
let array = [12, 11, 13, 5, 6];
console.log(insertionSort(array));

