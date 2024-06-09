package AOOP.extra;

import java.io.BufferedWriter;
import java.io.File;
import java.io.FileWriter;
import java.io.IOException;
import java.util.ArrayList;
import java.util.HashMap;
import java.util.HashSet;
import java.util.LinkedList;
import java.util.Map;

public class GTUPrac {
    public static void main(String[] args) {
        reverseDigits(123);
        sumOfDigits(123);
        maxOfThree(1, 2, 3);
        System.out.println("Series: ");
        fibonacci(4);
        stringMethods();
        thisDemo();
        copyConstructor();
        hierarchicalInheritance();
        wrapperClassDemo();
        overloadAreaDemo();
        carDemo();
        // threadDemo();
        createOrAppendFile();
        // collectionFWDemo();
    }
    public static void reverseDigits(int num) {
        int rev = 0;
        while (num > 0) {
            int digit = num % 10;
            rev = (rev * 10) + digit;
            num = num / 10;
        }
        System.out.println("Rev: " + rev);
    }
    public static void sumOfDigits(int num) {
        int sum = 0;
        while (num > 0) {
            int digit = num % 10;
            sum += digit;
            num = num / 10;
        }
        System.out.println("Sum: " + sum);
    }
    public static void maxOfThree(int a, int b, int c) {
        int max =  (a > b && a > c) ? a : (b > c ? b : c);
        System.out.println(max);
    }
    public static void fibonacci(int num) {
        int a = 1, b = 2;
        System.out.println(a);
        System.out.println(b);
        for (int i = 2; i < num; i++) {
            int c = a + b;
            System.out.println(c);
            a = b;
            b = c;
        }
    }
    public static void stringMethods() {
        String str = "Hello World!";
        System.out.println(str.charAt(2));
        System.out.println(str.contains("c"));
        System.out.println(String.format("Hello %s", "Kavan"));
        String[] strArr = str.split(" ");
        for (String string : strArr) {
            System.out.println(string);
        }
    }
    public static void thisDemo() {
        This obj = new This();
        obj.x = 12;
        obj.disp(10);
    }
    public static void copyConstructor() {
        Rectangle rect1 = new Rectangle(5,2);
        Rectangle rect2 = new Rectangle(rect1);
        System.out.println(rect1.area());
        System.out.println(rect2.area());
    }
    public static void hierarchicalInheritance() {
        AA objAa = new AA();
        AB objAb = new AB();
        objAa.methodA();
        objAb.methodA();
        objAb.methodAB();
    }
    private static void wrapperClassDemo() {
        Integer a = 12;
        String str = "Hello";
        System.out.println(a.intValue());
        System.out.println(Integer.parseInt("32"));
        System.out.println(String.valueOf(432));
        System.out.println(str.matches("([A-Z])\\w+"));
    }
    private static void overloadAreaDemo() {
        Shape shape = new Shape();
        shape.area(7);
        shape.area(5,2);
    }
    private static void carDemo() {
        Car[] cars = new Car[5];

        cars[0] = new Car("Porsche 911", 330); 
        cars[1] = new Car("Ferrari 488 GTB", 330); 
        cars[2] = new Car("Lamborghini Aventador", 350); 
        cars[3] = new Car("Dodge Challenger", 200);
        cars[4] = new Car("Ford Mustang", 250);

        for (Car car : cars) {
            System.out.println(car);
        }
    }
    private static void threadDemo() {
        Thread t1 = new MyThread1();
        Thread t2 = new MyThread2();
        Thread t3 = new MyThread3();
    }
    public static void createOrAppendFile() {
        String fileName = "example.txt";
        String content = "Hello, this is a test file.\nThis is the second line.";
        File file = new File(fileName);
        
        try (FileWriter fw = new FileWriter(file, true);  // 'true' enables append mode
             BufferedWriter bw = new BufferedWriter(fw)) {
            
            bw.write(content);
            System.out.println("Data has been written to the file successfully!");

        } catch (IOException e) {
            System.err.println("An error occurred while creating or writing to the file:");
            e.printStackTrace();
        }
    }
    public static void collectionFWDemo() {
        ArrayList<String> weekdays = new ArrayList<>();
        weekdays.add("Monday");
        weekdays.add("Tuesday");
        weekdays.add("Wednesday");
        weekdays.add("Thursday");
        weekdays.add("Friday");
        weekdays.add("Saturday");
        weekdays.add("Sunday");
        System.out.println("ArrayList (Weekdays):");
        for (String weekday : weekdays) {
            System.out.println(weekday);
        }

        LinkedList<String> months = new LinkedList<>();
        months.add("January");
        months.add("February");
        months.add("March");
        months.add("April");
        months.add("May");
        months.add("June");
        months.add("July");
        months.add("August");
        months.add("September");
        months.add("October");
        months.add("November");
        months.add("December");
        System.out.println("LinkedList (Months):");
        for (String month : months) {
            System.out.println(month);
        }

        
        
        HashSet<String> colors = new HashSet<>();
        colors.add("Red");
        colors.add("Green");
        colors.add("Blue");
        colors.add("Yellow");
        colors.add("Orange");
        colors.add("Purple");
        colors.add("Red"); // Duplicate not allowed

        System.out.println("Colors in the HashSet:");
        for (String color : colors) {
            System.out.println(color);
        }

        Map<Integer, String> students = new HashMap<>();
        students.put(1, "Ram");
        students.put(2, "Shyam");
        students.put(3, "Hari");
        students.put(4, "om");
        students.put(5, "Krish");
        int enroNum = 1003;
        String name = students.get(enroNum);
        if (name != null) {
            System.out.println("Student name: " + name + " Enrollment Number: " + enroNum);
        } else {
            System.out.println("Student not found.");
        }
    }
}

class This {
    int x;

    void disp(int x) {
        System.out.println("Argument x: " + x);
        System.out.println("Inner x: " + this.x);
    }
}
class Rectangle {
    int length;
    int breadth;
    
    Rectangle(int length, int breadth) {
        this.length = length;
        this.breadth = breadth;
    }

    Rectangle(Rectangle obj) {
        this.length = obj.length;
        this.breadth = obj.breadth;
    }
    int area() {
        return this.length * this.breadth;
    }
}
class A {
    void methodA() {
        System.out.println("This is method A");
    }
}
class AA extends A {
    void methodAA() {
        System.out.println("This is method AA");
    }
}
class AB extends A {
    void methodAB() {
        System.out.println("This is method AB");
    }
}
class Shape {
    float area(float radius) {
        return radius * radius * 3.14f;
    }
    float area (float length, float breadth) {
        return length * breadth;
    }
}
class Car {
    String name;
    int topSpeed;
        Car(String name, int topSpeed) {
        this.name  = name;
        this.topSpeed = topSpeed;
    }
    public String toString() {
        return "Car name: "+ name+", Top Speed:" + topSpeed;
    }
}
class MyThread1 extends Thread {
    MyThread1() {
        this.start();
    }
    @Override
    public void run() {
        for (int i = 5; i >= 1; i--) {
            System.out.println("Thread-1");
            try {
                Thread.sleep(2500);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
}
class MyThread2 extends Thread {
    MyThread2() {
        this.start();
    }
    @Override
    public void run() {
        for (int i = 5; i >= 1; i--) {
            System.out.println("Thread-2");
            try {
                Thread.sleep(5000);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
}
class MyThread3 extends Thread {
    MyThread3() {
        this.start();
    }
    @Override
    public void run() {
        for (int i = 5; i >= 1; i--) {
            System.out.println("Thread-3");
            try {
                Thread.sleep(7500);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
}
