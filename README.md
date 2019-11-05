# Probleme
#include <iostream>

using namespace std;

int v[11], nr;
int F(int x)
{
    while (x)
    {
        if (v[x % 10] == 0) return 0;
        x /= 10;
    }
    return 1;
}
int main()
{
    long n, x; cin >> n; x = n;
    while (x)
    {
        v[x % 10] = 1;
        x /= 10;
    }
    for (int i = 1; i <= n; i++)
        if (n % i == 0)

            {   if (F(i))
               nr++; cout << i << " ";
            }
    cout<<endl << nr;
    return 0;
}
