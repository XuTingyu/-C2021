//package treeSetDemo;
import java.util.*;
public class TreeSetDemo{
    public static void main(String[]args){
        System.out.println("4090E018 許廷宇正在學習");
        System.out.println("4090E018 Chen Yuzdhang is studying");
        var tset = new TreeSet<>();
        int[]number = {23,45,9,-6,18,93,100,76,54,66,89,34,0,-55,-27,61};
        for(int n : number)tset.add(n);
        System.out.println("物件內元素的內容:");
        System.out.println(""+tset);
        System.out.println("第一個元素內容為:"+tset.first());
        System.out.println("最後一個元素內容:"+tset.last());
        Scanner keyin = new Scanner (System.in);
        int num = 0;
        while(true){
            System.out.print("請輸入一個整數?");
            try{
                num = Integer.parseInt(keyin.nextLine());
            } catch (NumberFormatException ex){
                System.out.println("請輸入數值!");
                continue;
            }
            if (num >=(int)tset.first()&&num<=(int)tset.last())
            break;
            else
             System.out.println("範圍錯誤!");
        }
        System.out.print("元素內容大於等於"+unm+"香:");
        System.out.println(tset.tailSet(num));
        keyin.close();
    }
}
