import java.awt.*;
import javax.swing.*;
import java.awt.event.*;
//import java.sql.*;

public class listDatabase implements ActionListener{
	JFrame frame1;
	
	JLabel label1;
	JLabel label2;
	JLabel label3;
	
	JList list1;
	JList list2;
	
	JButton button_add;
	JButton button_clear;
	JButton button_submit;
	
	JTextField textField;
	JTextField textField_1;
	
	
	
	listDatabase(){
		
		frame1=new JFrame("Database");
		
		
		
		
		label1=new JLabel("List Database");
		label1.setBounds(150,20,200,30);
		
		
		label2= new JLabel("Item");
		label2.setBounds(50,80,100,30);
		
		
		label3= new JLabel("Quantity");
		label3.setBounds(225,80,90,30);
		
		
		textField= new JTextField();
		textField.setBounds(50,110,100,30);
	
		textField.setVisible(true);
		
		textField_1= new JTextField();
		textField_1.setBounds(225,110,90,30);
		
		list1= new JList();
		list1.setBounds(50,175,100,100);
		
		list2= new JList();
		list2.setBounds(225,175,90,100);
		
		button_add= new JButton("ADD");
		button_add.setBounds(320,110,80,20);
//		button_add.addKeyListener(new KeyAdapter()
//		{
//			public void keyPressed(KeyEvent e) 
//			{
//				if(e.getSource()==button_add) {
//					//lis.add(null,textField.getText());
//					textField_1.setText(textField.getText());
//					
//				}
//			}
//		});
		button_clear= new JButton("CLEAR");
		button_clear.setBounds(220,300,80,20);
		
		button_submit= new JButton("SUBMIT");
		button_submit.setBounds(50,300,80,20);
		
		
		frame1.setBackground(Color.blue);
		frame1.setLayout(null);
		frame1.setSize(450,450);
		frame1.setVisible(true);
		
		frame1.add(label1);
		frame1.add(label2);
		frame1.add(label3);
		frame1.add(textField);
		frame1.add(textField_1);
		frame1.add(list1);
		frame1.add(list2);
		frame1.add(button_add);
		frame1.add(button_clear);
		frame1.add(button_submit);
		
		
		
	}
	public static void main(String[] args) {
		new listDatabase();
	}
	public void actionPerformed(ActionEvent e) {
		if(e.getSource()==button_add) {
			if(textField.getText().equals("")) {
				JOptionPane.showMessageDialog(frame1, "");
				textField.requestFocus();
			}
			else {
				textField_1.setText(textField.getText());
			}
		}
	}
}
