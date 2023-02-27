// Program to print longest palindromic substring of a given string

#include <stdio.h>
#include <string.h>

int copystring(char *, char *, int, int);
int checkpalindrome(char *);
int main(int argc, char const *argv[])
{
    printf("Enter the string in which you want to find longest palindromic substring in a string\n");
    char arr[24], copyarr[24];

    gets(arr);
    int N;
    N = strlen(arr);

    for (int j = N; j >= 1; j -= 1)
    {
        for (int k = 0; k < N - j + 1; k++)
        {
            copystring(copyarr, arr, N - j - k, N - k);

            if (checkpalindrome(copyarr) == 1)
            {
                printf("\nThe largest palindromic substring is %s", copyarr);

                goto end;
            }
        }
    }
end:

    return 0;
}

int copystring(char *s1, char *s2, int a, int b)
{ 
    int i = a;
    for (; i < b; i++)
    {
        s1[i - a] = s2[i];
    }

    s1[i - a] = '\0';
    return 0;
}

int checkpalindrome(char *s)
{
    for (int i = 0; i < +(strlen(s)); i++)
    {
        int N = strlen(s);
        if (s[i] != s[N - i - 1])
        {
            return 0;
        }
    }
    return 1;
}
