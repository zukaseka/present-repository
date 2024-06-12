package breakout;

import javax.swing.JFrame;

public class Game extends JFrame {

    public Game() {
        initUI();
    }

    private void initUI() {
        add(new Board());
        setTitle("Breakout Game");
        setDefaultCloseOperation(EXIT_ON_CLOSE);
        setSize(800, 600);
        setLocationRelativeTo(null);
        setResizable(false);
    }

    public static void main(String[] args) {
        Game game = new Game();
        game.setVisible(true);
    }
}
