import re
def checkio(s):
    string=''
    l=re.split(r':',s)
    if len(l[0])==1:
        string=''+'.. '
        b=bin(eval(l[0]))
        string+=(4-(len(b)-2))*'.'
        for i in range(2,len(b)):
            if b[i]=='0':
                string+='.'
            else:
                string+='-'
        string+=" : "
    else:
        b = bin(eval(l[0][0]))
        string += (2 - (len(b) - 2)) * '.'
        for i in range(2,len(b)):
            if b[i]=='0':
                string+='.'
            else:
                string+='-'
        string+=' '
        b = bin(eval(l[0][1]))
        string += (4 - (len(b) - 2)) * '.'
        for i in range(2, len(b)):
            if b[i] == '0':
                string += '.'
            else:
                string += '-'
        string+=" : "
    if len(l[1])==1:
        string+="... "
        b = bin(eval(l[1]))
        string += (4 - (len(b) - 2)) * '.'
        for i in range(2, len(b)):
            if b[i] == '0':
                string += '.'
            else:
                string += '-'
        string+=" : "
    else:
        b = bin(eval(l[1][0]))
        string += (3 - (len(b) - 2)) * '.'
        for i in range(2, len(b)):
            if b[i] == '0':
                string += '.'
            else:
                string += '-'
        string += ' '
        b = bin(eval(l[1][1]))
        string += (4 - (len(b) - 2)) * '.'
        for i in range(2, len(b)):
            if b[i] == '0':
                string += '.'
            else:
                string += '-'
        string += " : "
    if len(l[2]) == 1:
        string += "... "
        b = bin(eval(l[2]))
        string += (4 - (len(b) - 2)) * '.'
        for i in range(2, len(b)):
            if b[i] == '0':
                string += '.'
            else:
                string += '-'
    else:
        b = bin(eval(l[2][0]))
        string += (3 - (len(b) - 2)) * '.'
        for i in range(2, len(b)):
            if b[i] == '0':
                string += '.'
            else:
                string += '-'
        string += ' '
        b = bin(eval(l[2][1]))
        string += (4 - (len(b) - 2)) * '.'
        for i in range(2, len(b)):
            if b[i] == '0':
                string += '.'
            else:
                string += '-'

    return string
    #eg:
    print(checkio("10:37:49"))
