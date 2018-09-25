def non_repeat(s):
    sub=''
    if len(s)==0:
        return sub
    for i in range(len(s),0,-1):
        for j in range(len(s)-i+1):
            sub=s[j:j+i]
            flag=True
            for k in sub:
                if not sub.count(k)==1:
                    flag=False
                    break
            if flag:
                return sub
#eg:
print(non_repeat('abcabcffab'))
