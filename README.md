# demo
i write test in java and practice
------------------------------------------
class book
import java.util.Scanner;
public class book {
    private int code;
    private String tittle,subject;
    private float price;
    public book(){

    }
    public book(int code,String tittle,String subject,float price){
        this.code=code;
        this.tittle=tittle;
        this.subject=subject;
        this.price=price;
    }
    public void setCode(int code) {
        this.code = code;
    }
    public void setTittle(String tittle) {
        this.tittle = tittle;
    }
    public void setSubject(String subject) {
        this.subject = subject;
    }
    public void setPrice(float price) {
        this.price = price;
    }
    public int getCode(){
        return code;
    }
    public String getTittle() {
        return tittle;
    }

    public String getSubject() {
        return subject;
    }

    public float getPrice() {
        return price;
    }
    public void input(){
        Scanner input=new Scanner(System.in);
        System.out.println("input code :");
        code=input.nextInt();
        System.out.print("input tittle:");
        tittle=input.next();
        System.out.print("input Subject:");
        subject=input.next();
        System.out.print("input price :");
        price=input.nextFloat();
    }
    public void output(){
        System.out.println("----------------------------");
        System.out.println("Code :"+code);
        System.out.println("Title:"+tittle);
        System.out.println("Subject:"+subject);
        System.out.println("Price:"+price);
    }
}
main

import java.util.Scanner;
public class Main{
    public static void main(String[] args) {
        String st;
        do {
            Scanner input = new Scanner(System.in);
            System.out.printf("Input n:");
            int n = input.nextInt();
            book[] b = new book[n];
            for (int i = 0; i < n; i++) {
                b[i] = new book();
                b[i].input();
            }
            for (int i = 0; i < n; i++) {
                b[i].output();
            }
            search(b, n);
            st=input.next();
        }while(st.equals("yes"));
    }
    public static void search(book books[],int n){
            int scode;
            int a = 0;
            Scanner input = new Scanner(System.in);
            System.out.printf("Input code to search :");
            scode = input.nextInt();
            for (int i = 0; i < n; i++) {
                if (scode == books[i].getCode()) {
                    a = 1;
                    books[i].output();
                } else if (a == 0) {
                    System.out.printf("Invalid code...");
                }
            }
        }
}
---------------------------------------------------

