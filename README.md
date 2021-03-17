# Выражения положительной и отрицательной полярности в Adwiser
Функция написана для выделения контекстов, в которых positive/negative polarity items использованы ошибочно (например, _And the diversity of internet languages can’t be overlooked **too**, there are so many interesting “dialects” like leetspeak or olbanian._, _They fear if their children may have disgustion to the process of study **at all** with the help of foreign languages._)

На вход функция принимает данные, обработанные в preprocessing.

Функция со spacy использует этот модуль для деления на клаузы. Пока что в ней есть проблемы с правильным распознаванием клауз в сложноподчинённых предложениях. 

Функция без spacy использует только частеречную разметку treetagger, принимая за начало клаузы знак пунктуации или любой союз, включая and/or и другие сочинительные союзы, поэтому если такой союз находится внутри клаузы и соединяет однородные члены, функция всё равно ошибочно делит эту клаузу на две.
