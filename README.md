# hello-world
just another repository
import java.awt.*;  
import java.awt.event.*;  
import java.lang.*;  
import javax.swing.*; 

public class app extends Frame  
{  
  JButton b0,b1,b2,b3,b4,b5,b6,b7,b8,b9,b10,b11,b12,b13,b14,b15,b16,b17,b18,b19,
          b20,b21,b22,b23,b24,b25,b26,b27,b28,b29,b30,b31;  //按钮
  GridLayout gl1, gl2,gl3,gl4,gl5;  //按钮布局
  Panel p0,p1,p2,p3,p4,p5,p6,p7; //方框 
  JTextField tf1;    
  StringBuffer str; 
  double x, y, pi=3.14159265358979323846,e=Math.E; 
  int z; 
  static double m; 
 
  public app()  
  { 
  
     p0 = new Panel();  
     p1 = new Panel();
     p2 = new Panel();  
     p3 = new Panel();  
     p4 = new Panel();
     p5 = new Panel(); 
     p6 = new Panel(); 
     p7 = new Panel();
     str = new StringBuffer(); 
     gl1 = new GridLayout(1, 2, 5, 0);
     gl2 = new GridLayout(3, 5, 5, 5); 
     gl3 = new GridLayout(2, 5, 5, 5);
     gl4 = new GridLayout(1, 4, 5, 5);
     gl5 = new GridLayout(1, 2, 5, 5); 
     tf1 = new JTextField(29); 
     tf1.setForeground(Color.red);  
     tf1.setHorizontalAlignment(JTextField.RIGHT);  
     tf1.setEnabled(false);
     tf1.setText("0."); 
    
     setBackground(new Color(0,0,0));  
     setBounds(300, 250, 330, 500); 
     p0.add(tf1);  
     p0.setBounds(0, 50, 330,40);  
     p1.setLayout(gl1); 
     p1.setBounds(6, 90, 317, 40); 
     p2.setLayout(gl2); 
     p2.setBounds(6, 140,317, 110);
     p3.setLayout(gl3); 
     p3.setBounds(6, 260, 317, 110);
     p4.setLayout(gl4);
     p4.setBounds(6, 374, 254, 55);
     p5.setLayout(gl5);
     p5.setBounds(134,435,123,55); 
     p6.setLayout(null);
     p6.setBounds(6,435,123,55);
     p7.setLayout(null);
     p7.setBounds(262,374,58,116);
     b0 = new JButton("Backspace");
     b0.setBackground(Color.darkGray);
     b0.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b0.setForeground(Color.white);   
     b0.addActionListener(new button());  
     b1 = new JButton("C");  
     b1.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b1.setForeground(Color.red);  
     b1.addActionListener(new button());
     b2 = new JButton("("); 
     b2.setBorder(BorderFactory.createRaisedBevelBorder());  
     b2.setForeground(Color.white);  
     b2.setBackground(Color.darkGray);
     b2.addActionListener(new button()); 
     b3 = new JButton(")");
     b3.setBorder(BorderFactory.createRaisedBevelBorder());   
     b3.setBackground(Color.darkGray);
     b3.setForeground(Color.white);  
     b3.addActionListener(new button()); 
     b4 = new JButton("sin");
     b4.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b4.setForeground(Color.white);  
     b4.addActionListener(new button()); 
     b5 = new JButton("cos");
     b5.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b5.setForeground(Color.white);  
     b5.addActionListener(new button());    
     b6 = new JButton("tan");
     b6.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b6.setForeground(Color.white);  
     b6.addActionListener(new button());       
     b7 = new JButton("7");
     b7.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b7.setBackground(Color.gray);
     b7.setForeground(Color.white);  
     b7.addActionListener(new button());  
     b8 = new JButton("8");
     b8.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b8.setBackground(Color.gray);  
     b8.setForeground(Color.white);
     b8.addActionListener(new button());  
     b9 = new JButton("9");
     b9.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b9.setBackground(Color.gray);  
     b9.setForeground(Color.white);
     b9.addActionListener(new button());  
     b10 = new JButton("/"); 
     b10.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b10.setBackground(Color.darkGray);
     b10.setForeground(Color.white);
     b10.addActionListener(new button());  
     b11 = new JButton("sqrt");
     b11.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b11.setForeground(Color.white);  
     b11.addActionListener(new button());  
     b12 = new JButton("4");
     b12.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b12.setBackground(Color.gray);  
     b12.setForeground(Color.white);
     b12.addActionListener(new button());  
     b13 = new JButton("5"); 
     b13.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b13.setBackground(Color.gray); 
     b13.setForeground(Color.white);
     b13.addActionListener(new button());  
     b14 = new JButton("6");
     b14.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b14.setBackground(Color.gray);
     b14.setForeground(Color.white);  
     b14.addActionListener(new button());  
     b15 = new JButton("*"); 
     b15.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b15.setBackground(Color.darkGray);
     b15.setForeground(Color.white);
     b15.addActionListener(new button());  
     b16 = new JButton("%");
     b16.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b16.setForeground(Color.white);  
     b16.addActionListener(new button());  
     b17 = new JButton("1"); 
     b17.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b17.setBackground(Color.gray);
     b17.setForeground(Color.white); 
     b17.addActionListener(new button());  
     b18 = new JButton("2");
     b18.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b18.setBackground(Color.gray);  
     b18.setForeground(Color.white);
     b18.addActionListener(new button());  
     b19 = new JButton("3");
     b19.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b19.setBackground(Color.gray);  
     b19.setForeground(Color.white);
     b19.addActionListener(new button());  
     b20 = new JButton("-");
     b20.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b20.setBackground(Color.darkGray);
     b20.setForeground(Color.white);  
     b20.addActionListener(new button());  
     b21 = new JButton("1/X"); 
     b21.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b21.setForeground(Color.white);
     b21.addActionListener(new button());  
     b22 = new JButton("0"); 
     b22.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b22.setSize(123,55);
     b22.setBackground(Color.gray);
     b22.setForeground(Color.white);
     b22.addActionListener(new button());   
     b24 = new JButton(".");
     b24.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b24.setBackground(Color.gray);
     b24.setForeground(Color.white);  
     b24.addActionListener(new button());  
     b25 = new JButton("+");
     b25.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b25.setBackground(Color.darkGray); 
     b25.setForeground(Color.white);
     b25.addActionListener(new button());  
     b26 = new JButton("="); 
     b26.setSize(58,116); 
     b26.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b26.setForeground(Color.white);
     b26.setBackground(Color.darkGray);
     b26.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b26.addActionListener(new button()); 
     b27 = new JButton("π");
     b27.setBorder(BorderFactory.createRaisedBevelBorder());   
     b27.setForeground(Color.white);
     b27.addActionListener(new button());  
     b28 = new JButton("!"); 
     b28.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b28.setForeground(Color.white);
     b28.addActionListener(new button());  
     b29 = new JButton("ln"); 
     b29.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b29.setForeground(Color.white);
     b29.addActionListener(new button());  
     b30 = new JButton("logx^y"); 
     b30.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b30.setForeground(Color.white);
     b30.addActionListener(new button());  
     b31 = new JButton("e"); 
     b31.setBorder(BorderFactory.createRaisedBevelBorder()); 
     b31.setForeground(Color.white);
     b31.addActionListener(new button());  
     p1.add(b1);  
     p1.add(b0);
     p2.add(b4);
     p2.add(b5);
     p2.add(b6);
     p2.add(b27);
     p2.add(b28);
     p2.add(b29);
     p2.add(b30);
     p2.add(b31);
     p2.add(b11);
     p2.add(b16);
     p2.add(b21);    
     p3.add(b7);  
     p3.add(b8);  
     p3.add(b9); 
     p3.add(b10); 
     p3.add(b2); 
     p3.add(b12);     
     p3.add(b13);  
     p3.add(b14);  
     p3.add(b15);  
     p3.add(b3);   
     p4.add(b17);  
     p4.add(b18);  
     p4.add(b19);  
     p4.add(b20);      
     p5.add(b24);  
     p5.add(b25);  
     p6.add(b22);
     p7.add(b26);
     setLayout(null);  
     add(p0);  
     add(p1); 
     add(p2);   
     add(p3); 
     add(p4);
     add(p5); 
     add(p6);
     add(p7);
     setResizable(false); 
     addWindowListener(new WindowAdapter() {  
        public void windowClosing(WindowEvent e1) {  
           System.exit(0);  
      }  
     });  
     setVisible(true);  
   } 
 
  class button implements ActionListener {  
     public void actionPerformed(ActionEvent e2)  {  
        try{  
           if(e2.getSource()==b1) {  
               tf1.setText("0"); 
               str.setLength(0);  
           }    
           else if(e2.getSource()==b25) {  
               x=Double.parseDouble(tf1.getText().trim()); //在获得的文本中除去空格,并转化为double 
               str.setLength(0);  
               y=0d;  
               z=0;
               System.out.print("+");     
           }  
           else if(e2.getSource()==b20) {  
               x=Double.parseDouble(tf1.getText().trim());  
               str.setLength(0);  
               y=0d;  
               z=1;  
               System.out.print("-");   
           } 
           else if(e2.getSource()==b15) {  
               x=Double.parseDouble(tf1.getText().trim());  
               str.setLength(0);  
               y=0d;  
               z=2;  
               System.out.print("*");   
           }  
           else if(e2.getSource()==b10) {  
               x=Double.parseDouble(tf1.getText().trim());  
               str.setLength(0);  
               y=0d;  
               z=3;
               System.out.print("/");     
           }  
           else if(e2.getSource()==b26) {  
               str.setLength(0);
               System.out.print("=");  
               switch(z)  {  
                  case 0 : tf1.setText(""+(x+y));   System.out.print(""+(x+y));  break;  
                  case 1 : tf1.setText(""+(x-y));   System.out.print(""+(x-y));  break;  
                  case 2 : tf1.setText(""+(x*y));   System.out.print(""+(x*y));  break;  
                  case 3 : tf1.setText(""+(x/y));   System.out.print(""+(x/y));  break; 
                  case 4 : tf1.setText(""+Math.log(y)/Math.log((double)x)); break;
                  case 5 : tf1.setText(""+Math.log(y)/Math.log(e)); break;
               }  
               System.out.println();   
           }    
           else if(e2.getSource()==b24) {  
               if(tf1.getText().trim().indexOf('.')!=-1) { 
 
               }  
               else {  
                  if(tf1.getText().trim().equals("0"))  {  
                     str.setLength(0);  
                     tf1.setText((str.append("0"+e2.getActionCommand())).toString());  
                  }  
                  else if(tf1.getText().trim().equals("")) {  
                  }  
                  else  {  
                     tf1.setText(str.append(e2.getActionCommand()).toString());  
                  }  
                  } 
 
               y=0d;
               System.out.print("."); 
 
           } 
           else if(e2.getSource()==b4) {
           	   x=Double.parseDouble(tf1.getText().trim());
           	   tf1.setText(""+Math.sin(x));
           	   str.setLength(0);
           	   y=0d;
           }
           else if(e2.getSource()==b5) {
           	   x=Double.parseDouble(tf1.getText().trim());
           	   tf1.setText(""+Math.cos(x));
           	   str.setLength(0);
           	   y=0d;
           }
           else if(e2.getSource()==b6) {
           	   x=Double.parseDouble(tf1.getText().trim());
               if(x%(pi/2)==0)
                  tf1.setText("x不能取π/2的倍数");
           	   tf1.setText(""+Math.tan(x));
           	   str.setLength(0);
           	   y=0d;
           }
           else if(e2.getSource()==b30){
           	   x=Double.parseDouble(tf1.getText().trim());
           	   tf1.setText("log"+x+"^");
           	   str.setLength(0);
           	   y=0d;
           	   z=4;
           }
           else if(e2.getSource()==b31){
           	   x=Double.parseDouble(tf1.getText().trim());
           	   tf1.setText("ln"+x+"^");
           	   str.setLength(0);
           	   y=0d;
           	   z=5;
           }
           else if(e2.getSource()==b11) {  
               x=Double.parseDouble(tf1.getText().trim());  
               tf1.setText("数字格式异常");  
               if(x<0)  
                  tf1.setText("负数没有平方根");  
               else  
                  tf1.setText(""+Math.sqrt(x));  
                  str.setLength(0);  
                  y=0d;  
                  System.out.print("sqrt");
           }  
           else if(e2.getSource()==b16)  {  
               x=Double.parseDouble(tf1.getText().trim());  
               tf1.setText(""+(0.01*x));  
               str.setLength(0);  
               y=0d; 
               System.out.print("%"); 
           }  
           else if(e2.getSource()==b21) {  
               x=Double.parseDouble(tf1.getText().trim());  
               if(x==0)  { 
                  tf1.setText("除数不能为零");  
               }  
               else  {  
               tf1.setText(""+(1/x));
               System.out.print("1/x");  
               }  
               str.setLength(0);  
               y=0d; 
           }   
           else {  
               if(e2.getSource()==b22) {  
                  if(tf1.getText().trim().equals("0")) { 
 
                  }  
               else  {  
                  tf1.setText(str.append(e2.getActionCommand()).toString());  
                  y=Double.parseDouble(tf1.getText().trim());  
               }  
           }  
           else if(e2.getSource()==b0) {  
               if(!tf1.getText().trim().equals("0")) {  
                  if(str.length()!=1)  {  
                      tf1.setText(str.delete(str.length()-1,str.length()).toString());// 可能抛出字符串越界异常  
                  }  
                  else  {  
                      tf1.setText("0");  
                      y=Double.parseDouble(tf1.getText().trim()); 
                  }  
                }  
               y=Double.parseDouble(tf1.getText().trim());  
           }  
           else if(e2.getSource()==b27){ 
           	   tf1.setText(str.append(e2.getActionCommand()).toString()); 
               x=pi; 
               System.out.print(pi);
           }
           else if(e2.getSource()==b31){
           	   tf1.setText("e");  
           }
           else { 
               tf1.setText(str.append(e2.getActionCommand()).toString());  
               y=Double.parseDouble(tf1.getText().trim()); 
               System.out.print(y);   
               if(z==4){
                  tf1.setText("log"+x+"^"+y);
                  z=4;
               }
               if(z==5){
                  tf1.setText("ln"+x+"^"+y);
                  z=5;
               }
           }
       }    
   }  
   catch(NumberFormatException e){  
      tf1.setText("数字格式异常");  
   }  
   catch(StringIndexOutOfBoundsException e){  
      tf1.setText("字符串索引越界");  
   }  
} 
} 
 
   public static void main(String args[]) {  
      new app();  
   } 
 
} 
