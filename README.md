# Втора лабораториска вежба по Софтверско инженерство

## Кристијан Митковски, бр. на индекс 195089

###  Control Flow Graph

Control flow graph - сликата е прикачена под име: " function_cfg "

### Цикломатска комплексност

Еден начин за пресметка на цикломатската комплексност е преку формулата:

V(G) = E - N + 2


E = 20 (број на ребра)
N = 16 (број на јазли)

V(G) = E - N + 2 = 20 - 16 + 2 = 6

Цикломатската комплексност на дадениот код е 6.

### Тест случаи според критериумот Every Branch

1. Проверка на условот дали user е null или дали user.getPassword() или user.getEmail() се null.

- Тест случаи:
- user е null или user.getPassword() или user.getEmail() се null.
- user не е null и user.getPassword() и user.getEmail() не се null.

2. Проверка на условот дали user.getUsername() е null.

- Тест случаи:
 - user.getUsername() е null.
 - user.getUsername() не е null.

3. Проверка на условот дали user.getEmail() содржи @ и точка.

- Тест случаи:
- user.getEmail() содржи @ и точка.
- user.getEmail() не содржи @ или точка.

4. Циклус за секој елемент existingUser во листата allUsers.

- Тест случаи:
- allUsers е празна листа.
- allUsers има еден елемент.
- allUsers има повеќе од еден елемент.
5. Проверка на условот дали existingUser.getEmail() е ист како user.getEmail().

- Тест случаи:
- existingUser.getEmail() и user.getEmail() се исти.
- existingUser.getEmail() и user.getEmail() не се исти.

Овие тест случаи ги покриваат сите можни премини во кодот според Every Branch критериумот.

### Тест случаи според критериумот Multiple Condition

Примери за тест случаи според Multiple Condition критериумот се:

1. user е null, user.getPassword() е null, user.getEmail() е null.
- Сите услови се true, затоа ќе се отфрли исклучокот (RuntimeException).

2. user е null, user.getPassword() е null, user.getEmail() не е null.
- Првиот и вториот услов се true, третиот услов е false.
- Се отфрла исклучокот.

3. user е null, user.getPassword() не е null, user.getEmail() е null.
- Првиот и третиот услов се true, вториот услов е false.
- Се отфрла исклучокот.

4. user е null, user.getPassword() не е null, user.getEmail() не е null.
- Првиот услов е true, останатите два услови се false.
- Се отфрла исклучокот.

5. user не е null, user.getPassword() е null, user.getEmail() е null.
- Првиот услов е false, останатите два услови се true.
- Се исфрла исклучокот.

6. user не е null, user.getPassword() е null, user.getEmail() не е null.
- Првиот и третиот услов се false, вториот услов е true.
- Се исфрла исклучокот.

7. user не е null, user.getPassword() не е null, user.getEmail() е null.
- Првиот и вториот услов се false, третиот услов е true.
- Се отфрла исклучокот.

8. user не е null, user.getPassword() не е null, user.getEmail() не е null.
- Сите услови се false.
- Не се отфрла исклучок.