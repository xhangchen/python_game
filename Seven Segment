u={'A','B','C','D','E','F','G'}
lo={'a','b','c','d','e','f','g'}
numu=[{'B','C'},{'A','B','G','E','D'},{'A','B','G','C','D'},{'F','G','B','C'},{'A','F','G','C','D'},
     {'A','F','E','G','C','D'},{'A','B','C'},{'A','B','C','D','E','F','G'},{'A','B','C','D','F','G'},
     {'A','B','C','D','E','F',}]
numl=[{'b','c'},{'a','b','g','e','d'},{'a','b','g','c','d'},{'f','g','b','c'},{'a','f','g','c','d'},
     {'a','f','e','g','c','d'},{'a','b','c'},{'a','b','c','d','e','f','g'},{'a','b','c','d','f','g'},
     {'a','b','c','d','e','f',}]
ar1=[]
ar2=[]
def comp(s):
    l=[0,0]
    if s&u in numu and not s&u in ar1:
        l[0]=1
        ar1.append(s&u)
    if s&lo in numl and not s&lo in ar2:
        l[1]=1
        ar2.append(s&lo)
    return l

def seven_segment(x1,x2):
    s1=set(x1)
    s2=set(x2)
    li=[x for x in s2]
    a=c=0
    x=[]
    for i in range(2**len(s2)):
        b = bin(i)[2:]
        l=[0]*(len(s2)-len(b))
        l+=list(b)
        comb=set()
        for j in range(len(s2)):
            if l[j]=='1':
                comb.add(li[j])
        x=comp(s1|comb)
        a+=x[0]
        c+=x[1]
    return a*c
#eg:
print(seven_segment(["B","C","a","f","g","c","d"],["A","G","D","e"]))
