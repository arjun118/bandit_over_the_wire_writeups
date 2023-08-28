this is not the optimal way but this is the way is solved this level, you can ofcourse get better solutions from the internet

get the text in data.txt file and execute this python script

```python
text = "Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi"
ans=""
for x in text:
    if ord(x)<65:
        ans+=x
    elif ord(x)>=97 and ord(x)<=122:
        a=ord(x)-13-97
        if a<0 : a+=26
        a+=97
        ans+=chr(a)
    elif ord(x)>=65 and ord(x)<=90:
        a=ord(x)-13-65
        if a<0 : a+=26
        a+=65
        ans+=chr(a)

            
print(ans)
```

replace the text with the content of data.txt

---

apparently this is a rot13 cypher and you can use the 
>tr 

command to translate the characters by certain positions

```bash
cat data.txt  | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

credits to the author of this [blog](https://sn0wbl4ck.wordpress.com/ctf/learning-basic-ctf/bandit-level-11-%E2%86%92-level-12/)

