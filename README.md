# Pointers-in-C-
#include <stdio.h>

void update(int *a,int *b) {
    int temp=*a;
    *a=*a+*b;
    if(b<a){
        *b=temp-*b;
    }
    else if(b>a){
        *b=*b-temp;
    }
}

int main() {
    int a, b;
    int *pa = &a, *pb = &b;
    
    scanf("%d %d", &a, &b);
    update(pa, pb);
    printf("%d\n%d", a, b);

    return 0;
}
