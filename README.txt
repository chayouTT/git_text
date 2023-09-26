import java.util.Scanner;

public class Homework2 {
    public static void main(String[] args) {
        System.out.println("-====================\n欢迎使用密码加密系统\n====================\n请选择操作：\n1：加密\n2：解密\n3：退出");
        System.out.println("请输入选择序号：");
        Scanner input1 = new Scanner(System.in);
        int a = input1.nextInt();

        if (a == 1) {
            System.out.println("请输入要加密的数字密码：");

            Scanner input2 = new Scanner(System.in);
            int b = input2.nextInt();
            int num01 = (b / 1000 + 5) % 10;
            int num02 = (b % 1000 /100 + 5) % 10;
            int num03 = (b % 1000 /10 + 5) % 10;
            int num04 = (b % 10 + 5) % 10;

            int result1 = num04 * 1000 + num03 * 100 + num01 * 10 + num02;

            System.out.println("加密后的数字密码为：" + result1);

        } else if (a == 2) {
            System.out.println("请输入要解密的数字密码：");

            Scanner input3 = new Scanner(System.in);
            int c = input3.nextInt();
            int num05 = (c % 10 + 10 - 5) % 10;
            int num06 = (c / 10 % 10 + 10 - 5) % 10;
            int num07 = (c / 100 % 10 + 10 - 5) % 10;
            int num08 = (c / 1000 + 10 - 5) % 10;

            int result2 = num06 * 1000 + num05 * 100 + num07 * 10 + num08;

            System.out.println("解密后的数字密码为：" + result2);

        }
    }

}
