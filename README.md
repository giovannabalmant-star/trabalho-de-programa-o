#include <stdio.h>

int main() {
    int opcao;
    double num1, num2, resultado;

    // Exibe o menu
    printf("===== MENU DE OPERAÇÕES =====\n");
    printf("1 - Somar\n");
    printf("2 - Subtrair\n");
    printf("3 - Multiplicar\n");
    printf("4 - Dividir\n");
    printf("Escolha uma opção: ");
    scanf("%d", &opcao);

    // Verifica se a opção é válida
    if (opcao < 1 || opcao > 4) {
        printf("Opção inválida!\n");
        return 0;
    }

    // Entrada dos números
    printf("Digite o primeiro número: ");
    scanf("%lf", &num1);
    printf("Digite o segundo número: ");
    scanf("%lf", &num2);

    // Executa a operação com base na opção
    switch (opcao) {
        case 1:
            resultado = num1 + num2;
            printf("Resultado: %.2lf + %.2lf = %.2lf\n", num1, num2, resultado);
            break;
        case 2:
            resultado = num1 - num2;
            printf("Resultado: %.2lf - %.2lf = %.2lf\n", num1, num2, resultado);
            break;
        case 3:
            resultado = num1 * num2;
            printf("Resultado: %.2lf x %.2lf = %.2lf\n", num1, num2, resultado);
            break;
        case 4:
            if (num2 == 0) {
                printf("Erro: divisão por zero não é permitida!\n");
            } else {
                resultado = num1 / num2;
                printf("Resultado: %.2lf ÷ %.2lf = %.2lf\n", num1, num2, resultado);
            }
            break;
        default:
            printf("Opção inválida!\n");
    }

    return 0;
}
