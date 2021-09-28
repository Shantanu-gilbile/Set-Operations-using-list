a = []
b = []
c = []


def cricket():
    n = int(input('how many students do you want in set a :'))
    for i in range(n):
        num = int(input('enter the Roll no of student who want to play cricket :'))
        a.append(num)
    return('cricket =', a)


def badminton():
    n1 = int(input('how many students do you want in set b :'))
    for i in range(n1):
        num1 = int(input('enter the Roll no of student who want to play badminton :'))
        b.append(num1)
    return('badminton =', b)


def football():
    n2 = int(input('how many students do you want in set c :'))
    for i in range(n2):
        num2 = int(input('enter the Roll no of student who want to play football :'))
        c.append(num2)
    return('football =', c)


cricket()
badminton()
football()

def Union(a, b):
    global U
    U=[]
    for i in range (len(a)):
        U.append(a[i])
    for i in b:
        if i not in a:
            for i in c:
                if i not in a and b:
                    U.append(i)
    return  U


def first(a, b):
    A = []

    for i in a:
        if i in b:
            A.append(i)
    return A


def second():
    B = []
    for i in a:
        if i not in b:
            B.append(i)
    for j in b:
        if j not in a:
            B.append(j)
    return B


def third():
    C=[]
    for i in U:
        if i not in a and b :
            C.append(i)
    return C


def fourth():
    D=[]
    for i in U :
        if i not in b :
            D.append(i)
    return D


print('Menu')
print('1.Union pf all Sets')
print('2.List of roll no who  play both cricket and badminton')
print('3.List of roll no who  play either cricket or badminton but not both')
print('4.List of roll no who  play neither cricket nor badminton are')
print('5.List of roll no who  play  cricket and football but not badminton')
print('6.Exit')
l = 1
while (l == 1):
    ch = int(input('What you want to perform :'))
    if (ch==1):
        print('Union of all Sets:',Union(a,b))
    if (ch == 2):
        print('List of roll no who  play both cricket and badminton ', first(a,b))

    elif (ch == 3):
        print('List of roll no who  play either cricket or badminton but not both', second())

    elif (ch == 4):
        print('List of roll no who  play neither cricket nor badminton are', third())

    elif (ch == 5):
        print('List of roll no who  play  cricket and football but not badminton', fourth())

    elif (ch == 6):
        print('Successfully Exited.')
        break;
else:
    print('You have entered wrong choice please check again')

