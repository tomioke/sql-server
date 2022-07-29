## Query offset dan fetch next untuk kecualikan 3 data teratas dan ambil 4 data setelahnya.
> SELECT
	id_barang,
	nama,
	jumlah,
	harga,
	diskon 
FROM tb_barang 
ORDER BY id_barang
OFFSET 3 ROWS 
FETCH NEXT 4 ROWS ONLY;
