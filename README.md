![](img/35cfdead-7acc-4a51-8a93-b8bf6c063d07.png)
# Як роблю аудіокнигу My little Pony: Love?
1. **Першу чергу я заходжу на сайт https://ttsfree.com/**. Для кожних героїв треба писати фразу окремо <br>
Ось приклад: 01_Старлайт.mp3, 02_Дискорд.mp3, 03_Старлайт.mp3, 04_My_little_pony.mp3, 05_Старлайт.mp3
2. Встановлення у Terrmux: <br>
```bash
pkg update && pkg upgrade -y
pkg install git -y
pkg install proot python tur-repo -y
pkg update
pkg install thc-hydra make mandoc -y
pkg install libjpeg-turbo libpng zlib -y
pkg install openssl rust -y
```
3. Встановлення ffmpeg: <br>
```bash
pkg install ffmpeg -y
```
4. Об'єднуємо за допомогою ffmpeg: <br>
```bash
ffmpeg -i "concat:01_Старлайт.mp3|02_Дискорд.mp3|03_Старлайт.mp3|04_My_little_pony.mp3|05_Старлайт.mp3" -acodec copy my_little_pony_love.mp3
```
5. Готовий файл my_little_pony_love.mp3 можна відправити на Telegram.
