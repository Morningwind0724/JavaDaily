# JavaDaily
import java.util.Scanner;

public class Myjava {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int i = in.nextInt();
        System.out.println(i);
    }
}
Day1

import java.util.Scanner;

public class daywork {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);                 //new Scanner(System.in) 创建Scanner类的构造函数创建一个新的Scanner对象
                                                                  // System.in 表示标准输入流（通常是键盘输入）
                                                                  //Scanner scanner 声明了一个名为scanner的变量，其类型是Scanner类
                                                                  //= 将新创建的Scanner对象赋值给变量scanner
        System.out.println("===== 简单计算器 =====");
        System.out.println("1. 加法");
        System.out.println("2. 减法");
        System.out.println("3. 乘法");
        System.out.println("4. 除法");
        System.out.println("5. 求模");
        System.out.print("请选择操作(1-5): ");

        int choice = scanner.nextInt();                         // 读取用户输入的整数
        System.out.print("输入第一个数字: ");
        double num1 = scanner.nextDouble();
        System.out.print("输入第二个数字: ");
        double num2 = scanner.nextDouble();

        if (choice == 1) {
            result = num1 + num2;
            System.out.println("结果: " + result);
        } else if (choice == 2) {
            result = num1 - num2;
            System.out.println("结果: " + result);
        } else if (choice == 3) {
            result = num1 * num2;
            System.out.println("结果: " + result);
        } else if (choice == 4) {                        //先判断if｛｝在else｛｝
            if (num2 != 0) {                             //除数不能为0，先判断除数是否为0.不为0则运行输出结果，else为0.则不输出
                result = num1 / num2;
                System.out.println("结果: " + result);
            } else {
                System.out.println("错误：除数不能为0！");}
        } else if (choice == 5) {
                result = num1 % num2;
                System.out.println("结果: " + result);
            } else {
            System.out.println("无效选择！");
        }

        scanner.close();
    }
}
day 2

