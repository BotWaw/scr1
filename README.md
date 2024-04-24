# lab-scr1-sim
## Вариант задания
Вид исключения: Illegal instruction

Тест: isa/rv32mi/illegal.S

Reset Vector: 0x2000

Trap Vector: 0x1880

Обработчик: Вывод строки "illexc"

## Выполненные действия:
Согласно варианту был отредактирован список тестов. Оставлен только isa/rv32mi/illegal.S

Согласно варианту в файле ./sim/tests/common/riscv_macros.h был реализован обработчик исключений с выводом строки "illexc"

В linker-скрипте  ./sim/tests/common/link.ld были изменены адреса обработчика прерываний согласно варианту. Добавлен ".text.start" по адресу Reset Vector (0x2000)

## Результаты работы
* result/illegal.dump - дизассемблер теста
* result/test_results.txt - результат симуляции
* result/tracelog_core_0.log - трейс лог

## Результат симуляции
Сброс (Reset Vector: 0x2000):

![1](https://github.com/BotWaw/scr1/assets/99167822/f5926476-cb22-47f7-89d7-9e9f599a7cd6)

Исключение "Illegal instruction" с кодом 2. Переход по адресу обработчика прерываний 0x1880:
![2](https://github.com/BotWaw/scr1/assets/99167822/873bde5c-87b5-4683-aea6-3f8f13dea9bc)
