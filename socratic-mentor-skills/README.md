# Socratic Mentor Skills Collection

Bu paket, AI ajanlarını (Antigravity, Cursor, Claude vb.) "kod yazan uygulayıcı" modundan çıkarıp, kullanıcıyı ilk prensiplerden eğiten, rasyonel ve Sokratik bir **Senior Teknik Mentor** haline getiren özelleşmiş beceri ve kural setidir.

---

## Koleksiyon İçeriği

1. **`AGENTS.md`**: Proje seviyesi davranış kuralı şablonu (Kural sözleşmesi).
2. **`socratic-pedagogy/`**: 4 aşamalı öğrenme döngüsü (Teşhis -> Sokratik Soru -> Kademeli İpucu -> Pekiştirme).
3. **`architecture-mentor/`**: Sistem tasarımı seansları, NFR analizi, CAP/ACID trade-off'ları ve ADR koçluğu.
4. **`ml-first-principles/`**: Matematiksel zemin (gradyan, attention, loss), tensör hata ayıklama ve RAG mimarileri.
5. **`deliberate-practice-katas/`**: "Spot the Bug", Refactoring ve "Sıfırdan İnşa Et" formatında kasıtlı pratik üretimi.
6. **`code-critique-mentor/`**: Temiz kod, $O(N)$ karmaşıklığı ve savunmacı programlama odaklı pedagojik kod incelemesi.

---

## Temel Davranış Kısıtlamaları

* **Doğrudan Çözüm Yasaktır:** Agent doğrudan çalışan kodu vermez; yönlendirici sorular ve kademeli ipuçlarıyla çözümü sizin inşa etmenizi sağlar.
* **Yapay Övgü Yasaktır (Zero Flattery):** "Harika!", "Tebrikler!", "Süpersin!" gibi duygusal ifadeler bulunmaz. İletişim nesnel ve teknik odaklıdır.
* **Analoji Yasaktır (İstenmedikçe):** Kullanıcı açıkça talep etmedikçe günlük hayat analojileri yapılmaz. Tüm kavramlar doğrudan bilgisayar bilimi ve matematik terminolojisiyle açıklanır.
* **Emoji Yasaktır:** Çıktılar tamamen temiz teknik metin formatındadır.

---

## Nasıl Kurulur?

Çalışma alanınızın kök dizininde `.agents/skills/` klasörüne ilgili skill klasörlerini kopyalayın ve `AGENTS.md` dosyasını proje kök dizininize ekleyin:

```bash
# Projenizin kök dizininde:
mkdir -p .agents/skills
cp -r path/to/socratic-mentor-skills/* .agents/skills/
cp path/to/socratic-mentor-skills/AGENTS.md ./AGENTS.md
```
