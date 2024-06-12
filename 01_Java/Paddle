package breakout;

import java.awt.event.KeyEvent;
import java.awt.Rectangle;

public class Paddle {

    private int x, y;
    private int dx;
    private final int PADDLE_WIDTH = 60;
    private final int PADDLE_HEIGHT = 10;

    public Paddle() {
        x = 370;
        y = 550;
    }

    public void move() {
        x += dx;
        if (x < 0) {
            x = 0;
        }
        if (x > 740) {
            x = 740;
        }
    }

    public int getX() {
        return x;
    }

    public int getY() {
        return y;
    }

    public int getWidth() {
        return PADDLE_WIDTH;
    }

    public int getHeight() {
        return PADDLE_HEIGHT;
    }

    public void keyPressed(KeyEvent e) {
        int key = e.getKeyCode();
        if (key == KeyEvent.VK_LEFT) {
            dx = -2;
        }
        if (key == KeyEvent.VK_RIGHT) {
            dx = 2;
        }
    }

    public void keyReleased(KeyEvent e) {
        int key = e.getKeyCode();
        if (key == KeyEvent.VK_LEFT || key == KeyEvent.VK_RIGHT) {
            dx = 0;
        }
    }

    public Rectangle getRect() {
        return new Rectangle(x, y, PADDLE_WIDTH, PADDLE_HEIGHT);
    }
}
