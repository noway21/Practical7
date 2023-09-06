#include <stdio.h>
#include <math.h>

int main() {
    double x1, y1, r1, x2, y2, r2;

    printf("Введіть координати центра першого кола (x1 y1): ");
    scanf("%lf %lf", &x1, &y1);
    printf("Введіть радіус першого кола (r1): ");
    scanf("%lf", &r1);

    printf("Введіть координати центра другого кола (x2 y2): ");
    scanf("%lf %lf", &x2, &y2);
    printf("Введіть радіус другого кола (r2): ");
    scanf("%lf", &r2);

    double distance = sqrt(pow(x2 - x1, 2) + pow(y2 - y1, 2));

    int intersectionPoints;

    if (distance == 0 && r1 == r2) {
        intersectionPoints = -1;
    } else if (distance < r1 + r2 && distance > fabs(r1 - r2)) {
        intersectionPoints = 2;
    } else if (distance == r1 + r2 || distance == fabs(r1 - r2)) {
        intersectionPoints = 1;
    } else {
        intersectionPoints = 0;
    }
   
    if (intersectionPoints == -1) {
        printf("Кола мають безкінечно багато точок перетину.\n");
    } else {
        printf("Кількість точок перетину кол: %d\n", intersectionPoints);
    }

    return 0;
}

