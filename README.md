# Prac3124
mport javax.swing.*;
import java.awt.*;

public class MarathonEventRegistrationAppGUI {
    private JFrame frame;
    private JLabel titleLabel;
    private JButton exitButton;
    private JLabel raceCodeLabel;
    private JTextField raceCodeTextField;
    private JLabel firstNameLabel;
    private JTextField firstNameTextField;
    private JLabel lastNameLabel;
    private JTextField lastNameTextField;
    private JLabel raceTypeLabel;
    private JComboBox<String> raceTypeComboBox;
    private JLabel clubLabel;
    private JRadioButton yesRadioButton;
    private JRadioButton noRadioButton;
    private JButton saveButton;
    private JButton resetButton;

    public MarathonEventRegistrationAppGUI() {
        createGUI();
    }

    private void createGUI() {
        frame = new JFrame("Marathon Event Registration App version 1.0");
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        JPanel panel = new JPanel();
        panel.setLayout(new GridBagLayout());
        GridBagConstraints constraints = new GridBagConstraints();
        constraints.insets = new Insets(5, 5, 5, 5);

        titleLabel = new JLabel("Marathon Event Registration");
        titleLabel.setFont(new Font("Arial", Font.BOLD, 16));
        constraints.gridx = 0;
        constraints.gridy = 0;
        constraints.gridwidth = 3;
        panel.add(titleLabel, constraints);

        exitButton = new JButton("X");
        exitButton.setFont(new Font("Arial", Font.BOLD, 14));
        constraints.gridx = 3;
        constraints.gridy = 0;
        constraints.gridwidth = 1;
        panel.add(exitButton, constraints);

        raceCodeLabel = new JLabel("Race Code:");
        constraints.gridx = 0;
        constraints.gridy = 1;
        constraints.gridwidth = 1;
        panel.add(raceCodeLabel, constraints);

        raceCodeTextField = new JTextField(15);
        constraints.gridx = 1;
        constraints.gridy = 1;
        constraints.gridwidth = 1;
        panel.add(raceCodeTextField, constraints);

        firstNameLabel = new JLabel("First Name:");
        constraints.gridx = 0;
        constraints.gridy = 2;
        constraints.gridwidth = 1;
        panel.add(firstNameLabel, constraints);

        firstNameTextField = new JTextField(15);
        constraints.gridx = 1;
        constraints.gridy = 2;
        constraints.gridwidth = 1;
        panel.add(firstNameTextField, constraints);

        lastNameLabel = new JLabel("Last Name:");
        constraints.gridx = 0;
        constraints.gridy = 3;
        constraints.gridwidth = 1;
        panel.add(lastNameLabel, constraints);

        lastNameTextField = new JTextField(15);
        constraints.gridx = 1;
        constraints.gridy = 3;
        constraints.gridwidth = 1;
        panel.add(lastNameTextField, constraints);

        raceTypeLabel = new JLabel("Race Type:");
        constraints.gridx = 0;
        constraints.gridy = 4;
        constraints.gridwidth = 1;
        panel.add(raceTypeLabel, constraints);

        raceTypeComboBox = new JComboBox<>();
        raceTypeComboBox.addItem("Ultra Marathon (56km)");
        raceTypeComboBox.addItem("Full Marathon (42km)");
        raceTypeComboBox.addItem("Half Marathon (21km)");
        constraints.gridx = 1;
        constraints.gridy = 4;
        constraints.gridwidth = 1;
        panel.add(raceTypeComboBox, constraints);

        clubLabel = new JLabel("Do you belong to a club?:");
        constraints.gridx = 0;
        constraints.gridy = 5;
        constraints.gridwidth = 1;
        panel.add(clubLabel, constraints);

        ButtonGroup clubButtonGroup = new ButtonGroup();
        yesRadioButton = new JRadioButton("Yes");
        noRadioButton = new JRadioButton("No");
        clubButtonGroup.add(yesRadioButton);
        clubButtonGroup.add(noRadioButton);
        JPanel radioPanel = new JPanel();
        radioPanel.add(yesRadioButton);
        radioPanel.add(noRadioButton);
        constraints.gridx = 1;
        constraints.gridy = 5;
        constraints.gridwidth = 1;
        panel.add(radioPanel, constraints);

        saveButton = new JButton("Save");
        constraints.gridx = 0;
        constraints.gridy = 6;
        constraints.gridwidth = 1;
        panel.add(saveButton, constraints);

        resetButton = new JButton("Reset");
        constraints.gridx = 1;
        constraints.gridy = 6;
        constraints.gridwidth = 1;
        panel.add(resetButton, constraints);

        frame.add(panel);
        frame.pack();
        frame.setVisible(true);
    }

    public static void main(String[] args) {
        SwingUtilities.invokeLater(() -> new MarathonEventRegistrationAppGUI());
    }
}
