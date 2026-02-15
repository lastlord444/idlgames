# MENTOR — Match3 + Idle TD Mimari Rehber

## 🎯 CORE LOOP
1. **Match3 Oynanış** → Hamle/Skor kazanma
2. **İlerleyiş** → Level tamamlama (hamle/zaman kısıtlı)
3. **Idle Entegrasyon** → Para kazanma, upgrade satın alma
4. **Tower Defense (Gelecek)** → İkincil oynanış

## 🧱 MİMARİ PRENSİPLER
- **State Management**: Level durumu, oyuncu ilerlemesi, kayıt/yükleme net olmalı
- **Modülerlik**: Match3 core, Idle sistem, TD sistemi birbirinden bağımsız
- **Performans**: Object pooling (Match3 taşlar için), minimal GC allocation
- **Save System**: JSON-based, versiyon takibi, migration yolu açık

## 📊 PERFORMANS CHECKLIST
- [ ] Match3 taş instantiate/destroy yerine pool kullanılıyor mu?
- [ ] UI element sayısı optimize mi? (100+ element → investigate)
- [ ] Idle hesaplamaları her frame yerine event-driven mı?
- [ ] Save/Load işlemi async yapılabilir mi?

## 💰 MONETİZASYON CHECKLIST
- [ ] Idle para kazanma dengeli mi? (oyuncu ilerleyişi çok hızlı/yavaş olmasın)
- [ ] Upgrade fiyatları exponential scaling kullanıyor mu?
- [ ] "Bekleme duvarı" (grind wall) çok erken gelmiyor mu?
- [ ] IAP/Ad entegrasyonu için hook'lar var mı?

## ⛔ STOP DOING LİSTESİ
1. **Dummy kod yazmak** — Eksik implementation varsa ERROR at veya TODO bırak
2. **Match3 core'u bozmak** — Çalışan GameGrid/GamePiece mantığına dokunma
3. **Senkron save/load** — Büyük veriler için async wrapper kullan
4. **Hardcoded values** — ScriptableObject veya config JSON kullan

## 🔗 İLİŞKİLER
- `GameGrid` → Match3 oynanış
- `LevelManager` → Level akışı
- `CurrencyManager` + `UpgradeManager` → Idle progression
- `SaveManager` → Persistence
