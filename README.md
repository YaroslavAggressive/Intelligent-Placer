# Intelligent-Placer

## Постановка задачи

На вход подается фотография, на которой расположены многоугольник, нарисованный на листе белой бумаги, и некоторое количество
различных предметов, расположенных на фоне светлой горизонтальной поверхности.
 Необходимо определить, можно ли расположить одновременно все предметы с фотографии на плоскости так, чтобы они влезли в 
этот многоугольник.
 Предметы и горизонтальная поверхность, которые могут оказаться на фотографии, заранее известны. Также заранее известно 
направление вертикальной оси Z у этих предметов. Многоугольник задается фигурой, нарисованной темным маркером 
на белом листе бумаги и сфотографированной вместе с предметами.

“Intelligent Placer” должен быть оформлен в виде python-библиотеки `intelligent_placer_lib`, которая поставляется
каталогом `intelligent_placer_lib` с файлом `intelligent_placer.py`, содержащим функцию - точку входа со следующей сигнатурой:

```Python
def check_image(<path_to_png_jpg_image_on_local_computer>, [<poligon_coordinates>])
```

Функция возвращает значение `True`, если предметы поместятся в многоугольник, иначе она возвращается `False`. 
Также требуется воспроизводимый файл `intelligent_placer.ipynb`, содержащий репрезентативные примеры работы алгоритма
с оценками качества его работы и их визуализацией.

## Ограничения на входные данные

* Входные картинки должны иметь пиксельные масштабы, не превышающие разрешения HD 720p (1280x720
  пикселей).
* Формат входных картинок - jpg и png.
* Съемка производится на высоте примерно 40 (+-2) см от поверхности с предметами.
* Допустимый угол оклонения камеры относительно нормали к фотографируемой поверхности - +- 3 градуса.
* Многоугольник должен быть выпуклым и содержать не более 8 вершин.
* Толщина маркера для изобращения многоугольника находится в пределах 5-7 пикселей.
* Предметы на фотографии могут пересекаться друг с другом, но не пересекают лист бумаги с изображением многоугольника.
* Предметы не могут выходить за границы фотографии (иначе будет учитываться лишь часть предмета, попавшая в кадр).
* Высота предметов не превышает 3 см.
* Предметы отличаются по оттенку.
* На поверхности должны отсутствовать черно-серые области.

## Предварительный набор предметов, выбранных для тестирования

* Синий маркер
* ![alt text](https://github.com/YaroslavAggressive/Intelligent-Placer/blob/develop/Test%20Kit/pen.jpg)
* Паспорт в обложке
* ![alt text](https://github.com/YaroslavAggressive/Intelligent-Placer/blob/develop/Test%20Kit/pasport.jpg)
* Кошелек
* ![alt text](https://github.com/YaroslavAggressive/Intelligent-Placer/blob/develop/Test%20Kit/wallet.jpg)
* Эспандер
* ![alt text](https://github.com/YaroslavAggressive/Intelligent-Placer/blob/develop/Test%20Kit/expander.jpg)
* Йо-йо синий
* ![alt text](https://github.com/YaroslavAggressive/Intelligent-Placer/blob/develop/Test%20Kit/yo-yo.jpg)
* Тюбик с йодом
* ![alt text](https://github.com/YaroslavAggressive/Intelligent-Placer/blob/develop/Test%20Kit/iodine.jpg)
* Пластиковая карта бирюзового цвета
* ![alt text](https://github.com/YaroslavAggressive/Intelligent-Placer/blob/develop/Test%20Kit/card.jpg)
* Складной нож
* ![alt text](https://github.com/YaroslavAggressive/Intelligent-Placer/blob/develop/Test%20Kit/knife.jpg)
* PowerBank Xiaomi
* ![alt text](https://github.com/YaroslavAggressive/Intelligent-Placer/blob/develop/Test%20Kit/powerbank.jpg)
* Зубная щетка в чехле
* ![alt text](https://github.com/YaroslavAggressive/Intelligent-Placer/blob/develop/Test%20Kit/case.jpg)
