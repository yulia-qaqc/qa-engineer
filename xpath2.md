XPath
Поиск по конкретному значению атрибута
//tag[@attribute='value'][2] второй элемент
//tag[@attribute='value'][last()] последний элемент

Поиск по нескольким значениям атрибута
//tag[@attribute1='value1'][@attribute2='value2']
//tag[@attribute1='value1' and @attribute2='value2']

Поиск по тексту
//tag[text()='example']

Поиск по значению атрибута по всем тэгам
//*[@attribute='value']

Метод Contains
//tag[contains(@attribute,'value')]
//tag[contains(text(),'example')]

Not contains
//tag[not(contains(text(),'example'))]

Поиск по вложенности
/ дочерние элементы на один уровень ниже
// дочерние элементы на всех уровнях вложенности
//tag[@attribute='value']//tag2[@attribute2='value2']

/.. родительские элементы на один уровень выше
//tag[@attribute='value']/..

Ancestor- поиск по всем родительским уровням
//tag[@attribute='value']/ancestor::div

Ancestor- поиск по первому родительскому уровню
//tag[@attribute='value']/parent::div
