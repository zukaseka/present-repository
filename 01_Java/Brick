package breakout;

public class Brick {

    private int x, y;
    private boolean destroyed;
    private final int BRICK_WIDTH = 50;
    private final int BRICK_HEIGHT = 20;

    public Brick(int x, int y) {
        this.x = x;
        this.y = y;
        destroyed = false;
    }

    public int getX() {
        return x;
    }

    public int getY() {
        return y;
    }

    public int getWidth() {
        return BRICK_WIDTH;
    }

    public int getHeight() {
        return BRICK_HEIGHT;
    }

    public boolean isDestroyed() {
        return destroyed;
    }

    public void setDestroyed(boolean destroyed) {
        this.destroyed = destroyed;
    }

    public java.awt.Rectangle getRect() {
        return new java.awt.Rectangle(x, y, BRICK_WIDTH, BRICK_HEIGHT);
    }
}
