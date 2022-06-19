# [2]使用Python標準函式庫進行BASE64的編碼與解碼

###  Python 標準函式庫 (Standard Library)
```
C++ 有強大的標準模板庫(Standard Template Library，STL）

Python也有強大的標準函式庫 (Standard Library)

本課程示範幾個範例,帶你認識Python 標準函式庫

推薦書籍與資源

[1]官方說明
英文 https://docs.python.org/3/library/
中文 https://docs.python.org/zh-tw/3/library/index.html

[2]厚達上千頁的範例示範說明書

The Python 3 Standard Library By Example
Doug Hellmann

https://pymotw.com/3/
https://bitbucket.org/dhellmann/pymotw-3/src/master/
```

## Python 標準函式庫的Base 64 模組
```
What does the 'b' character do in front of a string literal?

https://stackoverflow.com/questions/6269765/what-does-the-b-character-do-in-front-of-a-string-literal
```
### 使用Base 64 模組編碼:b64encode()
```
import base64

data =b'BreakAllCTF{HappyPythonDay}'
encoded_data = base64.b64encode(data)
print('Original Data :', data)
print('Encoded :', encoded_data)
```
### 使用Base 64 模組解碼:b64decode()
```
import base64

encoded_data = b'QnJlYWtBTExDVEZ7NTN1c1pRM2hXVzI1ZGNoWjdkWGV9'
decoded_data = base64.b64decode(encoded_data)
print('Encoded :', encoded_data)
print('Decoded :', decoded_data)
```
### 使用Base 64 模組也可以進行Base 32編碼與解碼
```
import base64

original_data = b'BreakAllCTF{HappyPythonDay}'
print('Original data:', original_data)

encoded_data = base64.b32encode(original_data)
print('Encoded :', encoded_data)

decoded_data = base64.b32decode(encoded_data)
print('Decoded :', decoded_data)
```
### [作業] 使用Pyhon程式解Crytpo 101: Base64及Base32哪兩題
