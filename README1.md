const int ledPin = 6;
int timeDelay = 1000;
bool modeLambat = false;

void setup() {
  pinMode(ledPin, OUTPUT);
}

void loop() {
  digitalWrite(ledPin, HIGH);
  delay(timeDelay);

  digitalWrite(ledPin, LOW);
  delay(timeDelay);

  if (timeDelay > 200 && modeLambat == false) {
    timeDelay -= 200; // dari lambat ke cepat
  } 
  else if (timeDelay <= 200 && modeLambat == false) {
    modeLambat = true; // ubah arah ke sedang
  } 
  else if (modeLambat == true && timeDelay < 1000) {
    timeDelay += 200; // dari cepat ke sedang/lambat
  } 
  else {
    timeDelay = 1000; // reset
    modeLambat = false;
  }
}
Penjelasan:
Program dimodifikasi dengan menambahkan variabel kontrol untuk mengatur perubahan kecepatan LED. Awalnya LED berkedip dari lambat menuju cepat. Setelah mencapai kecepatan tertentu, program tidak langsung reset, tetapi memperlambat kembali ke kecepatan sedang, kemudian ke lambat, sebelum akhirnya kembali ke kondisi awal. Dengan modifikasi ini, pola perubahan LED menjadi lebih halus dan tidak langsung kembali ke awal.
