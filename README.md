# KTP NIK Checker


Nomor Induk Kependudukan (NIK) adalah nomor identitas penduduk yang tercantum pada KTP. Namun, NIK terkadang tak tercatat di Dukcapil nasional.


Nomor Induk Kependudukan atau NIK adalah nomor identitas penduduk yang bersifat unik atau khas, tunggal dan melekat pada seseorang yang terdaftar secara khusus sebagai Penduduk Indonesia jika berada di Indonesia. NIK berlaku seumur hidup dan selamanya, yang diberikan oleh Pemerintah dan diterbitkan oleh Instansi Pelaksana kepada setiap Penduduk setelah dilakukan pencatatan biodata. NIK pertama kali diperkenalkan oleh Direktorat Jenderal Administrasi Kependudukan ketika Institusi Pemerintah ini menerapkan sistem KTP nasional yang terkomputerisasi.

NIK terdiri dari 16 digit. Kode penyusun NIK terdiri dari 2 digit awal merupakan kode provinsi, 2 digit setelahnya merupakan kode kota/kabupaten, 2 digit sesudahnya kode kecamatan, 6 digit selanjutnya merupakan tanggal lahir dalam format hhbbtt (untuk wanita tanggal ditambah 40), lalu 4 digit terakhir merupakan nomor urut yang dimulai dari 0001. Sebagai contoh, misalkan seorang perempuan lahir di Kota Bandung tanggal 17 Agustus 1990 maka NIK-nya adalah: 10 50 24 570890 0001. Apabila ada orang lain (perempuan) dengan domisili dan tanggal lahir yang sama mendaftar, maka NIK-nya adalah 10 50 24 570890 0002. Apabila ada orang lain (laki-laki) dengan domisili dan tanggal lahir yang sama mendaftar, maka NIK-nya adalah 10 50 24 170890 0001.

NIK dicantumkan dalam setiap Dokumen Kependudukan dan dijadikan dasar penerbitan KTP, paspor, surat izin mengemudi, nomor pokok wajib pajak, polis asuransi, sertifikat hak atas tanah, dan penerbitan dokumen identitas lainnya.

Menteri Dalam Negeri memastikan NIK ini siap pada 2011 



For Validate KTP Number With Name 
````
import http.client

conn = http.client.HTTPSConnection("nik-checker1.p.rapidapi.com")

payload = "nama=nama%20lengkap&nik=nomer%20ktp"

headers = {
    'x-rapidapi-key': "key",
    'x-rapidapi-host': "nik-checker1.p.rapidapi.com",
    'Content-Type': "application/x-www-form-urlencoded"
}

conn.request("POST", "/valid", payload, headers)

res = conn.getresponse()
data = res.read()

print(data.decode("utf-8"))
````

Surabaya Extract Data KTP

````
import http.client

conn = http.client.HTTPSConnection("nik-checker1.p.rapidapi.com")

payload = "nik=Nik%20Number"

headers = {
    'x-rapidapi-key': "key",
    'x-rapidapi-host': "nik-checker1.p.rapidapi.com",
    'Content-Type': "application/x-www-form-urlencoded"
}

conn.request("POST", "/sby", payload, headers)

res = conn.getresponse()
data = res.read()

print(data.decode("utf-8"))
````

For Extrac Data KTP Indonesia

````
import http.client

conn = http.client.HTTPSConnection("nik-checker1.p.rapidapi.com")

headers = {
    'x-rapidapi-key': "key",
    'x-rapidapi-host': "nik-checker1.p.rapidapi.com"
}

conn.request("GET", "/ktp?no=16%20digit%20nomer%20ktp", headers=headers)

res = conn.getresponse()
data = res.read()

print(data.decode("utf-8"))
````
