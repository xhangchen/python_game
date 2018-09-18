import re
def checkio(s):
    l=re.split(r'[\s\,\.\?]',s)

    count=0
    vowel=['a','e','i','o','u','y']
    con=['b','c','d','f','g','h','j','k','l','m','n','p','q','r','s','t','v','w','x','z']
    for i in range(len(l)):
        flag=0
        f2=True
        if i==len(l)-1:
            flag=0
        for j in range(len(l[i])):
            if not l[i][j].lower() in vowel and not l[i][j].lower() in con :
                f2=False
                break
            elif l[i][j].lower() in vowel:
                if flag==1:
                    f2=False
                    break
                else:
                    flag=1
            elif l[i][j].lower() in con:
                if flag==-1:
                    f2=False
                    break
                else:
                    flag=-1
        if f2 and len(l[i])>1:
            count+=1
    return count

# eg:
print(checkio("To take a trivial example, which of us ever undertakes laborious physical exercise, except to obtain some advantage from it?"))
