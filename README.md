#include <stdio.h>

int main() {
    int n;
    printf("Enter the number of highly composite numbers to find: ");
    scanf("%d", &n);
    
    if (n <= 0) {
        printf("Please enter a positive integer for the number of highly composite numbers.\n");
        return 1;
    }
    
    printf("The first %d highly composite numbers are:\n", n);
    
    int num = 1;
    
    for (int count = 0; count < n; num++) {
        int divisors = 0;
        
        for (int i = 1; i <= num; i++) {
            if (num % i == 0) {
                divisors++;
            }
        }
        
        if (divisors > count) {
            printf("%d (with %d divisors)\n", num, divisors);
            count = divisors;
        }
    }
    
    return 0;
}
