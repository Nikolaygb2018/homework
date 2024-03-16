 static void RangeRecursive(int m, int n)
{
    if (m <= n)
    {
        Console.WriteLine(m);
        RangeRecursive(m + 1, n);
    }
}
RangeRecursive(2, 15);


static int Ackermann(int m, int n)
{
    if (m == 0)
    {
        return n + 1;
    }
    else if (n == 0)
    {
        return Ackermann(m - 1, 1);
    }
    else
    {
        return Ackermann(m - 1, Ackermann(m, n - 1));
    }
}
Console.WriteLine(Ackermann(3, 4));



  static void ReversePrint(int[] arr)
{
    if (arr.Length == 0)
    {
        return;
    }
    ReversePrint(arr.Skip(1).ToArray());  
    Console.WriteLine(arr[0]);  
}
int[] arr = { 1, 2, 3, 4, 5 };
ReversePrint(arr);