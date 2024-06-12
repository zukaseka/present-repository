package breakout;

import javax.swing.JPanel;
import javax.swing.Timer;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import java.awt.event.KeyAdapter;
import java.awt.event.KeyEvent;

public class Board extends JPanel implements ActionListener {

    private Timer timer;
    private Ball ball;
    private Paddle paddle;
    private Brick[] bricks;

    public Board() {
        initBoard();
    }

    private void initBoard() {
        addKeyListener(new TAdapter());
        setFocusable(true);
        setPreferredSize(new Dimension(800, 600));
        setBackground(Color.BLACK);

        ball = new Ball();
        paddle = new Paddle();
        bricks = new Brick[30];
        int k = 0;
        for (int i = 0; i < 5; i++) {
            for (int j = 0; j < 6; j++) {
                bricks[k] = new Brick(40 + j * 60, 50 + i * 30);
                k++;
            }
        }

        timer = new Timer(10, this);
        timer.start();
    }

    @Override
    public void paintComponent(Graphics g) {
        super.paintComponent(g);
        drawObjects(g);
    }

    private void drawObjects(Graphics g) {
        g.setColor(Color.YELLOW);
        g.fillRect(paddle.getX(), paddle.getY(), paddle.getWidth(), paddle.getHeight());

        g.setColor(Color.RED);
        g.fillOval(ball.getX(), ball.getY(), ball.getDiameter(), ball.getDiameter());

        g.setColor(Color.GREEN);
        for (Brick brick : bricks) {
            if (!brick.isDestroyed()) {
                g.fillRect(brick.getX(), brick.getY(), brick.getWidth(), brick.getHeight());
            }
        }
    }

    @Override
    public void actionPerformed(ActionEvent e) {
        ball.move();
        paddle.move();
        checkCollision();
        repaint();
    }

    private void checkCollision() {
        if (ball.getRect().intersects(paddle.getRect())) {
            ball.setYDir(-ball.getYDir());
        }

        for (Brick brick : bricks) {
            if (!brick.isDestroyed() && ball.getRect().intersects(brick.getRect())) {
                ball.setYDir(-ball.getYDir());
                brick.setDestroyed(true);
            }
        }
    }

    private class TAdapter extends KeyAdapter {
        @Override
        public void keyReleased(KeyEvent e) {
            paddle.keyReleased(e);
        }

        @Override
        public void keyPressed(KeyEvent e) {
            paddle.keyPressed(e);
        }
    }
}
