# inf
## Python Shenanigans
### one line file import 
```py
[line.strip() for line in open(path_to_file, "r")]
#Changing type of elements in list:
list(map(type, iterable))
type = str, int, float
iterable = list()
```
> split & join
```py
greet = "Ahoj ja som Adam"
greet.split() = default je " " --> greet.split(str_to_split_by)
ls = ["Ahoj", "ja", "som", "Adam"]
"".join(ls) --> "" = "string ktorym spajame"
```
> sort - manual
```py
ls = [45,12,10,5,8,7,3]
last_ls = []
while True:
  for i in range(0, len(ls)-1):
    if ls[i] > ls[i+1]:
      ls[i], ls[i+1] = ls[i+1], ls[i]
  if ls == last_ls:
    break
  last_ls = ls
```
> sort - python
```py
ls = [45,12,10,5,8,7,3]
ls.sort()
```
`ls.sort()` --> od najm. po najv.

`ls.sort(reverse=True)` --> od najv. po najm.
```py
dic = {
  "Peter": 12,
  "Jozef": 5,
  "Daniel": 8
}

dic.sort(key=lambda x: x.values())
#vysledok je sortnuty podla cisel
dic: {
  "Jozef": 5,
  "Daniel": 8,
  "Peter": 12
}

lines = [ ["Peter", [10,8,2]], ["Jozef", [18,4,3]], ["Daniel", [5,2,2]] ]
lines.sort(key=lambda x: x[1][0])
```
kde x je element v poli takze napr: `x = ["Peter", [10,8,2]]`

takze `x[1]` bude: `[10,8,2]`

a `x[1][0]` bude: 10 --> usporiadavame podla prveho prvku v podzozname

## Tkinter
### initialization
```py
from tkinter import *
root = Tk()
c = Canvas(root, width=x, height=y)
c.pack()
#code
root.mainloop()
```
### binding a key
```py
root.bind(key:string, function:obj)
#example
root.bind("<space>", print_data)
```
> common keys: \<Enter\>, \<Escape\>, \<space\>, a-z, 0-9

### objects
```py
c.create_line(x,y, width)
c.create_rectangle(x1,y1,x2,y2, fill)
c.create_oval(x1,y1,x2,y2, fill)
c.create_text(x,y, text:str)
```
