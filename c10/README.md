## Транзиции

CSS транзицијата е ефект што овозможува промена на својствата на елемент кога ќе се случи промена на неговата состојба.

Карактеристики на транзициите:

- Работат само кога има промена во стиловите (на пример: hover, focus, active). Има потреба од интеракција.
- Се користат за поместување помеѓу две состојби.
  Се контролираат со следниве четири својства:

1. transition-property: кои својства ќе се променат (на пр. background-color, transform).
2. transition-duration: времетраење на промената (на пр. 0.3s).
3. transition-timing-function: брзина на промената (на пр. ease, linear).
4. transition-delay: задоцнување пред да почне транзицијата (на пр. 0.5s).

## Анимации

- CSS анимацијата е понапреден ефект кој овозможува креирање повеќестепени движења и промени на стиловите со тек на време.
  За разлика од транзициите, анимациите не бараат промена на состојба (на пр. hover) и можат да се репродуцираат бескрајно. Нема потреба од интеракција

Карактеристики на анимациите:

Се дефинираат со keyframes кои опишуваат различни состојби на елементот во различни моменти.
Се контролираат со следниве својства:

1. @keyframes: дефинирање на чекорите на анимацијата.
2. animation-name: името на keyframes што ќе се користат.
3. animation-duration: времетраење на анимацијата.
4. animation-timing-function: брзина на анимацијата.
5. animation-delay: задоцнување пред да почне.
6. animation-iteration-count: број на повторувања (infinite за бескрајно).
7. animation-direction: дали се репродуцира нанапред или наназад.

### **Разлика помеѓу транзиција и анимација**

| **Карактеристика**   | **Транзиција**                                | **Анимација**                                      |
| -------------------- | --------------------------------------------- | -------------------------------------------------- |
| **Кога се активира** | При промена на состојба (на пр. `hover`).     | Може да работи автоматски или континуирано.        |
| **Сложеност**        | Едноставна (почетна и крајна состојба).       | Сложена (повеќе состојби со `@keyframes`).         |
| **Контролирање**     | Потребна е интеракција за промена.            | Може да работи автоматски, без интеракција.        |
| **Примена**          | За мали и брзи ефекти (на пр. менување боја). | За покомплексни ефекти (на пр. движење, ротирање). |

## Демонстрација на разликите за работа со SVG:

1. <img>
   Применуваме CSS филтер (hue-rotate) за да ја промениме бојата на целата SVG слика кога ќе се помине со глувчето.
   Резултат: Само надворешниот ефект е достапен, не може да се стилизира внатрешната содржина на SVG.
2. <embed>
   Применуваме CSS стил за рамката на елементот <div> што го содржи <embed>.
   Резултат: Рамката ја менува бојата при hover, но содржината на SVG останува непроменета.
3. Inline svg
   Директно вграден SVG каде што:
   Првото SVG е статично без CSS класа.
   Второто SVG користи CSS класа circletest за интерактивно менување на бојата на circle.
   Резултат: Само inline SVG може директно да се стилизира и да реагира на интеракции со CSS.

- Кога треба да се користи:

1. img: Кога ви треба SVG како статична слика.
2. embed: Кога SVG треба да биде дел од документот, но без интеракции.
3. Inline svg: За интерактивност и целосна контрола со CSS.
