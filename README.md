# Reflection
## Understanding publisher and messagebroker.

1. Dalam sekali run, akan ada 5 data yang dikirim publisher ke message broker. Hal ini dapat kita lihat dari jumlah `publish_event` yang ada pada fungsi main
2. Dengan kedua program memiliki link yang sama, artinya keduanya akan terhubung ke broker AMQP yang sama, menggunakan _credentials, host_, dan _port_ yang sama. Dengan demikian, keduanya akan terkoneksi dan dapat melakukan komunikasi satu sama lain secara efektif

## Running RabbitMQ as message broker
![image](https://github.com/bangjai123/modul8-publisher/assets/120235144/2c907132-ee16-4880-9810-a0e32da8e229)

## Sending and processing event.
![image](https://github.com/bangjai123/modul8-publisher/assets/120235144/f03d2487-5f73-472a-abf6-3220cbdc1dd3)

Pada gambar di atas, dapat kita lihat bahwa publisher melakukan pengiriman event dan diterima oleh message broker yang kemudian diproses oleh subsciber. Lalu, dapat kita lihat bahwa subscriber mengeluarkan message pada console subscriber sebanyak 5 message bahwa event. 

## Monitoring chart based on publisher.
![image](https://github.com/bangjai123/modul8-publisher/assets/120235144/94094dce-3804-4fd3-ac87-01a16a3378eb)

Pada gambar di atas terlihat terdapat dua _spike_ pada grafik _message rates_. Hal ini menggambarkan dua kali _messagge_ yang disebabkan _event_ terjadi. Hal ini dapat terjadi karena saya melakukan perintah cargo run, yang berfungsi untuk menjalankan program, sebanyak dua kali pada _publisher_. Hal ini menyebabkan _event_ terjadi sebanyak dua kali.
