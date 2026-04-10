# Calculator

#include <stdio.h>
#include <string.h>

int main(){
    int a, b, h;
    char s;
    do {
        do {
        printf("===============================\n   Calculadora Simples\n===============================\nSelecione uma operação:\n1. Adição\n2. Subtração\n3. Multiplicação\n4. Divisão\n5. Sair\nOpção: ");
        scanf("%d", &h);
        switch (h){
            case 1:
                printf("Digite o primeiro número: ");
                scanf("%d", &a);
                printf("Digite o segundo número: ");
                scanf("%d", &b);
                printf("\nResultado: %d + %d = %d\n", a, b, a+b);
                break;
            case 2:
                printf("Digite o primeiro número: ");
                scanf("%d", &a);
                printf("Digite o segundo número: ");
                scanf("%d", &b);
                printf("\nResultado: %d - %d = %d\n", a, b, a-b);
                break;
            case 3:
                printf("Digite o primeiro número: ");
                scanf("%d", &a);
                printf("Digite o segundo número: ");
                scanf("%d", &b);
                printf("\nResultado: %d * %d = %d\n", a, b, a*b);
                break;
            case 4:
                printf("Digite o primeiro número: ");
                scanf("%d", &a);
                printf("Digite o segundo número: ");
                scanf("%d", &b);
                if (b == 0){
                    printf("Erro: Divisão por zero não é permitida.\n");
                } 
                else {
                printf("\nResultado: %d / %d = %d\n", a, b, a/b);
                }
                break;
            case 5:
                printf("Obrigado por usar a calculadora! Até a próxima.");
                s = 'n';
                break;
            default:
                printf("\nOperação inválida. Por favor, digite uma operação correspondente.\n\n");
        }
        if (h != 5){
            printf("Deseja realizar outra operação? (s/n): ");
            getchar();
            scanf("%c", &s);  
        } 
    } while ((s == 's' || s == 'S'));
    if (s != 'n' && s != 'N' && h != 5){
        printf("Resposta inválida. Por favor, digite 's' para sim ou 'n' para não.\n");
        if (s != 'n' && s != 'N'){
            printf("Deseja realizar outra operação? (s/n): ");
            getchar();
            scanf("%c", &s);
        }
    } } while ( s == 's' || s == 'S' );

    if (h != 5){
        printf("Obrigado por usar a calculadora! Até a próxima.\n");
    }
}
