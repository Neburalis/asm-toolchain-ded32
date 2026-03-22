# asm32 (repacked)

Этот репозиторий содержит перепакованную версию учебного архива с тулчейном по ассемблеру, собранного [Дедом]((https://ded32.net.ru/)).

## Что это такое

Оригинальный архив распространяется в формате `RAR SFX` (`.rar.exe`). Такой формат на современных Linux/macOS часто распаковывается с проблемами или не распаковывается вовсе.

Чтобы архивом можно было нормально пользоваться вне Windows, он был:

1. извлечён из исходного `RAR SFX`;
2. перепакован в обычный `tar.gz`;
3. разбит на несколько частей, чтобы обойти ограничения GitHub по размеру файлов.

Этот репозиторий **не является новым проектом** и **не меняет содержимое тулчейна по существу** — это просто более совместимая упаковка исходного набора.

## Что внутри

Это учебный тулчейн для практики низкоуровневого программирования и ассемблера под Windows/Linux/macOS.

Внутри:

- примеры на x86 / x64 assembler;
- разные ассемблеры и линковщики (NASM, FASM, MASM/ML и др.);
- заготовки под сборку программ;
- примеры работы с:
  - Win32 API;
  - Linux syscalls;
  - macOS ABI;
- кейсы интеграции C/C++ и asm.

## Как скачать и распаковать

Выполните одну команду:

```bash
curl -L \
  https://raw.githubusercontent.com/Neburalis/asm-toolchain-ded32/refs/heads/main/asm32_64.tar.gz.part0 \
  https://raw.githubusercontent.com/Neburalis/asm-toolchain-ded32/refs/heads/main/asm32_64.tar.gz.part1 \
  https://raw.githubusercontent.com/Neburalis/asm-toolchain-ded32/refs/heads/main/asm32_64.tar.gz.part2 \
  https://raw.githubusercontent.com/Neburalis/asm-toolchain-ded32/refs/heads/main/asm32_64.tar.gz.part3 \
  https://raw.githubusercontent.com/Neburalis/asm-toolchain-ded32/refs/heads/main/asm32_64.tar.gz.part4 \
  https://raw.githubusercontent.com/Neburalis/asm-toolchain-ded32/refs/heads/main/asm32_64.tar.gz.part5 \
  https://raw.githubusercontent.com/Neburalis/asm-toolchain-ded32/refs/heads/main/asm32_64.tar.gz.part6 \
  | cat > asm32_64.tar.gz && tar -xzf asm32_64.tar.gz