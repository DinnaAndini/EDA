# Exploratory Data Analysis
## 1. Load Data
"Load data" pada Python berarti membaca atau mengambil data dari sumber eksternal (seperti kaggle, BPS, satudata, dll) ke dalam program Python agar dapat digunakan atau dianalisis lebih lanjut. Ini biasanya dilakukan dengan menggunakan pustaka atau modul tertentu seperti pandas untuk bekerja dengan data berbentuk tabel, seperti CSV atau Excel.

contoh :

input
```sh
import pandas as pd
df = pd.read_csv("C:/Users/ACER/Downloads/Spotify Most Streamed Songs.csv")
df
```
Dari contoh diatas, kita tahu, bahwa dengan menggunakan library pandas, kita bisa membaca file CSV menggunakan python.

## 2. Basic Information about the Dataset
input
```sh
df.head()
```
```sh
df.tail()
```
Dengan menggunakan 'df.head()' dan 'df.tail(), kita dapat mengetahui 5 informasi teratas dan terbawah dari file diatas.

input
```sh
df.info()
```
Dengan menggunakan 'df.info()', kita dapat mengetahui tipe data dari dataset yang sedang diekplorasi.

input
```sh
df.describe()
```
Dengan menggunakan 'df.describe()', kita dapat mengetahui statistika deskriptif dari dataset tersebut.

## 3. Cek Nilai Duplikat dan Nilai Unik
##### Nilai Duplikat
Untuk mengetahui dalam dataset tersebut ada nilai duplikatnya atau tidak, kita bisa menggunakan metode 'df.duplicated().sum()'.

input
```sh
duplikat = df.duplicated().sum()
print(duplikat)
```
output
```sh
0
```
Dari output diatas kita dapat mengetahui bahwa dataset tersebut tidak memiliki nilai duplikat.
##### Nilai Unik
input
```sh
unik = df.nunique()
print(unik)
```
output
```sh
track_name              943
artist(s)_name          645
artist_count              8
released_year            50
released_month           12
released_day             31
in_spotify_playlists    879
in_spotify_charts        82
streams                 949
in_apple_playlists      234
in_apple_charts         172
in_deezer_playlists     348
in_deezer_charts         34
in_shazam_charts        198
bpm                     124
key                      11
mode                      2
danceability_%           72
valence_%                94
energy_%                 80
acousticness_%           98
instrumentalness_%       39
liveness_%               68
speechiness_%            48
cover_url               535
dtype: int64
```

##### 4. Visualisasi Jumlah Nilai Unik
input
```sh
unik.plot(kind='hist')
```
output
```sh
<Axes: ylabel='Frequency'>
```
![image](https://github.com/user-attachments/assets/6d0b7c76-4236-4a4f-8b35-41697cab4e91)

