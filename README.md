# Midtest



class Bazmankyun:
    def __init__(self):
        self.type_of_triangle = None
        self.patasxan = None
        self.patasxan2 = None
        self.i = 1
        self.lst = []
        self.count_of_sides = int(input("input count of sides: "))
        self.patasxan2 = "Sa bazmankun ernakyuna haves chunem asem inchqan"
        self.patasxan3 = "Ay qyal esi erankyun chi esi vabshe incha, qo matemi dasatun ova exel?!"

        if self.count_of_sides < 3:
            print(self.patasxan3)
        elif self.count_of_sides > 4:
            print(self.patasxan2)


P = Bazmankyun()


class Erankyun(Bazmankyun):

    def __init__(self):
        super(Bazmankyun).__init__()
        if P.count_of_sides == 3:
            def erankyun(a, b, c):
                if a + b > c or a + c > b or c + b > a:
                    if a == b and b == c:
                        P.type_of_triangle = "havasarakoxm e"
                    elif a == b and b != c:
                        P.type_of_triangle = "havasarasrun e"
                    elif a != b and b != c:
                        P.type_of_triangle = "sovorakan erankyun e"
                    while P.i != 0:
                        P.i -= 1
                        P.lst.append(a)
                        P.lst.append(b)
                        P.lst.append(c)
                P.patasxan = f"{P.type_of_triangle}, esel koxmery: {P.lst}"
                print(P.patasxan)

            erankyun(int(input("input a: ")), int(input("input b: ")), int(input("input c: ")))


class Qarankyun(Bazmankyun):
    def __init__(self):
        super(Bazmankyun).__init__()
        if P.count_of_sides == 4:
            P.type_of_triangle = "Qarankyun e"
            while P.i < P.count_of_sides + 1:
                P.i += 1
                n = int(input())
                P.lst.append(n)
            P.patasxan = f"{P.type_of_triangle}, esel koxmery: {P.lst}"
            print(P.patasxan)


E = Erankyun()
Q = Qarankyun()


class Baby(Erankyun, Qarankyun):
    def __init__(self):
        super(Bazmankyun).__init__()
        if P.count_of_sides == 3:
            print(E.patasxan)
        elif P.count_of_sides == 4:
            print(Q.patasxan)
        elif P.count_of_sides > 4:
            print(P.patasxan2)
        elif P.count_of_sides < 3:
            print(P.patasxan3)
