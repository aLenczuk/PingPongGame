# PingPongGame

import java.awt.*;


public class Player2 extends GameObject {

    private Handler handler;

    public Player2(float x, float y, ID id, Handler handler) {
        super(x, y, id);
        this.handler=handler;
    }

    @Override
    public void tick() {

        x+=velX;
        y+=velY;

        y=Game.clamp((int)y, 0, 385);
    }

    @Override
    public void render(Graphics g) {

        g.setColor(Color.green);
        g.fillRect((int)x, (int)y, 20, 80);
    }

    @Override
    public Rectangle getBounds() {
        return new Rectangle((int)x, (int)y, 20, 80);
    }
}
