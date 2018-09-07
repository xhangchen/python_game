def cut_sentence(s,num):
    if num>=len(s):
        return s
    else:
        if s[num]==' ':
            return s[:num]+"..."
        else:
            ls=s[:num]
            if len(ls)==1:
                return "..."
            else:
                while not ls[-1]==' ':
                    ls=ls[:-1]
                    if len(ls)==1:
                        break
            ls=ls[:-1]
            return ls+"..."
#eg:
#print(cut_sentence("Hi my name is Alex", 4))
