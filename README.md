# numbers-in-weeks

"""вводится количество дней, а программа выводит количество недель и остаточных дней до неполной недели"""

d = int(input(f"введите количество дней: "))
ost = d%7
if d%7 >= 0:
    b= d-ost
    # определение дня
    if ost in (0, 5, 6, 7, 8, 9):
        end_ost = "дней"
    elif ost in (2, 3, 4):
        end_ost = "дня"
    else:
        end_ost = "день"
    # определение недели
    if d >7 and d<14:
        end_w = "неделя"
    elif d > 14 and d < 35:
        end_w = "недели"
    else:
        end_w = "недель"
    #вывод
    print(f"[{int(b/7)}] {end_w} и [{ost}] {end_ost} в [{d}] днях")
