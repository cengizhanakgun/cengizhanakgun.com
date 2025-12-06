---
title: "DNS Nasıl Çalışır? İnternetin Görünmeyen Telefon Rehberi"
description: "DNS nedir, nasıl çalışır, DNS kayıt türleri nelerdir? İnternetin arka planındaki bu kritik sistemin işleyişini sade ve anlaşılır bir dille ele alan kapsamlı rehber."
date: 2025-01-12
tags: ["dns", "internet", "ağ teknolojileri", "domain"]
categories: ["network"]
draft: false
---

DNS, internetin en kritik sistemlerinden biridir.  
Her gün farkında olmadan yüzlerce kez DNS sorgusu yapıyoruz, fakat çoğu kullanıcı DNS’in ne olduğunu dahi bilmez.

DNS’i en basit hâliyle şöyle tanımlayabiliriz:

> **DNS, alan adlarını IP adreslerine çeviren dijital bir telefon rehberidir.**

---

## 📞 DNS Neden Gereklidir?

İnternette her cihaz, bir **IP adresi** ile tanımlanır:

- `142.250.187.78` gibi sayılar  
- Ya da IPv6 formunda uzun adresler  

Fakat insanlar sayıları değil, **isimleri** hatırlamak ister.

Örneğin:

- `cengizhanakgun.com`  
- `google.com`  
- `github.com`  

DNS olmasaydı, bu sitelere erişmek için IP adreslerini ezberlemek gerekirdi.

DNS bu sorunu çözer ve:

**Alan adını → IP adresine çevirir.**

---

## ⚙ DNS Nasıl Çalışır? (Adım Adım)

Bir siteye girdiğinde arka planda şu adımlar gerçekleşir:

---

### 🟦 1. DNS Resolver Devreye Girer  
Tarayıcı, işletim sistemi DNS’e sorar:

> “Bu alan adı hangi IP’ye karşılık geliyor?”

Resolver genelde internet servis sağlayıcısında bulunur.

---

### 🟩 2. Root DNS Sunucuları  
Resolver, internetin en üst seviyesindeki root sunuculara giderek hangi TLD sunucusuna (".com", ".net" vb.) yönlendirilmesi gerektiğini öğrenir.

---

### 🟨 3. TLD Sunucuları  
“.com” gibi uzantıları yöneten sunucular, alan adının sahibi olan yetkili DNS sunucusunun adresini verir.

---

### 🟧 4. Yetkili DNS Sunucusu  
Bu sunucu, gerçek IP adresini döndürür:


---

### 🟥 5. Tarayıcı IP'ye Bağlanır  
IP adresi artık bellidir, bağlantı gerçekleşir ve site açılır.

Tüm bu işlem:  
**20–40 milisaniye** sürer.

---

## 📦 Yaygın DNS Kayıt Türleri

### ✔ A Kaydı  
Alan adını bir IPv4 adresine yönlendirir.

### ✔ AAAA Kaydı  
IPv6 adresi.

### ✔ CNAME  
Bir alan adını başka bir alan adına yönlendirir.

### ✔ MX  
E-posta sunucularını belirtir.

### ✔ TXT  
DMARC, SPF gibi doğrulama kayıtlarında kullanılır.

### ✔ NS  
Alan adının hangi DNS sunucuları tarafından yönetildiğini belirtir.

---

## 🧠 DNS Önbelleği (Cache) Nedir?

DNS sonuçları, tekrar sorgu yapılmaması için cihazlarda ve ISP’lerde önbelleğe alınır.  
Bu hem performansı artırır hem de DNS yükünü azaltır.

---

## 🔐 DNS Güvenliği Neden Önemlidir?

Kötü niyetli kişiler DNS’i manipüle edebilir:

- **DNS Spoofing**  
- **DNS Hijacking**  
- **Cache Poisoning**  

Bu saldırılar sonucunda kullanıcılar sahte sitelere yönlendirilebilir.

Bu nedenle DNSSEC gibi güvenlik mekanizmaları geliştirilmiştir.

---

## 🌍 Gerçek Hayatta DNS Kullanım Senaryoları

- Web sitelerinin yayınlanması  
- E-posta sunucularının yapılandırılması  
- CDN yönlendirmeleri  
- Cloudflare gibi servislerde proxy işlemleri  

DNS olmadan internet de olmazdı.

---

## 📌 Sonuç

DNS, internetin görünmeyen ancak en temel yapı taşlarından biridir.  
Kullanıcı dostu alan adlarını IP adreslerine çevirir, güvenilir şekilde yönlendirir ve internetin akıcı çalışmasını sağlar.

Her web geliştiricinin, sistem yöneticisinin ve güvenlik uzmanının DNS’i iyi anlaması gerekir.

---
