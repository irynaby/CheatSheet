# Command Line API Reference 

### Elements

**$_** - возвращает последнее выполненное выражение.

![picture alt](https://developers.google.com/web/tools/chrome-devtools/console/images/recently-evaluated-expression-1.png)

**$0 — $4** - Команды $0, $1, $2, $3 и $4 содержат последние 5 проинспектированных DOM элементов через панель Elements или последние 5 JavaScript обектов выбранные в панели Profiles. $0 возвращает самый последний выделенный элемент или JavaScript объект, $1 возвращает предыдущий выделенный элемент и так далее.

![picture alt](https://developers.google.com/web/tools/chrome-devtools/console/images/element-0.png)

**$(selector, [startNode])** 
$(selector) возвращает первый DOM элемент подходящий под переданный CSS селектор. Эта функция алиас для document.querySelector().

![picture alt](https://developers.google.com/web/tools/chrome-devtools/console/images/selector-img.png)

Клик правой кнопки мыши по результату и выберите “Reveal in Elements Panel”, чтобы найти элемент в DOM или “Scroll in to View”, чтобы перейти к этому элементу на странице.

Эта функция также принимает второй параметр, startNode, элемент или узел(node) в котором нужно искать элемент. По умолчанию это параметр равен document .

![picture alt](https://cdn-images-1.medium.com/max/2400/0*MqnVxiMliS-8BwbT.png)

**$$(selector, [startNode])** - возвращает массив всех элементов подходящих под CSS селектор. Эта команда эквивалента document.querySelectorAll().

![picture alt](https://developers.google.com/web/tools/chrome-devtools/console/images/all-selector.png)

$$() так же принимает параметр startNode и работает точно так же как и предыдущая функция.

**$x(path, [startNode])**
$x(path) вернет массив DOM элементов которые соответствуют XPath выражению.

пример возвращает все теги <p> на странице:
![picture alt](https://developers.google.com/web/tools/chrome-devtools/console/images/xpath-p-example.png)

пример вернет все <p> у которых имеется дочерний элемент <a>:
![picture alt](https://developers.google.com/web/tools/chrome-devtools/console/images/xpath-p-a-example.png)
  
 ### Functions/Code
 ### Common
 
  **clear()** - очищает консоль
  **copy(object)** - копирует переданный объект как строку в буфер обмена
  
```js
copy($0);
```


  ![picture alt]()
  

