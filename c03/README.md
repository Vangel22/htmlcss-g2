# HTML Формулари

## Што се HTML формулари?

HTML формулари се структура што овозможува внесување и испраќање на податоци од корисникот до серверот.
Тие се клучен елемент за интерактивност на веб-страници.

---

## Полиња за внес на податоци

### 1. `input`

`input` е најчестото поле за внес на податоци. Има повеќе типови, како што се:

- **text**: Текстуален внес.
- **password**: За лозинки.
- **email**: Внес на е-пошта.
- **number**: Бројки.
- **radio** и **checkbox**: За селекции.
- **file**: За прикачување датотеки.

#### Пример:

```html
<label for="username">Корисничко име:</label>
<input type="text" id="username" name="username" />

<label for="password">Лозинка:</label>
<input type="password" id="password" name="password" />
```

\*\*\* for - атрибутот се користи за лабели и прави референца на id-то за елементот за кој се однесува таа лабела

### 2. `textarea`

`textarea` се користи за внесување на текст со повеќе линии

#### Пример:

```html
<label for="message">Порака:</label>
<textarea id="message" name="message" rows="4" cols="50"></textarea>
```

\*\*\* rows - атрибутот се користи за број на редови во празниот простор за пишување
\*\*\* cols - атрибутот се користи за број на колони во празниот простор за пишување

### 3. `select`

`select` се користи како листа со избор на повеќе опции

#### Пример:

```html
<label for="country">Изберете држава:</label>
<select id="country" name="country">
  <option value="mk">Северна Македонија</option>
  <option value="us">САД</option>
  <option value="de">Германија</option>
</select>
```

### 4. `button`

`button` претставува копче кое има некаква функција. Имаме повеќе типови од кои:

- **submit**: Default режим на копче, со него испраќаме некоја форма на клик.
- **button**: За копчиња кои сакаме да им додадеме некоја дополнителна Javascript логика.
- **reset**: Прави ресетирање/чистење на формата на нивните default/основни вредности.

#### Пример:

```html
<button type="submit">Испрати</button>
```

### 5. `label`

`label` лабела на полето за внес на податоци

#### Пример:

```html
<label for="email">Е-пошта:</label>
<input type="email" id="email" name="email" />
```

---

## GET и POST методи?

1. GET - податоците се испраќаат како дел од URL-то

#### Пример:

```html
<form action="/search" method="GET">
  <label for="query">Пребарај:</label>
  <input type="text" id="query" name="query" />
  <button type="submit">Пребарај</button>
</form>
```

2. POST - податоците се испраќаат како дел од телото на барањето

#### Пример:

```html
<form action="/submit" method="POST">
  <label for="name">Име:</label>
  <input type="text" id="name" name="name" />
  <button type="submit">Испрати</button>
</form>
```

## Multipart Формулари

- Се користат за испраќање на датотеки или комбинирани податоци

#### Пример:

```html
<form action="/upload" method="POST" enctype="multipart/form-data">
  <label for="file">Прикачи датотека:</label>
  <input type="file" id="file" name="file" />
  <button type="submit">Прикачи</button>
</form>
```

## Групирање на формулари

### `fieldset` - за групирање на формата во граница со нејзините елементи

### `legend` - за caption/натпис на fieldset

#### Пример:

```html
<form action="/submit" method="POST">
  <fieldset>
    <legend>Лични податоци</legend>
    <label for="fname">Име:</label>
    <input type="text" id="fname" name="fname" />
    <label for="lname">Презиме:</label>
    <input type="text" id="lname" name="lname" />
  </fieldset>
</form>
```
