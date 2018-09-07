class Friend:
    name=''
    inv='No party...'
    def __init__(self,n):
        self.name=n
    def show_invite(self):
        return self.inv

class Party:
    place=''
    l=[]
    def __init__(self,s):
        self.place=s
        self.l=[]
    def add_friend(self,x):
        self.l.append(x)
    def del_friend(self,x):
        del self.l[self.l.index(x)]
    def send_invites(self,time):
        for i in self.l:
            i.inv=self.place+": "+time
#eg:
'''
party = Party("Midnight Pub")
nick = Friend("Nick")
john = Friend("John")
lucy = Friend("Lucy")
chuck = Friend("Chuck")

party.add_friend(nick)
party.add_friend(john)
party.add_friend(lucy)
party.send_invites("Friday, 9:00 PM")
party.del_friend(nick)
party.send_invites("Saturday, 10:00 AM")
party.add_friend(chuck)
print(john.show_invite())
print(lucy.show_invite())
print(nick.show_invite())
print(chuck.show_invite())
john.show_invite() == "Midnight Pub: Saturday, 10:00 AM"
lucy.show_invite() == "Midnight Pub: Saturday, 10:00 AM"
nick.show_invite() == "Midnight Pub: Friday, 9:00 PM"
chuck.show_invite() == "No party..."'''
