
1. 安裝 CRF++ 套件：
```
$ git clone https://github.com/mhbai/CRFPP
$ cd CRFPP
$ ./configure
$ make 
$ sudo make install
```

2. 設定 so library 管理，使新安裝的 CRF++ 能被找到：
```
$ sudo vi /etc/ld.so.conf.d/local.conf
/usr/local/lib
```

```
$ sudo ldconfig -v
```

3. 安裝 CRF++ 的 python 套件

要注意使用哪一個 python 版本，如果是安裝到系統的 python
，要先切換成 root 帳號。如果是 anaconda ，則是要先切換
到正確的版本，再執行下列的安裝指令。
```
$ cd CRFPP/python
$ python setup.py build
$ pip install .
```
