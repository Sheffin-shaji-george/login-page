package com.code;

import sample.*;
import javax.swing.*;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class GUI4 implements  ActionListener {

    private static JLabel label;
    private static JLabel label1;
    private static JTextField box;
    private static JLabel password;
    private static JTextField box2;
    private static JButton button;
    private static JButton button2;
    private static JLabel success;
    private static JLabel reset;
    private static JLabel label2;




        public static void main(String[] args) {

        JPanel panel = new JPanel();
        JFrame frame = new JFrame();
        frame.setSize(500, 500);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setTitle("WELCOME TO SHEFFIN's WORLD OF SECRET");
        frame.add(panel);

        panel.setLayout(null);

        label = new JLabel("USER");
        label.setBounds(50, 50, 50, 50);
        panel.add(label);

        label1 = new JLabel("user : hello , password : world ");
        label1.setBounds(50,250,500,200);
        panel.add(label1);


        label2 = new JLabel( "thank you for your valid time ");
        label2.setBounds(50,300,500,200);
        panel.add(label2);

        box = new JTextField();
        box.setBounds(150,60,155,25);
        panel.add(box);


        password = new JLabel("PASSWORD");
        password.setBounds(50, 85, 80, 50);
        panel.add(password);

        box2 = new JTextField();
        box2.setBounds(150,100,155,25);
        panel.add(box2);

        button = new JButton("LOGIN");
        button.setBounds(50,150,100,30);
        button.addActionListener((ActionListener) new GUI4());
        panel.add(button);

        button2 = new JButton("RESET YOUR PASSWORD");
        button2.setBounds(50,190,200,30);
        panel.add(button2);


        success =  new JLabel();
        success.setBounds(10,200,1000,100);
        panel.add(success);

        reset = new JLabel();
        reset.setBounds(10,250,500,100);
        panel.add(reset);

        frame.setVisible(true);
    }

    @Override
    public void actionPerformed(ActionEvent e) {

        String user = box.getText();
        String password = box2.getText();
        System.out.println(user + " , " + password);

        if (user.equals("hello") && password.equals("world")) {
            success.setText("LOGIN SUCCESSFULL...  " + "\nYOUR DETAILS WILL SHORTLY SENT TO THE DOMAIN\n ");



          MyCalculator frame =  new MyCalculator();
        /*    frame.setSize(350,350);
            frame.setVisible(true);
            frame.setDefaultCloseOperation(WindowConstants.DISPOSE_ON_CLOSE);*/


            JFrame frame1 = new JFrame("MyCalculator");
            frame1.setContentPane(new MyCalculator());
            frame1.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
            frame1.setSize(500,500);
            frame1.pack();
            frame1.setVisible(true);



            } else{
            success.setText("LOGIN FAILED" + " INVALID USERNAME AND PASSWORD");
        }




    }



    }

