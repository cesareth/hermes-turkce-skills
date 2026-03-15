# Hermes Türkçe Skills

Türk kullanıcılar ve Türkçe yazılım projeleri için [Hermes Agent](https://github.com/NousResearch/hermes-agent) skill seti. [agentskills.io](https://agentskills.io) standardına tam uyumlu.

---

## Skills

### 1. `turkce-asistan` — Türkçe Dil Asistanı

Doğru, profesyonel ve doğal Türkçe yazışmalar için.

- Sen/siz ayrımı ve üslup seviyeleri (resmi → samimi)
- Yabancı kelime yerine Türkçe karşılık tablosu
- E-posta şablonları (iş, müşteri, teknik)
- TDK yazım kuralları özeti ve sık yapılan hatalar

**Örnek kullanım:**
> "Bu e-postayı müdürüme resmi bir dille yeniden yaz."
> "Bu metindeki yabancı kelimeleri Türkçe karşılıklarıyla değiştir."

---

### 2. `kvkk-denetim` — KVKK Uyum Denetimi

6698 Sayılı Kişisel Verilerin Korunması Kanunu uyum analizi.

- Aydınlatma metni ve açık rıza formu şablonları
- Metin analizi ve uyum puanlama (Python CLI dahil)
- Madde referansları (Madde 3, 5, 6, 10, 11, 12)
- Ceza tablosu ve VERBİS kayıt gereksinimleri
- KVKK vs GDPR karşılaştırması

**Örnek kullanım:**
> "Uygulamamızın aydınlatma metnini KVKK'ya uygun hale getir."
> "Bu gizlilik politikasını KVKK açısından denetle."

```bash
# Python CLI ile denetim
python kvkk-denetim/scripts/kvkk_check.py --metin gizlilik.txt
```

---

### 3. `resmi-yazi` — Resmi Yazı ve Dilekçe Şablonları

Türk bürokratik yazışmalar için hazır şablonlar.

- Dilekçe (genel format ve kurum başvurusu)
- SGK başvuruları ve itiraz dilekçeleri
- Vergi dairesi yazışmaları
- İstifa mektubu (tazminatlı ve tazminatsız)
- İhtarname (iş, kira, alacak)
- İş başvuru mektubu

**Örnek kullanım:**
> "SGK hizmet dökümü için dilekçe hazırla."
> "Kiracıma kira artışı ihtarnamesi gönder."

---

### 4. `turkce-kod` — Türkçe Kod Dokümantasyonu

Türkçe yazılım projeleri için kod kalite standardları.

- Python, JS/TS, Go yorum satırı örnekleri
- Türkçe değişken ve fonksiyon isimlendirme rehberi
- Commit mesajı formatı (Türkçe conventional commits)
- README.md şablonu
- Hata mesajları ve log yazımı
- 200+ teknik terim sözlüğü (genel, veritabanı, ağ, DevOps, güvenlik, AI/ML)

**Örnek kullanım:**
> "Bu Python fonksiyonuna Türkçe docstring yaz."
> "Commit mesajlarımı Türkçe conventional commits formatına çevir."

---

## Kurulum

### Hermes Agent ile

```bash
# Tüm skill setini klon'la
git clone https://github.com/KULLANICI/hermes-turkce-skills ~/.hermes/skills/turkce

# Hermes otomatik algılar, restart gerekmez
hermes skills list
```

### Manuel

Skills dizinine kopyala:
```bash
cp -r turkce-asistan kvkk-denetim resmi-yazi turkce-kod ~/.hermes/skills/
```

### npx skills ile (agentskills.io uyumlu)

```bash
npx skills add KULLANICI/hermes-turkce-skills
```

### Claude Code ile

```bash
/plugin marketplace add KULLANICI/hermes-turkce-skills
```

---

## Standart Uyumluluğu

| Gereksinim | Durum |
|-----------|-------|
| agentskills.io spec | ✅ Tam uyumlu |
| SKILL.md frontmatter (name, description) | ✅ |
| references/ dizin desteği | ✅ |
| scripts/ dizin desteği | ✅ (kvkk-denetim) |
| Hermes Agent | ✅ |
| Claude Code | ✅ |
| OpenClaw / Codex / Cline | ✅ |

---

## Katkı Sağlama

Yeni Türkçe skill önerileri için issue açın ya da PR gönderin. Önerilen konular:

- `hukuk-sozluk/` — Türk hukuk terimleri ve sözleşme şablonları
- `akademik-yazi/` — Türkçe akademik yazım kuralları (APA, APA-TR)
- `basin-bulteni/` — Basın bülteni ve duyuru şablonları

---

## Lisans

MIT — Ayrıntılar için [LICENSE](LICENSE) dosyasına bakın.

---

*[Hermes Agent](https://github.com/NousResearch/hermes-agent) tarafından desteklenmektedir · [Nous Research](https://nousresearch.com)*
