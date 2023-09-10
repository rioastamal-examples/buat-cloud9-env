### Menggunakan Cloud IDE AWS Cloud9

AWS Cloud9 adalah IDE berbasis cloud yang menyediakan fitur text editor, akses ke Terminal untuk menjalankan shell dan built-in debugger. Yang diperlukan untuk menjalankan AWS Cloud9 hanyalah web browser.

Pada workshop ini Anda akan menggunakan Cloud9 untuk menjalankan perintah di terminal dan melakukan code editing.

Untuk membuat sebuah environment di Cloud9 ikuti langkah berikut.

1. Masuk ke [AWS Cloud9](https://console.aws.amazon.com/cloud9control/home)
2. Pilih **Create environment**
![AWS Cloud9 - Create environment](https://user-images.githubusercontent.com/469847/224514038-926afe2e-c4bf-4878-9aa4-f24c7655464f.png)
3. Pada **Name** isikan &quot;workshop-{{NICKNAME}}&quot; contoh milik saya **workshop-rioastamal**
4. Pada **Environment type** pilih **New EC2 instance** pada **Instance type** pilih **t3.small**
5. Pada **Platform**, pilih **Amazon Linux 2**, **Timeout** pilih **4 hours**
6. Pada **Network Settings** bagian **Connection** pilih **AWS Systems Manager (SSM)**
7. Biarkan sisanya sesuai nilai bawaan, pilih **Create**

Tunggu beberapa saat hingga proses pembuatan environment selesai. Pilih **Open** di sebelah nama environment yang baru dibuat.

![New Cloud9 IDE Environment](https://user-images.githubusercontent.com/469847/222607823-990285f8-ca16-49e4-8a40-707fed4935d8.png)

Anda akan mendapat tampilan Cloud9. Layout default di sebelah kiri adalah file manager, tengah adalah file editor dan di bawah adalah Terminal window.

![Tampilan AWS Cloud9](https://user-images.githubusercontent.com/469847/222608860-9fcc210e-06a1-4c4d-a897-b5dbf79163c0.png)

> Anda dapat mengubah ukuran masing-masing window pane dengan menggeser pada tepian border. Silahkan tutup Welcome file.

#### Menjalankan Bootstrap Script

Sekarang jalankan perintah berikut di Terminal AWS Cloud9 untuk menginstal beberapa paket yang diperlukan selama workshop.

```sh
curl -s 'https://gist.githubusercontent.com/rioastamal/e0882594e6b34aedf03a56a6efc0b7c0/raw/12af5c42f3468b284accc8222eab70d2a539db12/bootstrap-cloud9-workshop.sh' | bash
```

Cek versi mayor dari AWS CLI harusnya 2.x.y.

```sh
aws --version
```

```
aws-cli/2.11.2 Python/3.11.2 Linux/4.14.305-227.531.amzn2.x86_64 exe/x86_64.amzn.2 prompt/off
```

Cek versi Node harusnya 16.x.y

```sh
node --version
```

```
v16.19.1
```
