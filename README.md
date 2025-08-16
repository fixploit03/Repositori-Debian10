# Repositori Debian 10

Cara Memperbaiki Repositori Debain 10

1. Masuk kedalam user root:

   ```
   su
   ```
   
2. Backup terlebih dahulu repositori default debiannya:

   ```
   cp /etc/apt/sources.list /etc/apt/sources.list.back
   ```
   
3. Ganti repositorinya:

   ```
   cat sources.list > /etc/apt/sources.list
   ```

4. Tambahkan kunci GPG jika terjadi error:

   ```
   apt-key adv --keyserver keyserver.ubuntu.com --recv-keys \
   605C66F00D6C9793 0E98404D386FA1D9 648ACFD622F3D138 \
   648ACFD622F3D138 0E98404D386FA1D9 DCC9EFBF77E11517 \
   6ED0E7B82643E131 112695A0E562B32A 54404762BBB6E853
   ```

5. Coba update dan upgrade repositorinya:

   ```
   apt-get update && apt-get upgrade
   ```
