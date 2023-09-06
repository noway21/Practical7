#include <stdio.h>
#include <math.h>

int main() {
    double x1, y1, x2, y2;
    
    printf("Введіть координати початку вектора (x1 y1): ");
    scanf("%lf %lf", &x1, &y1);
    
    printf("Введіть координати кінця вектора (x2 y2): ");
    scanf("%lf %lf", &x2, &y2);
    
    double length = sqrt(pow(x2 - x1, 2) + pow(y2 - y1, 2));
    
    printf("Довжина вектора: %.6lf\n", length);
    
    return 0;
}
