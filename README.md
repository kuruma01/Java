import javax.swing.*;
import java.awt.FlowLayout;
import java.awt.Font;
import java.awt.Color;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.JTextField;

public class JHelloFrame extends JFrame implements ActionListener

{

  JLabel namePrompt = new JLabel("What is your name?");
  Font bigFont1 = new Font("Arial", Font.BOLD, 15); 

JTextField answer1 = new JTextField(10);

JLabel addressPrompt = new JLabel("Address");
Font bigFont2 = new Font("Arial", Font.BOLD, 15); 

JTextField answer2 = new JTextField(10);

  JLabel phonePrompt = new JLabel("Phone #");
Font bigFont3 = new Font("Arial", Font.BOLD, 15); 

JTextField answer3 = new JTextField(10);

JButton ok = new JButton("OK");

  JLabel greeting = new JLabel("");

  final int WIDTH = 175;

  final int HEIGHT = 225;


public JHelloFrame()

{

super("Hello Frame");

setSize(WIDTH, HEIGHT);
JLabel heading = new JLabel("Enter your Details");

heading.setFont(new Font("Algerian", Font.BOLD,16));

setLayout(new FlowLayout());

namePrompt.setFont(bigFont1);
addressPrompt.setFont(bigFont2);
  phonePrompt.setFont(bigFont3);


greeting.setFont(bigFont1);
add(heading);
add(namePrompt);
add(addressPrompt);
add(phonePrompt);
  add(answer1);
add(answer2);
add(answer3);

add(ok);

add(greeting);

setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

ok.addActionListener(this);
ok.setBackground(Color.ORANGE);
}

  public void actionPerformed(ActionEvent e)

  {

    String name = namePrompt.getText();
    String addresss = addressPrompt.getText();
    String greet = "Hello, " + answer1 + "from" + answer2 ;

    greeting.setText(greet);
    ok.setVisible(false);
    answer1.setVisible(false);
    answer2.setVisible(false);
    answer3.setVisible(false);
    namePrompt.setVisible(false);
    addressPrompt.setVisible(false);
    phonePrompt.setVisible(false);

  }
}
