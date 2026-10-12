# my-skills

Kişiselleştirilmiş, modüler AI ajan becerileri (skills), kuralları ve iş akışları kütüphanesi. 

Bu depo, Google Antigravity ve uyumlu AI kodlama ajanları için tasarlanmış özel yetenek koleksiyonlarını tek bir çatı altında barındırır. Yeni yetenek paketleri geliştikçe bu çatı altında modüler olarak listelenecektir.

---

## Koleksiyonlar (Skill Collections)

### 1. `socratic-mentor-skills`
AI ajanını "kodu doğrudan yazan uygulayıcı" modundan çıkarıp, kullanıcıyı ilk prensiplerden eğiten rasyonel bir **Senior Teknik Mentor** haline getiren beceri seti.

* **`socratic-pedagogy`**: 4 aşamalı öğrenme döngüsü (Teşhis -> Sokratik Soru -> Kademeli İpucu -> Pekiştirme).
* **`architecture-mentor`**: Sistem tasarımı, NFR analizi, CAP/ACID trade-off'ları ve ADR koçluğu.
* **`ml-first-principles`**: Matematiksel zemin (gradyan, attention mekanizması, loss fonksiyonları), tensör hata ayıklama ve RAG mimarileri.
* **`deliberate-practice-katas`**: "Spot the Bug", Refactoring ve "Sıfırdan İnşa Et" formatında kasıtlı pratik görevleri.
* **`code-critique-mentor`**: Temiz kod, $O(N)$ karmaşıklığı ve savunmacı programlama odaklı nesnel kod incelemesi.
* **`AGENTS.md`**: Çalışma alanında daima devrede olan mentorluk kural sözleşmesi.

---

## Hızlı Başlangıç & Kurulum

Bu yetenekleri kendi Antigravity veya AI kodlama ortamınızda kullanmak için:

1. Bu depoyu klonlayın veya ilgili skill klasörünü projenize kopyalayın:
   ```bash
   git clone https://github.com/hamza-jpg/my-skills.git
   ```

2. Projenizin kök dizininde `.agents/skills/` dizini oluşturun ve kullanmak istediğiniz becerileri içine yerleştirin:
   ```bash
   mkdir -p .agents/skills
   cp -r my-skills/socratic-mentor-skills/* .agents/skills/
   ```

3. Mentor davranış kuralını projenizin kök dizinine ekleyin:
   ```bash
   cp my-skills/socratic-mentor-skills/AGENTS.md ./AGENTS.md
   ```

---

## Tasarım İlkeleri & Kısıtlamalar

Bu repodaki mentor becerileri katı pedagojik kısıtlamalarla donatılmıştır:

1. **Doğrudan Çözüm Yasaktır:** Agent kodu doğrudan yazmaz; kullanıcının zihinsel modellerini geliştirecek hedef sorular sorar.
2. **Yapay Övgü Yasaktır (Zero Flattery):** "Harika!", "Tebrikler!", "Süpersin!" gibi dolgu ifadeler bulunmaz. İletişim nesnel, soğukkanlı ve doğrudan teknik gerçek odaklıdır.
3. **Analoji Yasaktır (İstenmedikçe):** Kullanıcı açıkça talep etmedikçe günlük hayat analojileri yapılmaz. Tüm konular doğrudan bilgisayar bilimi ve matematik terminolojisiyle açıklanır.
4. **Emoji Yasaktır:** Çıktılar tamamen temiz ve profesyonel teknik metin formatındadır.

---

## Referanslar & İlham Kaynakları (References & Citations)

Bu depodaki yetenekler ve kurallar aşağıdaki açık kaynak kaynaklardan, akademik çalışmalardan ve mühendislik literatüründen ilham almıştır:

* **ClawForge Skill Repository:** [https://github.com/jackjin1997/ClawForge](https://github.com/jackjin1997/ClawForge) - Temel temiz kod ve yazılım geliştirme pratikleri.
* **Google Antigravity Customization Architecture:** Antigravity YAML frontmatter tabanlı aşamalı açığa çıkarma (progressive disclosure) skill mimarisi.
* **Clean Code & Software Craftsmanship:** Robert C. Martin ("Uncle Bob") - Temiz kod ve SOLID tasarım prensipleri.
* **Deliberate Practice Framework:** K. Anders Ericsson ("The Role of Deliberate Practice in the Acquisition of Expert Performance").
* **Machine Learning from First Principles:** Andrej Karpathy (Micrograd & "Neural Networks: Zero to Hero" pedagojik yaklaşımı).
* **Distributed Systems Architecture:** Martin Kleppmann ("Designing Data-Intensive Applications", O'Reilly Media).
* **Architecture Decision Records (ADR):** Michael Nygard ("Documenting Architecture Decisions").

---

## Lisans

Bu proje [MIT Lisansı](LICENSE) altında lisanslanmıştır.
