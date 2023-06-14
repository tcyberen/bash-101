```bash
#!/bin/bash

# Bu betik, terminal ekranında girilen bir mesajı dikeyde ortalamak için kullanılır.

cols=$( tput cols )  # Terminal ekranındaki sütun sayısını hesaplar ve "cols" değişkenine atar.
rows=$( tput lines )  # Terminal ekranındaki satır sayısını hesaplar ve "rows" değişkenine atar.
message=$@           # Betiğe geçirilen parametreleri alarak "message" adlı değişkene atar.

# Mesaj uzunluğunu belirler ve yarı uzunluğunu hesaplamak üzere ikiye böler.
input_length=${#message}
half_input_length=$(( $input_length / 2))

# Ekrandaki orta noktanın bulunduğu satır numarasını hesaplar. 
middle_row=$(( $rows / 2))

# Mesajın merkezini sağlamak için gereken boşluk miktarını belirler (yani mesaj nerede görüntüleneceğini belirler).
middle_col=$(( ($cols / 2) - $half_input_length ))

tput clear             # Terminal ekranını temizler.
tput cup $middle_row $middle_col   # Mesajın ekranda nerede görüntüleneceğini belirleyen koordinatları ayarlar.
tput bold              # Kalın karakterler kullanmak için terminale uygun ayarlama yapar.
echo $@                # Girilen mesajı ekrana yazdırır.
tput sgr0              # Terminale eski ayarları geri yüklemek için kullanılır.
tput cup $( tput lines ) 0        # Cursor'u terminalin alt kısmına taşıyarak, sonuçların üst üste binmesini önler ve boşluk bırakmayı sağlar. 
```
