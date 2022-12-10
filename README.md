# Programacao-de-Solucoes-Computacionais-Ex13-Lista05
Desenha moldura
import java.util.Scanner;

public class Ex13 {
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);
        System.out.println("Informe o número de linhas que deseja que tenha o retângulo (entre 1 e 20): ");
        int linha = sc.nextInt();
        System.out.println("Informe o número de colunas que deeja que tenha o retângulo (entre 1 e 20): ");
        int colunas = sc.nextInt();
        if (linha > 20) {
            linha = 20;
        } else if (linha < 1) {
            linha = 1;
        }
        if (colunas > 20) {
            colunas = 20;
        } else if (colunas < 1) {
            colunas = 1;
        }
        desenhaRetangulo(linha, colunas);
        sc.close();
    }

    public static void desenhaRetangulo(int linha, int coluna) {

        System.out.print("+");
        for (int i = 0; i < linha; i++) {
            System.out.print("-");
        }
        System.out.println("+");

        for (int i = 0; i < coluna; i++) {
            System.out.print("|");
            for (int j = 0; j < linha; j++) {
                System.out.print(" ");
            }
            System.out.println("|");

        }
        System.out.print("+");
        for (int i = 0; i < linha; i++) {
            System.out.print("-");
        }
        System.out.println("+");
    }
}
