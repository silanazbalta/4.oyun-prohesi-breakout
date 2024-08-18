BREAKOUT
 Oyun Kurulumu :
Tuval ve Bağlam : Oyun, <canvas>oyunun grafiklerini işlemek için bir tuval öğesi ( ) kullanır. Bağlam ( ) , 2B işleme izin vermek için ctxkullanılarak elde edilir .getContext('2d')
Etkinlik Dinleyicileri :
keydownve keyupolaylar küreği sola ve sağa hareket ettirmek için kullanılır.
mousemoveFarenin x koordinatına göre kürek hareketine izin verir.
Oyun Durumu ( gamenesne) : Bu nesne oyunun durumunu, açık mı kapalı mı olduğunu, ses efektlerinin ve müziğin etkin olup olmadığını ve leftKeyve gibi bazı kontrolleri tutar rightKey.
2. Oyun Öğeleri :
Kürek : Kürek belirli bir yükseklik ve genişlikte tanımlanır ve konumu tuval boyutuna göre dinamik olarak hesaplanır.
Top : Topun pozisyonu, hızı ve yönü ( dx, dy) oyunun başında belirlenir ve gerektiğinde (örneğin top kaybedildiğinde) sıfırlanır.
Tuğlalar : Tuğlalar bir ızgarada düzenlenmiştir. İşlev, initBricks()bu tuğlaları satıra bağlı olarak renkler, boyutlar ve can puanlarıyla başlatır.
3. Oyun Mekanikleri :
Çarpışma Algılama : Oyun, top ile duvarlar, kürek ve tuğlalar arasındaki çarpışmaları kontrol eder:
Duvarlar : Top sol veya sağ duvara çarparsa, yatay yönü ( dx) tersine döner. Üst duvara çarparsa, dikey yönü ( dy) tersine döner.
Kürek : Top küreğe çarptığında dikey yönü tersine döner, küreğe çarptığı yere göre yatay yönü ise biraz değişir.
Tuğlalar : Top bir tuğlaya çarparsa tuğlanın can puanı azalır. Can puanı sıfıra indiğinde tuğla kaldırılır.
Puan ve Canlar : Oyuncu tuğlalara vurduğunda puan kazanır. Top kaybolursa (yani, raketin altına giderse), oyuncu bir can kaybeder. Oyuncunun canları bittiğinde oyun sona erer.
Seviyeler : Tüm tuğlalar yok edildiğinde oyuncu bir sonraki seviyeye geçer ve oyun hızı artar.
4. Kullanıcı Etkileşimi :
Oyunun Başlatılması : Oyun, oyuncunun boşluk tuşuna basması ile başlar.
Müzik ve Ses Efektleri : Oyuncu tuşuyla müziği M, tuşuyla da ses efektlerini değiştirebilir S. Ok tuşları sesi ayarlar.
5. İşleme :
paint()fonksiyon : Bu fonksiyon, oyun elemanlarını tuval üzerine yeniden çizmek için tekrar tekrar çağrılır ve animasyon efekti oluşturulur.
Oyun Bitti ve Seviye Tamamlandı : Oyun bittiğinde veya bir seviye tamamlandığında ekrana metin mesajları çizilir.
6. Başlatma :
onImageLoad(): Bu fonksiyon, arka plan resmi yüklendiğinde oyunu kurar, tuğlaları başlatır, küreği sıfırlar ve "BAŞLAT'A BAS" mesajını görüntüler.
initSounds(): Bu, seslerin seviyesini ayarlar ve arka plan müziğini döngüye alır.
7. HTML ve Meta Veriler :
Sağlanan HTML, SEO ve sosyal paylaşım için meta verileri (örneğin OpenGraph ve Twitter Card etiketleri) içerir.
Oyunun başlığı, açıklaması ve anahtar kelimeler, arama motorlarında ve sosyal medya platformlarında oyunu tanımlayacak şekilde tanımlanır.
Bu yapı basit bir Breakout oyunu için iyi organize edilmiştir. Daha fazla özellik ekleyerek, grafikleri iyileştirerek veya oyun mekaniklerini ayarlayarak genişletebilir veya değiştirebilirsiniz.
