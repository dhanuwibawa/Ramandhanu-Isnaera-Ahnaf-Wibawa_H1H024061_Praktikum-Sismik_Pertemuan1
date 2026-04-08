void loop() {
  // LED kiri
  for (int i = 2; i <= 4; i++) {
    digitalWrite(i, HIGH);
  }
  delay(500);

  for (int i = 2; i <= 4; i++) {
    digitalWrite(i, LOW);
  }

  // LED kanan
  for (int i = 5; i <= 7; i++) {
    digitalWrite(i, HIGH);
  }
  delay(500);

  for (int i = 5; i <= 7; i++) {
    digitalWrite(i, LOW);
  }
}

Penjelasan:
Program ini membagi LED menjadi dua kelompok, yaitu kelompok kiri dan kelompok kanan. Pada tahap pertama, LED di sisi kiri dinyalakan secara bersamaan, kemudian dimatikan. Setelah itu, LED di sisi kanan dinyalakan dan dimatikan. Proses ini dilakukan secara berulang sehingga menghasilkan pola nyala bergantian antara kedua sisi.
