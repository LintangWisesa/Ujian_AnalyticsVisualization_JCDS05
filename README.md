# Soal Ujian Data Science - Analytics & Visualization

![Lintang_Purwadhika](https://static.wixstatic.com/media/2e6af2_f69a4271c3534ae1869a7ed63e278b2b~mv2.png/v1/fill/w_246,h_39,al_c,usm_0.66_1.00_0.01/2e6af2_f69a4271c3534ae1869a7ed63e278b2b~mv2.png)

#

### **Soal 1 - MySQL World Database**

MySQL secara default menyertakan database ```world``` yang dapat digunakan oleh user untuk mempelajari teknik penggunaan database di MySQL. Database ```world``` merupakan sample real database yang bersumber dari [Statistics Finland](https://www.stat.fi/index_en.html) dan dirilis sekitar awal tahun 2000-an. Database ini berisi 3 buah tabel yang saling berhubungan satu sama lain:

- Tabel ```city``` berisi informasi tentang __4079__ kota di dunia.
- Tabel ```country``` berisi informasi tentang __239__ negara/wilayah yang dianggap sebagai negara di dunia.
- Tabel ```countrylanguage``` berisi informasi tentang bahasa yang digunakan oleh negara-negara di dunia.

*__Soal :__* Aktifkan server MySQL Anda, lalu gunakan database ```world``` dan tuliskan langkah-langkah/query MySQL untuk menyelesaikan perintah di bawah. Anda dilarang membuat database baru, menambah table/data, membuat view atau segala bentuk tindakan yang mengubah struktur database.

1. Tampilkan daftar __10 kota terpadat di Indonesia__. Urutkan data dari kota dengan populasi terbanyak. Kolom yang diwajibkan tampil adalah __id kota__, __nama kota__, __kode negara__, __distrik/provinsi__ dan __populasi__. Output yang diharapkan:

    ```bash
    +-----+----------------+-------------+------------------+------------+
    | ID  | Name           | CountryCode | District         | Population |
    +-----+----------------+-------------+------------------+------------+
    | 939 | Jakarta        | IDN         | Jakarta Raya     |    9604900 |
    | 940 | Surabaya       | IDN         | East Java        |    2663820 |
    | 941 | Bandung        | IDN         | West Java        |    2429000 |
    | 942 | Medan          | IDN         | Sumatera Utara   |    1843919 |
    | 943 | Palembang      | IDN         | Sumatera Selatan |    1222764 |
    | 944 | Tangerang      | IDN         | West Java        |    1198300 |
    | 945 | Semarang       | IDN         | Central Java     |    1104405 |
    | 946 | Ujung Pandang  | IDN         | Sulawesi Selatan |    1060257 |
    | 947 | Malang         | IDN         | East Java        |     716862 |
    | 948 | Bandar Lampung | IDN         | Lampung          |     680332 |
    +-----+----------------+-------------+------------------+------------+
    ```

2. Tampilkan daftar __10 kota terpadat di dunia beserta asal negaranya__. Urutkan data dari kota dengan populasi terbanyak. Kolom yang diwajibkan ada minimal adalah __id kota__, __nama kota__, __distrik/provinsi__, __nama negara__ dan __populasi__. Output yang diharapkan:

    ```bash
    +------+-------------------+------------------+--------------------+------------+
    | id   | nama_kota         | district         | negara             | population |
    +------+-------------------+------------------+--------------------+------------+
    | 1024 | Mumbai (Bombay)   | Maharashtra      | India              |   10500000 |
    | 2331 | Seoul             | Seoul            | South Korea        |    9981619 |
    |  206 | SÃ£o Paulo        | SÃ£o Paulo       | Brazil             |    9968485 |
    | 1890 | Shanghai          | Shanghai         | China              |    9696300 |
    |  939 | Jakarta           | Jakarta Raya     | Indonesia          |    9604900 |
    | 2822 | Karachi           | Sindh            | Pakistan           |    9269265 |
    | 3357 | Istanbul          | Istanbul         | Turkey             |    8787958 |
    | 2515 | Ciudad de MÃ©xico | Distrito Federal | Mexico             |    8591309 |
    | 3580 | Moscow            | Moscow (City)    | Russian Federation |    8389200 |
    | 3793 | New York          | New York         | United States      |    8008278 |
    +------+-------------------+------------------+--------------------+------------+
    ```

3. Tampilkan daftar __10 negara yang tercatat merdeka paling awal__. Daftar negara yang tidak diketahui tahun kemerdekaannya, tidak perlu diikutsertakan. Kolom yang diwajibkan ada minimal adalah __kode negara__, __nama negara__, __benua__, __regional__ dan __tahun merdeka (*Independence Year*)__. Output yang diharapkan:

    ```bash
    +------+----------------+-----------+------------------+---------------+
    | code | name           | continent | region           | tahun_merdeka |
    +------+----------------+-----------+------------------+---------------+
    | CHN  | China          | Asia      | Eastern Asia     |         -1523 |
    | ETH  | Ethiopia       | Africa    | Eastern Africa   |         -1000 |
    | JPN  | Japan          | Asia      | Eastern Asia     |          -660 |
    | DNK  | Denmark        | Europe    | Nordic Countries |           800 |
    | SWE  | Sweden         | Europe    | Nordic Countries |           836 |
    | FRA  | France         | Europe    | Western Europe   |           843 |
    | SMR  | San Marino     | Europe    | Southern Europe  |           885 |
    | GBR  | United Kingdom | Europe    | British Islands  |          1066 |
    | PRT  | Portugal       | Europe    | Southern Europe  |          1143 |
    | AND  | Andorra        | Europe    | Southern Europe  |          1278 |
    +------+----------------+-----------+------------------+---------------+
    ```

4. Tampilkan daftar __benua yang memiliki lebih dari 10 negara di dalamnya__. Kolom yang ditampilkan minimal: __nama benua__, __jumlah negara di dalam benua__, __total populasi__ dan __rata-rata angka harapan hidup (*Life Expectancy*)__ kemudian urutkan dari benua yang memiliki populasi terbanyak. Output yang diharapkan:

    ```bash
    +---------------+---------------+------------+-------------------+
    | Benua         | Jumlah_Negara | Populasi   | Rata_AngkaHrpnHdp |
    +---------------+---------------+------------+-------------------+
    | Asia          |            51 | 3705025700 |          67.44118 |
    | Africa        |            58 |  784475000 |          52.57193 |
    | Europe        |            46 |  730074600 |          75.14773 |
    | North America |            37 |  482993000 |          72.99189 |
    | South America |            14 |  345780000 |          70.94615 |
    | Oceania       |            28 |   30401150 |          69.71500 |
    +---------------+---------------+------------+-------------------+
    ```

5. Tampilkan daftar __negara-negara Asia yang memiliki angka harapan hidup lebih dari rata-rata angka harapan hidup negara-negara Eropa__. Kolom yang diwajibkan ada yaitu __nama negara__, __nama benua__, __angka harapan hidup__ dan **Pendapatan Nasional Bruto/GNP (_Gross National Product_)**. Urutkan data dari negara Asia dengan angka harapan hidup tertinggi. Output yang diharapkan:

    ```bash
    +-----------+-------+-------------------+------------+
    | Nama      | Benua | AngkaHarapanHidup | GNP        |
    +-----------+-------+-------------------+------------+
    | Macao     | Asia  |              81.6 |    5749.00 |
    | Japan     | Asia  |              80.7 | 3787042.00 |
    | Singapore | Asia  |              80.1 |   86503.00 |
    | Hong Kong | Asia  |              79.5 |  166448.00 |
    | Israel    | Asia  |              78.6 |   97477.00 |
    | Jordan    | Asia  |              77.4 |    7526.00 |
    | Cyprus    | Asia  |              76.7 |    9333.00 |
    | Taiwan    | Asia  |              76.4 |  256254.00 |
    | Kuwait    | Asia  |              76.1 |   27037.00 |
    +-----------+-------+-------------------+------------+
    ```

6. Tampilkan daftar __10 negara yang bahasa resminya (_official language_) adalah bahasa Inggris, dan memiliki persentase pengguna bahasa Inggris tertinggi di dunia__. Kolom yang diwajibkan ada yaitu __kode negara__, __nama negara__, __bahasa__, __kolom isOfficial__ dan __percentage__. Urutkan dari persentase pengguna bahasa Inggris tertinggi. Output yang diharapkan:

    ```bash
    +-------------+----------------------+----------+------------+------------+
    | countrycode | name                 | language | isOfficial | percentage |
    +-------------+----------------------+----------+------------+------------+
    | BMU         | Bermuda              | English  | T          |      100.0 |
    | IRL         | Ireland              | English  | T          |       98.4 |
    | GBR         | United Kingdom       | English  | T          |       97.3 |
    | GIB         | Gibraltar            | English  | T          |       88.9 |
    | NZL         | New Zealand          | English  | T          |       87.0 |
    | USA         | United States        | English  | T          |       86.2 |
    | VIR         | Virgin Islands, U.S. | English  | T          |       81.7 |
    | AUS         | Australia            | English  | T          |       81.2 |
    | CAN         | Canada               | English  | T          |       60.4 |
    | BLZ         | Belize               | English  | T          |       50.8 |
    +-------------+----------------------+----------+------------+------------+
    ```

7. Tampilkan daftar __negara ASEAN beserta populasi negaranya, Pendapatan Nasional Bruto/GNP (_Gross National Product_), ibukota & populasi ibukota__. ASEAN (_Association of Southeast Asian Nations_) merupakan sebuah organisasi geo-politik dan ekonomi dari negara-negara di kawasan Asia Tenggara, yang didirikan di Bangkok, 8 Agustus 1967 dengan tujuan untuk meningkatkan pertumbuhan ekonomi, kemajuan sosial, pengembangan kebudayaan negara-negara anggotanya, serta memajukan perdamaian dan stabilitas di tingkat regional. Negara Asia Tenggara yang terdaftar sebagai anggota ASEAN adalah: 

    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/9/9c/Flag_of_Brunei.svg/33px-Flag_of_Brunei.svg.png' alt='lintang' style='height:13px; width:18px'/> Brunei
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Flag_of_Cambodia.svg/33px-Flag_of_Cambodia.svg.png' alt='lintang' style='height:13px; width:18px'/> Cambodia
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/2/26/Flag_of_East_Timor.svg/33px-Flag_of_East_Timor.svg.png' alt='lintang' style='height:13px; width:18px'/> East Timor
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/9/9f/Flag_of_Indonesia.svg/33px-Flag_of_Indonesia.svg.png' alt='lintang' style='height:13px; width:18px'/> Indonesia
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/5/56/Flag_of_Laos.svg/33px-Flag_of_Laos.svg.png' alt='lintang' style='height:13px; width:18px'/> Laos
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/6/66/Flag_of_Malaysia.svg/33px-Flag_of_Malaysia.svg.png' alt='lintang' style='height:13px; width:18px'/> Malaysia
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/8/8c/Flag_of_Myanmar.svg/33px-Flag_of_Myanmar.svg.png' alt='lintang' style='height:13px; width:18px'/> Myanmar
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Flag_of_the_Philippines.svg/33px-Flag_of_the_Philippines.svg.png' alt='lintang' style='height:13px; width:18px'/> Philippines
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Flag_of_Singapore.svg/33px-Flag_of_Singapore.svg.png' alt='lintang' style='height:13px; width:18px'/> Singapore 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/a/a9/Flag_of_Thailand.svg/33px-Flag_of_Thailand.svg.png' alt='lintang' style='height:13px; width:18px'/> Thailand
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/2/21/Flag_of_Vietnam.svg/33px-Flag_of_Vietnam.svg.png' alt='lintang' style='height:13px; width:18px'/> Vietnam
    
    Tampilkan daftar __negara ASEAN beserta populasi negaranya, Pendapatan Nasional Bruto/GNP (_Gross National Product_), ibukota & populasi ibukota__, dengan kolom yang diwajibkan ada yaitu __nama negara__, __populasi negara__, __pendapatan nasional bruto (GNP)__, __nama ibukota__ dan __populasi ibukota__. Urutkan berdasarkan abjad nama negara. Output yang diharapkan:

    ```bash
    +--------------+-----------------+-----------+---------------------+------------------+
    | Negara_ASEAN | Populasi_Negara | GNP       | Ibukota             | Populasi_Ibukota |
    +--------------+-----------------+-----------+---------------------+------------------+
    | Brunei       |          328000 |  11705.00 | Bandar Seri Begawan |            21484 |
    | Cambodia     |        11168000 |   5121.00 | Phnom Penh          |           570155 |
    | East Timor   |          885000 |      0.00 | Dili                |            47900 |
    | Indonesia    |       212107000 |  84982.00 | Jakarta             |          9604900 |
    | Laos         |         5433000 |   1292.00 | Vientiane           |           531800 |
    | Malaysia     |        22244000 |  69213.00 | Kuala Lumpur        |          1297526 |
    | Myanmar      |        45611000 | 180375.00 | Rangoon (Yangon)    |          3361700 |
    | Philippines  |        75967000 |  65107.00 | Manila              |          1581082 |
    | Singapore    |         3567000 |  86503.00 | Singapore           |          4017733 |
    | Thailand     |        61399000 | 116416.00 | Bangkok             |          6320174 |
    | Vietnam      |        79832000 |  21929.00 | Hanoi               |          1410000 |
    +--------------+-----------------+-----------+---------------------+------------------+
    ```

8. Tampilkan daftar __negara G20 beserta populasi negaranya, Pendapatan Nasional Bruto/GNP (_Gross National Product_), ibukota & populasi ibukota__. G20 merupakan kelompok 19 negara dengan perekonomian besar di dunia, ditambah dengan Uni Eropa, yang dibentuk sejak 1999 sebagai forum untuk mendiskusikan berbagai masalah kunci di bidang ekonomi dunia. Negara yang terdaftar sebagai anggota G20 adalah: 

    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/1/1a/Flag_of_Argentina.svg/35px-Flag_of_Argentina.svg.png' alt='lintang' style='height:13px; width:18px'/> Argentina 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/8/88/Flag_of_Australia_%28converted%29.svg/35px-Flag_of_Australia_%28converted%29.svg.png' alt='lintang' style='height:13px; width:18px'/> Australia 
    - <img src='https://upload.wikimedia.org/wikipedia/en/thumb/0/05/Flag_of_Brazil.svg/33px-Flag_of_Brazil.svg.png' alt='lintang' style='height:13px; width:18px'/> Brazil 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/d/d9/Flag_of_Canada_%28Pantone%29.svg/35px-Flag_of_Canada_%28Pantone%29.svg.png' alt='lintang' style='height:13px; width:18px'/> Canada 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/f/fa/Flag_of_the_People%27s_Republic_of_China.svg/35px-Flag_of_the_People%27s_Republic_of_China.svg.png' alt='lintang' style='height:13px; width:18px'/> China 
    - <img src='https://upload.wikimedia.org/wikipedia/en/thumb/c/c3/Flag_of_France.svg/35px-Flag_of_France.svg.png' alt='lintang' style='height:13px; width:18px'/> France 
    - <img src='https://upload.wikimedia.org/wikipedia/en/thumb/b/ba/Flag_of_Germany.svg/35px-Flag_of_Germany.svg.png' alt='lintang' style='height:13px; width:18px'/> Germany 
    - <img src='https://upload.wikimedia.org/wikipedia/en/thumb/4/41/Flag_of_India.svg/35px-Flag_of_India.svg.png' alt='lintang' style='height:13px; width:18px'/> India 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/9/9f/Flag_of_Indonesia.svg/35px-Flag_of_Indonesia.svg.png' alt='lintang' style='height:13px; width:18px'/> Indonesia 
    - <img src='https://upload.wikimedia.org/wikipedia/en/thumb/0/03/Flag_of_Italy.svg/35px-Flag_of_Italy.svg.png' alt='lintang' style='height:13px; width:18px'/> Italia 
    - <img src='https://upload.wikimedia.org/wikipedia/en/thumb/9/9e/Flag_of_Japan.svg/35px-Flag_of_Japan.svg.png' alt='lintang' style='height:13px; width:18px'/> Japan 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/f/fc/Flag_of_Mexico.svg/35px-Flag_of_Mexico.svg.png' alt='lintang' style='height:13px; width:18px'/> Mexico 
    - <img src='https://upload.wikimedia.org/wikipedia/en/thumb/f/f3/Flag_of_Russia.svg/35px-Flag_of_Russia.svg.png' alt='lintang' style='height:13px; width:18px'/> Russian Federation 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/0/0d/Flag_of_Saudi_Arabia.svg/35px-Flag_of_Saudi_Arabia.svg.png' alt='lintang' style='height:13px; width:18px'/> Saudi Arabia 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/Flag_of_South_Africa.svg/35px-Flag_of_South_Africa.svg.png' alt='lintang' style='height:13px; width:18px'/> South Africa 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/0/09/Flag_of_South_Korea.svg/35px-Flag_of_South_Korea.svg.png' alt='lintang' style='height:13px; width:18px'/> South Korea 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/b/b4/Flag_of_Turkey.svg/35px-Flag_of_Turkey.svg.png' alt='lintang' style='height:13px; width:18px'/> Turkey
    - <img src='https://upload.wikimedia.org/wikipedia/en/thumb/a/ae/Flag_of_the_United_Kingdom.svg/35px-Flag_of_the_United_Kingdom.svg.png' alt='lintang' style='height:13px; width:18px'/> United Kingdom 
    - <img src='https://upload.wikimedia.org/wikipedia/en/thumb/a/a4/Flag_of_the_United_States.svg/35px-Flag_of_the_United_States.svg.png' alt='lintang' style='height:13px; width:18px'/> United States
    
    Tampilkan daftar __negara G20 beserta populasi negaranya, Pendapatan Nasional Bruto/GNP (_Gross National Product_), ibukota & populasi ibukota__, dengan kolom yang diwajibkan ada yaitu __nama negara__, __populasi negara__, __pendapatan nasional bruto (GNP)__, __nama ibukota__ dan __populasi ibukota__. Urutkan berdasarkan abjad nama negara. Output yang diharapkan:

    ```bash
    +--------------------+-----------------+------------+-------------------+------------------+
    | Negara_G20         | Populasi_Negara | GNP        | Ibukota           | Populasi_Ibukota |
    +--------------------+-----------------+------------+-------------------+------------------+
    | Argentina          |        37032000 |  340238.00 | Buenos Aires      |          2982146 |
    | Australia          |        18886000 |  351182.00 | Canberra          |           322723 |
    | Brazil             |       170115000 |  776739.00 | BrasÃ­lia          |          1969868 |
    | Canada             |        31147000 |  598862.00 | Ottawa            |           335277 |
    | China              |      1277558000 |  982268.00 | Peking            |          7472000 |
    | France             |        59225700 | 1424285.00 | Paris             |          2125246 |
    | Germany            |        82164700 | 2133367.00 | Berlin            |          3386667 |
    | India              |      1013662000 |  447114.00 | New Delhi         |           301297 |
    | Indonesia          |       212107000 |   84982.00 | Jakarta           |          9604900 |
    | Japan              |       126714000 | 3787042.00 | Tokyo             |          7980230 |
    | Mexico             |        98881000 |  414972.00 | Ciudad de MÃ©xico |          8591309 |
    | Russian Federation |       146934000 |  276608.00 | Moscow            |          8389200 |
    | Saudi Arabia       |        21607000 |  137635.00 | Riyadh            |          3324000 |
    | South Africa       |        40377000 |  116729.00 | Pretoria          |           658630 |
    | South Korea        |        46844000 |  320749.00 | Seoul             |          9981619 |
    | Turkey             |        66591000 |  210721.00 | Ankara            |          3038159 |
    | United Kingdom     |        59623400 | 1378330.00 | London            |          7285000 |
    | United States      |       278357000 | 8510700.00 | Washington        |           572059 |
    +--------------------+-----------------+------------+-------------------+------------------+
    ```

    ✅ _Lampirkan jawaban berupa daftar query MySQL dalam bentuk file __.txt__ dan kirimkan via email ke _lintang@purwadhika.com_!_

#

### **Soal 2 - Infografis ASEAN**

Sama seperti soal pertama, soal kedua kali ini masih menggunakan database ```world``` MySQL dan berfokus pada data negara-negara yang tergabung dalam __ASEAN (_Association of Southeast Asian Nations_)__. Aktifkan server MySQL Anda, lalu gunakan database ```world``` dan selesaikan beberapa soal berikut. Anda dilarang membuat database baru, menambah table/data, membuat view atau segala bentuk tindakan yang mengubah struktur database.

1. __Populasi ASEAN__

    Buatlah sebuah __file python__ yang dapat mengakses daftar negara ASEAN dari database ```world``` dan menampilkan populasi negara-negara ASEAN dalam bentuk diagram batang. Output yang diharapkan berupa __diagram batang__ dengan __nilai/jumlah populasi tertera__ di atas diagram. Style, desain & warna tidak harus sama, utamakan validitas data:

    ![populasi ASEAN](./populasiASEAN.png)

#

2. __Persentase Populasi ASEAN__

    Buatlah sebuah __file python__ yang dapat mengakses daftar negara ASEAN dari database ```world``` dan menampilkan persentase populasi negara-negara ASEAN dalam bentuk diagram lingkaran. Output yang diharapkan berupa __diagram lingkaran__ dengan __nilai persentase populasi tertera__ dalam diagram. Style, desain & warna tidak harus sama, utamakan validitas data:

    ![persen populasi ASEAN](./persenPopASEAN.png)

#

3. __Gross National Product ASEAN__

    Buatlah sebuah __file python__ yang dapat mengakses daftar negara ASEAN dari database ```world``` dan menampilkan Pendapatan Bruto Nasional/GNP (Gross National Product) negara-negara ASEAN dalam bentuk diagram batang. Output yang diharapkan berupa __diagram batang__ dengan __nilai GNP tertera__ di atas diagram. Style, desain & warna tidak harus sama, utamakan validitas data:

    ![GNP ASEAN](./gnpASEAN.png)

#

4. __Persentase Luas Daratan ASEAN__

    Buatlah sebuah __file python__ yang dapat mengakses daftar negara ASEAN dari database ```world``` dan menampilkan persentase luas daratan negara-negara ASEAN dalam bentuk diagram lingkaran. Output yang diharapkan berupa __diagram lingkaran__ dengan __nilai persentase luas daratan tertera__ dalam diagram. Style, desain & warna tidak harus sama, utamakan validitas data:

    ![persen luas daratan ASEAN](./persenLuasASEAN.png)

    ✅ *Commit & push source code jawaban soal ini ke __Github__ Anda, buatlah repo dengan nama __Infografis_ASEAN__, kemudian lampirkan __url link repo Github__ Anda via email ke _lintang@purwadhika.com!_*

#

### **Soal 3 - Cari Pokemon**

Buatlah sebuah __aplikasi Flask__ yang dapat memfasilitasi user untuk mencari data __Pokemon__ dengan nama tertentu, memanfaatkan __Poke API__ ([_klik sini_](https://pokeapi.co/)). API endpoint yang digunakan adalah __GET__ ke https://pokeapi.co/api/v2/pokemon/{nama_Pokemon}. Aplikasi yang dibuat harus memenuhi syarat minimal berikut:

1. Server aplikasi akan berjalan di __localhost:5000__ dan ketika user melakukan GET request via browser akan tampil sebuah halaman __HTML__ sederhana yang memuat __1 buah text input__ dan __1 buah button__. Desain tampilan HTML tidak harus sama seperti contoh soal, utamakan fitur!

    ![poke_1](./poke_1.png)

2. User dapat memasukkan nama Pokemon yang dicari ke dalam text input yang sudah disediakan. Saat user menekan tombol button, aplikasi akan mengambil data Pokemon yang dicari via Poke API: __GET__ ke https://pokeapi.co/api/v2/pokemon/{nama_Pokemon}.

    ![poke_2](./poke_2.png)

3. Jika data ditemukan, maka user akan di-redirect ke __localhost:5000/hasil__ yang berisi halaman __HTML__, yang menampilkan data seputar Pokemon yang dicari. Data yang ditampilkan hanya: __nama Pokemon__, __gambar depan Pokemon__, __nomor id Pokemon__, __tinggi badan Pokemon__ & __berat badan Pokemon__. Halaman ini juga dilengkapi __1 buah button__ untuk kembali ke halaman awal. Desain tampilan HTML tidak harus sama seperti contoh soal, utamakan fitur!

    ![poke_3](./poke_3a.png)

    ![poke_3](./poke_3b.png)

4. Namun jika data tidak ditemukan atau tidak ada di dalam database Poke API, maka user akan di-redirect ke halaman __HTML__ yang memberikan informasi bahwa data tidak ditemukan. Halaman ini juga dilengkapi __1 buah button__ untuk kembali ke halaman awal. Desain tampilan HTML tidak harus sama seperti contoh soal, utamakan fitur!

    ![poke_4](./poke_4.png)

    _**Catatan:**_

    ⚠ Poke API memiliki batasan __100 API request per IP address per menit__. Jika Anda mengalami kendala dikarenakan telah mencapai limit, maka tunggulah sejenak beberapa menit, lalu coba call API kembali.

    ✅ _Commit & push source code jawaban soal ini ke __Github__ Anda, buatlah repo dengan nama __Ujian_Cari_Pokemon__, kemudian lampirkan __url link repo Github__ Anda via email ke lintang@purwadhika.com!_

#

### *__#HappyCoding__* :relaxed:

#### Lintang Wisesa :love_letter: _lintangwisesa@ymail.com_

[Facebook](https://www.facebook.com/lintangbagus) | 
[Twitter](https://twitter.com/Lintang_Wisesa) |
[Google+](https://plus.google.com/u/0/+LintangWisesa1) |
[Youtube](https://www.youtube.com/user/lintangbagus) | 
:octocat: [GitHub](https://github.com/LintangWisesa) |
[Hackster](https://www.hackster.io/lintangwisesa)