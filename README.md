# SI_lab2_183272
## Димитар Слезенковски, број на индекс 183272

**Група на код:**

Ја добив групата на код 3

* Control Flow Graph

![CFG](CFG.jpg)


* Цикломатска комплексност
Цикломатската комплексност на функцијата е 9.
Истата ја добив со помош на формулата P+1, каде P е бројот на предикатни јазли. Во случајoв P=8, па цикломатската комплексност изнесува 9.

* Тест случаи според критериумот **Every Branch**

Табелата за овој критериум може да ја најдете во репото под име EBC.xlsx. 
Има вкупно 11 тест случаи според овој критериум.

![Every Branch Criteria](EveryBranchC.jpg)

* Тест случаи според критериумот **Every Path**

Табелата за овој критериум може да ја најдете во репото под име EPC.xlsx. 
Има вкупно 11 тест случаи според овој критериум.

![Every Path Criteria](EPC.png)

* Објаснување на напишаните unit tests

**Every Branch tests**

Inputs -> (Корисничко име, Лозинка, Е-маил)\
User1 (null)\
User2 (Dimitar, null, asd@gmail.com)\
User3 (Dimitar, dimitars, dsa@gmail.com)\
User4 (Dimitar, taska, "")\
User5 (Dimitar, Sl#z#nkovski, p!ck1eR!ck@gmail.com)\
User6 (Dimitar, Sl3z3novsk!, john@gmail.com)\
User7 (Dimitar, Pa2$Wor|), asdf@gmail.com)\
User8 (Dimitar, Sl3z3nk0vsk1, haos@gmail.com)\
User9 (Dimitar, res!stor, nesumodtuka@gmail.com)\
User10 (Dimitar, C@p@c1t0R, "")\

```
Кај првиот тест случај (User1) вредноста на user објектот е null. Со ова првиот услов од кодот е исполнет и програмата фрла exception. Тестот ги опфаќа A и B јазлите. 

Кај вториот тест случај (User2) вредноста на променливата корисничко име е null со што се задоволува вториот услов од кодот и програмата фрла exception. Тестот ги опфаќа A, C и D јазлите.

Кај треттиот тест случај (User3) вредноста на корисничкото име се содржи во вредноста на лозинката. Со тоа се задоволува условот if(passwordLower.contains(user.getUsername().toLowerCase())) и програмата враќа false.  Тестот ги опфаќа A, C, E и F јазлите.

Кај четврттиот тест случај (User4) вредноста на лозинката е помала од 8 карактери и со условот if(passwordLower.length()<8) е задоволен и програмата враќа false. Тестот ги опфаќа A, C, E, G, и H јазлите.

Кај петтиот тест случај (User5) имаме објект каде што променливата лозинка има погрешна вредност (не содржи број). Поради ова условот if (!digit || !upper || !special) нема да биде задоволен и програмата ќе врати резултат false. Овој тест ги опфаќа јазлите A, C, E, G, I, J, K, M, O, P, Q, R, L, S и Т.

Kaj шесттиот тест случај (User6) имеме објект каде што внесените вредности на променливите се валидни па затоа програмата ќе врати true. Поточно има соодветна внесена вредост за корисничко име и лозинка и дополнително лозинката не е помала од 8 карактери и содржи и бројка и голема буква и спрецијален знак. Овој тест ги опфаќа јазлите A, C, E, G, I, J, K, M, N, O, P, Q, R, L, S и U.

Kaj седмиот тест случај (User7) имеме објект каде што внесените вредности на променливите се валидни па затоа програмата ќе врати true. Поточно има соодветна внесена вредост за корисничко име и лозинка и дополнително лозинката не е помала од 8 карактери и содржи и бројка и голема буква и спрецијален знак. Овој тест ги опфаќа јазлите A, C, E, G, I, J, K, M, N, O, P, Q, R, L, S и U.

Кај осмиот тест случај (User8) имаме објект каде што променливата лозинка има погрешна вредност (не содржи специјален знак). Поради ова условот if (!digit || !upper || !special) нема да биде задоволен и програмата ќе врати резултат false. Овој тест ги опфаќа јазлите A, C, E, G, I, J, K, M, N, O, P, Q, L, S и Т.

Кај деветтиот тест случај (User9) имаме објект каде што променливата лозинка има погрешна вредност (не содржи бројка и голема буква). Поради ова условот if (!digit || !upper || !special) нема да биде задоволен и програмата ќе врати резултат false. Овој тест ги опфаќа јазлите A, C, E, G, I, J, K, M, O, Q, R, L, S и Т.

Kaj десеттиот тест случај (User10) имеме објект каде што внесените вредности на променливите се валидни па затоа програмата ќе врати true. Поточно има соодветна внесена вредост за корисничко име и лозинка и дополнително лозинката не е помала од 8 карактери и содржи и бројка и голема буква и спрецијален знак. Овој тест ги опфаќа јазлите A, C, E, G, I, J, K, M, N, O, P, Q, R, L, S и U.

```

**Every Path tests**

Inputs -> (Корисничко име, Лозинка, Е-маил)\
User1 (null)\
User2 (Dimitar, null, asd@gmail.com)\
User3 (Dimitar, dimitar, dsa@gmail.com)\
User4 (Dimitar, asdf, "")\
User5 (Dimitar, Sl3z#nkovsk1, p!ck1eR!ck@gmail.com)\
User6 (Dimitar, Sl3z3nkovsk1, john@gmail.com)\
User7 (Dimitar, Slezenkovski, asdf@gmail.com)\
User8 (Dimitar, Sl#z#nkovsk!, haos@gmail.com)\
User9 (Dimitar, 123456789, nesumodtuka@gmail.com)\
User10 (Dimitar, password, "")\

```
Кај првиот тест случај (User1) вредноста на user објектот е null. Со ова првиот услов од кодот е исполнет и програмата фрла exception. Тестот ги опфаќа A и B јазлите. 

Кај вториот тест случај (User2) вредноста на променливата корисничко име е null со што се задоволува вториот услов од кодот и програмата фрла exception. Тестот ги опфаќа A, C и D јазлите.

Кај треттиот тест случај (User3) вредноста на корисничкото име се содржи во вредноста на лозинката. Со тоа се задоволува условот if(passwordLower.contains(user.getUsername().toLowerCase())) и програмата враќа false.  Тестот ги опфаќа A, C, E и F јазлите.

Кај четврттиот тест случај (User4) вредноста на лозинката е помала од 8 карактери и со условот if(passwordLower.length()<8) е задоволен и програмата враќа false. Тестот ги опфаќа A, C, E, G, и H јазлите.

Kaj петтиот тест случај (User5) имеме објект каде што внесените вредности на променливите се валидни па затоа програмата ќе врати true. Поточно има соодветна внесена вредост за корисничко име и лозинка и дополнително лозинката не е помала од 8 карактери и содржи и бројка и голема буква и спрецијален знак. Овој тест ги опфаќа јазлите A, C, E, G, I, J, K, M, N, O, P, Q, R, L, S и U.

Кај шесттиот тест случај (User6) имаме објект каде што променливата лозинка има погрешна вредност (не содржи специјален знак). Поради ова условот if (!digit || !upper || !special) нема да биде задоволен и програмата ќе врати резултат false. Овој тест ги опфаќа јазлите A, C, E, G, I, J, K, M, N, O, P, Q, L, S и Т.

Кај седмиот тест случај (User7) имаме објект каде што променливата лозинка има погрешна вредност (не содржи бројка и специјален знак). Поради ова условот if (!digit || !upper || !special) нема да биде задоволен и програмата ќе врати резултат false. Овој тест ги опфаќа јазлите A, C, E, G, I, J, K, M, O, P, Q, L, S и Т.

Кај осмиот тест случај (User8) имаме објект каде што променливата лозинка има погрешна вредност (не содржи бројка). Поради ова условот if (!digit || !upper || !special) нема да биде задоволен и програмата ќе врати резултат false. Овој тест ги опфаќа јазлите A, C, E, G, I, J, K, M, O, P, Q, R, L, S и Т.

Кај деветтиот тест случај (User9) имаме објект каде што променливата лозинка има погрешна вредност (не содржи голема буква и специјален знак). Поради ова условот if (!digit || !upper || !special) нема да биде задоволен и програмата ќе врати резултат false. Овој тест ги опфаќа јазлите A, C, E, G, I, J, K, M, N, O, Q, L, S и Т.

Кај десеттиот тест случај (User10) имаме објект каде што променливата лозинка има погрешна вредност (не содржи ниту бројка, ниту буква, ниту специјален знак). Поради ова условот if (!digit || !upper || !special) нема да биде задоволен и програмата ќе врати резултат false. Овој тест ги опфаќа јазлите A, C, E, G, I, J, K, M, O, Q, L, S и Т.

```
