# Smooth Frames — как получить .ipa

Приложение: выбираешь видео → 60 к/с превращается в 120 к/с (достраиваются промежуточные кадры),
опционально «Сглаживание» (повышенное качество), настраиваемый битрейт, сохранение в «Фото».
Только iOS 26+, только реальный iPhone (в симуляторе не работает).

## Вариант А — без Mac (через GitHub, бесплатно)
1. Зарегистрируйся на github.com, создай новый репозиторий (можно приватный).
2. Загрузи в него ВСЕ файлы из этого архива (Add file → Upload files),
   включая папку .github (если она не видна — загрузи через GitHub Desktop или git).
3. Вкладка Actions → "Build IPA" → Run workflow. Через 5–10 минут появится артефакт SmoothFrames-ipa.
4. Скачай архив, внутри будет SmoothFrames.ipa. Установи через ESign (подпись своим сертификатом).

## Вариант Б — на Mac
    brew install xcodegen
    cd SmoothFrames && xcodegen generate
    открой SmoothFrames.xcodeproj в Xcode 26 → Product → Archive
или тот же xcodebuild из .github/workflows/build.yml.
