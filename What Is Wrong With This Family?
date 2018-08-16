def is_family(l):
    count=0
    li=[]
    for i in l:
        f=True
        for j in l:
            if i[0]==j[1]:
                f=False
                break
        if f==True and  not i[0] in li:
            count+=1
            li.append(i[0])
    if count>1:
        return False

    for i in l:
        if[i[1],i[0]] in l:
            return False

    for i in l:
        for j in l:
            for k in l:
                if j[0]==k[0] and j[1] in i and k[1]in i and not j[1]==k[1]:
                    return False
    return True
#eg:
print(is_family([
  ['Logan', 'Mike'],
  ['Logan', 'Jack'],
  ['Mike', 'Jack']
]))
