#include <stdio.h>

int main(void)
{
    int grade;

    printf("\nEnter a numerical grade: ");
    scanf("%d", &grade);

    if (grade < 0 || grade > 100) {
        printf("Numerical grade must be from 0 to 100\n\n");
        return 0;
    }

    grade = grade - (grade % 10);  

    printf("Letter grade: ");

    switch (grade) {
        case 100: case 90: 
                  printf("A");
                  break;
        case 80:  printf("B");
                  break;
        case 70:  printf("C");
                  break;
        case 60:  printf("D");
                  break;
        case 50: 
        case 40: 
        case 30:
        case 20: 
        case 10: 
        case 0:   printf("F");  /* Numerical grades 0 - 59 Fail */
                  break;
    }
   
    printf("\n\n");

    return 0;
} 
