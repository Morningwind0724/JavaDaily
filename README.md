# JavaDaily
Day1 输出输入的内容
import java.util.Scanner;

public class Myjava {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int i = in.nextInt();
        System.out.println(i);
    }
}

-----------------------------------------------

day 2 制作简单计算器
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

-----------------------------------------------

day3BMI计算器的交互
import java.util.Scanner;

public class daywork {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("请输入你的名字：");
        String name = sc.nextLine();
        System.out.print("请输入你的身高(m): ");
        double height = sc.nextDouble();
        System.out.print("请输入你的体重(kg): ");
        double weight = sc.nextDouble();

        // 任务1: 计算BMI值（公式：体重 / (身高*身高)）
        double bmi = weight / (height * height);
        System.out.println("名字：" + name);
        System.out.printf("你的BMI值: %.2f\n", +bmi);

        // 任务2: 用if-else判断健康状态
        // BMI < 18.5: 偏瘦
        // 18.5 ≤ BMI < 24: 正常
        // BMI ≥ 24: 偏胖
        if (bmi < 18.5) {
            System.out.println("健康状态：偏瘦");
        } else if (bmi >= 18.5 && bmi <= 24) {
            System.out.println("健康状态：正常");
        } else { 
            System.out.println("健康状态：偏胖");
        }

        String healthStatus;              //判断健康状态，并配合switch case语句
        if (bmi < 18.5) {
            healthStatus = "偏瘦";        //String healthStatus = (bmi < 18.5) ? "偏瘦" : (bmi < 24) ? "正常" : "偏胖";
        }
        else if (bmi >= 18.5 && bmi <= 24) {
            healthStatus = "正常";
        }
        else  {
            healthStatus = "偏胖";
        }

        // 3. 用switch-case给出健康建议
        switch (healthStatus) {
            case "偏瘦":
                System.out.println("健康建议：建议适当增加营养摄入，多吃高蛋白食物。");
                break;
            case "正常":
                System.out.println("健康建议：继续保持健康的生活方式！");
                break;
            case "偏胖":
                System.out.println("健康建议：建议控制饮食，增加运动量。");
                break;
            default:
                System.out.println("健康建议：未知状态，请咨询医生。");
        }
    }
}



