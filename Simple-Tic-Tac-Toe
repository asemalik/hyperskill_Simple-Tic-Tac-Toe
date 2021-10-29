def vvod_setki_na_konsol(b):
    print("---------")
    print("|", b[0], b[1], b[2], "|")
    print("|", b[3], b[4], b[5], "|")
    print("|", b[6], b[7], b[8], "|")
    print("---------")


def analiz_setki(a, bukva):
    b, c = input("Enter the coordinates:").split()
    if b.isalpha() == True or c.isalpha() == True:
        print("You should enter numbers!")
        analiz_setki(a, bukva)
    else:
        k = (int(b) - 1) * 3 + int(c) - 1

        if int(b) > 3 or int(c) > 3:
            print("Coordinates should be from 1 to 3!")
            analiz_setki(a, bukva)
        elif a[k] == 'X' or a[k] == 'O':
            print("This cell is occupied! Choose another one!")
            analiz_setki(a, bukva)
        else:
            a[k] = bukva
            vvod_setki_na_konsol(a)
            return a


def proverka(a):
    def proverka_kolichestv(a):
        X = 0  # ойындағы х-тің саны
        Y = 0  # ойындағы у-тің саны
        for i in a:
            if i == 'X':
                X += 1
            elif i == 'O':
                Y += 1
        return X, Y

    X, Y = proverka_kolichestv(a)
    if X > Y:
        analiz_setki(a, "O")
    else:
        analiz_setki(a, "X")
    x = 0
    y = 0
    if a[0] == a[1] == a[2] == 'X' or a[3] == a[4] == a[5] == 'X' or a[6] == a[7] == a[8] == 'X':
        x = 1
    elif a[0] == a[3] == a[6] == 'X' or a[1] == a[4] == a[7] == 'X' or a[2] == a[5] == a[8] == 'X':
        x = 1
    elif a[0] == a[4] == a[8] == 'X' or a[2] == a[4] == a[6] == 'X':
        x = 1
    if a[0] == a[1] == a[2] == 'O' or a[3] == a[4] == a[5] == 'O' or a[6] == a[7] == a[8] == 'O':
        y = 1
    elif a[0] == a[3] == a[6] == 'O' or a[1] == a[4] == a[7] == 'O' or a[2] == a[5] == a[8] == 'O':
        y = 1
    elif a[0] == a[4] == a[8] == 'O' or a[2] == a[4] == a[6] == 'O':
        y = 1

    X, Y = proverka_kolichestv(a)
    if x == 0 and y == 0 and X + Y == 9:
        print("Draw")
    elif x == 1 and y == 0:
        print("X wins")
    elif x == 0 and y == 1:
        print("O wins")
    else:
        proverka(a)

b = [' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ']
vvod_setki_na_konsol(b)
proverka(b)
