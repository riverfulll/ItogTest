1. Сначала я ввела два массива, один, в котором хранятся данные, а второй, в котором будут храниться новые данные с заданными условиями.

string[] array1 = new string[6] {"573", "Russia", "Rim", ":-)", "Morokko","cat"};
string[] array2 = new string[array1.Length];

2. Далее использую метод void, а так же применяю цикл for, в котором проеряется соответсвие длинее данного массива.

void SecondArray(string[] array1, string[] array2)
{
    int count = 0;
    for (int i = 0; i < array1.Length; i++)
    {
    if (array1[i].Length <= 3)
        {
        array2[count] = array1[i];
        count++;
        }
    }
}   
void PrintArray(string[] array)
{
    for (int i = 0; i < array.Length; i++)
    {
        Console.Write($"{array[i]} ");
    }
    Console.WriteLine();
}

Внутри цикла ставлю условие: кол-во символов <= 3? Если да, то элемент первого массива переносится в "count" элемента второго массива. После того, как мы присвоили новое значение, переменная "count" увеличивается на 1 и возвращается к циклу for, в котором "i" так же увеличивается на 1.

3. ЗАвершаю программу печатью итогового массива с элементами <=3.

SecondArray(array1, array2);
PrintArray(array2);
