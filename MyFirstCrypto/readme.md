
# classical ciphers古典密碼及其破密分析

# 現代密碼  快速入門篇

>* 本課程將主要以openssl來示範現代密碼的加解密
>* OpenSSLhttps://zh.wikipedia.org/wiki/OpenSSL
>* https://www.openssl.org/
>* https://github.com/openssl/openssl

## openssl
```
OpenSSL is a robust, commercial-grade, and full-featured toolkit for the Transport Layer Security (TLS) 
and Secure Sockets Layer (SSL) protocols. 

It is also a general-purpose cryptography library.
```



## 對稱式密碼 symmetric key algorithms  Private-key cryptogra

### DES
```
https://zh.wikipedia.org/wiki/資料加密標準

```
```
DES是一種對稱密鑰加密塊密碼(Block cipher)演算法
1976年被美國聯邦政府國家標準局(NIST)確定為聯邦資料處理標準（FIPS），隨後在國際上廣泛流傳。
```

## 非對稱式密碼 asymmetric key algorithms Public-key cryptography

```
https://en.wikipedia.org/wiki/Public-key_cryptography

RSA
ElGamal
elliptic curve techniques 
```
## RSA
```
RSA加密演算法- 维基百科

https://www.slideshare.net/shafaan/public-key-cryptography-and-rsa

```
### 簡單範例:

步驟一:Key generation(產生key pair)
```
(1)Select primes p=17, q=11
(2)Compute n=pq=187
(3)Compute φ(n)=(p-1)(q-1)=160
(4)Select e=7  ==> GCD(7,160)=1
(5)Compute d: d=23 ==>7*23 mod 160=1 (use the extended Euclid’s algorithm)

公鑰pub={e,n}={7,187}
私鑰pri={d,n}={23,187}
```
步驟二:加密
```
明文M=88
加密(Encrypt): 88^7mod 187
88^7mod 187 =  11(密文C)
```
步驟三:解密
```
解密Decrypt   C=11: 11^23mod 187
M=11^23 mod 187=88
```


# 現代密碼之破密分析[請參加HackingWeekend]