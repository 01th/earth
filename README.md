# earth

Вращающаяся Земля в терминале, нарисованная точками Unicode Braille, в духе `cmatrix`.

Один файл без зависимостей: нужен только Python 3. Карта суши Natural Earth (1:110m) вшита в сам скрипт, интернет не нужен.

## Запуск

```sh
./earth
```

Клавиши: `q` / `Esc` / `Ctrl+C` — выход, пробел — пауза, `+` / `-` — скорость.

| параметр | что делает | по умолчанию |
|---|---|---|
| `-s, --speed` | скорость вращения, °/с (отрицательная — в обратную сторону) | 12 |
| `-f, --fps` | частота кадров | 30 |
| `-z, --size` | размер шара как доля окна (0.2–1) | 1.0 |
| `--start` | долгота, обращённая к зрителю при старте | 15 |
| `-V, --version` | показать версию | |

## Установка

**Arch Linux** — как обычный пакет, программа встанет в `/usr/bin/earth`:

```sh
git clone https://github.com/01th/earth
cd earth && makepkg -si
cd .. && rm -rf earth
```

Для сборки нужны инструменты `base-devel` (`sudo pacman -S --needed base-devel`). Удаление: `sudo pacman -R earth`.

**Любой Linux** — одной командой, без пакета:

```sh
sudo curl -fL https://raw.githubusercontent.com/01th/earth/main/earth -o /usr/local/bin/earth
sudo chmod +x /usr/local/bin/earth
```

Удаление: `sudo rm /usr/local/bin/earth`.

## Заметки

- Чем мельче шрифт терминала, тем подробнее и ровнее картинка (например, `kitty -o font_size=8 earth`).
- Нужен терминал с поддержкой 24-битного цвета (kitty, Alacritty, WezTerm, foot, GNOME Terminal и т. д.) и шрифт с символами Braille (U+2800–U+28FF).
- Данные карты: [Natural Earth](https://www.naturalearthdata.com/), общественное достояние.

## Лицензия

MIT, см. [LICENSE](LICENSE).
