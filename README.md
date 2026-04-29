# Привет, я Настя 👋

**iOS-разработчик** · 16 лет · Учусь в 10 классе


## 🛠 Стек

| Область | Технологии |
|---------|------------|
| **Языки** | Swift |
| **UI** | SwiftUI |
| **Архитектура** | MVVM, разделение на View / ViewModel / Service / Networking |
| **Сеть** | `URLSession`, `Codable`, `multipart/form-data`, собственный слой `APIClient` / `Requestable` / `Resource` |
| **Хранение данных** | Core Data (`NSPersistentContainer`, `@FetchRequest`), `UserDefaults`, FileManager |

![Swift](https://img.shields.io/badge/Swift-FA7343?style=for-the-badge&logo=swift&logoColor=white)
![SwiftUI](https://img.shields.io/badge/SwiftUI-007AFF?style=for-the-badge&logo=swift&logoColor=white)
![Combine](https://img.shields.io/badge/Combine-4B0082?style=for-the-badge&logo=swift&logoColor=white)
![Xcode](https://img.shields.io/badge/Xcode-1575F9?style=for-the-badge&logo=xcode&logoColor=white)
![Core%20Data](https://img.shields.io/badge/Core_Data-3DDC84?style=for-the-badge&logo=apple&logoColor=white)

---

## 🏆 Достижения

| Награда | Описание |
|---------|----------|
| 🥇 Финалист **PROD** | Международная олимпиада по промышленной разработке |
| 🥇 Финалист **«Высшая проба»** | Олимпиада по промышленному программированию |
| 🥇 Финалист **NlogN** | Олимпиада по алгоритмам |

---

## 📚 Образование

- курс IOS-разработчик от MerionAcademy

### Яндекс Лицей
- Основы программирования на Python
- Основы промышленного программирования
- Специализация: веб-разработка на Go
- Самостоятельные курсы Go 1 и Go 2


### Т-Поколение
- Кружок по алгоритмам *(в процессе)*

### Самостоятельно — iOS
- Swift, SwiftUI, Combine, Core Data, AVFoundation, URLSession
- MVVM-архитектура и собственный сетевой слой
- Регулярная практика на пет-проектах

---

## 📱 iOS-проекты

### [ScreenEx](https://github.com/AnastasiaYuhimenko/ScreenEx) — приложение-портфель для отслеживания крипты
SwiftUI-приложение с собственным портфелем монет, поиском и просмотром топ-рынка.

- Архитектура **MVVM** с разделением на `BaseViewModel`, `SearchViewModel`, `PortfolioModelView`, `AddCoinsToPortfolioViewModel`.
- Свой сетевой слой: `APIClient`, протоколы `Requestable`, `Resource`, расширение `URLRequest+Requestable`, `JSONEncoder/Decoder` со snake_case.
- **Core Data** для хранения портфеля (`Portfolio.xcdatamodeld`, `Coins+CoreDataClass`, `PersistenceController`).
- Сервисный слой: `MarketDataService`, `CoinImageDataService`, `PortfolioService`, `SearchService`.
- Поддержка тёмной/светлой темы через свои `colorset`-палитры.

**Стек:** SwiftUI · URLSession · Core Data

---

### [EngineChecker](https://github.com/AnastasiaYuhimenko/EngineChecker) — диагностика двигателя по звуку
Приложение записывает звук двигателя с микрофона и отправляет его на ML-сервис, который классифицирует состояние: норма / аномалия. Поддерживает пакетный режим — загрузку ZIP с записями.

- Запись и склейка нескольких сегментов в один WAV через `AVAudioRecorder`.
- Загрузка файлов на сервер через `multipart/form-data` (`URLSession`).
- Экраны: `MainScreen`, `ScanScreen`, `ResultScreen`, `BatchResultScreen` — построены на SwiftUI
- Работа с разрешениями на микрофон, кастомные шрифты (Orbitron), Asset Catalog для палитры.

**Стек:** SwiftUI · Combine · AVFoundation · URLSession · multipart/form-data

---

### [GPU-manager-IOS](https://github.com/AnastasiaYuhimenko/GPU-manager-IOS) — приложение для управления GPU-ресурсами
Мобильный клиент для системы, в которой студенты, преподаватели и администраторы делят вычислительные ресурсы (GPU)

- Авторизация и регистрация: `Login`, `SignUp`, `LoginService`, обработка JWT.
- Три роли — три набора экранов: `homePageStudent`, `teacherHomePage`, `homePageAdmin` + админский `AllGpus`, `GroupInfo`, `GroupInfoAdmin`.
- Экран `UsingGPU` — мониторинг текущего использования.
- Интеграция с бекендом на Python

**Стек:** SwiftUI · URLSession · ролевая модель экранов

---

### [MiniBankApp](https://github.com/AnastasiaYuhimenko/MiniBankApp) — главный экран банковского приложения
Учебный концепт: главный экран онлайн-банка с карточкой баланса, быстрыми переводами и историей операций.

- Чистая компоновка из переиспользуемых View: `CardViewContent`, `QuickSendCard`, `RecentActivitieCard`, `cardShape`, `header`.
- Кастомная цветовая схема (10+ colorsets), работа с PNG-ассетами (PayPal, Amazon).
- Адаптация под тёмную/светлую тему.

**Стек:** SwiftUI · Asset Catalog · композиция View

---

### [CryptoWalletAppSwift](https://github.com/AnastasiaYuhimenko/CryptoWalletAppSwift) — главный экран крипто-кошелька
SwiftUI-проект с акцентом на UI: «шапка», карточка с общим балансом, блок быстрых действий и список расходов.

- Композиция экрана из независимых модулей в папке `parts/`: `hat`, `totalFundsCard`, `actions`, `costs`.
- Работа с градиентами и кастомной палитрой (`cardGradientBlue`, `cardGradientPurple`, `lineBlue`, `linePurple` и др.).

**Стек:** SwiftUI

---

### [RandomScreens](https://github.com/AnastasiaYuhimenko/RandomScreens) — сборник экранов, которые я воспроизводила по дизайнам из Figma и Pinterest, чтобы прокачать SwiftUI и насмотренность.

- **FoodApp**: главный экран ресторана, страница блюда, корзина, оформление заказа, оплата, история, логин/регистрация, состояние «нет интернета», экран ошибки «не найдено», профиль.
- **StudyAppMainScreen**: дашборд курсов с прогрессом и поиском.

**Стек:** SwiftUI 

---

## 🧩 Что я умею в iOS

- Проектировать приложение по слоям: **Views / ViewModels / Services / Networking**, не путать UI-логику с бизнесовой.
- Писать сетевой слой с нуля: типизированные запросы, `Codable`, snake_case decoder/encoder, обработка ошибок.
- Подключать **Core Data**: модель, контейнер, фоновые контексты, `@FetchRequest`.
- Работать с **AVFoundation**: запись звука, склейка сегментов, экспорт в WAV/PCM, загрузка через multipart.
- Делать аккуратный UI на **SwiftUI**: Asset Catalog, кастомные шрифты, тёмная/светлая тема, плавные переходы и анимации.
- Состояние через **Combine** и property wrappers (`@StateObject`, `@ObservedObject`, `@EnvironmentObject`, `@Published`).
- Договариваться с бэкендом — у меня есть опыт собственных API на Python и Go, поэтому я понимаю, что происходит «по другую сторону».

---

## 💼 Почему меня стоит выбрать

- ✅ Делаю не «один экран», а приложения с архитектурой, сетевым слоем и хранилищем
- ✅ Понимаю, как работает бэкенд
- ✅ Умею аккуратно работать с UI: тема, шрифты, ассеты, адаптация
- ✅ Быстро учусь, довожу задачи до конца и не боюсь сложных тем
- ✅ Я крутая и вообще молодец ✨

---

> Открыта к стажировкам и интересным проектам.
