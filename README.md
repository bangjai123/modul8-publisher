# Reflection
## Understanding publisher and messagebroker.

1. Dalam sekali run, akan ada 5 data yang dikirim publisher ke message broker. Hal ini dapat kita lihat dari jumlah `publish_event` yang ada pada fungsi main
2. Dengan kedua program memiliki link yang sama, artinya keduanya akan terhubung ke broker AMQP yang sama, menggunakan _credentials, host_, dan _port_ yang sama. Dengan demikian, keduanya akan terkoneksi dan dapat melakukan komunikasi satu sama lain secara efektif

## Running RabbitMQ as message broker

![image](https://github.com/bangjai123/modul8-publisher/assets/120235144/2c907132-ee16-4880-9810-a0e32da8e229)

