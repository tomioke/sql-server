## Ini query select data seluruh barang

bash```
SELECT list_data FROM nama_tabel;
```

## select semua data dengan id barang = 2
SELECT * FROM tb_barang WHERE id_barang = 2;

## perintah cari barang dengan urutan id lebih dari 1 dari harga termahal
SELECT * FROM tb_barang WHERE id_barang > 1 ORDER BY jumlah DESC;

## penggunaan grub by untuk kedepannya dalam mengelola data yang besar
SELECT id_barang, nama, jumlah, harga
FROM tb_barang
WHERE id_barang > 1
GROUP BY id_barang, nama, jumlah, harga 
ORDER BY harga DESC;
