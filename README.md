# mss
вхідні дані
![image](https://github.com/ronin49/mss/assets/49647614/bfe72eb2-0d75-4b0d-8b1b-32020919929c)
<details>
<summary>мета</summary>
Дослідити і оцінити регресійну модель для даної вибірки, використовуючи різні методи оцінки коефіцієнтів регресії та провести статистичний аналіз отриманих результатів.
</details>

<details>
<summary>постановка задачі</summary>
1. Перевірити вибірку на однорідність (критерій Бартлета, Кохрена, модифікація Мкритерію Бартлета, граничний критерій неоднорідності дисперсій Харисона і Ман-Кейба, параметричний критерій Голдфільда і Квандта) 2. Оцінити коефіцієнти регресії за допомогою узагальненого методу найменших квадратів. 3. Оцінити коефіцієнти регресії за допомогою методу найменших квад-ратів. 4. Виконати статистичний аналіз результатів оцінювання. 5. Оцінити коефіцієнти регресії першого порядку. 6. Здійснити оцінювання узагальненої регресійної моделі.
</details>

<details>
<summary>теоретичні відомості: метод розвʼязання та його опис</summary>
  Критерій Бартлета - це статистичний тест, який використовується для перевірки гіпотези про однорідність дисперсій у групах даних. Цей критерій чутливий до нормального розподілу даних.

Його головна ідея полягає в порівнянні дисперсій між групами даних. Якщо дисперсії однорідні (тобто різниці між групами нестатистично значущі), то значення критерію буде незначним, що свідчить про прийняття нульової гіпотези про однорідність дисперсій. В іншому випадку, якщо дисперсії статистично відрізняються, значення критерію буде великим, що означатиме відхилення від нульової гіпотези.

Формально, для застосування критерію Бартлета ви можете використовувати наступні кроки:

1. Сформулювати нульову та альтернативну гіпотези. Нульова гіпотеза припускає, що дисперсії всіх груп даних однорідні, тоді як альтернативна гіпотеза стверджує, що дисперсії відрізняються хоча б у двох групах.
2. Обчислити значення критерію Бартлета.
3. Порівняти обчислене значення критерію з критичним значенням з відповідної таблиці для визначення статистичної значущості результату.
4. Зробити висновок про однорідність або неоднорідність дисперсій в групах даних на основі порівняння обчисленого значення критерію та його критичного значення.

Зокрема, для застосування критерію Бартлета важливо мати рівність кількості спостережень у різних групах та нормальний розподіл даних.

Критерій Кохрена - це статистичний тест, який використовується для перевірки однорідності дисперсій у групах даних. Він також відомий як критерій однорідності дисперсій.

Основна ідея критерію полягає у порівнянні максимальної та мінімальної дисперсій між групами. Якщо ці значення статистично не відрізняються, то припускається, що дисперсії у всіх групах однорідні.

Процедура застосування критерію Кохрена така:

1. Сформулювати нульову та альтернативну гіпотези. Нульова гіпотеза припускає, що дисперсії у всіх групах однорідні, альтернативна гіпотеза - що є хоча б одна відмінність між дисперсіями.
2. Обчислити максимальну та мінімальну дисперсії в групах.
3. Обчислити вибіркову дисперсію по кожній групі.
4. Обчислити статистику Кохрена шляхом ділення максимальної вибіркової дисперсії на суму всіх вибіркових дисперсій.
5. Порівняти обчислене значення статистики Кохрена з критичним значенням з таблиці для визначення статистичної значущості результату.
6. Зробити висновок щодо однорідності або неоднорідності дисперсій в групах на основі порівняння обчисленого значення статистики Кохрена та його критичного значення.

Критерій Кохрена є досить простим у застосуванні та може бути використаний для перевірки однорідності дисперсій у випадку, коли кількість груп не більше деякого певного обмеження, зазвичай до десяти.
Модифікація М-критерію Бартлета - це адаптація критерію Бартлета для випадку, коли дані мають нормальний розподіл, але немають однорідність дисперсій. Цей критерій використовується для порівняння дисперсій у групах даних, коли вибірки не мають однакових дисперсій.

Процедура застосування модифікації М-критерію Бартлета аналогічна до звичайного критерію Бартлета, але перед застосуванням необхідно виконати попередню нормалізацію даних. Після цього кроки такі:

1. Сформулювати нульову та альтернативну гіпотези. Нульова гіпотеза стверджує, що всі групи мають однакову дисперсію, альтернативна гіпотеза - що є хоча б одна відмінність між дисперсіями.
2. Виконати нормалізацію даних (якщо необхідно).
3. Обчислити вибіркові дисперсії по кожній групі.
4. Обчислити середню вибіркову дисперсію.
5. Обчислити статистику М-критерію Бартлета, яка базується на порівнянні середньої вибіркової дисперсії з максимальною вибірковою дисперсією.
6. Порівняти обчислене значення статистики М-критерію Бартлета з критичним значенням з таблиці для визначення статистичної значущості результату.
7. Зробити висновок щодо однорідності або неоднорідності дисперсій в групах на основі порівняння обчисленого значення статистики М-критерію Бартлета та його критичного значення.

Цей підхід дозволяє враховувати нормальний розподіл даних та вирішує проблему нерівномірності дисперсій у групах.
Граничний критерій неоднорідності дисперсій Харісона і Манна-Кейба (Hartley's and Mann-Whitney's heteroscedasticity test) - це статистичний тест, який використовується для оцінки однорідності дисперсій у групах даних. Він оцінює максимальне відношення дисперсій між групами.

Процедура застосування цього критерію наступна:

1. Сформулювати нульову та альтернативну гіпотези. Нульова гіпотеза припускає, що всі групи мають однакову дисперсію, тоді як альтернативна гіпотеза стверджує, що є хоча б одна відмінність між дисперсіями.
   
2. Обчислити вибіркові дисперсії по кожній групі.

3. Знайти максимальне і мінімальне значення вибіркових дисперсій.

4. Обчислити відношення максимальної до мінімальної вибіркової дисперсії.

5. Знайти критичне значення граничного відношення дисперсій відповідно до обраного рівня значущості та кількості груп.

6. Порівняти обчислене відношення з критичним значенням.

7. Зробити висновок щодо однорідності або неоднорідності дисперсій в групах на основі порівняння обчисленого відношення з критичним значенням.

Цей критерій виявляється корисним в тих випадках, коли потрібно оцінити неоднорідність дисперсій у групах, особливо коли розподіл даних може бути важко інтерпретувати за допомогою інших методів.
Параметричний критерій Голдфільда і Квандта - це статистичний тест, який використовується для перевірки гіпотези про однорідність дисперсій у групах даних. Цей критерій передбачає, що дані мають нормальний розподіл.

Процедура застосування критерію Голдфільда і Квандта наступна:

1. Сформулювати нульову та альтернативну гіпотези. Нульова гіпотеза припускає, що дисперсії в усіх групах однакові, тоді як альтернативна гіпотеза стверджує, що є хоча б одна відмінність між дисперсіями.

2. Обчислити вибіркові дисперсії по кожній групі.

3. Впорядкувати вибіркові дисперсії за зростанням.

4. Визначити кількість спостережень у кожній групі, включаючи всі групи.

5. Знайти критичне значення для потрібного рівня значущості та кількості груп у таблиці критичних значень для критерію Голдфільда і Квандта.

6. Порівняти обчислене критерієм значення тесту з критичним значенням.

7. Зробити висновок щодо однорідності або неоднорідності дисперсій в групах на основі порівняння обчисленого значення критерію з критичним.

Цей критерій є корисним у випадках, коли потрібно перевірити однорідність дисперсій у групах і дані відповідають умовам нормального розподілу. Він може бути особливо корисним, коли кількість груп велика і групи мають різний обсяг.
Узагальнений метод найменших квадратів (УМНК) - це метод оцінювання параметрів регресійної моделі, який використовується у випадку, коли відомо, що похибки моделі не мають гауссівського розподілу. Цей метод є розширенням класичного методу найменших квадратів (МНК), який передбачає нормальний розподіл похибок.

Припустимо, що ми маємо регресійну модель у вигляді:

\[Y_i = \beta_0 + \beta_1 X_{i1} + \beta_2 X_{i2} + \ldots + \beta_k X_{ik} + \varepsilon_i\]

де \(Y_i\) - це залежна змінна, \(X_{ij}\) - незалежні змінні, \(\beta_0, \beta_1, \ldots, \beta_k\) - параметри моделі, а \(\varepsilon_i\) - випадкові похибки.

Основна ідея узагальненого методу найменших квадратів полягає в мінімізації суми квадратів вагованих відхилень між спостережуваними значеннями і значеннями, передбаченими моделлю. Ваги при цьому встановлюються відповідно до властивостей похибок.

Процедура оцінювання параметрів за допомогою УМНК включає наступні кроки:

1. Сформулювати регресійну модель і припущення про похибки моделі.
2. Обрати ваги для мінімізації функції втрат (зазвичай ваги вибираються залежно від природи похибок).
3. Мінімізувати суму квадратів вагованих відхилень між спостережуваними значеннями і значеннями, передбаченими моделлю.
4. Оцінити параметри моделі, що мінімізують цю суму.

Оцінки параметрів, отримані за допомогою УМНК, зазвичай є менш ефективними порівняно з оцінками, отриманими за допомогою МНК у випадку, коли похибки мають нормальний розподіл. Однак УМНК залишається корисним інструментом у випадках, коли це припущення про розподіл похибок не виконується.
Метод найменших квадратів (МНК) - це стандартний метод оцінювання параметрів регресійної моделі, який полягає в мінімізації суми квадратів відхилень між спостережуваними значеннями залежної змінної і значеннями, передбаченими моделлю.

Припустимо, що у нас є регресійна модель у вигляді:

\[Y_i = \beta_0 + \beta_1 X_{i1} + \beta_2 X_{i2} + \ldots + \beta_k X_{ik} + \varepsilon_i\]

де \(Y_i\) - це залежна змінна, \(X_{ij}\) - незалежні змінні, \(\beta_0, \beta_1, \ldots, \beta_k\) - параметри моделі, а \(\varepsilon_i\) - випадкові похибки.

Основна ідея МНК полягає в тому, щоб знайти такі значення параметрів \(\beta_0, \beta_1, \ldots, \beta_k\), які мінімізують суму квадратів відхилень між спостережуваними і передбаченими значеннями залежної змінної. Формально, ця сума квадратів відхилень (SSE) обчислюється як:

\[SSE = \sum_{i=1}^{n} (Y_i - \hat{Y}_i)^2\]

де \(\hat{Y}_i\) - це передбачене значення \(Y_i\), яке обчислюється за допомогою регресійної моделі.

Оцінки параметрів \(\beta_0, \beta_1, \ldots, \beta_k\), що мінімізують SSE, можуть бути знайдені аналітично або чисельно за допомогою різних методів оптимізації, таких як градієнтний спуск або метод Ньютона.

Оцінки, отримані за допомогою МНК, надають найкращі значення параметрів для регресійної моделі в тому сенсі, що вони мінімізують суму квадратів відхилень. Цей метод є широко використовуваним і дозволяє отримати найкращі оцінки параметрів, якщо припущення про нормальний розподіл похибок виконується.

Для виконання статистичного аналізу результатів оцінювання параметрів регресії за допомогою методу найменших квадратів, можна виконати наступні кроки:

1. **Перевірка припущень моделі**: Перш ніж переходити до аналізу результатів, слід перевірити припущення, які лежать в основі регресійної моделі, такі як нормальність розподілу похибок, лінійність зв'язку між змінними тощо. Для цього можна використовувати графічні методи (наприклад, Q-Q графіки, графіки залишків), а також статистичні тести (наприклад, тест Шапіро-Уілка для нормальності розподілу похибок).

2. **Оцінка значущості параметрів моделі**: Для оцінки статистичної значущості кожного з параметрів регресії можна використовувати t-тест. Порівнюючи оцінки коефіцієнтів регресії з їх стандартними помилками, можна обчислити t-статистики та визначити статистичну значущість параметрів на певному рівні значущості.

3. **Оцінка адекватності моделі**: Для оцінки того, наскільки добре побудована модель пояснює варіацію в залежній змінній, можна використовувати різноманітні статистичні метрики, такі як коєфіцієнт детермінації \(R^2\), кореляційний коефіцієнт Пірсона, а також F-тест на значущість моделі в цілому.

4. **Аналіз залишків моделі**: Перевірка залишків моделі є важливим етапом аналізу. Графіки залишків (наприклад, розподіл залишків, графік "залишків-прогнозованих значень") можуть допомогти виявити систематичні відхилення в моделі. Додатково можна застосувати тести на автокореляцію залишків, якщо це відповідає контексту дослідження.

5. **Перевірка мультіколінеарності**: Якщо в моделі присутня мультіколінеарність (високий рівень кореляції між незалежними змінними), це може спричинити проблеми при оцінці параметрів. Для виявлення мультіколінеарності можна використовувати статистичні тести, такі як визначення факторного числа, або обчислення кореляційної матриці між змінними.

6. **Інтерпретація результатів**: Нарешті, після виконання усіх статистичних аналізів, слід зробити висновки щодо статистичної значущості та адекватності моделі, а також провести інтерпретацію кожного з коефіцієнтів регресії в контексті дослідження.

Ці кроки допоможуть вам здійснити повний та об'єктивний статистичний аналіз результатів оцінювання параметрів регресії за допомогою методу найменших квадратів.

Оцінка коефіцієнтів регресії першого порядку полягає у визначенні параметрів \( \beta_0 \) та \( \beta_1 \) у рівнянні простої лінійної регресії:

\[ Y = \beta_0 + \beta_1 X + \varepsilon \]

де \( Y \) - залежна змінна, \( X \) - незалежна змінна, \( \beta_0 \) та \( \beta_1 \) - коефіцієнти регресії, а \( \varepsilon \) - випадкова похибка.

Для оцінки коефіцієнтів регресії першого порядку можна використовувати метод найменших квадратів (МНК). Метод полягає у мінімізації суми квадратів відхилень між фактичними значеннями залежної змінної та значеннями, які передбачає модель регресії.

Оцінки коефіцієнтів \( \beta_0 \) та \( \beta_1 \) можуть бути знайдені за наступними формулами МНК:

\[ \hat{\beta}_1 = \frac{\sum_{i=1}^{n}(x_i - \bar{x})(y_i - \bar{y})}{\sum_{i=1}^{n}(x_i - \bar{x})^2} \]

\[ \hat{\beta}_0 = \bar{y} - \hat{\beta}_1 \bar{x} \]

де \( \hat{\beta}_1 \) - оцінка коефіцієнта нахилу, \( \hat{\beta}_0 \) - оцінка вільного члена, \( x_i \) та \( y_i \) - значення змінних \( X \) та \( Y \) відповідно для \( i \)-го спостереження, \( \bar{x} \) та \( \bar{y} \) - середні значення змінних \( X \) та \( Y \) відповідно, а \( n \) - кількість спостережень.

Після обчислення цих оцінок можна перевірити їх статистичну значимість за допомогою t-тесту. Також можна визначити коефіцієнт детермінації \( R^2 \) для оцінки якості підгонки моделі до даних.

Узагальнена регресійна модель використовується, коли дані не відповідають класичним умовам простої лінійної регресії. Це може включати випадки, коли залежна змінна не має нормального розподілу, коли похибки мають гетероскедастичну або асиметричну структуру, або коли залежність між змінними не лінійна.

Для оцінки узагальненої регресійної моделі можна використовувати методи, такі як метод найменших квадратів з вагами, робустні методи оцінювання (наприклад, регресія Хубера), або методи, які враховують структуру похибок (наприклад, гребнева регресія або ласо).

Основні кроки оцінювання узагальненої регресійної моделі:

1. **Вибір моделі**: Спочатку необхідно визначити структуру моделі, включаючи вибір залежних і незалежних змінних, а також вибір форми функціонального відношення між ними.

2. **Визначення функції ваг**: У випадках, коли похибки мають гетероскедастичну або асиметричну структуру, можна використовувати функції ваг, які дають більший вагу менш варіативним спостереженням.

3. **Оцінка параметрів моделі**: Після визначення моделі та функції ваг можна застосувати методи оцінювання, такі як МНК з вагами або робустні методи, для отримання оцінок параметрів моделі.

4. **Оцінка статистичної значимості параметрів**: Після отримання оцінок параметрів можна провести тести на їх статистичну значимість, такі як t-тест або тести Вальда.

5. **Оцінка адекватності моделі**: Для оцінки адекватності моделі можна використовувати різноманітні статистичні тести, такі як тест на гомоскедастичність похибок, тест на адекватність підгонки моделі тощо.

6. **Перевірка припущень**: Нарешті, необхідно перевірити, чи виконуються припущення, на яких ґрунтується модель, та вирішити, чи вони задовольняються. 

Ці кроки допоможуть здійснити оцінювання узагальненої регресійної моделі та зробити висновки щодо її адекватності та значущості.
</details>
<details>
<summary>опис програмного забезпечення</summary>
  <details>
<summary>вихідні дані</summary>
> formula <- data$net_sqm*data$center_distance*data$metro_distance*data$floor*data$age*data$price
> bartlett.test(formula,data$bedroom_count)

        Bartlett test of homogeneity of variances

data:  formula and data$bedroom_count
Bartlett's K-squared = 2043.1, df = 13, p-value < 2.2e-16
> cohensD(formula,data$bedroom_count)
[1] 0.7679533
> lm(formula ~ data$bedroom_count)

Call:
lm(formula = formula ~ data$bedroom_count)

Coefficients:
       (Intercept)  data$bedroom_count  
         6.276e+14          -2.946e+13  

> mod <- lm(formula ~ data$bedroom_count)
> X <- cbind(1,data$bedroom_count)
> betaHat <- solve(t(X) %*% X) %*% t(X) %*% formula
> var_betaHat <- anova(mod)[[3]][2] * solve(t(X) %*% X)
> mod$coef
       (Intercept) data$bedroom_count 
      6.276244e+14      -2.945699e+13 
> c(betaHat[1], betaHat[2])
[1]  6.276244e+14 -2.945699e+13
> summary(mod)$coefficients[, 2]
       (Intercept) data$bedroom_count 
      2.624523e+13       5.868340e+12 
> sqrt(diag(var_betaHat))
[1] 2.624523e+13 5.868340e+12
> harrison_mccabe(mod)
# A tibble: 1 × 4
  statistic p.value parameter alternative
      <dbl>   <dbl>     <dbl> <chr>      
1     0.541   0.473       0.5 less       
>
</details>
  <details>
<summary>інструкцію користувача</summary>
?
</details>
  <details>
<summary>контрольний приклад</summary>
?
</details>
  <details>
<summary>таблицю варіантів</summary>
?
</details>
</details>
<details>
<summary>лістинг програми</summary>

R version 4.3.2 (2023-10-31 ucrt) -- "Eye Holes"
Copyright (C) 2023 The R Foundation for Statistical Computing
Platform: x86_64-w64-mingw32/x64 (64-bit)

R is free software and comes with ABSOLUTELY NO WARRANTY.
You are welcome to redistribute it under certain conditions.
Type 'license()' or 'licence()' for distribution details.

  Natural language support but running in an English locale

R is a collaborative project with many contributors.
Type 'contributors()' for more information and
'citation()' on how to cite R or R packages in publications.

Type 'demo()' for some demos, 'help()' for on-line help, or
'help.start()' for an HTML browser interface to help.
Type 'q()' to quit R.

> data <- read.csv('house.csv')
> View(data)
> formula <- data$net_sqm*data$center_distance*data$metro_distance*data$floor*data$age*data$price
> bartlett.test(formula,data$bedroom_count)

        Bartlett test of homogeneity of variances

data:  formula and data$bedroom_count
Bartlett's K-squared = 2043.1, df = 13, p-value < 2.2e-16

> library(lsm)
Error in library(lsm) : there is no package called ‘lsm’
> library(lsr)
Error in library(lsr) : there is no package called ‘lsr’
> library(psych)
> ? cohen.d
starting httpd help server ... done
> cohen.d(formula,"bedroom_count")
Error in data[, group] : incorrect number of dimensions
> cohen.d(formula~data$bedroom_count)
Error in get(ps$y) : first argument has length > 1
Error in cohen.d(formula ~ data$bedroom_count) : 
  You need to specify the data if asking for a specific variable
> cohen.d(formula,data$bedroom_count)
Error in `.rowNamesDF<-`(x, value = value) : invalid 'row.names' length
> cohen.d(data,data$bedroom_count)
Error in svd(X) : infinite or missing values in 'x'
In addition: Warning messages:
1: In cor(diffs, use = use, method = method) :
  the standard deviation is zero
2: In cov2cor(xvals$rwg) :
  diag(.) had 0 or NA entries; non-finite result is doubtful
3: In cor(new.data[, (nvar + 1):ncol(new.data)], diffs, use = "pairwise",  :
  the standard deviation is zero
> cohen.d(data$net_sqm,data$bedroom_count)
Error in `.rowNamesDF<-`(x, value = value) : invalid 'row.names' length
> cohen.d(data$net_sqm,data)
Error in data[, group] : incorrect number of dimensions
> cohen.d(data,data$bedroom_count)
Error in svd(X) : infinite or missing values in 'x'
In addition: Warning messages:
1: In cor(diffs, use = use, method = method) :
  the standard deviation is zero
2: In cov2cor(xvals$rwg) :
  diag(.) had 0 or NA entries; non-finite result is doubtful
3: In cor(new.data[, (nvar + 1):ncol(new.data)], diffs, use = "pairwise",  :
  the standard deviation is zero
> install.packages('lsr')
Installing package into ‘C:/Users/OZadorozhnyi/AppData/Local/R/win-library/4.3’
(as ‘lib’ is unspecified)
--- Please select a CRAN mirror for use in this session ---
trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/lsr_0.5.2.zip'
Content type 'application/zip' length 209457 bytes (204 KB)
downloaded 204 KB

package ‘lsr’ successfully unpacked and MD5 sums checked

The downloaded binary packages are in
        C:\Users\OZadorozhnyi\AppData\Local\Temp\Rtmpqsabaz\downloaded_packages
> library(lsr)
> cohenD(formula,data$bedroom_count)
Error in cohenD(formula, data$bedroom_count) : 
  could not find function "cohenD"
> cohensD(formula,data$bedroom_count)
[1] 0.7679533
> install.packages('skedastic')
Installing package into ‘C:/Users/OZadorozhnyi/AppData/Local/R/win-library/4.3’
(as ‘lib’ is unspecified)
also installing the dependencies ‘listenv’, ‘parallelly’, ‘future’, ‘globals’, ‘digest’, ‘shape’, ‘future.apply’, ‘numDeriv’, ‘progressr’, ‘SQUAREM’, ‘fastmap’, ‘crayon’, ‘prettyunits’, ‘colorspace’, ‘diagram’, ‘lava’, ‘utf8’, ‘cachem’, ‘lobstr’, ‘farver’, ‘labeling’, ‘munsell’, ‘RColorBrewer’, ‘viridisLite’, ‘tzdb’, ‘prodlim’, ‘timechange’, ‘cli’, ‘magrittr’, ‘pillar’, ‘tidyselect’, ‘vctrs’, ‘stringi’, ‘fansi’, ‘pkgconfig’, ‘cpp11’, ‘memoise’, ‘pryr’, ‘RcppGSL’, ‘gtable’, ‘isoband’, ‘scales’, ‘proxy’, ‘iterators’, ‘data.table’, ‘clock’, ‘gower’, ‘hardhat’, ‘ipred’, ‘lubridate’, ‘timeDate’, ‘rbibutils’, ‘backports’, ‘dplyr’, ‘ellipsis’, ‘generics’, ‘glue’, ‘lifecycle’, ‘purrr’, ‘rlang’, ‘stringr’, ‘tibble’, ‘tidyr’, ‘kimisc’, ‘Rcpp’, ‘RcppZiggurat’, ‘RcppParallel’, ‘RcppArmadillo’, ‘ggplot2’, ‘e1071’, ‘foreach’, ‘ModelMetrics’, ‘plyr’, ‘pROC’, ‘recipes’, ‘reshape2’, ‘withr’, ‘registry’, ‘checkmate’, ‘R6’, ‘Rdpack’, ‘broom’, ‘pracma’, ‘CompQuadForm’, ‘bazar’, ‘quadprog’, ‘inflection’, ‘Rfast’, ‘caret’, ‘quadprogXT’, ‘slam’, ‘ROI’, ‘osqp’, ‘ROI.plugin.qpoases’

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/listenv_0.9.1.zip'
Content type 'application/zip' length 109085 bytes (106 KB)
downloaded 106 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/parallelly_1.37.0.zip'
Content type 'application/zip' length 362522 bytes (354 KB)
downloaded 354 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/future_1.33.1.zip'
Content type 'application/zip' length 677489 bytes (661 KB)
downloaded 661 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/globals_0.16.2.zip'
Content type 'application/zip' length 107014 bytes (104 KB)
downloaded 104 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/digest_0.6.34.zip'
Content type 'application/zip' length 206145 bytes (201 KB)
downloaded 201 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/shape_1.4.6.zip'
Content type 'application/zip' length 786293 bytes (767 KB)
downloaded 767 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/future.apply_1.11.1.zip'
Content type 'application/zip' length 156896 bytes (153 KB)
downloaded 153 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/numDeriv_2016.8-1.1.zip'
Content type 'application/zip' length 116116 bytes (113 KB)
downloaded 113 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/progressr_0.14.0.zip'
Content type 'application/zip' length 387237 bytes (378 KB)
downloaded 378 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/SQUAREM_2021.1.zip'
Content type 'application/zip' length 183115 bytes (178 KB)
downloaded 178 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/fastmap_1.1.1.zip'
Content type 'application/zip' length 132886 bytes (129 KB)
downloaded 129 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/crayon_1.5.2.zip'
Content type 'application/zip' length 162448 bytes (158 KB)
downloaded 158 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/prettyunits_1.2.0.zip'
Content type 'application/zip' length 157616 bytes (153 KB)
downloaded 153 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/colorspace_2.1-0.zip'
Content type 'application/zip' length 2633207 bytes (2.5 MB)
downloaded 2.5 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/diagram_1.6.5.zip'
Content type 'application/zip' length 682134 bytes (666 KB)
downloaded 666 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/lava_1.7.3.zip'
Content type 'application/zip' length 2563159 bytes (2.4 MB)
downloaded 2.4 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/utf8_1.2.4.zip'
Content type 'application/zip' length 149771 bytes (146 KB)
downloaded 146 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/cachem_1.0.8.zip'
Content type 'application/zip' length 72620 bytes (70 KB)
downloaded 70 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/lobstr_1.1.2.zip'
Content type 'application/zip' length 454584 bytes (443 KB)
downloaded 443 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/farver_2.1.1.zip'
Content type 'application/zip' length 1505907 bytes (1.4 MB)
downloaded 1.4 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/labeling_0.4.3.zip'
Content type 'application/zip' length 62568 bytes (61 KB)
downloaded 61 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/munsell_0.5.0.zip'
Content type 'application/zip' length 244247 bytes (238 KB)
downloaded 238 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/RColorBrewer_1.1-3.zip'
Content type 'application/zip' length 56066 bytes (54 KB)
downloaded 54 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/viridisLite_0.4.2.zip'
Content type 'application/zip' length 1300105 bytes (1.2 MB)
downloaded 1.2 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/tzdb_0.4.0.zip'
Content type 'application/zip' length 1032602 bytes (1008 KB)
downloaded 1008 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/prodlim_2023.08.28.zip'
Content type 'application/zip' length 415625 bytes (405 KB)
downloaded 405 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/timechange_0.3.0.zip'
Content type 'application/zip' length 507701 bytes (495 KB)
downloaded 495 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/cli_3.6.2.zip'
Content type 'application/zip' length 1341597 bytes (1.3 MB)
downloaded 1.3 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/magrittr_2.0.3.zip'
Content type 'application/zip' length 226892 bytes (221 KB)
downloaded 221 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/pillar_1.9.0.zip'
Content type 'application/zip' length 659156 bytes (643 KB)
downloaded 643 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/tidyselect_1.2.0.zip'
Content type 'application/zip' length 223781 bytes (218 KB)
downloaded 218 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/vctrs_0.6.5.zip'
Content type 'application/zip' length 1334186 bytes (1.3 MB)
downloaded 1.3 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/stringi_1.8.3.zip'
Content type 'application/zip' length 14998651 bytes (14.3 MB)
downloaded 14.3 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/fansi_1.0.6.zip'
Content type 'application/zip' length 313980 bytes (306 KB)
downloaded 306 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/pkgconfig_2.0.3.zip'
Content type 'application/zip' length 22441 bytes (21 KB)
downloaded 21 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/cpp11_0.4.7.zip'
Content type 'application/zip' length 304062 bytes (296 KB)
downloaded 296 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/memoise_2.0.1.zip'
Content type 'application/zip' length 50046 bytes (48 KB)
downloaded 48 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/pryr_0.1.6.zip'
Content type 'application/zip' length 549531 bytes (536 KB)
downloaded 536 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/RcppGSL_0.3.13.zip'
Content type 'application/zip' length 702926 bytes (686 KB)
downloaded 686 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/gtable_0.3.4.zip'
Content type 'application/zip' length 225847 bytes (220 KB)
downloaded 220 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/isoband_0.2.7.zip'
Content type 'application/zip' length 1968359 bytes (1.9 MB)
downloaded 1.9 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/scales_1.3.0.zip'
Content type 'application/zip' length 703930 bytes (687 KB)
downloaded 687 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/proxy_0.4-27.zip'
Content type 'application/zip' length 179961 bytes (175 KB)
downloaded 175 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/iterators_1.0.14.zip'
Content type 'application/zip' length 353093 bytes (344 KB)
downloaded 344 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/data.table_1.15.0.zip'
Content type 'application/zip' length 2387217 bytes (2.3 MB)
downloaded 2.3 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/clock_0.7.0.zip'
Content type 'application/zip' length 2131875 bytes (2.0 MB)
downloaded 2.0 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/gower_1.0.1.zip'
Content type 'application/zip' length 314815 bytes (307 KB)
downloaded 307 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/hardhat_1.3.1.zip'
Content type 'application/zip' length 836869 bytes (817 KB)
downloaded 817 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/ipred_0.9-14.zip'
Content type 'application/zip' length 388589 bytes (379 KB)
downloaded 379 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/lubridate_1.9.3.zip'
Content type 'application/zip' length 984563 bytes (961 KB)
downloaded 961 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/timeDate_4032.109.zip'
Content type 'application/zip' length 1438969 bytes (1.4 MB)
downloaded 1.4 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/rbibutils_2.2.16.zip'
Content type 'application/zip' length 764751 bytes (746 KB)
downloaded 746 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/backports_1.4.1.zip'
Content type 'application/zip' length 101330 bytes (98 KB)
downloaded 98 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/dplyr_1.1.4.zip'
Content type 'application/zip' length 1559256 bytes (1.5 MB)
downloaded 1.5 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/ellipsis_0.3.2.zip'
Content type 'application/zip' length 40465 bytes (39 KB)
downloaded 39 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/generics_0.1.3.zip'
Content type 'application/zip' length 80053 bytes (78 KB)
downloaded 78 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/glue_1.7.0.zip'
Content type 'application/zip' length 161359 bytes (157 KB)
downloaded 157 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/lifecycle_1.0.4.zip'
Content type 'application/zip' length 139666 bytes (136 KB)
downloaded 136 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/purrr_1.0.2.zip'
Content type 'application/zip' length 498900 bytes (487 KB)
downloaded 487 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/rlang_1.1.3.zip'
Content type 'application/zip' length 1574792 bytes (1.5 MB)
downloaded 1.5 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/stringr_1.5.1.zip'
Content type 'application/zip' length 319198 bytes (311 KB)
downloaded 311 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/tibble_3.2.1.zip'
Content type 'application/zip' length 690922 bytes (674 KB)
downloaded 674 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/tidyr_1.3.1.zip'
Content type 'application/zip' length 1267408 bytes (1.2 MB)
downloaded 1.2 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/kimisc_0.4.zip'
Content type 'application/zip' length 120905 bytes (118 KB)
downloaded 118 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/Rcpp_1.0.12.zip'
Content type 'application/zip' length 2877687 bytes (2.7 MB)
downloaded 2.7 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/RcppZiggurat_0.1.6.zip'
Content type 'application/zip' length 799079 bytes (780 KB)
downloaded 780 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/RcppParallel_5.1.7.zip'
Content type 'application/zip' length 1285470 bytes (1.2 MB)
downloaded 1.2 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/RcppArmadillo_0.12.8.0.0.zip'
Content type 'application/zip' length 2053194 bytes (2.0 MB)
downloaded 2.0 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/ggplot2_3.4.4.zip'
Content type 'application/zip' length 4298749 bytes (4.1 MB)
downloaded 4.1 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/e1071_1.7-14.zip'
Content type 'application/zip' length 664739 bytes (649 KB)
downloaded 649 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/foreach_1.5.2.zip'
Content type 'application/zip' length 148293 bytes (144 KB)
downloaded 144 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/ModelMetrics_1.2.2.2.zip'
Content type 'application/zip' length 484859 bytes (473 KB)
downloaded 473 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/plyr_1.8.9.zip'
Content type 'application/zip' length 1164969 bytes (1.1 MB)
downloaded 1.1 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/pROC_1.18.5.zip'
Content type 'application/zip' length 1169925 bytes (1.1 MB)
downloaded 1.1 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/recipes_1.0.10.zip'
Content type 'application/zip' length 1608469 bytes (1.5 MB)
downloaded 1.5 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/reshape2_1.4.4.zip'
Content type 'application/zip' length 455856 bytes (445 KB)
downloaded 445 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/withr_3.0.0.zip'
Content type 'application/zip' length 245877 bytes (240 KB)
downloaded 240 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/registry_0.5-1.zip'
Content type 'application/zip' length 197368 bytes (192 KB)
downloaded 192 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/checkmate_2.3.1.zip'
Content type 'application/zip' length 747315 bytes (729 KB)
downloaded 729 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/R6_2.5.1.zip'
Content type 'application/zip' length 84326 bytes (82 KB)
downloaded 82 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/Rdpack_2.6.zip'
Content type 'application/zip' length 747278 bytes (729 KB)
downloaded 729 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/broom_1.0.5.zip'
Content type 'application/zip' length 1863439 bytes (1.8 MB)
downloaded 1.8 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/pracma_2.4.4.zip'
Content type 'application/zip' length 1731413 bytes (1.7 MB)
downloaded 1.7 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/CompQuadForm_1.4.3.zip'
Content type 'application/zip' length 91283 bytes (89 KB)
downloaded 89 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/bazar_1.0.11.zip'
Content type 'application/zip' length 110559 bytes (107 KB)
downloaded 107 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/quadprog_1.5-8.zip'
Content type 'application/zip' length 37185 bytes (36 KB)
downloaded 36 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/inflection_1.3.6.zip'
Content type 'application/zip' length 303822 bytes (296 KB)
downloaded 296 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/Rfast_2.1.0.zip'
Content type 'application/zip' length 3118823 bytes (3.0 MB)
downloaded 3.0 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/caret_6.0-94.zip'
Content type 'application/zip' length 3577399 bytes (3.4 MB)
downloaded 3.4 MB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/quadprogXT_0.0.5.zip'
Content type 'application/zip' length 27730 bytes (27 KB)
downloaded 27 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/slam_0.1-50.zip'
Content type 'application/zip' length 189475 bytes (185 KB)
downloaded 185 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/ROI_1.0-1.zip'
Content type 'application/zip' length 477356 bytes (466 KB)
downloaded 466 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/osqp_0.6.3.2.zip'
Content type 'application/zip' length 466864 bytes (455 KB)
downloaded 455 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/ROI.plugin.qpoases_1.0-3.zip'
Content type 'application/zip' length 573498 bytes (560 KB)
downloaded 560 KB

trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.3/skedastic_2.0.2.zip'
Content type 'application/zip' length 4178033 bytes (4.0 MB)
downloaded 4.0 MB

package ‘listenv’ successfully unpacked and MD5 sums checked
package ‘parallelly’ successfully unpacked and MD5 sums checked
package ‘future’ successfully unpacked and MD5 sums checked
package ‘globals’ successfully unpacked and MD5 sums checked
package ‘digest’ successfully unpacked and MD5 sums checked
package ‘shape’ successfully unpacked and MD5 sums checked
package ‘future.apply’ successfully unpacked and MD5 sums checked
package ‘numDeriv’ successfully unpacked and MD5 sums checked
package ‘progressr’ successfully unpacked and MD5 sums checked
package ‘SQUAREM’ successfully unpacked and MD5 sums checked
package ‘fastmap’ successfully unpacked and MD5 sums checked
package ‘crayon’ successfully unpacked and MD5 sums checked
package ‘prettyunits’ successfully unpacked and MD5 sums checked
package ‘colorspace’ successfully unpacked and MD5 sums checked
package ‘diagram’ successfully unpacked and MD5 sums checked
package ‘lava’ successfully unpacked and MD5 sums checked
package ‘utf8’ successfully unpacked and MD5 sums checked
package ‘cachem’ successfully unpacked and MD5 sums checked
package ‘lobstr’ successfully unpacked and MD5 sums checked
package ‘farver’ successfully unpacked and MD5 sums checked
package ‘labeling’ successfully unpacked and MD5 sums checked
package ‘munsell’ successfully unpacked and MD5 sums checked
package ‘RColorBrewer’ successfully unpacked and MD5 sums checked
package ‘viridisLite’ successfully unpacked and MD5 sums checked
package ‘tzdb’ successfully unpacked and MD5 sums checked
package ‘prodlim’ successfully unpacked and MD5 sums checked
package ‘timechange’ successfully unpacked and MD5 sums checked
package ‘cli’ successfully unpacked and MD5 sums checked
package ‘magrittr’ successfully unpacked and MD5 sums checked
package ‘pillar’ successfully unpacked and MD5 sums checked
package ‘tidyselect’ successfully unpacked and MD5 sums checked
package ‘vctrs’ successfully unpacked and MD5 sums checked
package ‘stringi’ successfully unpacked and MD5 sums checked
package ‘fansi’ successfully unpacked and MD5 sums checked
package ‘pkgconfig’ successfully unpacked and MD5 sums checked
package ‘cpp11’ successfully unpacked and MD5 sums checked
package ‘memoise’ successfully unpacked and MD5 sums checked
package ‘pryr’ successfully unpacked and MD5 sums checked
package ‘RcppGSL’ successfully unpacked and MD5 sums checked
package ‘gtable’ successfully unpacked and MD5 sums checked
package ‘isoband’ successfully unpacked and MD5 sums checked
package ‘scales’ successfully unpacked and MD5 sums checked
package ‘proxy’ successfully unpacked and MD5 sums checked
package ‘iterators’ successfully unpacked and MD5 sums checked
package ‘data.table’ successfully unpacked and MD5 sums checked
package ‘clock’ successfully unpacked and MD5 sums checked
package ‘gower’ successfully unpacked and MD5 sums checked
package ‘hardhat’ successfully unpacked and MD5 sums checked
package ‘ipred’ successfully unpacked and MD5 sums checked
package ‘lubridate’ successfully unpacked and MD5 sums checked
package ‘timeDate’ successfully unpacked and MD5 sums checked
package ‘rbibutils’ successfully unpacked and MD5 sums checked
package ‘backports’ successfully unpacked and MD5 sums checked
package ‘dplyr’ successfully unpacked and MD5 sums checked
package ‘ellipsis’ successfully unpacked and MD5 sums checked
package ‘generics’ successfully unpacked and MD5 sums checked
package ‘glue’ successfully unpacked and MD5 sums checked
package ‘lifecycle’ successfully unpacked and MD5 sums checked
package ‘purrr’ successfully unpacked and MD5 sums checked
package ‘rlang’ successfully unpacked and MD5 sums checked
package ‘stringr’ successfully unpacked and MD5 sums checked
package ‘tibble’ successfully unpacked and MD5 sums checked
package ‘tidyr’ successfully unpacked and MD5 sums checked
package ‘kimisc’ successfully unpacked and MD5 sums checked
package ‘Rcpp’ successfully unpacked and MD5 sums checked
package ‘RcppZiggurat’ successfully unpacked and MD5 sums checked
package ‘RcppParallel’ successfully unpacked and MD5 sums checked
package ‘RcppArmadillo’ successfully unpacked and MD5 sums checked
package ‘ggplot2’ successfully unpacked and MD5 sums checked
package ‘e1071’ successfully unpacked and MD5 sums checked
package ‘foreach’ successfully unpacked and MD5 sums checked
package ‘ModelMetrics’ successfully unpacked and MD5 sums checked
package ‘plyr’ successfully unpacked and MD5 sums checked
package ‘pROC’ successfully unpacked and MD5 sums checked
package ‘recipes’ successfully unpacked and MD5 sums checked
package ‘reshape2’ successfully unpacked and MD5 sums checked
package ‘withr’ successfully unpacked and MD5 sums checked
package ‘registry’ successfully unpacked and MD5 sums checked
package ‘checkmate’ successfully unpacked and MD5 sums checked
package ‘R6’ successfully unpacked and MD5 sums checked
package ‘Rdpack’ successfully unpacked and MD5 sums checked
package ‘broom’ successfully unpacked and MD5 sums checked
package ‘pracma’ successfully unpacked and MD5 sums checked
package ‘CompQuadForm’ successfully unpacked and MD5 sums checked
package ‘bazar’ successfully unpacked and MD5 sums checked
package ‘quadprog’ successfully unpacked and MD5 sums checked
package ‘inflection’ successfully unpacked and MD5 sums checked
package ‘Rfast’ successfully unpacked and MD5 sums checked
package ‘caret’ successfully unpacked and MD5 sums checked
package ‘quadprogXT’ successfully unpacked and MD5 sums checked
package ‘slam’ successfully unpacked and MD5 sums checked
package ‘ROI’ successfully unpacked and MD5 sums checked
package ‘osqp’ successfully unpacked and MD5 sums checked
package ‘ROI.plugin.qpoases’ successfully unpacked and MD5 sums checked
package ‘skedastic’ successfully unpacked and MD5 sums checked

The downloaded binary packages are in
        C:\Users\OZadorozhnyi\AppData\Local\Temp\Rtmpqsabaz\downloaded_packages
> library(skedastic)
> harrison_mccabe(formula)
Error in apply(X, 2, function(x) all(x == 1)) : 
  dim(X) must have a positive length
> ?lm
> lm(formula)
Error in formula.default(object, env = baseenv()) : invalid formula
> formula
   [1] 9.726059e+14 2.684364e+14 1.608745e+14 3.532836e+13 2.669934e+12
   [6] 1.176702e+14 0.000000e+00 8.805933e+13 1.243043e+14 2.162694e+15
  [11] 5.784623e+13 2.919756e+12 3.932718e+13 3.703361e+14 2.254455e+13
  [16] 1.529180e+13 3.629187e+14 3.466034e+14 4.441564e+14 7.044991e+14
  [21] 8.309902e+13 2.941063e+13 3.361253e+14 2.252329e+14 1.572971e+14
  [26] 1.766406e+14 2.716794e+12 2.141257e+13 2.764928e+13 3.744116e+13
  [31] 2.222908e+14 8.562613e+12 0.000000e+00 2.907445e+12 2.659430e+14
  [36] 2.298236e+14 3.057587e+14 4.042273e+12 5.248235e+13 5.252656e+13
  [41] 1.453712e+13 2.541423e+12 3.624480e+12 1.452871e+13 4.161212e+14
  [46] 1.326720e+14 9.697046e+13 2.889754e+11 1.263531e+15 1.727870e+12
  [51] 6.191880e+13 1.410516e+14 4.481222e+14 3.848052e+14 1.312497e+13
  [56] 2.310273e+12 3.938298e+13 1.613511e+12 1.682702e+12 6.154180e+13
  [61] 2.197641e+14 1.514302e+14 5.313685e+13 1.276189e+13 1.875090e+14
  [66] 5.424340e+14 6.605454e+13 6.363857e+12 6.874198e+12 1.426096e+14
  [71] 1.831081e+14 1.463955e+15 1.784828e+11 7.960949e+14 1.118016e+14
  [76] 1.313190e+14 6.126454e+14 5.497412e+13 1.796075e+14 1.655773e+15
  [81] 4.008076e+13 1.264385e+14 3.494776e+14 1.889257e+14 1.207874e+15
  [86] 1.887017e+14 1.024794e+14 4.208493e+14 1.189290e+13 4.127918e+14
  [91] 8.043351e+12 3.959666e+13 2.610288e+14 1.615974e+14 4.181581e+11
  [96] 2.732743e+13 5.290245e+14 8.729550e+13 1.140962e+15 1.725853e+14
 [101] 1.087995e+14 2.317229e+14 5.890818e+12 6.484634e+13 1.807990e+14
 [106] 7.568496e+14 9.965023e+13 2.140521e+14 6.131918e+14 1.134198e+14
 [111] 4.309302e+14 2.836564e+14 1.850186e+12 1.391060e+15 7.170017e+14
 [116] 1.138629e+15 1.856314e+14 1.383347e+14 2.272732e+13 5.951287e+13
 [121] 9.049833e+13 7.413759e+13 4.106274e+13 1.558878e+13 3.732385e+13
 [126] 1.986551e+14 7.549936e+13 2.190954e+15 8.091238e+13 1.102358e+14
 [131] 3.964915e+12 1.193966e+14 1.463590e+14 1.624560e+14 4.600841e+14
 [136] 3.503681e+14 2.967417e+13 8.263630e+12 6.659481e+13 2.996277e+14
 [141] 1.301056e+15 1.426936e+13 3.339522e+15 7.364188e+13 2.665141e+13
 [146] 1.198862e+13 0.000000e+00 3.263950e+12 5.591457e+13 5.153278e+14
 [151] 1.519628e+14 1.970440e+14 2.058138e+13 2.754695e+12 1.003797e+14
 [156] 3.848943e+14 1.603106e+14 4.491096e+13 5.211862e+13 9.267649e+11
 [161] 1.582759e+14 6.136669e+14 3.747656e+11 5.888334e+13 1.803399e+14
 [166] 3.433933e+13 5.384496e+14 1.257251e+15 5.968728e+14 6.164528e+14
 [171] 2.889682e+13 1.576877e+14 1.308903e+15 8.451002e+13 7.733155e+13
 [176] 3.895645e+13 1.790783e+13 5.209797e+14 3.570476e+13 2.193687e+13
 [181] 1.243896e+13 4.963628e+14 1.560677e+14 4.728299e+14 8.292748e+14
 [186] 2.766629e+12 1.428709e+14 2.187037e+14 1.326040e+15 1.803436e+12
 [191] 2.180201e+15 3.656822e+14 8.415104e+14 6.926233e+14 1.472787e+15
 [196] 8.991088e+12 9.023179e+11 4.785475e+13 2.218466e+13 2.974764e+12
 [201] 4.770018e+14 1.814721e+14 4.399394e+12 5.733687e+14 3.558773e+12
 [206] 1.743256e+14 6.906215e+14 4.437846e+13 2.039956e+13 2.618215e+14
 [211] 5.197317e+13 1.509368e+13 1.057318e+14 1.363332e+12 1.536913e+14
 [216] 3.379620e+14 1.509678e+14 3.348794e+14 9.471921e+13 5.293850e+14
 [221] 1.757029e+13 8.472355e+13 2.115306e+13 4.848023e+13 2.365872e+14
 [226] 8.544099e+14 9.648583e+11 5.421725e+11 5.432233e+13 2.193047e+15
 [231] 5.338227e+13 3.231130e+13 5.393997e+14 3.230079e+13 1.325171e+14
 [236] 3.527009e+14 9.866069e+13 3.697936e+14 7.370809e+14 1.331361e+14
 [241] 1.139752e+14 1.582776e+13 7.880380e+12 1.223970e+14 8.121275e+13
 [246] 1.016336e+14 6.046885e+13 2.115683e+15 6.594226e+13 5.395429e+13
 [251] 1.971037e+13 2.943530e+14 4.115921e+14 9.214767e+14 1.841722e+14
 [256] 5.305242e+11 7.369865e+13 1.027213e+15 1.061443e+12 5.277963e+13
 [261] 1.140873e+15 4.209265e+13 8.709282e+13 7.644584e+13 1.220740e+14
 [266] 5.633414e+11 5.880600e+14 5.710321e+12 5.004081e+14 1.272773e+14
 [271] 1.982902e+14 1.452822e+14 1.828070e+13 2.760876e+14 6.164985e+13
 [276] 1.698941e+14 1.502727e+12 3.738937e+12 2.334516e+14 1.645898e+14
 [281] 2.129655e+13 1.076873e+13 2.014850e+14 5.949107e+14 3.180430e+13
 [286] 3.750827e+14 1.628416e+14 8.543128e+14 3.696084e+14 2.155415e+14
 [291] 4.607893e+12 1.214673e+15 5.446712e+14 1.946997e+11 3.027903e+13
 [296] 1.790172e+14 7.270827e+13 4.544384e+13 4.855842e+14 9.378492e+13
 [301] 7.820923e+13 5.247018e+10 2.546969e+14 9.100944e+13 4.086715e+13
 [306] 8.183209e+14 1.206834e+14 2.330828e+14 2.882581e+14 3.822638e+13
 [311] 7.357246e+13 2.581859e+14 8.229308e+13 4.972052e+14 3.467522e+14
 [316] 7.393622e+14 7.458753e+14 1.170829e+14 8.071017e+12 3.742554e+14
 [321] 3.015030e+14 2.049347e+13 6.273366e+12 3.879455e+14 9.728858e+13
 [326] 1.033917e+14 5.739400e+13 6.623516e+14 1.670553e+14 1.009003e+13
 [331] 2.846406e+13 6.129515e+14 9.441592e+13 1.871237e+13 3.320518e+12
 [336] 8.570765e+14 8.785891e+14 9.695651e+12 8.556823e+12 1.197638e+14
 [341] 6.263672e+13 4.237879e+14 2.249281e+12 1.157103e+13 3.714174e+14
 [346] 7.026240e+14 4.491417e+13 1.931517e+12 6.082807e+13 5.420478e+13
 [351] 1.229843e+14 2.433477e+13 4.171898e+14 7.703697e+12 8.991857e+14
 [356] 2.645072e+13 7.936592e+12 1.032286e+14 3.289567e+12 3.401961e+14
 [361] 1.501784e+13 1.454197e+14 2.138414e+14 4.833092e+13 4.754500e+12
 [366] 1.136129e+15 5.248917e+14 1.823473e+14 5.668334e+14 7.877153e+11
 [371] 7.644245e+12 1.768419e+14 7.154295e+14 1.012686e+14 1.038784e+13
 [376] 5.657686e+14 3.054637e+13 2.913754e+13 7.332145e+14 3.090882e+14
 [381] 2.989999e+13 3.958005e+11 1.751373e+13 8.382913e+13 3.954427e+14
 [386] 4.135817e+14 1.756275e+11 3.325094e+14 3.413475e+12 1.144430e+14
 [391] 3.306924e+13 5.655766e+14 6.167455e+13 1.385006e+14 5.692491e+14
 [396] 1.129090e+15 1.414875e+15 1.334249e+15 1.609331e+14 2.274981e+13
 [401] 1.606564e+14 1.143516e+15 5.233311e+13 5.017293e+14 3.771552e+12
 [406] 6.727839e+13 8.490245e+14 5.058907e+13 2.172533e+14 4.855465e+14
 [411] 6.626172e+13 3.043966e+13 2.385418e+14 7.286214e+13 1.533970e+13
 [416] 7.633542e+14 5.472619e+12 5.987682e+14 3.942325e+13 7.725405e+14
 [421] 1.494856e+13 5.221885e+13 6.664343e+11 6.804731e+12 2.443800e+14
 [426] 9.855164e+14 1.917103e+13 2.958641e+13 5.422529e+13 1.726765e+14
 [431] 8.293397e+13 1.506422e+14 9.475646e+13 2.478335e+15 1.079122e+14
 [436] 6.075298e+14 2.074798e+15 6.236774e+13 9.311489e+13 7.037480e+12
 [441] 2.387038e+14 8.050521e+14 4.006901e+12 2.682569e+14 8.656887e+13
 [446] 1.006189e+13 4.479531e+11 6.804732e+14 2.692889e+13 6.802109e+13
 [451] 1.762181e+13 2.115349e+11 4.021133e+14 9.127211e+14 5.645108e+13
 [456] 8.378867e+12 1.792330e+15 9.302102e+14 2.453194e+14 4.694126e+14
 [461] 1.947883e+14 4.278663e+13 4.684789e+13 6.836046e+13 2.013332e+13
 [466] 8.365471e+12 2.118007e+14 5.474501e+14 8.997941e+14 2.378989e+14
 [471] 1.555565e+13 5.543395e+14 5.214587e+13 2.421005e+14 1.155429e+15
 [476] 1.198239e+14 3.556410e+13 4.757419e+13 2.590195e+14 2.537019e+14
 [481] 2.068293e+13 8.606633e+14 5.800167e+13 2.182563e+14 3.203961e+14
 [486] 8.230528e+14 8.289747e+13 2.029050e+13 4.916740e+13 2.139856e+14
 [491] 2.475264e+14 8.081769e+12 8.707452e+14 1.113014e+14 5.216902e+13
 [496] 1.047120e+15 8.777764e+13 3.581965e+11 2.679563e+15 6.772932e+13
 [501] 1.550619e+14 1.858153e+13 2.245109e+13 3.790633e+14 2.520360e+14
 [506] 9.069592e+13 5.555920e+13 1.205793e+13 3.495479e+13 1.371476e+15
 [511] 1.132997e+14 3.608003e+14 7.453160e+13 2.549703e+13 1.174069e+14
 [516] 3.521560e+13 2.904826e+15 6.071689e+13 9.536187e+14 2.048649e+14
 [521] 1.321593e+14 2.804648e+13 1.638273e+14 6.884986e+13 2.271979e+15
 [526] 2.243995e+14 1.028906e+14 6.890553e+14 8.159914e+14 4.726535e+13
 [531] 4.329961e+14 9.867935e+13 2.884396e+13 1.324459e+14 6.338676e+13
 [536] 1.210309e+14 1.755731e+13 6.146583e+14 8.221619e+14 8.045356e+12
 [541] 4.380598e+13 1.645660e+14 1.589780e+14 1.297160e+15 1.739264e+13
 [546] 3.290281e+14 5.522694e+13 3.877059e+12 1.015528e+15 9.799721e+14
 [551] 5.851976e+12 9.040914e+14 2.276425e+15 4.224708e+14 2.326689e+14
 [556] 3.366154e+14 1.062453e+15 7.687982e+14 9.525566e+13 4.700502e+14
 [561] 2.472360e+14 2.670918e+13 2.199790e+13 2.323834e+13 1.636072e+14
 [566] 1.186545e+14 1.982753e+13 1.739942e+15 9.002804e+13 6.418411e+14
 [571] 1.021024e+13 8.361288e+13 4.948429e+13 1.165923e+15 6.370600e+14
 [576] 1.034478e+13 7.659237e+12 9.717663e+13 5.071476e+13 1.294809e+13
 [581] 5.031458e+14 1.203730e+14 2.144320e+14 3.403254e+11 4.834538e+14
 [586] 8.256154e+12 1.367988e+14 6.869258e+12 3.687641e+14 6.257039e+13
 [591] 3.054768e+15 1.874621e+15 1.249612e+13 3.637872e+13 1.524348e+13
 [596] 1.434674e+13 2.339842e+13 5.896829e+14 2.824919e+14 1.879673e+14
 [601] 1.092912e+14 7.851037e+14 1.366872e+13 1.746917e+13 4.502741e+13
 [606] 2.931332e+14 1.588188e+13 3.844634e+14 1.147870e+15 1.796878e+14
 [611] 1.986126e+15 2.160343e+13 1.124259e+13 3.932907e+14 1.394694e+14
 [616] 2.843362e+15 8.714076e+14 5.837700e+14 2.282510e+14 1.421141e+14
 [621] 1.402432e+15 2.802895e+14 2.549543e+14 4.850938e+14 2.296141e+13
 [626] 8.668756e+14 3.440652e+12 7.933073e+12 3.501488e+13 4.218251e+14
 [631] 6.295944e+13 3.088751e+14 1.087717e+15 2.761718e+14 7.605059e+14
 [636] 5.135989e+14 1.004336e+13 6.811984e+13 3.620872e+12 0.000000e+00
 [641] 1.505756e+14 4.135474e+14 1.283372e+14 1.961605e+14 3.627873e+14
 [646] 1.092471e+15 2.482367e+14 2.954019e+12 2.385886e+15 9.200339e+13
 [651] 4.835847e+14 6.142151e+13 2.023589e+15 8.520367e+14 2.499573e+12
 [656] 6.034553e+13 5.988990e+13 2.153182e+14 8.708141e+13 1.146670e+14
 [661] 4.037038e+14 4.025709e+14 2.697434e+12 3.293597e+14 2.516415e+13
 [666] 5.132553e+12 5.048508e+12 6.075124e+13 4.818780e+12 2.828900e+14
 [671] 2.116012e+14 2.677128e+14 4.304989e+13 9.681042e+12 9.111354e+14
 [676] 2.013118e+15 2.072115e+14 3.042848e+13 6.654408e+12 2.363167e+14
 [681] 7.798162e+13 5.408204e+14 1.743978e+15 8.364775e+11 1.621405e+14
 [686] 6.852213e+13 1.137768e+14 2.230541e+14 9.645416e+14 2.608881e+14
 [691] 1.820447e+14 0.000000e+00 1.753221e+14 3.469213e+13 2.244981e+15
 [696] 6.614753e+14 5.664715e+14 3.492662e+14 7.454664e+13 3.494580e+13
 [701] 1.473122e+13 1.183028e+15 3.284305e+14 8.031481e+13 2.332558e+14
 [706] 2.610724e+15 8.853039e+13 1.361022e+15 3.933189e+12 3.411625e+14
 [711] 1.732354e+14 1.173430e+14 8.738948e+13 1.577571e+15 8.517514e+13
 [716] 4.691208e+11 4.097173e+14 1.417109e+15 4.564731e+13 1.774261e+14
 [721] 4.462018e+14 2.635259e+13 2.492788e+13 1.040796e+14 1.927107e+13
 [726] 2.125248e+13 1.242521e+12 1.944791e+10 1.059482e+15 1.779006e+14
 [731] 2.207564e+14 5.291209e+14 4.067818e+14 5.776024e+13 4.307462e+14
 [736] 9.873635e+13 3.081549e+14 2.349911e+12 8.562123e+13 1.636651e+15
 [741] 1.152735e+15 7.195978e+14 1.376119e+14 1.885656e+14 6.795174e+14
 [746] 4.911375e+12 1.448531e+14 1.277872e+15 3.989531e+15 3.009244e+12
 [751] 1.336814e+15 1.869466e+13 7.577078e+12 4.015721e+13 2.665576e+15
 [756] 5.714665e+14 1.092210e+13 1.564636e+13 1.423164e+14 2.556009e+13
 [761] 6.227763e+14 2.080686e+14 2.294802e+14 9.916744e+14 6.524696e+14
 [766] 3.393615e+13 2.934107e+14 2.984305e+15 9.486686e+14 3.032910e+14
 [771] 4.767344e+14 1.901255e+15 2.022473e+14 5.929006e+15 1.668033e+15
 [776] 3.400225e+14 4.327792e+14 4.754472e+14 5.608497e+15 3.536513e+13
 [781] 6.467901e+13 1.138667e+14 1.239805e+14 3.715427e+14 1.840437e+14
 [786] 7.076108e+13 2.495230e+14 1.616320e+13 8.385641e+14 1.781845e+14
 [791] 7.367784e+12 1.680960e+15 4.141804e+13 1.701617e+14 3.296166e+15
 [796] 2.007856e+14 8.908996e+14 2.516885e+14 3.490088e+15 1.959611e+13
 [801] 2.948779e+14 1.438281e+13 2.595385e+15 6.432336e+13 1.184257e+14
 [806] 3.603958e+14 4.188234e+14 4.707011e+14 1.399302e+14 2.062926e+13
 [811] 5.377953e+14 3.193540e+12 6.156809e+13 1.950496e+15 1.166332e+13
 [816] 6.824323e+14 5.496483e+14 3.286121e+14 2.842506e+14 4.478856e+14
 [821] 9.587140e+14 2.846034e+12 3.799634e+13 1.753860e+14 7.623274e+13
 [826] 4.473114e+13 3.888057e+12 1.792086e+15 3.996617e+14 1.520135e+14
 [831] 3.727472e+14 2.046247e+14 3.927817e+13 2.022778e+15 8.205520e+13
 [836] 9.828321e+14 4.590196e+13 5.045820e+13 4.416430e+13 4.543318e+13
 [841] 1.118446e+14 5.095843e+12 6.394017e+13 1.889760e+15 2.462104e+15
 [846] 1.962659e+14 1.187202e+11 1.718298e+13 1.017046e+14 1.859895e+12
 [851] 4.118394e+12 9.115697e+12 1.065209e+15 3.689883e+13 1.754208e+15
 [856] 1.054911e+15 2.298041e+14 5.474211e+14 8.419902e+14 1.562899e+14
 [861] 4.072845e+14 1.392387e+14 9.295202e+14 1.165127e+15 1.345414e+13
 [866] 1.916266e+14 9.571120e+12 2.669274e+14 3.593582e+13 2.464679e+13
 [871] 4.640254e+14 5.252663e+14 4.006652e+14 1.047809e+14 1.251933e+15
 [876] 8.628997e+14 8.245994e+13 3.004901e+13 1.200118e+14 1.102917e+15
 [881] 1.538590e+12 9.739999e+14 4.667185e+13 1.196788e+13 1.592788e+15
 [886] 3.919612e+14 7.373316e+14 1.637283e+14 1.964199e+14 3.052751e+13
 [891] 1.055410e+14 1.548149e+13 6.268068e+12 5.981107e+13 3.642168e+14
 [896] 1.174501e+15 2.041995e+15 7.319675e+13 1.213725e+14 1.151968e+14
 [901] 1.021905e+14 9.553523e+13 2.383117e+14 5.776431e+12 1.864162e+15
 [906] 3.417783e+14 4.267855e+14 9.171035e+14 5.205593e+14 1.455718e+14
 [911] 5.702247e+14 8.097499e+14 4.482431e+14 8.165736e+14 3.818036e+13
 [916] 1.096359e+14 3.836084e+14 1.073531e+13 2.095354e+13 1.453185e+13
 [921] 1.898645e+13 6.116626e+14 3.220652e+14 2.586474e+14 2.728132e+14
 [926] 1.279002e+14 4.593079e+13 1.508285e+15 9.040046e+14 2.927046e+13
 [931] 4.121880e+13 9.095672e+12 1.461195e+13 2.944729e+14 2.628769e+14
 [936] 7.304869e+14 8.767111e+13 1.676594e+13 1.756389e+13 2.098028e+14
 [941] 1.632476e+15 7.224233e+13 8.282345e+14 3.948125e+13 1.377804e+15
 [946] 2.967639e+15 4.714357e+14 3.293849e+13 6.211098e+14 2.560569e+13
 [951] 1.424982e+15 7.174580e+13 2.273361e+14 6.574101e+14 8.951762e+13
 [956] 8.361242e+14 3.617319e+14 3.683071e+14 2.824325e+14 3.752989e+14
 [961] 6.633502e+13 5.815641e+14 5.936787e+14 2.580509e+14 1.746600e+13
 [966] 2.610089e+14 6.191182e+13 5.733025e+14 1.604999e+15 1.652931e+13
 [971] 3.556556e+14 8.996852e+13 1.842709e+14 5.668110e+14 1.955270e+13
 [976] 7.211684e+13 1.187648e+15 7.906283e+14 1.179529e+15 2.627764e+15
 [981] 1.590341e+14 1.077766e+13 8.024473e+13 3.099723e+13 1.607253e+13
 [986] 1.229211e+13 2.719490e+14 6.126800e+15 2.408319e+15 5.638359e+14
 [991] 2.490241e+13 3.525220e+14 1.259903e+14 1.377938e+13 1.507008e+13
 [996] 1.766247e+13 6.615887e+14 5.807632e+12 3.000872e+13 6.654577e+12
[1001] 6.710636e+13 1.316206e+15 1.012310e+14 2.082309e+14 1.957945e+13
[1006] 8.936961e+14 2.162758e+14 6.012465e+14 4.387980e+14 1.112920e+15
[1011] 8.681723e+14 8.573694e+13 7.293989e+14 5.042388e+13 3.784520e+15
[1016] 3.569419e+13 8.077816e+14 1.973073e+15 7.904045e+14 2.130716e+15
[1021] 1.155795e+15 3.515550e+12 3.161738e+12 7.575355e+14 1.181796e+14
[1026] 8.062825e+14 5.141948e+14 3.427422e+14 3.069114e+14 4.958474e+13
[1031] 1.608734e+14 3.915200e+14 1.876468e+12 2.984604e+15 3.706739e+13
[1036] 8.846375e+14 1.190933e+15 3.206334e+12 1.641100e+15 5.937882e+14
[1041] 6.663661e+13 7.557703e+14 2.298246e+15 1.551160e+15 3.918607e+14
[1046] 1.878269e+15 1.077433e+14 2.646850e+12 3.552047e+14 4.211024e+14
[1051] 2.933555e+14 2.383845e+14 3.975053e+13 6.731342e+14 3.732335e+13
[1056] 1.103105e+14 1.480912e+14 3.281560e+14 1.396456e+15 2.368903e+14
[1061] 7.578413e+13 4.734665e+13 4.399066e+13 1.033551e+14 5.094800e+14
[1066] 1.160979e+14 6.409270e+14 2.487461e+13 2.802181e+13 4.614662e+14
[1071] 7.032410e+14 2.691497e+14 4.653310e+14 2.512345e+14 5.877157e+12
[1076] 7.171022e+13 1.432712e+14 4.869339e+12 8.377209e+13 1.039411e+15
[1081] 6.383718e+11 1.700108e+12 1.804810e+13 1.111120e+13 9.505227e+14
[1086] 4.276577e+14 9.857793e+12 1.206791e+14 4.488144e+15 1.737760e+14
[1091] 1.438185e+14 1.166843e+13 6.277025e+14 2.891403e+15 2.327296e+14
[1096] 9.352059e+12 5.334881e+13 0.000000e+00 2.765556e+14 1.398228e+14
[1101] 5.307976e+13 0.000000e+00 2.068388e+15 1.987713e+13 5.599644e+14
[1106] 2.571233e+12 5.597975e+14 4.206959e+13 1.942970e+14 2.788826e+15
[1111] 4.575961e+14 1.138289e+14 5.424677e+13 7.357784e+13 5.161544e+14
[1116] 3.049955e+13 8.247103e+11 2.979701e+15 7.996829e+14 3.299977e+13
[1121] 9.209796e+12 3.771288e+12 6.783514e+13 1.001437e+14 1.376751e+14
[1126] 3.398049e+15 1.003579e+15 2.392861e+13 2.355215e+14 9.818487e+14
[1131] 3.082774e+14 1.603607e+14 1.609696e+14 2.140845e+14 1.748918e+15
[1136] 3.270807e+14 9.466427e+14 2.461387e+13 2.946688e+13 1.395409e+15
[1141] 4.050678e+13 2.120926e+14 1.792324e+15 8.591148e+12 1.162189e+15
[1146] 2.323225e+14 3.342150e+15 3.592349e+14 5.039138e+13 3.687834e+14
[1151] 2.145362e+15 2.272165e+12 1.838205e+13 1.474254e+15 3.564612e+14
[1156] 6.845046e+14 4.204079e+12 1.541456e+15 8.106233e+14 1.426549e+15
[1161] 4.207005e+14 7.759080e+12 1.330800e+13 4.289724e+14 1.613801e+14
[1166] 1.496368e+14 1.701660e+14 8.208426e+12 1.552600e+14 1.503849e+14
[1171] 1.076050e+14 3.170630e+15 1.571576e+15 8.194456e+13 8.178835e+12
[1176] 8.431800e+14 4.370423e+13 6.351741e+12 4.580838e+14 0.000000e+00
[1181] 9.409137e+13 1.413826e+14 4.499791e+13 2.602467e+12 8.179316e+12
[1186] 1.393315e+13 1.161985e+15 1.576774e+14 2.365302e+14 1.216954e+15
[1191] 4.614539e+13 7.658259e+14 1.923049e+13 2.013072e+12 2.178544e+14
[1196] 7.064251e+14 3.230219e+12 4.847260e+14 1.944168e+13 2.029206e+14
[1201] 1.166237e+15 6.037786e+14 6.865627e+14 4.163778e+12 8.668216e+13
[1206] 3.031038e+14 1.165417e+14 7.354175e+15 1.360510e+15 1.514244e+13
[1211] 1.610652e+12 3.708327e+14 4.690076e+13 5.323069e+12 3.495131e+14
[1216] 5.018629e+14 2.131450e+13 7.239276e+14 3.191509e+15 9.094087e+14
[1221] 1.012759e+14 3.452128e+12 4.747110e+14 8.859988e+14 1.831523e+13
[1226] 2.298806e+14 4.018454e+14 9.091018e+13 1.253236e+15 1.085188e+15
[1231] 3.054672e+14 2.437948e+14 2.573464e+14 1.359640e+14 1.237546e+14
[1236] 2.496090e+14 2.433559e+13 4.915361e+11 4.306992e+14 5.278541e+14
[1241] 9.213961e+13 7.525310e+12 4.233156e+14 1.159979e+14 2.187503e+15
[1246] 1.413855e+14 4.296981e+14 1.538694e+14 5.172746e+15 3.694855e+13
[1251] 2.018606e+14 3.964606e+14 1.198111e+15 1.244442e+15 3.531411e+11
[1256] 5.820672e+14 5.939175e+13 2.026755e+14 1.771946e+14 1.323247e+13
[1261] 2.900578e+14 8.004336e+13 3.313169e+12 5.500579e+13 2.875238e+15
[1266] 1.804462e+15 1.460226e+15 5.342922e+15 4.811470e+14 9.949607e+14
[1271] 1.458457e+15 2.055453e+14 3.949335e+14 2.893817e+14 1.534693e+14
[1276] 3.071369e+15 3.885180e+14 1.213190e+13 9.092793e+12 2.729358e+13
[1281] 5.382561e+14 1.034064e+14 1.286323e+15 6.232043e+14 1.564167e+13
[1286] 7.139188e+13 1.383052e+12 2.370849e+14 5.719727e+12 3.010168e+13
[1291] 1.815999e+15 6.572585e+12 5.939054e+14 4.206638e+14 2.724791e+14
[1296] 1.546962e+13 1.437956e+15 6.681811e+13 5.949809e+13 2.056469e+15
[1301] 1.385692e+14 1.596001e+14 8.233130e+12 1.614853e+14 5.398707e+14
[1306] 2.466973e+14 2.006659e+14 3.664015e+15 7.922001e+11 7.443398e+14
[1311] 2.701029e+15 4.688755e+14 1.107651e+14 2.620611e+14 1.128622e+14
[1316] 1.732517e+15 2.834470e+13 3.650515e+12 8.716512e+13 1.714874e+14
[1321] 1.900133e+14 4.476526e+12 6.834346e+13 2.773552e+15 1.783286e+13
[1326] 1.648364e+13 1.396622e+13 1.724361e+15 9.353412e+12 4.559470e+13
[1331] 1.020442e+15 2.406497e+13 2.043472e+13 1.563488e+14 4.083417e+15
[1336] 1.380534e+14 5.769456e+13 7.494220e+12 1.803839e+14 3.891530e+14
[1341] 1.189307e+14 1.040909e+14 3.856553e+15 3.596948e+13 2.562944e+14
[1346] 9.243123e+13 1.790393e+15 2.666180e+14 1.473360e+15 9.150020e+13
[1351] 2.911626e+14 1.416919e+12 1.237918e+15 2.129558e+14 2.287512e+15
[1356] 2.811548e+14 2.394687e+14 4.000502e+15 7.971100e+13 1.033516e+15
[1361] 5.308097e+14 1.218510e+14 5.805870e+14 2.649575e+13 1.981954e+13
[1366] 1.503497e+15 3.810686e+14 5.396411e+14 2.383361e+13 6.512471e+12
[1371] 2.003316e+13 3.014815e+13 6.782318e+14 2.703928e+12 9.567620e+14
[1376] 8.661537e+13 2.335827e+14 1.961468e+15 5.941776e+12 9.187263e+13
[1381] 1.315020e+13 9.607321e+13 9.899569e+14 4.331982e+14 1.144190e+15
[1386] 4.966423e+15 8.669086e+13 1.350364e+15 1.890190e+14 3.590101e+13
[1391] 1.969255e+15 2.490401e+14 1.106536e+15 1.296033e+14 2.995675e+11
[1396] 7.659150e+14 3.641760e+13 3.332391e+15 2.089825e+14 1.106573e+15
[1401] 2.615996e+15 9.326402e+12 1.230700e+14 1.649261e+14 5.625206e+14
[1406] 6.015267e+12 5.037183e+13 5.490452e+15 2.535432e+12 1.160706e+15
[1411] 1.451384e+14 3.877399e+14 8.418180e+14 4.012579e+12 2.720430e+13
[1416] 7.068939e+14 1.136380e+15 1.386677e+14 8.521899e+14 5.645651e+13
[1421] 3.713202e+13 3.121887e+14 7.943445e+14 7.488711e+14 1.437049e+14
[1426] 1.404640e+14 1.300693e+15 6.607593e+12 8.251533e+13 2.954190e+14
[1431] 6.245265e+13 3.945658e+14 7.803902e+14 8.724677e+13 4.733038e+14
[1436] 1.999055e+14 3.131502e+14 6.854916e+13 3.219769e+14 5.248602e+15
[1441] 1.768511e+14 4.002901e+15 4.571559e+12 1.303561e+15 4.168672e+14
[1446] 1.266427e+14 2.506470e+15 2.984474e+14 3.579199e+13 5.089999e+14
[1451] 5.944698e+14 4.351414e+14 2.649213e+15 1.341832e+14 6.608852e+15
[1456] 2.483147e+15 3.071691e+14 1.292188e+14 1.183485e+15 5.595125e+14
[1461] 1.632612e+15 4.566746e+14 1.502982e+15 1.913122e+14 2.641105e+12
[1466] 8.537883e+14 2.034567e+15 3.401802e+13 2.222476e+14 7.594416e+14
[1471] 1.309846e+15 4.510026e+13 2.993994e+15 4.958530e+14 1.603019e+14
[1476] 1.775669e+14 2.234544e+14 1.349400e+15 5.420986e+15 4.795033e+14
[1481] 1.185362e+15 7.690885e+13 7.588461e+14 5.337013e+14 6.176677e+14
[1486] 5.446531e+13 1.489416e+15 1.333203e+12 3.238060e+14 4.633585e+14
[1491] 5.608934e+15 3.332825e+15 4.292203e+14 1.069557e+15 1.037023e+14
[1496] 5.011562e+15 1.754585e+14 1.705602e+15 6.663085e+15 2.291647e+14
[1501] 2.273582e+13 2.628466e+13 2.190647e+13 2.983776e+13 6.210479e+12
[1506] 2.310036e+14 1.368351e+13 2.805534e+14 1.981313e+14 3.721605e+14
[1511] 1.403880e+15 1.993827e+15 2.955627e+15 2.134900e+12 7.706201e+13
[1516] 1.407270e+15 3.670263e+14 3.827969e+14 1.421365e+14 1.509256e+15
[1521] 8.403716e+13 3.178659e+14 6.281804e+11 6.539647e+14 1.260076e+13
[1526] 3.095394e+12 7.573035e+14 1.005376e+13 7.378639e+13 2.027434e+14
[1531] 3.397565e+14 1.867527e+14 1.854658e+15 4.265259e+13 2.694042e+15
[1536] 1.249798e+14 2.938725e+15 7.047723e+12 8.846460e+14 1.737471e+13
[1541] 3.776827e+15 4.770734e+14 9.015169e+13 1.858518e+14 4.783161e+11
[1546] 1.318522e+13 2.567841e+13 4.276047e+14 1.344384e+13 2.053685e+14
[1551] 6.841292e+12 1.465224e+15 4.358801e+15 8.888964e+14 2.596760e+14
[1556] 2.134816e+15 5.853513e+12 1.034665e+14 1.176053e+15 7.044341e+14
[1561] 6.332656e+13 0.000000e+00 5.478874e+13 1.341048e+13 1.062675e+14
[1566] 2.684086e+15 2.738001e+14 1.025160e+14 5.355255e+14 1.883489e+14
[1571] 4.821612e+14 4.169193e+11 2.271320e+14 3.573653e+14 1.786381e+15
[1576] 1.734665e+13 1.368029e+14 1.001786e+14 6.005242e+14 4.121897e+14
[1581] 3.182538e+14 1.587686e+14 5.258574e+14 4.840186e+14 6.364936e+12
[1586] 1.219855e+15 3.617662e+15 4.932601e+14 2.574635e+15 2.782640e+15
[1591] 1.621468e+13 2.014764e+15 2.186052e+13 8.659741e+14 2.800466e+15
[1596] 5.373727e+15 5.351814e+13 2.550402e+13 2.242748e+14 2.183333e+14
[1601] 1.485910e+14 7.591958e+15 4.975027e+13 1.116239e+15 1.219724e+13
[1606] 2.072765e+15 7.354113e+12 2.955786e+14 8.021019e+13 8.539456e+14
[1611] 3.393929e+15 1.716724e+14 3.429742e+13 4.683051e+14 2.917997e+14
[1616] 8.956366e+13 2.213295e+14 6.992758e+14 1.380839e+14 3.559476e+14
[1621] 6.687296e+14 1.533965e+15 1.675052e+13 4.987229e+12 3.613427e+14
[1626] 1.309108e+14 1.893752e+14 1.058430e+15 4.540449e+15 1.857514e+15
[1631] 5.957873e+13 1.019103e+15 1.210211e+14 1.373023e+12 1.275785e+14
[1636] 2.475413e+15 2.702420e+12 8.286328e+13 2.447875e+15 4.674460e+13
[1641] 1.898255e+15 1.741327e+14 1.489881e+13 4.045213e+12 2.499571e+14
[1646] 1.458195e+15 6.736209e+13 8.664545e+14 3.983232e+14 4.532964e+14
[1651] 2.260641e+15 1.749615e+14 1.883718e+15 7.477172e+14 1.642633e+13
[1656] 5.356521e+15 4.118610e+15 1.486847e+13 1.473067e+15 2.307659e+14
[1661] 3.864857e+13 1.800649e+14 1.665002e+15 3.193568e+14 3.767516e+14
[1666] 1.095391e+13 8.839245e+14 5.629450e+14 6.722401e+15 8.210925e+14
[1671] 4.816369e+13 5.496080e+14 5.598742e+14 1.202183e+15 1.550476e+15
[1676] 9.609695e+12 2.300985e+15 6.015067e+14 2.025230e+12 9.229266e+14
[1681] 1.475369e+13 4.903841e+13 8.615891e+14 2.174325e+13 3.392038e+15
[1686] 5.954622e+14 4.544323e+14 1.158450e+15 5.591066e+14 6.479218e+14
[1691] 3.706960e+14 3.005968e+13 2.985294e+15 3.417380e+14 2.400985e+14
[1696] 2.767881e+14 5.953123e+14 6.899622e+14 5.623192e+12 1.842134e+12
[1701] 2.683068e+13 1.936803e+13 8.749765e+12 3.889397e+13 5.401166e+14
[1706] 9.147306e+14 9.158539e+13 3.872683e+12 5.411768e+14 1.075271e+13
[1711] 2.191825e+14 1.043377e+14 1.844331e+14 5.058261e+14 1.167742e+13
[1716] 3.310226e+14 3.467914e+14 9.844137e+14 5.939112e+14 1.845391e+15
[1721] 1.142418e+15 1.541903e+13 1.187910e+15 8.238200e+13 2.990874e+14
[1726] 1.041705e+15 1.226502e+14 1.334987e+15 1.033192e+13 2.406452e+14
[1731] 5.475262e+13 6.807132e+12 3.377145e+14 8.494441e+14 3.326360e+14
[1736] 1.189935e+13 2.092988e+15 1.241026e+14 5.859905e+14 7.575587e+14
[1741] 5.379130e+12 2.674160e+13 3.636845e+15 5.488854e+14 9.370453e+13
[1746] 2.410913e+15 3.683860e+14 7.232930e+14 1.387193e+15 9.921920e+14
[1751] 4.709263e+12 7.128655e+14 3.676425e+14 4.556845e+13 1.106413e+14
[1756] 2.632892e+14 2.214426e+15 1.075288e+14 8.412862e+12 1.009705e+15
[1761] 3.014552e+14 7.577315e+15 5.043117e+13 7.862233e+12 2.322667e+14
[1766] 3.049521e+14 6.150655e+14 6.549040e+14 2.510683e+14 0.000000e+00
[1771] 2.197029e+14 2.300665e+14 4.733649e+13 1.585271e+13 8.641682e+13
[1776] 2.272679e+14 5.399106e+12 5.470845e+14 2.847123e+14 2.006657e+15
[1781] 1.386224e+15 3.338341e+14 1.497063e+15 1.103201e+15 7.617919e+13
[1786] 2.801119e+14 3.009857e+15 6.753836e+14 5.873987e+13 1.138726e+14
[1791] 7.161952e+13 9.311470e+13 4.043141e+13 1.294389e+15 1.958580e+14
[1796] 2.865506e+12 0.000000e+00 1.648977e+15 2.961336e+13 7.717849e+14
[1801] 1.063662e+13 1.670674e+14 9.249199e+14 1.072837e+14 2.590147e+14
[1806] 7.144884e+14 5.236575e+14 2.411874e+14 3.813796e+14 8.814134e+13
[1811] 2.396605e+14 1.326927e+15 3.491697e+15 1.005651e+14 6.931237e+14
[1816] 1.630145e+15 5.785336e+15 2.610094e+13 8.566753e+14 2.578049e+14
[1821] 3.492073e+12 2.910138e+15 7.531571e+13 1.014091e+15 3.077235e+14
[1826] 4.723391e+13 6.791255e+14 1.618625e+15 4.940784e+14 2.941522e+14
[1831] 8.579021e+12 6.126074e+14 2.524411e+14 6.471225e+14 3.120385e+14
[1836] 1.029159e+14 6.334639e+14 2.686255e+15 2.039492e+13 1.003328e+14
[1841] 8.116683e+12 6.698249e+13 2.288571e+13 1.127511e+14 1.330626e+14
[1846] 1.813861e+15 1.904292e+14 6.918814e+13 1.086160e+15 1.213915e+15
[1851] 5.366914e+14 4.575024e+14 4.156505e+13 2.211482e+15 7.291643e+15
[1856] 3.258669e+13 1.024508e+15 3.719212e+13 7.038467e+14 2.192065e+15
[1861] 3.157609e+14 2.379023e+14 1.719695e+14 1.289265e+14 3.398180e+15
[1866] 2.044207e+14 1.606467e+14 1.913240e+15 4.828701e+13 3.583934e+14
[1871] 1.299994e+14 4.238066e+14 5.312951e+14 2.134386e+13 2.562611e+14
[1876] 4.984601e+12 2.849550e+15 2.508811e+14 1.503157e+13 1.411311e+15
[1881] 4.078243e+14 9.154287e+13 1.307586e+15 1.021360e+15 1.041951e+13
[1886] 1.486597e+15 3.381230e+12 4.835266e+15 7.442968e+14 8.346682e+14
[1891] 3.133885e+14 5.739349e+13 2.795619e+15 1.104633e+15 1.225635e+15
[1896] 1.190378e+14 2.971403e+15 1.518809e+14 1.159921e+12 1.010475e+14
[1901] 2.042048e+13 4.753536e+14 6.135682e+14 1.660452e+15 1.297421e+13
[1906] 6.746161e+14 9.120300e+14 9.302310e+14 1.675142e+15 4.365611e+13
[1911] 0.000000e+00 5.015850e+14 1.955001e+14 4.360299e+13 1.332978e+15
[1916] 2.097521e+15 1.540636e+13 6.841848e+13 1.018685e+15 2.836773e+12
[1921] 9.616248e+14 2.613126e+14 6.381235e+13 4.668468e+14 1.740033e+15
[1926] 1.464034e+13 5.763840e+12 6.663651e+14 1.089578e+15 6.917552e+15
[1931] 5.851402e+14 1.871730e+15 1.833504e+15 1.708301e+13 1.487748e+14
[1936] 6.968332e+13 3.389371e+13 3.894257e+13 4.352469e+14 3.737928e+15
[1941] 1.004914e+15 5.716915e+14 5.930691e+13 2.002456e+14 3.957934e+11
[1946] 2.778934e+15 1.133451e+14 2.712153e+13 3.333075e+15 4.036831e+12
[1951] 1.963464e+14 1.853412e+14 1.162015e+15 2.942245e+15 2.412748e+14
[1956] 1.288547e+14 1.753251e+15 4.942440e+15 1.547054e+15 7.364982e+14
[1961] 1.539835e+14 2.711813e+13 6.785477e+13 7.973749e+12 1.098878e+15
[1966] 2.019956e+13 1.896834e+13 2.805059e+15 2.566928e+13 9.416310e+13
[1971] 2.700311e+13 2.116202e+15 1.767503e+14 1.887193e+14 3.870709e+12
[1976] 7.900742e+13 2.462614e+15 3.922222e+12 1.723110e+14 6.449161e+12
[1981] 1.852745e+15 3.677178e+14 5.509469e+14 3.822482e+14 5.651862e+15
[1986] 1.760049e+15 2.179426e+14 8.450474e+14 3.706237e+14 2.637900e+14
[1991] 1.386579e+14 6.591369e+14 3.260508e+14 2.218632e+14 6.404150e+12
[1996] 1.052167e+14 5.458628e+14 4.695908e+14 4.983530e+13 5.509574e+15
[2001] 8.848913e+14 2.082915e+12 7.950152e+11 1.913567e+14 1.067662e+14
[2006] 1.609223e+15 4.820274e+14 2.207080e+14 1.795136e+15 9.163312e+14
[2011] 7.505283e+14 2.732627e+15 9.127270e+15 3.053091e+13 4.137449e+14
[2016] 9.190331e+14 4.943565e+14 4.620653e+15 9.788253e+14 1.895576e+14
[2021] 1.964289e+15 2.555685e+15 1.575196e+15 6.615780e+14 1.450659e+15
[2026] 3.295672e+14 7.744335e+14 2.911974e+12 8.225357e+13 0.000000e+00
[2031] 1.808665e+15 4.523748e+14 2.614172e+15 1.885323e+14 2.594399e+14
[2036] 1.309264e+15 7.635199e+13 1.213877e+14 1.245111e+14 1.497866e+14
[2041] 2.194561e+14 7.540432e+14 7.576046e+13 2.821088e+14 1.784646e+14
[2046] 2.133899e+15 2.450794e+14 3.866390e+13 4.870895e+14 6.269574e+13
[2051] 1.307460e+15 2.510097e+15 7.594415e+14 2.098056e+14 1.529027e+14
[2056] 1.649806e+14 2.349196e+14 5.899308e+14 7.778884e+14 3.175365e+14
[2061] 8.933827e+12 8.961209e+13 1.108723e+15 5.196542e+14 5.253166e+12
[2066] 4.356366e+15 7.414453e+12 1.421124e+14 1.279991e+14 3.599764e+14
[2071] 1.550495e+14 1.706896e+14 4.351498e+14 1.844628e+13 7.424708e+13
[2076] 6.823523e+13 1.204760e+15 1.752056e+13 1.672307e+14 3.105923e+14
[2081] 7.546634e+12 6.524198e+14 6.252459e+13 3.179421e+13 4.669659e+14
[2086] 1.224108e+15 7.151547e+12 0.000000e+00 1.747607e+14 2.674926e+14
[2091] 9.372834e+13 4.820296e+13 3.978929e+14 9.241755e+12 1.830763e+14
[2096] 6.382219e+13 1.172402e+14 3.570849e+15 3.590779e+14 3.945271e+14
[2101] 2.983215e+14 2.625969e+15 1.019775e+13 3.311270e+14 1.427880e+13
[2106] 1.537303e+14 3.562401e+13 1.817934e+15 3.464974e+14 1.314727e+15
[2111] 1.026602e+14 1.392294e+15 2.952226e+14 2.470235e+15 1.001000e+14
[2116] 1.810094e+14 3.157757e+14 2.868382e+13 3.697249e+15 8.444933e+13
[2121] 2.971714e+15 1.875385e+15 4.218798e+13 2.766597e+15 1.630809e+14
[2126] 6.409083e+14 2.931302e+14 6.304294e+13 9.248114e+13 1.939787e+15
[2131] 1.716279e+14 1.716551e+15 4.889266e+13 1.331888e+14 2.722932e+13
[2136] 4.698654e+14 4.541773e+13 9.238389e+14 2.252208e+14 3.587649e+15
[2141] 2.296742e+14 1.008224e+14 1.860492e+15 2.093714e+14 1.794307e+15
[2146] 5.875302e+14 9.563731e+14 8.065578e+15 4.694241e+12 1.817321e+14
[2151] 2.541143e+15 2.139633e+15 3.555316e+12 4.173406e+13 4.283043e+15
[2156] 1.024692e+15 5.590549e+14 3.452950e+13 7.753636e+14 1.814867e+15
[2161] 2.274336e+14 9.884106e+14 1.035451e+13 1.585336e+13 2.995101e+13
[2166] 1.917101e+13 6.873651e+14 2.010198e+15 3.379036e+13 7.976165e+13
[2171] 1.316325e+15 8.068510e+14 2.285404e+15 1.253828e+13 1.174142e+14
[2176] 1.497832e+15 1.918821e+14 5.957231e+13 3.099275e+14 1.970220e+14
[2181] 7.932541e+14 2.277646e+15 3.242514e+14 7.156586e+13 2.721454e+15
[2186] 3.415901e+14 7.606369e+13 1.096041e+15 6.669273e+14 7.529995e+14
[2191] 1.124196e+15 1.074786e+16 1.852659e+14 4.076987e+15 5.753614e+14
[2196] 7.585848e+13 1.195416e+13 9.230525e+15 5.365797e+13 2.394656e+15
[2201] 8.347983e+14 9.007386e+14 6.470931e+12 1.986035e+15 9.653816e+13
[2206] 2.719658e+12 5.647539e+15 5.385547e+14 2.710377e+14 1.795637e+14
[2211] 1.069989e+15 2.440566e+12 1.774749e+15 8.549815e+14 1.217004e+15
[2216] 5.607839e+14 1.695207e+15 1.529638e+15 2.275330e+15 7.454193e+14
[2221] 9.070995e+15 1.731202e+15 2.939264e+15 1.087315e+13 1.880567e+15
[2226] 3.953926e+14 1.463939e+14 1.352003e+15 2.268029e+14 2.446077e+14
[2231] 4.841082e+14 4.395518e+15 1.377997e+15 1.612460e+14 2.874235e+15
[2236] 2.592201e+15 8.099760e+13 1.457901e+14 4.874197e+14 2.738156e+15
[2241] 1.586661e+14 1.273844e+15 1.694302e+14 3.727089e+14 1.552137e+15
[2246] 7.675528e+15 4.101548e+15 3.093167e+12 2.661791e+15 3.972297e+15
[2251] 1.304662e+15 1.590757e+14 8.216105e+14 5.771100e+14 2.724902e+15
[2256] 3.119845e+14 5.693079e+15 3.036801e+14 3.955330e+14 7.329451e+13
[2261] 8.587023e+12 5.323441e+12 1.258168e+15 1.634167e+13 7.758616e+14
[2266] 2.267923e+14 4.615649e+14 1.377315e+15 2.833500e+15 5.348760e+14
[2271] 8.263304e+14 2.723481e+13 7.876265e+11 2.997812e+15 1.281355e+15
[2276] 1.002563e+15 1.639614e+14 5.070808e+12 1.600215e+14 2.470232e+14
[2281] 1.177584e+15 6.669144e+15 1.760215e+15 2.823418e+14 1.484106e+14
[2286] 3.760562e+14 3.289783e+14 1.186803e+14 3.354392e+13 3.842162e+13
[2291] 3.115959e+14 2.701351e+14 4.041729e+14 5.810855e+14 1.140424e+14
[2296] 5.137500e+14 6.840297e+13 2.434118e+15 2.008243e+15 5.596239e+14
[2301] 2.360816e+13 1.034598e+14 1.374308e+14 2.139315e+14 1.840037e+13
[2306] 1.089000e+13 7.060365e+11 2.326371e+14 2.253391e+15 3.943351e+15
[2311] 1.820106e+14 5.480895e+11 4.375380e+13 1.096910e+15 1.219745e+15
[2316] 7.793349e+13 2.744031e+14 8.563830e+13 1.684068e+15 2.158002e+15
[2321] 1.258356e+15 1.122228e+15 2.733451e+15 2.390442e+15 1.426866e+15
[2326] 4.882579e+15 1.583908e+14 2.998509e+15 3.548797e+12 1.366048e+15
[2331] 9.134660e+12 3.516688e+11 3.058629e+14 1.577049e+13 8.818013e+14
[2336] 1.392980e+13 9.095715e+12 2.629566e+14 1.155380e+14 3.980649e+14
[2341] 1.299995e+14 4.886403e+12 1.139963e+15 5.606886e+13 1.132316e+14
[2346] 1.249698e+14 1.323837e+15 1.785996e+14 7.754849e+13 5.771994e+14
[2351] 1.362483e+14 5.829754e+13 1.642812e+13 7.275462e+14 3.560428e+14
[2356] 1.806244e+15 3.968850e+15 6.463964e+14 2.603834e+11 2.248506e+15
[2361] 1.591890e+14 2.438178e+14 8.300693e+13 1.588733e+15 3.799215e+15
[2366] 1.137862e+13 0.000000e+00 1.170142e+13 2.132529e+14 8.658301e+14
[2371] 1.071378e+14 3.162568e+14 8.932498e+13 2.268875e+13 8.964243e+14
[2376] 2.775023e+14 4.705744e+13 5.243898e+13 7.872712e+12 6.355435e+13
[2381] 9.109196e+13 1.295212e+14 7.654481e+14 5.317404e+15 5.334479e+15
[2386] 7.738831e+14 4.205353e+12 2.052309e+14 2.956854e+14 1.807257e+15
[2391] 2.797878e+14 8.392170e+12 5.458613e+13 3.989436e+14 6.668717e+14
[2396] 1.253495e+14 5.883026e+13 1.037636e+15 2.092832e+13 6.504657e+13
[2401] 5.307166e+14 6.985955e+13 3.789354e+13 9.691839e+14 3.102687e+14
[2406] 3.625064e+14 6.920541e+14 1.877948e+14 2.686715e+13 2.669899e+14
[2411] 1.299857e+15 2.688183e+13 9.502452e+13 2.555687e+14 2.058441e+14
[2416] 2.122416e+15 4.099084e+14 8.495639e+14 3.825649e+13 4.634232e+14
[2421] 0.000000e+00 1.110451e+13 4.515338e+13 3.524918e+14 7.354728e+13
[2426] 1.583318e+15 4.403370e+14 5.152488e+14 4.077385e+13 6.171730e+14
[2431] 1.485723e+14 5.532676e+13 2.603211e+14 6.135198e+14 3.174805e+12
[2436] 8.709754e+13 1.549469e+13 1.375960e+15 4.483813e+14 2.189619e+14
[2441] 1.374842e+14 4.182512e+15 5.181481e+14 2.530455e+15 4.909867e+14
[2446] 1.391941e+12 1.472209e+14 1.496667e+14 0.000000e+00 6.606060e+13
[2451] 6.915743e+14 1.004314e+15 5.891048e+12 1.135885e+14 8.451620e+13
[2456] 5.546573e+14 3.223188e+14 1.349869e+15 2.185631e+13 6.628841e+13
[2461] 5.321928e+14 1.831830e+14 3.864255e+13 3.328629e+14 5.101100e+14
[2466] 3.748861e+14 5.549026e+15 4.158759e+15 6.242982e+12 9.986342e+13
[2471] 4.221632e+13 1.318928e+14 1.759790e+14 6.240596e+14 1.998018e+14
[2476] 1.231520e+15 4.499100e+14 6.779232e+13 3.820660e+14 7.937153e+15
[2481] 3.364737e+15 7.508424e+11 4.953141e+14 2.404069e+15 1.058081e+15
[2486] 2.370304e+15 5.656132e+14 1.255220e+15 2.784927e+14 5.837078e+14
[2491] 8.645155e+14 1.448269e+14 5.264728e+14 6.139862e+14 6.174441e+14
[2496] 3.484158e+14 1.817385e+14 5.687895e+13 7.683785e+13 6.139497e+13
[2501] 1.193556e+15 7.622937e+14 5.977714e+13 2.741504e+14 1.206663e+13
[2506] 4.201311e+15 1.493775e+14 1.554256e+15 4.288773e+14 2.532577e+13
[2511] 7.316233e+13 2.814831e+14 8.800145e+13 4.540326e+14 6.119308e+13
[2516] 1.369101e+15 1.192340e+12 5.258243e+14 6.922982e+13 1.086471e+15
[2521] 2.198194e+15 1.164017e+15 0.000000e+00 6.549368e+13 2.165085e+15
[2526] 1.236853e+15 6.311912e+13 3.145677e+15 5.386529e+13 3.522601e+13
[2531] 1.931682e+15 1.874767e+14 8.112118e+13 3.457613e+13 8.537916e+13
[2536] 5.529376e+15 1.712424e+14 5.741173e+13 7.626139e+13 1.372895e+13
[2541] 1.035945e+14 8.694074e+12 5.563623e+14 2.920862e+14 2.476760e+14
[2546] 5.204898e+14 6.658094e+12 3.161193e+14 4.227225e+15 1.437445e+15
[2551] 1.149815e+15 4.534902e+14 1.726299e+15 2.664152e+13 2.657573e+14
[2556] 5.211642e+14 3.974585e+14 1.194173e+15 6.867658e+13 2.538012e+13
[2561] 2.954340e+14 1.482027e+13 2.851494e+14 6.958304e+13 1.219094e+14
[2566] 1.083128e+13 3.863152e+13 3.739154e+13 3.270711e+12 2.107442e+14
[2571] 6.040247e+13 1.065293e+14 8.519072e+14 0.000000e+00 7.846079e+13
[2576] 6.723717e+13 6.700255e+12 1.411876e+14 1.716018e+13 3.474923e+14
[2581] 1.062833e+14 1.032355e+13 1.092128e+14 1.736082e+13 2.035417e+14
[2586] 3.117082e+13 2.224831e+13 4.883742e+14 5.883229e+12 5.133163e+13
[2591] 2.767276e+12 3.053583e+14 3.187985e+14 3.271598e+14 2.775836e+14
[2596] 1.127323e+15 1.051439e+15 6.428581e+12 9.747064e+11 2.411565e+14
[2601] 7.226220e+13 7.446775e+13 2.447813e+14 4.533283e+13 1.616528e+14
[2606] 2.140455e+13 6.095496e+13 1.720767e+13 1.083439e+14 3.554694e+13
[2611] 0.000000e+00 2.453915e+13 5.529198e+13 3.679783e+14 2.931820e+12
[2616] 5.189607e+13 2.548623e+13 7.820080e+12 4.488734e+14 2.039262e+14
[2621] 3.728344e+13 1.302190e+14 5.829750e+13 1.208693e+13 1.304219e+14
[2626] 4.176918e+14 2.516080e+13 1.078960e+15 5.370506e+11 7.872327e+14
[2631] 2.626767e+12 1.661905e+12 2.074581e+14 3.098074e+12 4.923053e+13
[2636] 3.308773e+14 1.036756e+12 1.311144e+13 3.074847e+13 8.155440e+13
[2641] 4.277246e+14 1.383365e+15 3.517081e+13 1.223458e+14 4.052874e+13
[2646] 5.555686e+13 2.450418e+13 1.416872e+14 2.932495e+13 1.924041e+14
[2651] 2.662225e+13 2.483905e+14 3.279982e+14 1.127830e+13 6.505275e+12
[2656] 2.502344e+14 1.248380e+14 3.166491e+14 9.458278e+13 1.609344e+13
[2661] 2.111779e+14 7.686133e+13 6.380962e+13 9.221796e+12 1.293840e+13
[2666] 1.343951e+13 4.257771e+14 3.589904e+14 6.724743e+14 9.210718e+13
[2671] 0.000000e+00 7.844709e+11 1.022594e+15 1.345326e+14 3.753300e+13
[2676] 6.281526e+13 3.972905e+13 1.156737e+14 1.066336e+14 3.537599e+13
[2681] 1.724465e+14 1.082373e+15 2.784050e+13 7.798382e+12 2.108826e+14
[2686] 2.063042e+13 9.319178e+13 7.393708e+13 1.843097e+12 1.002499e+14
[2691] 0.000000e+00 7.431743e+13 2.113920e+14 2.309180e+12 7.136359e+11
[2696] 8.486283e+14 1.667591e+12 1.238685e+13 2.672728e+12 1.247394e+14
[2701] 7.058959e+13 1.208301e+15 1.159275e+14 1.772970e+13 2.755744e+14
[2706] 1.014178e+13 5.774242e+14 0.000000e+00 3.067059e+14 1.822697e+14
[2711] 3.044691e+14 1.609585e+13 9.042601e+12 3.338374e+12 1.022057e+14
[2716] 1.384169e+14 3.320049e+14 3.029624e+13 3.752923e+13 1.427290e+14
[2721] 1.040489e+15 1.386838e+14 5.896283e+12 6.864779e+12 8.325375e+13
[2726] 1.395858e+14 5.213391e+13 6.622356e+13 9.255157e+13 5.998786e+13
[2731] 2.801487e+13 2.729800e+14 2.574817e+13 1.345081e+14 4.307133e+14
[2736] 5.733280e+13 1.817343e+13 6.745346e+13 9.632989e+13 2.455760e+14
[2741] 3.497434e+14 1.043137e+14 2.860273e+12 2.038461e+14 3.553123e+14
[2746] 1.078830e+14 1.025041e+12 9.957082e+13 1.306393e+12 4.893096e+13
[2751] 1.958248e+13 2.408142e+14 2.545816e+14 1.285159e+14 3.211876e+13
[2756] 0.000000e+00 3.924209e+14 1.436167e+13 2.588166e+13 1.008730e+14
[2761] 8.949913e+13 2.042269e+14 3.630605e+13 3.435622e+14 5.715051e+13
[2766] 9.162648e+13 4.088142e+14 3.472119e+14 1.739864e+14 3.304175e+13
[2771] 7.163124e+14 4.432635e+12 4.453020e+13 1.712362e+14 4.038286e+13
[2776] 8.406923e+11 1.071929e+14 2.152679e+14 3.220195e+13 4.890397e+13
[2781] 7.047598e+12 1.554052e+14 5.765248e+13 5.119182e+12 3.186137e+14
[2786] 2.630775e+13 3.152246e+13 6.091635e+13 9.320049e+13 5.661485e+13
[2791] 7.763501e+14 2.177877e+13 9.905112e+12 5.563026e+13 1.184120e+13
[2796] 3.969652e+14 3.423266e+12 1.554823e+14 3.511513e+12 7.085516e+13
[2801] 1.727464e+14 1.039470e+13 1.968512e+14 4.252003e+13 1.079600e+13
[2806] 1.014619e+13 2.314189e+14 9.149343e+13 1.581768e+14 1.820008e+14
[2811] 7.025293e+13 2.479464e+13 2.472035e+13 3.811051e+13 1.402924e+13
[2816] 9.889043e+14 1.940970e+13 4.097842e+13 2.667360e+14 2.449409e+15
[2821] 1.187535e+13 7.574117e+13 8.636778e+13 3.216570e+11 2.711911e+14
[2826] 1.475097e+13 5.541838e+13 3.261576e+14 4.476394e+13 6.726625e+13
[2831] 1.040923e+14 5.504799e+13 1.448541e+14 5.922896e+13 5.754433e+14
[2836] 1.060411e+12 1.812017e+13 1.250690e+14 7.373555e+13 3.290595e+14
[2841] 8.098300e+13 9.274268e+12 1.290030e+13 8.357944e+12 6.018192e+14
[2846] 1.387060e+13 5.203437e+14 1.380427e+15 7.629333e+13 3.049468e+14
[2851] 5.138765e+13 1.512493e+13 1.946824e+15 2.206126e+12 3.329552e+14
[2856] 4.679235e+13 2.744880e+13 7.307038e+14 5.852213e+13 7.195884e+13
[2861] 3.165712e+11 8.825221e+14 5.061488e+13 6.900418e+12 9.799244e+13
[2866] 2.015768e+13 2.808896e+14 4.745803e+13 6.929206e+14 3.368515e+14
[2871] 3.583485e+13 2.889170e+14 3.102130e+13 1.885937e+14 1.727395e+15
[2876] 3.405904e+13 3.031273e+13 3.781926e+13 3.409819e+12 7.074402e+14
[2881] 1.467666e+13 4.179764e+14 2.519492e+13 2.684456e+14 5.478532e+12
[2886] 6.241060e+13 4.797192e+13 1.949424e+13 9.218048e+13 1.425589e+13
[2891] 3.104254e+13 1.644604e+14 3.989981e+13 3.576543e+14 1.434325e+13
[2896] 4.823528e+13 2.207800e+14 1.088963e+14 1.099724e+14 6.371253e+12
[2901] 2.509378e+14 1.677939e+13 1.189466e+14 7.646768e+13 7.372401e+13
[2906] 5.280437e+12 1.704356e+14 1.187543e+14 3.870271e+14 6.526521e+14
[2911] 3.396825e+13 1.069130e+15 8.937608e+13 3.959669e+14 5.319227e+14
[2916] 7.867895e+12 2.076171e+14 2.203807e+12 1.312034e+12 3.625326e+11
[2921] 1.127746e+12 5.141155e+14 2.381687e+12 1.644602e+14 4.273841e+13
[2926] 4.511202e+12 9.740340e+14 1.589853e+13 3.040274e+14 7.358022e+13
[2931] 4.229042e+14 3.507002e+14 9.380888e+13 1.115091e+15 2.406196e+12
[2936] 2.674942e+13 6.452570e+13 1.452219e+13 3.705173e+14 4.703458e+14
[2941] 2.153321e+14 4.758446e+11 2.390313e+13 1.315990e+14 1.584585e+14
[2946] 8.311841e+13 2.127037e+13 8.151110e+14 1.622846e+13 1.205844e+13
[2951] 1.439692e+13 1.576032e+13 1.665356e+14 7.897780e+13 3.670742e+13
[2956] 9.530618e+13 2.169005e+13 1.931693e+14 9.597897e+14 1.275795e+12
[2961] 8.613932e+14 3.757852e+14 4.554697e+13 1.457922e+14 4.535770e+12
[2966] 9.107272e+13 7.269951e+14 4.100282e+14 9.459938e+12 3.864936e+13
[2971] 1.830648e+14 1.171752e+14 1.870374e+14 3.641238e+14 2.650063e+15
[2976] 3.178588e+12 1.206755e+14 2.303347e+14 6.801452e+13 8.273184e+12
[2981] 5.191530e+12 1.624827e+13 2.019796e+14 7.476585e+13 4.357619e+13
[2986] 1.660127e+13 1.096688e+15 9.308001e+13 1.185913e+15 9.854289e+13
[2991] 7.279655e+14 4.508623e+14 1.653576e+14 2.582381e+12 1.780704e+14
[2996] 5.392901e+13 1.209140e+14 1.450889e+13 5.420869e+14 5.088904e+13
[3001] 3.254514e+14 4.355992e+13 6.813281e+13 2.347976e+13 1.517141e+14
[3006] 1.896821e+14 8.540241e+13 6.783804e+13 1.469462e+14 8.102237e+14
[3011] 2.847804e+13 1.950383e+14 2.558430e+13 7.956997e+13 2.757715e+13
[3016] 6.888048e+13 2.332998e+12 7.395368e+14 8.411202e+12 1.867822e+13
[3021] 5.305745e+12 6.277954e+14 1.885661e+14 2.506263e+13 1.310396e+13
[3026] 1.082977e+10 5.033581e+13 6.300079e+13 9.734614e+13 3.887429e+12
[3031] 6.726582e+13 7.572518e+13 1.245836e+14 1.650552e+13 5.455565e+12
[3036] 1.219720e+13 1.812085e+14 2.732928e+14 2.412727e+13 4.012568e+13
[3041] 4.481792e+14 7.343171e+12 8.125372e+13 1.648476e+13 3.863750e+12
[3046] 4.261593e+11 2.232556e+14 6.912220e+13 7.696251e+12 2.390463e+12
[3051] 4.538487e+13 3.661378e+14 0.000000e+00 8.246967e+11 8.901604e+13
[3056] 3.629185e+12 7.730212e+12 7.766716e+13 1.843799e+14 5.451213e+13
[3061] 3.506673e+14 1.212972e+13 5.034546e+13 2.239934e+11 0.000000e+00
[3066] 5.906990e+12 2.344935e+13 3.073343e+14 6.562628e+12 6.735350e+13
[3071] 4.751705e+13 1.548273e+13 8.552196e+13 4.396358e+12 5.309515e+12
[3076] 8.260942e+12 4.080449e+12 2.144814e+14 7.097112e+12 2.106050e+13
[3081] 8.974215e+12 1.079247e+14 1.864399e+14 1.074339e+12 1.438768e+12
[3086] 2.021416e+13 1.968637e+13 2.424415e+14 5.850681e+13 5.627358e+14
[3091] 4.942034e+13 9.823912e+13 3.903070e+13 2.222013e+12 5.657319e+14
[3096] 2.476067e+14 9.256696e+13 2.630971e+14 9.398588e+14 8.316466e+11
[3101] 1.113035e+15 1.294076e+13 3.046264e+14 1.486170e+14 1.195160e+14
[3106] 4.098051e+13 6.771081e+11 2.182907e+11 1.818476e+14 3.404518e+14
[3111] 2.086972e+13 1.187802e+15 1.468064e+13 1.007145e+14 9.890927e+12
[3116] 1.342596e+13 1.679985e+13 1.866721e+14 3.069187e+13 4.325514e+14
[3121] 3.127778e+13 2.424571e+14 1.615084e+14 4.147939e+13 1.966661e+13
[3126] 3.358204e+14 9.875298e+13 1.097166e+14 1.532551e+14 3.650398e+14
[3131] 3.025011e+14 9.494752e+11 1.249814e+13 4.865831e+13 2.986580e+13
[3136] 2.061421e+13 9.048675e+13 1.597291e+14 3.785872e+11 1.036241e+14
[3141] 1.037649e+14 7.149783e+13 4.249434e+14 4.096796e+13 2.426470e+13
[3146] 1.405759e+14 6.377987e+12 3.029892e+13 4.314743e+13 9.123785e+13
[3151] 9.396657e+12 6.215203e+13 1.540783e+14 4.458918e+13 1.125510e+14
[3156] 1.655809e+14 3.150365e+12 6.115341e+12 2.387360e+13 2.116063e+14
[3161] 5.899556e+13 1.144379e+14 2.300630e+13 1.049832e+13 7.830773e+13
[3166] 1.418656e+13 1.166425e+12 8.046937e+12 1.716741e+13 1.418334e+12
[3171] 9.161317e+13 7.810569e+14 5.862944e+13 4.982287e+12 0.000000e+00
[3176] 5.111498e+13 1.072811e+14 4.713758e+14 1.085860e+13 4.539040e+14
[3181] 1.801112e+12 3.518192e+13 3.477889e+14 7.237640e+13 1.652673e+12
[3186] 1.240787e+14 1.464876e+14 2.502325e+14 2.245037e+13 1.504207e+13
[3191] 6.088384e+14 1.283149e+13 0.000000e+00 7.678222e+14 7.456474e+14
[3196] 2.010171e+13 1.136913e+12 7.528982e+14 3.457255e+14 4.859585e+14
[3201] 2.505026e+13 4.881480e+12 4.955313e+14 1.558065e+14 1.811087e+14
[3206] 2.438413e+13 6.794077e+12 5.897370e+12 2.368695e+14 2.025482e+14
[3211] 1.241539e+14 1.175230e+15 9.212711e+14 4.676099e+14 4.478020e+13
[3216] 4.225738e+12 3.606040e+14 2.437734e+13 1.171838e+12 2.585304e+13
[3221] 5.585719e+13 1.035520e+14 0.000000e+00 9.290660e+13 1.672330e+12
[3226] 8.554007e+13 2.521402e+15 4.156092e+13 3.574659e+13 3.362602e+14
[3231] 9.530243e+13 3.093482e+14 1.441335e+15 4.118787e+14 4.680065e+13
[3236] 1.494218e+14 7.995645e+12 3.004304e+14 2.831998e+13 2.823211e+14
[3241] 4.232248e+14 8.235037e+13 1.996739e+13 6.430994e+13 1.557185e+14
[3246] 4.260541e+13 3.832953e+13 3.332702e+12 6.175824e+13 3.141721e+14
[3251] 1.466485e+13 4.807602e+12 6.494231e+13 4.287974e+14 1.170956e+15
[3256] 2.660499e+14 5.842981e+12 8.281714e+13 3.169964e+14 3.163139e+13
[3261] 4.673273e+13 4.169604e+13 1.154569e+14 6.304203e+14 5.203963e+14
[3266] 3.040503e+13 3.833198e+13 5.307372e+14 9.391439e+12 3.797996e+11
[3271] 1.068470e+14 1.037465e+13 2.945398e+13 3.089438e+13 2.305195e+14
[3276] 1.006954e+15 1.264652e+13 8.679383e+13 1.551807e+14 1.615384e+13
[3281] 2.762477e+12 9.208976e+13 1.864598e+14 2.702876e+13 1.813248e+13
[3286] 1.609784e+14 1.453361e+14 1.260250e+15 7.428632e+13 3.650205e+14
[3291] 7.222679e+13 1.651357e+14 6.812699e+12 2.163938e+12 4.329942e+14
[3296] 3.088524e+13 4.018988e+13 1.778603e+14 9.935844e+13 4.511166e+13
[3301] 7.276056e+13 6.110564e+13 3.137990e+14 1.306293e+13 1.728498e+14
[3306] 2.715650e+13 1.952381e+14 1.450054e+14 2.428838e+14 3.709437e+13
[3311] 2.461279e+14 5.549143e+13 1.394192e+14 9.862840e+13 1.457667e+14
[3316] 4.534948e+13 3.257011e+12 3.091904e+11 2.133199e+14 1.697307e+14
[3321] 1.642210e+14 1.023448e+14 2.593420e+14 3.006779e+14 2.769201e+13
[3326] 3.143816e+13 7.712069e+13 5.584462e+14 1.278552e+15 1.791347e+13
[3331] 5.202686e+13 1.402377e+13 1.170075e+14 2.229455e+12 1.179995e+13
[3336] 5.873654e+11 3.689572e+13 1.134482e+15 2.594239e+14 1.703964e+13
[3341] 1.850535e+14 9.077275e+12 2.377115e+14 1.626368e+15 1.250877e+13
[3346] 1.179135e+15 3.390594e+14 3.367956e+13 7.207059e+13 3.693579e+13
[3351] 1.594867e+13 6.401361e+13 1.967574e+14 6.699156e+12 2.268957e+14
[3356] 1.507221e+13 9.030511e+13 1.032113e+14 1.228574e+14 6.859354e+14
[3361] 0.000000e+00 3.696920e+14 2.866614e+14 1.075955e+14 3.782937e+13
[3366] 1.159967e+13 5.865386e+14 3.274113e+14 5.217760e+14 4.283794e+13
[3371] 4.119300e+13 1.047561e+14 1.762065e+14 9.813929e+12 3.234187e+14
[3376] 1.671633e+14 1.912375e+14 1.788650e+14 9.263044e+11 1.232451e+15
[3381] 2.146011e+14 1.424745e+13 3.444924e+14 1.364467e+13 1.089761e+13
[3386] 1.217072e+14 7.106736e+13 2.915830e+14 3.396964e+13 1.912598e+14
[3391] 4.068821e+13 1.509442e+14 1.527582e+15 3.476829e+14 1.169695e+14
[3396] 2.776511e+11 1.033195e+14 3.212561e+13 2.789573e+12 2.799710e+14
[3401] 5.202835e+13 2.232329e+14 6.790647e+14 4.662835e+13 2.419203e+15
[3406] 1.654288e+12 1.459460e+14 8.645940e+13 1.221904e+14 2.168223e+15
[3411] 2.842414e+14 2.198392e+13 8.003935e+14 1.187006e+14 0.000000e+00
[3416] 7.520102e+13 3.684660e+14 8.490318e+13 2.414767e+13 8.508556e+13
[3421] 1.142296e+13 2.016577e+14 1.997939e+12 4.466015e+13 2.167417e+14
[3426] 1.050279e+15 6.168639e+13 1.123980e+13 3.998671e+13 5.007144e+13
[3431] 1.612860e+14 2.754387e+14 3.675917e+14 2.990167e+14 4.981239e+14
[3436] 9.233209e+14 5.929449e+14 1.064578e+14 9.982766e+14 1.065358e+14
[3441] 1.417759e+13 2.893432e+13 4.215928e+13 3.730008e+13 1.819983e+13
[3446] 1.138211e+13 1.207813e+14 8.570218e+12 1.565158e+13 3.546067e+14
[3451] 1.287835e+13 7.508889e+13 1.113802e+13 2.021922e+14 5.104792e+13
[3456] 6.663536e+13 5.262979e+14 8.016176e+14 1.331289e+12 2.064158e+14
[3461] 8.774420e+12 1.844354e+15 1.313237e+15 9.041758e+14 6.250733e+14
[3466] 9.410875e+14 5.124953e+12 8.873252e+13 2.107429e+13 3.544575e+13
[3471] 5.462255e+13 6.775957e+13 3.392684e+15 1.372566e+14 4.345906e+14
[3476] 1.154467e+11 3.437782e+12 9.092398e+13 4.260161e+13 1.159731e+14
[3481] 1.302231e+15 1.061320e+13 3.200763e+14 3.157718e+14 8.626278e+14
[3486] 7.705413e+13 9.661989e+13 5.100481e+13 5.602300e+13 2.329386e+14
[3491] 2.983969e+14 7.972943e+13 1.020223e+15 9.415827e+14 1.429288e+14
[3496] 9.740199e+14 4.142235e+14 4.389991e+14 1.882291e+13 4.124209e+14
[3501] 2.243122e+14 1.466898e+14 2.796006e+14 3.830001e+14 3.966491e+15
[3506] 1.179051e+14 1.643051e+13 1.173439e+14 2.191001e+14 2.332506e+12
[3511] 8.023256e+10 5.753639e+14 3.936053e+14 8.149074e+13 6.721872e+12
[3516] 9.424237e+14 4.471364e+14 1.636822e+14 5.428389e+14 4.112298e+14
[3521] 5.345518e+14 1.678914e+14 1.753629e+14 2.135452e+12 1.549334e+15
[3526] 8.558889e+12 1.642529e+14 5.849732e+12 2.189476e+14 1.420985e+15
[3531] 1.171174e+14 2.768627e+14 6.964734e+14 7.381273e+14 2.674651e+14
[3536] 8.409194e+13 3.116621e+15 5.348078e+15 3.926880e+14 9.591032e+14
[3541] 3.048898e+13 1.090930e+16 1.617364e+12 1.542558e+14 6.377557e+14
[3546] 1.576993e+15 1.039986e+15 2.609700e+14 3.444141e+14 4.989379e+12
[3551] 1.160707e+15 1.327313e+14 1.322212e+13 5.150106e+14 3.556088e+14
[3556] 3.362475e+15 5.452526e+15 5.631810e+14 2.534159e+14 1.021876e+15
[3561] 1.502287e+15 1.313366e+14 2.517627e+15 5.445665e+14 1.511348e+14
[3566] 1.024392e+15 4.632536e+14 3.329463e+13 4.776153e+14 5.698875e+14
[3571] 2.649279e+14 7.413621e+13 1.630372e+15 1.617359e+14 8.560294e+14
[3576] 4.475429e+13 3.053111e+14 4.182422e+14 3.869752e+14 4.560170e+14
[3581] 5.382824e+15 4.932246e+15 1.360945e+15 2.669713e+15 4.726987e+14
[3586] 2.012845e+14 2.388920e+13 6.942846e+13 2.264525e+14 7.986063e+14
[3591] 1.819752e+14 4.418130e+15 1.292387e+15 8.423685e+14 3.703556e+14
[3596] 1.704863e+14 1.309289e+14 1.063978e+15 5.182475e+14 2.298038e+15
[3601] 3.838624e+12 1.962093e+14 8.107639e+14 2.361827e+15 2.422974e+14
[3606] 8.723883e+14 2.288630e+13 3.642558e+15 7.743416e+14 9.020487e+13
[3611] 1.575568e+14 5.794526e+14 2.387558e+15 9.555521e+14 2.885938e+14
[3616] 1.613423e+15 2.245410e+15 6.638101e+14 5.638263e+14 4.074472e+14
[3621] 1.119467e+15 2.866125e+13 2.315653e+12 9.413554e+13 1.326714e+14
[3626] 1.726721e+14 3.451538e+12 1.029029e+15 7.214079e+14 4.559005e+15
[3631] 2.095347e+14 3.016652e+14 5.573316e+13 1.729225e+15 5.041729e+14
[3636] 3.827918e+13 5.012079e+14 4.643344e+14 2.477745e+14 1.853751e+15
[3641] 2.545469e+14 1.721557e+14 3.140198e+14 3.806404e+14 1.170836e+15
[3646] 6.742607e+14 8.155839e+14 2.239038e+14 3.767417e+14 7.126982e+14
[3651] 3.861968e+14 2.675964e+14 4.125358e+14 1.585233e+14 2.320408e+14
[3656] 1.528713e+15 1.012068e+15 1.894679e+15 1.179393e+13 2.283465e+14
[3661] 4.713955e+13 6.043302e+14 2.660981e+14 9.676118e+14 1.232988e+15
[3666] 1.466858e+15 7.376547e+14 1.250850e+15 4.430621e+15 1.847617e+15
[3671] 6.617885e+14 2.228826e+14 1.344751e+14 1.232802e+15 3.602648e+15
[3676] 3.544050e+14 5.873406e+13 4.225640e+14 4.705628e+14 9.097953e+13
[3681] 1.653071e+15 3.980892e+14 3.637826e+15 5.223682e+15 7.899982e+14
[3686] 2.923524e+14 1.729318e+15 2.823473e+14 4.915237e+14 1.904985e+15
[3691] 2.923008e+15 2.091115e+15 1.342201e+14 3.518032e+14 6.194356e+14
[3696] 5.197539e+14 5.853684e+13 3.271936e+14 6.113587e+14 1.709749e+14
[3701] 2.694165e+14 1.375277e+15 1.734916e+13 2.830379e+14 1.391864e+14
[3706] 6.957955e+12 2.449683e+13 5.552368e+14 1.678090e+14 4.945135e+14
[3711] 4.675666e+14 8.163493e+14 2.636915e+13 5.470080e+14 1.960347e+15
[3716] 6.985226e+14 1.314093e+15 8.451935e+14 7.297896e+14 3.971596e+14
[3721] 2.039741e+14 1.333951e+15 8.678813e+14 1.293786e+15 2.706108e+14
[3726] 6.894043e+14 1.109487e+15 2.471317e+15 8.730303e+14 2.432907e+14
[3731] 1.328980e+14 9.153527e+13 3.255428e+14 5.010968e+15 1.851842e+14
[3736] 5.792002e+14 5.878989e+14 2.483208e+15 4.302700e+15 2.266701e+14
[3741] 9.125761e+13 7.416710e+14 1.315740e+15 2.005294e+14 3.969399e+15
[3746] 3.508461e+15 4.883912e+14 7.387778e+14 2.085536e+14 2.885378e+14
[3751] 4.238123e+15 7.964589e+14 6.457652e+14 2.699894e+15 2.227252e+14
[3756] 1.296886e+15 3.801562e+15 2.847889e+14 9.215979e+14 3.132546e+15
[3761] 1.492706e+14 3.315370e+14 2.334644e+13 1.711505e+14 9.801056e+14
[3766] 4.264474e+15 1.547052e+15 1.611312e+14 1.089891e+14 2.206736e+14
[3771] 7.793379e+14 1.976015e+14 1.855567e+15 4.300486e+13 5.141703e+14
[3776] 4.427279e+14 7.444629e+14 2.456954e+15 1.117869e+13 1.428185e+15
[3781] 7.652260e+12 4.675752e+14 2.377560e+15 2.625201e+14 1.595460e+15
[3786] 2.920460e+14 2.244328e+14 1.732086e+13 6.340171e+14 1.764702e+15
[3791] 4.671458e+14 1.192021e+14 1.010696e+14 2.313830e+14 1.883963e+14
[3796] 3.562703e+14 2.832774e+14 1.083327e+15 1.042358e+15 3.561098e+14
[3801] 4.842770e+14 5.369423e+14 1.401618e+14 2.602514e+14 1.490052e+15
[3806] 7.198041e+14 8.767547e+14 4.834626e+14 4.283284e+14 6.122516e+14
[3811] 1.141378e+13 2.632422e+14 1.577530e+14 9.741620e+14 1.717601e+14
[3816] 7.520171e+14 2.118531e+14 9.679857e+12 2.387166e+14 3.149163e+14
[3821] 8.843064e+14 3.878258e+14 1.606565e+15 4.580430e+14 5.897922e+13
[3826] 7.072807e+13 1.359277e+15 4.532651e+13 1.147296e+15 1.782142e+14
[3831] 3.059581e+13 1.171918e+15 1.109167e+14 4.461287e+14 3.228864e+14
[3836] 3.561793e+14 4.522207e+14 2.371323e+13 5.092513e+14 1.399937e+14
[3841] 2.042727e+14 1.515844e+14 3.766911e+14 1.065034e+15 3.757440e+13
[3846] 2.943876e+14 6.302263e+14 7.514968e+14 3.891045e+14 1.722195e+14
[3851] 1.400216e+14 1.200229e+14 1.111491e+14 1.362660e+15 9.220184e+14
[3856] 1.936988e+14 2.097594e+15 1.317119e+14 2.919673e+14 3.364115e+14
[3861] 5.718353e+14 2.760104e+14 3.170881e+14 1.820288e+15 7.101071e+14
[3866] 1.727093e+14 3.087210e+14 8.208643e+13 1.888359e+14 2.852970e+14
[3871] 7.837319e+14 1.875047e+14 1.869598e+14 1.824354e+15 3.741192e+13
[3876] 1.807287e+14 3.576009e+14 8.345699e+14 2.146728e+15 1.573045e+14
[3881] 3.268578e+14 1.465486e+14 3.230645e+14 2.752615e+15 8.412297e+14
[3886] 3.262769e+13 1.211621e+14 4.728572e+13 2.886602e+15 2.102657e+15
[3891] 3.864067e+14 2.041728e+14 3.903101e+14 7.536935e+13 6.837468e+12
[3896] 3.108163e+14 7.601917e+13 1.010934e+15 3.091266e+14 1.889430e+14
[3901] 2.356435e+14 2.827435e+14 2.645878e+14 4.573474e+14 4.023252e+14
[3906] 6.016671e+13 4.321084e+14 1.401038e+14 5.831246e+14 4.681070e+14
[3911] 2.361849e+14 1.516299e+15 1.750145e+14 7.690842e+13 2.055496e+14
[3916] 3.956688e+13 5.885726e+14 2.127604e+12 4.137061e+14 1.208929e+14
[3921] 1.237975e+14 1.055274e+15 1.024366e+14 1.591391e+14 9.482689e+13
[3926] 4.257920e+12 1.793569e+13 1.854875e+14 1.583516e+14 3.172474e+14
[3931] 7.067746e+13 4.454157e+14 6.819755e+14 9.000162e+14 1.908091e+13
[3936] 2.790496e+14 3.296076e+13 7.786685e+14 1.512141e+14 4.704426e+13
[3941] 1.596953e+15 2.007956e+15 8.771198e+14 1.289024e+14 4.234652e+14
[3946] 1.662724e+15 8.321234e+14 2.653000e+12 6.440485e+13 2.179177e+13
[3951] 5.449634e+14 3.000306e+12 3.698827e+14 1.688038e+15 2.481968e+15
[3956] 1.592913e+15 8.777343e+13 1.355319e+15 4.667170e+13 5.735648e+14
[3961] 2.425747e+14 3.845785e+14 2.816460e+14 2.808856e+14 8.173581e+13
[3966] 1.099252e+14 5.453686e+13 2.565842e+14 8.923281e+13 3.611539e+13
[3971] 2.132599e+14 1.797381e+14 2.414333e+15 1.408805e+13 9.172819e+14
[3976] 2.644268e+14 1.522157e+15 2.826238e+14 5.040448e+13 2.433747e+14
[3981] 5.952523e+14 4.379750e+13 1.171177e+13 1.759730e+14 2.653440e+14
[3986] 5.227312e+14 1.983225e+14 4.210429e+13 1.199168e+15 1.249603e+14
[3991] 4.321591e+14 2.361488e+14 1.894653e+13 1.178246e+15 1.003662e+14
[3996] 9.865364e+14 1.201262e+12 9.270854e+14 6.278105e+13 9.141584e+14
[4001] 9.810305e+14 7.278405e+13 1.556220e+14 7.229405e+13 1.660175e+13
[4006] 2.791016e+14 1.098003e+14 1.715141e+14 7.097652e+14 2.239131e+14
[4011] 2.581729e+14 2.943347e+14 2.949176e+14 5.817824e+13 9.547082e+13
[4016] 2.055332e+14 3.554422e+14 8.082418e+14 1.495654e+14 1.587104e+14
[4021] 3.295184e+14 7.139460e+14 2.453300e+14 2.982157e+13 2.184394e+14
[4026] 7.801753e+14 7.171337e+14 2.299488e+14 1.031409e+12 1.903052e+15
[4031] 3.633099e+14 2.274261e+15 4.651334e+14 4.810109e+13 1.865100e+14
[4036] 6.568630e+13 2.918297e+14 7.562708e+14 3.038264e+13 1.700014e+14
[4041] 6.513154e+14 1.773522e+14 6.600548e+14 6.109275e+14 2.508509e+14
[4046] 7.360723e+13 4.603834e+13 7.620036e+14 1.938600e+14 2.280885e+14
[4051] 2.728894e+14 1.194191e+15 4.680746e+14 3.394012e+14 7.087210e+13
[4056] 1.040605e+14 3.425419e+13 5.356622e+14 1.752548e+15 3.637026e+14
[4061] 3.234175e+14 1.668814e+13 5.501066e+13 4.641445e+13 2.605870e+12
[4066] 2.173918e+13 1.476351e+14 4.129527e+14 4.191189e+14 1.509600e+14
[4071] 5.331981e+13 7.823781e+14 1.543366e+14 2.154369e+14 1.348038e+14
[4076] 5.289731e+14 1.054365e+13 1.530408e+14 6.563843e+14 3.456187e+13
[4081] 4.366686e+14 2.589465e+13 6.907031e+12 8.023124e+13 6.215773e+14
[4086] 7.982564e+14 1.702723e+14 1.276697e+14 4.050194e+13 8.605233e+14
[4091] 2.688152e+14 1.713215e+14 2.285166e+13 3.648466e+13 5.812787e+14
[4096] 1.540628e+14 2.068249e+14 1.240305e+14 1.132868e+15 2.680412e+13
[4101] 6.953356e+13 1.422254e+15 1.521292e+13 5.117404e+13 1.586352e+14
[4106] 2.635452e+14 2.733707e+13 9.840489e+14 2.252561e+14 2.843323e+14
[4111] 1.387684e+15 8.291921e+13 1.008300e+14 7.519914e+14 8.028937e+13
[4116] 3.258471e+13 6.917559e+13 9.141832e+12 1.178822e+14 4.479078e+14
[4121] 5.260859e+13 6.120958e+14 5.685525e+15 3.311080e+13 3.438151e+14
[4126] 1.788747e+14 3.480325e+14 4.577395e+13 1.141705e+15 1.224025e+14
[4131] 1.707764e+14 7.888831e+13 2.758595e+14 2.130645e+14 1.486118e+13
[4136] 9.832204e+12 6.317002e+14 6.780782e+14 1.174477e+15 2.682879e+14
[4141] 1.063663e+14 8.810159e+13 2.124415e+14 3.695436e+14 1.041455e+13
[4146] 1.250261e+15 3.002903e+14 6.503643e+14 1.388424e+13 5.909862e+13
[4151] 8.526731e+14 2.117646e+13 3.109886e+13 1.077314e+14 5.563071e+12
[4156] 7.712762e+14 2.102186e+14 1.411018e+13 1.946375e+14 1.251681e+13
[4161] 3.498435e+13 2.975454e+14 5.087500e+13 6.043883e+13 6.569374e+12
[4166] 4.875495e+13 1.433068e+14 8.378078e+13 2.285292e+14 3.350335e+14
[4171] 3.400324e+14 3.831321e+14 6.294158e+12 5.610854e+13 4.485469e+13
[4176] 2.675617e+13 2.272918e+14 4.014429e+13 9.108812e+12 1.411139e+13
[4181] 6.094760e+13 7.476635e+13 2.486005e+13 1.503024e+13 9.656934e+12
[4186] 1.012278e+14 3.761787e+14 1.180429e+14 4.243464e+13 1.879756e+14
[4191] 1.881662e+13 4.310765e+12 2.560567e+14 3.428521e+14 5.056423e+11
[4196] 3.025947e+14 4.386441e+13 7.039596e+14 7.029380e+12 3.963093e+13
[4201] 9.229823e+13 1.326884e+14 1.550693e+14 2.215298e+14 4.755578e+14
[4206] 3.353531e+13 3.298254e+14 1.337530e+14 4.291357e+12 1.075572e+14
[4211] 3.534000e+14 8.943891e+13 9.441469e+12 2.020461e+15 4.181457e+14
[4216] 2.927749e+13 3.054101e+14 1.900245e+14 1.095353e+14 2.616981e+13
[4221] 7.123209e+13 9.789697e+13 5.853540e+14 2.974516e+12 2.128285e+13
[4226] 3.217014e+13 3.802510e+13 3.796067e+13 4.624854e+12 2.379420e+14
[4231] 5.922563e+12 3.179891e+14 4.382350e+13 2.473541e+14 2.339885e+13
[4236] 1.214106e+12 2.917643e+13 6.177288e+13 2.154017e+14 3.927519e+14
[4241] 5.314829e+14 2.278147e+13 2.134308e+12 5.418531e+13 6.211364e+13
[4246] 1.169355e+12 1.277361e+13 6.519350e+13 1.748004e+14 4.895039e+12
[4251] 1.297308e+13 5.643873e+14 6.958444e+13 1.462261e+12 1.072525e+14
[4256] 1.293439e+13 7.175690e+13 6.502474e+13 6.595214e+14 1.817250e+14
[4261] 6.416268e+12 4.456614e+13 8.721590e+12 6.265041e+13 5.556292e+13
[4266] 3.461933e+13 2.308047e+13 2.276265e+14 6.093348e+13 2.166540e+13
[4271] 1.052710e+14 2.298431e+12 6.821458e+13 1.037828e+14 9.866245e+14
[4276] 1.673088e+14 9.688781e+13 2.615610e+13 5.148368e+12 8.129199e+13
[4281] 9.390196e+12 1.160919e+14 1.272425e+14 1.191495e+13 7.699074e+13
[4286] 1.434703e+12 6.758969e+13 2.402498e+13 6.342216e+13 2.629465e+12
[4291] 1.821377e+13 4.817899e+13 1.642612e+14 8.451738e+12 1.223505e+14
[4296] 4.933997e+12 5.839040e+13 3.804763e+13 1.894452e+11 4.932325e+12
[4301] 4.449253e+13 2.881867e+13 1.927205e+13 5.091379e+13 1.572682e+14
[4306] 1.573955e+14 6.058092e+12 0.000000e+00
> lm(formula ~ data$bedroom_count)

Call:
lm(formula = formula ~ data$bedroom_count)

Coefficients:
       (Intercept)  data$bedroom_count  
         6.276e+14          -2.946e+13  

> mod <- lm(formula ~ data$bedroom_count)
> X <- cbind(1,data$bedroom_count)
> betaHat <- solve(t(X) %*% X) %*% t(X) %*% formula
> var_betaHat <- anova(mod)[[3]][2] * solve(t(X) %*% X)
> mod$coef
       (Intercept) data$bedroom_count 
      6.276244e+14      -2.945699e+13 
> c(betaHat[1], betaHat[2])
[1]  6.276244e+14 -2.945699e+13
> summary(mod)$coefficients[, 2]
       (Intercept) data$bedroom_count 
      2.624523e+13       5.868340e+12 
> sqrt(diag(var_betaHat))
[1] 2.624523e+13 5.868340e+12
> 

</details>
