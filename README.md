# console-tictactoe
Создается двумерный массив board размером 3x3, который представляет игровое поле, и переменная currentPlayer, которая хранит текущего игрока (начинает игрок 'X').

Функция Main является точкой входа в программу. Она вызывает функцию InitializeBoard для инициализации игрового поля и начинает бесконечный цикл игры.

Внутри цикла игры вызывается функция DrawBoard, которая очищает консоль и выводит текущее состояние игрового поля.

Затем игроку текущего хода выводится приглашение ввести свой ход, указав координаты клетки в формате "строка столбец" (например, "0 2" для третьей клетки в первом ряду).

Введенный ход проверяется на корректность с помощью функции MakeMove. Если ход некорректен (например, клетка уже занята или введены некорректные координаты), игроку выводится сообщение об ошибке и предлагается ввести ход заново.

Если ход корректен, символ текущего игрока ('X' или 'O') помещается в соответствующую клетку на игровом поле.

После каждого хода проверяется условие победы с помощью функции CheckForWin. Она проверяет все возможные комбинации символов на игровом поле (строки, столбцы и диагонали) и возвращает true, если одна из комбинаций совпадает (то есть, один игрок выиграл), иначе возвращает false.

Если условие победы выполняется, игровое поле выводится на экран, и выводится сообщение о победе текущего игрока. Затем игра завершается.

Если условие победы не выполняется, проверяется условие ничьи с помощью функции CheckForDraw. Она проверяет, заполнены ли все клетки на игровом поле, и возвращает true, если все клетки заполнены (ничья), иначе возвращает false.

Если условие ничьи выполняется, игровое поле выводится на экран, и выводится сообщение о ничьей. Затем игра завершается.

Если ни условие победы, ни условие ничьи не выполняются, ход передается следующему игроку путем изменения значения переменной currentPlayer.

Цикл игры продолжается до тех пор, пока не будет выполнено условие победы или ничьи. При вводе команды "exit" игра завершается.

Код также содержит несколько вспомогательных функций:

InitializeBoard инициализирует игровое поле, заполняя его пробелами.
DrawBoard выводит текущее состояние игрового поля на экран.
MakeMove проверяет введенный ход на корректность и, если ход корректен, помещает символ текущего игрока в указанную клетку на игровом поле.
CheckForWin проверяет игровое поле на наличие выигрышной комбинации символов.
CheckForDraw проверяет игровое поле на ничью, то есть заполненность всех клеток без победы одного из игроков.
