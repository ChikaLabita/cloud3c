~

Rangkuman - Materi 2

Layanan Cloud Computing

Cloud Computing dikategorikan menjadi 3 : 
- SaaS (Software as a Service)
- PaaS (Platform as a Service)
- IaaS (Infrastructure as a Service)

Oracle Cloud Infrastructure (OCI) Core Services :

OCI Core Services meliputi 5 hal :
1. Compute -> terdapat 5 Komponen yaitu :
	- Bare metal : blank server sehingga pengguna harus menangani virtualisasi, operating system, language runtime, app container dan code.
	- Dedicated virtual host : single tenant model
	atau tidak ada resource yang akan dibagi dengan pengguna lain dan layer virtualisasi ditangani oleh Oracle. 
	- Virtual machines : multitenant model dengan virtualisasi berbasis hypervisor, yang berbeda dengan dedicated virtual hosts adalah berbagi resource dengan pengguna yang lain.
	- Container engine : dapat melakukan setup pada app container dan code aplikasi. Container runtime environment yang mengeksekusi Containers dan mengelola Container Image pada node. 
	- Function : layanan yang memungkinkan pengguna hanya menulis code.

		#catatan_kecil : 
 		Oracle -> membayar sesuai dengan resource yang digunakan ketika mengeksekusi code.
2. Storage(Penyimpanan)
	^^Storage Model OCI, yaitu:
		- Mendukung persistent and non persistent storage
		- Multiple format seperti data terstruktur, semi-terstruktur dan streaming
		- High Performance Computing dengan biaya yang rendah
		- Data dilindungi dari kerusakan perangkat keras
		- Data dapat disimpan di lokal untuk keperluan sendiri atau di remote storage untuk keperluan berbagi data
		- Data diakses menggunakan protokol tertentu
	^^Storage Services (Layanan Penyimpanan)
		- Block Volume : 
			*Digunakan ketika mendeploy SAN (Storage Area Network)
			*Menggunakan low latency NVME SSD
			*Secara otomatis direplikasi untuk menghindari kehilangan data
			*dsb
		- Local NVMW
			*NVME storage merupakah penyimpanan non-persistent (data hilang ketika direboot) sehingga perlu dibackup menggunakan RAID. RAID yang dapat digunakan pada OCI ada 3 macam yaitu RAID 1, RAID 10 dan RAID 6.
		- File Storage
			*Mendukung distributed file system seolah-olah seperti local file system
			*Mendukung 2 sistem file yaitu NFS (Network File System) dan SMB (Server Message Block). Dapat digunakan pada Windows dan Unix.
			*Dapat diakses melalui jaringan, pada umumnya tidak
			memerlukan software tambahan.
		- Object Storage
			*Semua data dikelola seperti object sehingga dapat menyimpan data apapun sesuai format aslinya.
			*Dapat digunakan untuk menyimpan data yang berasal dari banyak sumber yang berguna untuk analisa, backup, atau arsip (archive)
		- Archive Storage
			*Terdiri dari 2 tier yaitu : 
				1) Standard Storage Tier (Hot)
					-Cepat, segera dan sering diakses.
					-Standard bucket tidak dapat didowngrade ke archive storage.
					-dsb
				2) Archive Storage Tier (Cold)
					-Jarang diakses tetapi data tetap harus disimpan untuk jangka waktu yang lama.
					-Data minimum disimpan 90 hari
					-Object harus direstore sebelum didownload
					-Tidak dapat diupgrade menjadi standard tier.
					-dsb
3. Networking
	Virtual Cloud Network -> layanan Infrastructures as a Service (IaaS). VCN memungkinkan pengguna untuk mengatur jaringan yang ada di lingkungan cloud.

	Manfaat Virtual Cloud Network ( VCN ) yaitu: 
	a. Untuk memperluas jaringan lokal ke Oracle Cloud.
	b. Meningkatkan keamanan pada jaringan VM.
	c. Mengatur lalu lintas data yang masuk dan juga keluar.

	Komponen-komponen dalam VCN :
	a. Subnets
	b. Route Table
	c. Security List
	d. Internet Gateway
	e. Nat Gateway
	f. Service Gateway
	g. Dynamic Router Gateway

4. Identity and Access Management (IAM)
	->IAM policy adalah dokumen yang menentukan siapa dan bagaimana cara yang dapat digunakan untuk mengakses sumber daya.
	->Compartment adalah kumpulan resource yang saling terkait yang membantu Anda untuk menentukan akses ke resources yang anda miliki.

5. Database Cloud Service
	Oracle adalah satu-satunya cloud publik yang mendukung sistem database VM, yang menawarkan penyediaan yang sangat cepat.
	OCI menawarkan sistem Exadata DB, yang menawarkan kinerja ekstrem baik untuk Online Transaction Processing (OLTP) maupun aplikasi pergudangan data.

	Layanan Oracle Autonomous Database
		*^ membebaskan administrator database dari tugas operasional yang bahkan ketika database sudah dideploy di cloud. Tugas-tugas ini mencakup journaling functions, keamanan database, dan pemecahan masalah (troubleshooting).
~