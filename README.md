# PoolAreaChallenge
package academy.learnprogrmming;

public class Rectangle {
  private double width, length;

    public Rectangle(double width, double length){
        this. width = width;
        this. length = length;
        if(width < 0) {
            width = 0;
        }
    }

    public double getWidth() {
        return width;
    }

    public double getLength(){
        return length;
    }

    public double getArea(){
        return (width * length);
    }
}

package academy.learnprogrmming;

public class Cuboid extends Rectangle {
    double height;

    public Cuboid (double width, double length, double height){
        super(width, length);
        this.height = height;
        if(height < 0) {
            height = 0;
        }
    }

    public double getHeight() {
        return height;
    }

    public double getVolume(){
        double volume = height * getArea();
        return volume;
    }
}

package academy.learnprogrmming;

public class Main {

    public static void main(String[] args) {

        Rectangle rectangle = new Rectangle(5,10);
        System.out.println("rectangle.width= " + rectangle.getWidth());
        System.out.println("rectangle.length= " + rectangle.getLength());
        System.out.println("rectangle.area= " + rectangle.getArea());
        Cuboid cuboid = new Cuboid(5,10,5);
        System.out.println("cuboid.width= " + cuboid.getWidth());
        System.out.println("cuboid.length= " + cuboid.getLength());
        System.out.println("cuboid.area= " + cuboid.getArea());
        System.out.println("cuboid.height= " + cuboid.getHeight());
        System.out.println("cuboid.volume= " + cuboid.getVolume());


    }
}
OutPut:
rectangle.width= 5.0
rectangle.length= 10.0
rectangle.area= 50.0
cuboid.width= 5.0
cuboid.length= 10.0
cuboid.area= 50.0
cuboid.height= 5.0
cuboid.volume= 250.0
