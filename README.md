Docker Composo ile çalıştırmak için

1. önce client klasörüne git
2 npm run build ile react projesini oluştur. wwwroot içerisinde oluşur. 
3. daha sonra proje ana dizinine çık ve docker compose up komutunu ver. bu konteynerleri oluşturu ve projeyi çalıştırır. env dosyası localhost adresi var. kontrol et. gerekirse düzelt baştan başla.
4. bazen compose içerisinde api postgresden sonra değil önce başlıyor. bu durumda api conteynerini durdur tekrar başlat. diğerlerine gerek yok.



Docker Compose olmadan.

1. aşağıdaki komutla bir postgres konteyneri oluştur.
docker run --name dev -e POSTGRES_USER=appuser -e POSTGRES_PASSWORD=secret -p 5432:5432 -d postgres:latest

2. client klasörüne git ve npm run build ile react projesini oluştur. 
3. dotnet run watch ile dotnet projesini çalıştır. proje 5000 portunda çalışır ve  5432 deki postgrese bağlanır. 
4. 

Compose ile çalıştığında browser ile uyuşmazlık oluyor ve inventory menüsü çıkmıyor. vakit olunca bak.