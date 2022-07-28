## Ini query select seluruh data 

```
SELECT list_data FROM nama_tabel;
```
> SELECT * FROM tb_barang;

## select semua data dengan id = 2

```
SELECT list_data FROM nama_tabel WHERE id = 2;
```
> SELECT * FROM tb_barang WHERE id_barang = 2;

## perintah cari data dengan urutan id lebih dari 1 dari index secara deskending

```
SELECT list_data FROM nama_tabel WHERE id > 1 ORDER BY index_data DESC;
```
> SELECT * FROM tb_barang WHERE id_barang > 1 ORDER BY jumlah DESC;

## penggunaan grub by untuk kedepannya dalam mengelola data yang besar

> SELECT 

>  id_barang, 
>  nama, 
  
>  jumlah, 
  
>  harga
  
> FROM tb_barang

> WHERE id_barang > 1

> GROUP BY id_barang, nama, jumlah, harga 

> ORDER BY harga DESC;
