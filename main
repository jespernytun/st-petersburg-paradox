from random import randint

def CasinoPetersburg(iterasjoner):
    Gains = 0
    Gain_max = 0
    forsøk = 0

    while forsøk <= iterasjoner:
        Heads = False
        n = 0
        while Heads == False:
            x = randint(1,2)
            if x == 2:
                Heads = True
            n = n +1

            if 2**n > Gain_max:
                Gain_max = 2**n

        Gains = Gains + 2**n
        forsøk = forsøk + 1

    expected_return = Gains/iterasjoner

    print(expected_return)
    print((Gains-Gain_max)/(iterasjoner-1))
    print(Gain_max)

CasinoPetersburg(100000)
