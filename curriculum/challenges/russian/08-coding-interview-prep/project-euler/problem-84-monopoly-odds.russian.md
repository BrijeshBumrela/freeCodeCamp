---
id: 5900f3c11000cf542c50fed3
challengeType: 5
title: 'Problem 84: Monopoly odds'
videoUrl: ''
localeTitle: 'Задача 84: Монопольные коэффициенты'
---

## Description
<section id="description"> В игре «Монополия» стандартная доска устанавливается следующим образом: <p> GO A1 CC1 A2 T1 R1 B1 CH1 B2 B3 JAIL H2 </p><p> C1 T2 </p><p> U1 H1 </p><p> C2 CH3 </p><p> C3R4 </p><p> R2 G3 </p><p> D1 CC3 </p><p> CC2 G2 </p><p> D2 G1 </p><p> D3 G2J F3 U2 F2 F1 R3 E3 E2 CH2 E1 FP </p><p> Игрок начинает с квадрата GO и добавляет оценки на двух 6-сторонних кубиках, чтобы определить количество квадратов, которые они продвигают по часовой стрелке. Без каких-либо дополнительных правил мы ожидали бы посетить каждый квадрат с равной вероятностью: 2,5%. Однако посадку на G2J (Go To Jail), CC (сундук сообщества) и CH (шанс) меняют это распределение. В дополнение к G2J и одной карте от каждой из CC и CH, которая приказывает игроку напрямую попасть в тюрьму, если игрок выполняет три последовательных удвоения, они не продвигают результат своего третьего броска. Вместо этого они отправляются непосредственно в тюрьму. В начале игры карты CC и CH перетасовываются. Когда игрок приземляется на CC или CH, они берут карту с верхней части соответствующей сваи и, следуя инструкциям, возвращаются на дно кучи. В каждой куче шестнадцать карточек, но для этой проблемы мы имеем дело только с карточками, которые заказывают движение; любая инструкция, не связанная с движением, будет проигнорирована, и игрок останется на квадрате CC / CH. Community Chest (2/16 карт): Advance to GO Перейти в JAIL </p><p> Шанс (10/16 карт): Advance to GO Перейти в JAIL Перейти к C1 Перейти к E3 Перейти к H2 Перейти к R1 Перейти к следующей R (железнодорожная компания) Перейти к следующей R Перейти к следующей U (коммунальная компания) Вернуться назад 3 квадрата , </p><p> Сердце этой проблемы связано с вероятностью посещения определенной площади. То есть, вероятность окончания на этом квадрате после рулона. По этой причине должно быть ясно, что за исключением G2J, для которого вероятность завершения на нем равна нулю, квадраты CH будут иметь наименьшую вероятность, так как 5/8 запрашивают движение на другой квадрат, и это окончательный квадрат, который игрок заканчивает на каждом броске, который нам интересен. Мы не будем проводить различие между «Just Visiting» и отправлением в JAIL, и мы также будем игнорировать правило о требовании двойного «выйти из тюрьмы», предполагая, что они платят, чтобы выйти на следующий ход. Начиная с GO и нумерации квадратов последовательно от 00 до 39, мы можем объединить эти двузначные числа, чтобы создать строки, соответствующие наборам квадратов. Статистически можно показать, что три наиболее популярных квадрата в порядке: JAIL (6.24%) = Square 10, E3 (3.18%) = Квадрат 24 и GO (3.09%) = Квадрат 00. Таким образом, эти три самых популярных квадрата могут быть перечислены с шестизначной модальной строкой: 102400. Если вместо использования двух 6-сторонних кубиков используются две 4-сторонние кости, найдите шестизначную модальную строку. </p></section>

## Instructions
<section id="instructions">
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: <code>euler84()</code> должен вернуть 101524.
    testString: 'assert.strictEqual(euler84(), 101524, "<code>euler84()</code> should return 101524.");'

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='js-seed'>

```js
function euler84() {
  // Good luck!
  return true;
}

euler84();

```

</div>



</section>

## Solution
<section id='solution'>

```js
// solution required
```
</section>
