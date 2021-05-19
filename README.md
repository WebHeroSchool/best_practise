# РАБОЧИЙ МЕТОД  

# СОТРУДНИКА ПОДРАЗДЕЛЕНИЯ 

# ТОВАРООБОРОТА .
1. [Придерживайтесь строгого стиля кодирования](#Придерживайтесь-строгого-стиля-кодирования)
2. [Строго «используйте строгое»](#Строго-используйте-строгое)
3. [Используйте линтинг](#Используйте-линтинг)
4. [Прочтите руководства по стилю кода](#Прочтите-руководства-по-стилю-кода)
5. [Избегайте глобальных переменных](#Избегайте-глобальных-переменных)
6. [Установите приоритет доступа к локальным переменным](#Установите-приоритет-доступа-к-локальным-переменным)
7. [Объявления сверху](#Объявления-сверху)
8. [Инициализировать переменные](#Инициализировать-переменные)
9. [Сделайте это понятным](#Сделайте-это-понятным)
10. [Используйте строгое сравнение](#Используйте-строгое-сравнение)









# Придерживайтесь строгого стиля кодирования
Браузеры очень снисходительны к синтаксису JavaScript.<br />
Но это не повод писать плохой код. Даже если браузеры могут это переварить.<br />
Небрежный стиль кодирования вернется к вам, когда вы перейдете в другую среду.<br />
Это если коллеги не отомстят вам за то, что вы сначала страдали.

# Строго «используйте строгое»
Строгий режим вносит множество изменений в работу JavaScript, от очевидных до тонких (за которые вы будете очень благодарны).
При использовании "_строгого использования_" тихие ошибки теперь будут вызывать ошибки. Теперь будут устранены ошибки, затрудняющие 
оптимизацию движка Javascript. Ваш код может даже работать быстрее.
В ES5 строгий режим не является обязательным, но в ES6 он необходим для многих функций ES6.
Вы можете прочитать ссылку Mozilla на строгий режим для получения дополнительной информации.
# Используйте линтинг
Инструмент линтинга для JavaScript - JSLint . Он предоставит вам подробный отчет 
о синтаксических предупреждениях и их значении. 
Вы также можете использовать JSHint , инструмент статического анализа кода.

# Прочтите руководства по стилю кода
Наиболее часто используемым и рекомендуемым руководством по стилю кода для JavaScript является Руководство по стилю кода Google для 
JavaScript . Вы также можете прочитать Idiomatic.js .
# Избегайте глобальных переменных
Сведите к минимуму использование глобальных переменных. Глобальные переменные - ужасно плохая идея.
Проблема с глобальными переменными и функциями заключается в том, что они могут быть перезаписаны другими скриптами.
Вы можете обернуть все это анонимной функцией. Или используйте литерал объекта.
# Установите приоритет доступа к локальным переменным
JavaScript сначала выполняет поиск, чтобы увидеть, существует ли переменная локально, а затем постепенно выполняет поиск на более 
высоких уровнях области видимости до глобальных переменных. Следовательно, локальные переменные будут найдены быстрее.
Чтобы определить текущую область видимости, перед каждой переменной ставьте let или const . Это предотвратит поиск, а также ускорит код.
# Объявления сверху
Поместите все объявления поверх сценария или функции, чтобы получить более чистый код. Вы не хотите, чтобы объявления были по всему коду. 
И вы хотите уменьшить возможность повторных заявлений.
# Инициализировать переменные
Лучше всего также инициализировать переменные при их объявлении. Объявите и инициируйте с самого начала.
```
let what = "javascript"; 
let one;      // эта переменная неявно инициализируется значением "undefined", лучше всего установить для нее значение
let two = 2;  // эта переменная явно инициализируется числовым значением 2

```
# Сделайте это понятным
```
let i1, pio, rialtv; 
let   newOrderIfItemIsOnStockAndCustomerFromAustralia;
```
`*i1, pio, rialt v*` - неправильные имена переменных. 
Также `*newOrderIfItemIsOnStockAndCustomerFromAustralia*` не совсем читабельный. 
Представьте себе чтение кода с этими переменными. Вы хотите, чтобы ваш код был понятным, используя короткие и содержательные имена. 
Имя переменной должно иметь смысл.
Представьте себя художником, писателем. Вы хотите, чтобы за вашей историей было легко следить.

# Используйте строгое сравнение

При использовании `==` ваши переменные будут преобразованы в типы соответствия.
```
0 == "" ; // истина 
0 === "" ; // ложный
0 == «»; Это даст истину.
```

Где `0 === «»; произведет ложь.`<br />
Это потому, `===` что оператор вызывает сравнение значений и типов.
