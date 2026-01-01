# strong-number-checker
Store original number. Extract digits using %10 inside a loop. For each digit, calculate factorial using another loop. Add factorials of all digits and compare sum with original number.


#include <stdio.h>
int main() {
    int num, originalNum, digit;
    int sum = 0;

    printf("Enter a number: ");
    scanf("%d", &num);

    originalNum = num;

    while (num > 0) {
        digit = num % 10;

        int fact = 1;
        for (int i = 1; i <= digit; i++) {
            fact = fact * i;
        }

        sum = sum + fact;
        num = num / 10;
    }

    if (sum == originalNum)
        printf("Strong");
    else
        printf("Not");

    return 0;
}

