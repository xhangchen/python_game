import re
di={'a':[[1,0],[0,0],[0,0]],'b':[[1,0],[1,0],[0,0]],'c':[[1,1],[0,0],[0,0]],'d':[[1,1],[0,1],[0,0]], \
    'e': [[1, 0], [0, 1], [0, 0]],'f':[[1,1],[1,0],[0,0]],'g':[[1,1],[1,1],[0,0]],'h':[[1,0],[1,1],[0,0]], \
    'i': [[0, 1], [1, 0], [0, 0]],'j':[[0,1],[1,1],[0,0]],'k':[[1,0],[0,0],[1,0]],'l':[[1,0],[1,0],[1,0]], \
    'm': [[1, 1], [0, 0], [1, 0]],'n':[[1,1],[0,1],[1,0]],'o':[[1,0],[0,1],[1,0]],'p':[[1,1],[1,0],[1,0]], \
    'q': [[1, 1], [1, 1], [1, 0]],'r':[[1,0],[1,1],[1,0]],'s':[[0,1],[1,0],[1,0]],'t':[[0,1],[1,1],[1,0]], \
    'u': [[1, 0], [0, 0], [1, 1]],'v':[[1,0],[1,0],[1,1]],'w':[[0,1],[1,1],[1,1]],'x':[[1,1],[0,0],[1,1]], \
    'y': [[1, 1], [0, 1], [1, 1]],'z':[[1,0],[0,1],[1,1]],'capital':[[0,0],[0,0],[0,1]],'number':[[0,1],[0,1],[1,1]], \
    ',': [[0, 0], [1, 0], [0, 0]],'.':[[0,0],[1,1],[0,1]],'-':[[0,0],[1,1],[0,0]],'?':[[0,0],[1,0],[1,1]],\
    '_':[[0,0],[0,0],[1,1]],'!':[[0,0],[1,1],[1,0]]}

def braille_page(text):
    total=[]
    l1=[]
    l2=[]
    l3=[]
    for i in range(len(text)):
        if re.search(r'[A-Z]',text[i]):
            l1+=di['capital'][0]
            l2+=di['capital'][1]
            l3+=di['capital'][2]
            if len(l1)==29:
                total=total+[tuple(l1),tuple(l2),tuple(l3),tuple([0]*29)]
                l1=[] ; l2=[] ; l3=[]
                l1 =l1+ di[text[i].lower()][0]+[0]
                l2 = l2 + di[text[i].lower()][1] + [0]
                l3 = l3 + di[text[i].lower()][2] + [0]
            else:
                l1 = l1 +[0]+ di[text[i].lower()][0]
                l2 = l2 +[0]+ di[text[i].lower()][1]
                l3 = l3 +[0]+ di[text[i].lower()][2]
                if len(l1)==29:
                    total = total + [tuple(l1), tuple(l2), tuple(l3), tuple([0] * 29)]
                    l1 = []; l2 = [];  l3 = []
                else:
                    l1+=[0]; l2+=[0]; l3+=[0]

        elif re.search(r'\d',text[i]):
            l1+=[0,1]
            l2+=[0,1]
            l3+=[1,1]
            if len(l1)==29:
                total=total+[tuple(l1),tuple(l2),tuple(l3),tuple([0]*29)]
                l1=[] ; l2=[] ; l3=[]
                if not text[i]=='0':
                    l1 = l1 + di[chr(96+eval(text[i]))][0] + [0]
                    l2 = l2 + di[chr(96+eval(text[i]))][1] + [0]
                    l3 = l3 + di[chr(96+eval(text[i]))][2] + [0]
                else:
                    l1 = l1 + di['j'][0] + [0]
                    l2 = l2 + di['j'][1] + [0]
                    l3 = l3 + di['j'][2] + [0]
            else:
                if not text[i]=='0':
                    l1 = l1 +[0]+ di[chr(96+eval(text[i]))][0]
                    l2 = l2 +[0]+ di[chr(96+eval(text[i]))][1]
                    l3 = l3 +[0]+ di[chr(96+eval(text[i]))][2]
                else:
                    l1 = l1 + [0] + di['j'][0]
                    l2 = l2 + [0] + di['j'][1]
                    l3 = l3 + [0] + di['j'][2]
                if len(l1)==29:
                    total = total + [tuple(l1), tuple(l2), tuple(l3), tuple([0] * 29)]
                    l1 = [];   l2 = [];  l3 = []
                else:
                    l1 += [0];  l2 += [0];  l3 += [0]

        elif text[i]==' ':
            l1+=[0,0];  l2+=[0,0];  l3+=[0,0]
            if len(l1)==29:
                total = total + [tuple(l1), tuple(l2), tuple(l3), tuple([0] * 29)]
                l1 = [];    l2 = [];    l3 = []
            else:
                l1 += [0];  l2 += [0];   l3 += [0]

        else:
            l1 = l1 + di[text[i]][0]#l1 = l1 + di[text[i]][0]
            l2 = l2 + di[text[i]][1]
            l3 = l3 + di[text[i]][2]
            if len(l1)==29:
                total = total + [tuple(l1), tuple(l2), tuple(l3), tuple([0] * 29)]
                l1 = [];    l2 = [];    l3 = []
            else:
                l1 += [0];  l2 += [0];   l3 += [0]

    if len(total)==0:
        total=[tuple(l1[:-1]),tuple(l2[:-1]),tuple(l3[:-1])]
        return tuple(total)

    elif not len(total) == 0 and len(l1) == 0:
        total = total[:-1]

    elif not len(total)==0 and not len(l1)==29 and not len(l1)==0:
        while not len(l1)==29:
            l1+=[0]; l2+=[0]; l3+=[0]
        total = total + [tuple(l1), tuple(l2), tuple(l3)]

    return tuple(total)
#eg:
print(braille_page("hello 1st World!"))

