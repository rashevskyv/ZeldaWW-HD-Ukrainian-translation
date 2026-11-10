# The Legend of Zelda: The Wind Waker HD (Wii U) — патчер українського перекладу

Патчер завантажує з цього репозиторію актуальні файли перекладу і робить із них мод для Cemu та для справжньої Wii U.
Ваш дамп гри патчер лише читає і не змінює.

## Вимоги

1. Власний дамп гри Wii U (USA, title ID `0005000010143500`) у вигляді теки з підтеками `code`, `content`, `meta`.
   Образи `.wux`/`.wud`/`.wua` спочатку розпакуйте у теку (наприклад, через Cemu).
2. Інтернет для завантаження файлів перекладу.
3. Windows: `WWHD_Patcher.exe`. macOS / Linux: Python 3.10+ і команда `python3 patcher.py`.

## Покрокова інструкція

1. Покладіть теку гри в теку `ISO` поруч із патчером: `ISO\<тека гри>\code`, `content`, `meta`.
2. Запустіть `WWHD_Patcher.exe` (або `python3 patcher.py`).
3. Патчер:
   - завантажить актуальні файли перекладу з GitHub;
   - перевірить title ID і контрольну суму `content\Common\Pack\permanent_2d_UsEnglish.pack`;
   - якщо дамп інший або вже змінений, попередить і спитає, чи продовжувати;
   - створить теку `ISO\<тека гри>_UA`.
4. Після напису «Готово!» натисніть Enter.

## Результат

У теці `ISO\<тека гри>_UA`:
- `graphicPacks\Picoripi_UA_WWHD` — графічний пакет для Cemu. Скопіюйте його в теку `graphicPacks` Cemu
  і ввімкніть у Cemu: Options → Graphic packs → Picoripi UA.
- `sdcafiine\wiiu` — для Wii U з Aroma і SDCafiine: скопіюйте теку `wiiu` у корінь SD-картки.
