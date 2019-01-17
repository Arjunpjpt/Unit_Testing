/**
 * 
 */
package tests;

import static org.junit.Assert.*;

import java.awt.Color;
import java.awt.Point;
import org.junit.Before;
import org.junit.Test;
import shapes.Circle;

/**
 * TCSS 305 - Autumn 2017
 * arjun92-testing 
 * 
 * This is a JUnit testing framework to test the Circle class.
 * 
 * @author Arjun Prajapati
 * @version 5 October 2017
 * 
 */
public class CircleTest {

    /** A tolerance used when comparing double values for equality. */
    private static final double TOLERANCE = .000001;
    
    /**
     * The test fixture. The Objects I will use in the tests.
     * Private field myCircle, object for Circle class.
     */
    private Circle myCircle;
    
    /**
     * A method to initialize the default value of Circle.
     */
    @Before
    public void setUp() {
        myCircle = new Circle();
        myCircle = new Circle(1.0, new Point(0, 0), Color.BLACK);
        
    }
 
//    /**
//     * A method to test the constructor with the given default value of Circle class.
//     */
//    @Test
//    public void testDefaultConstructorCircle() {
//        assertEquals(1.0, myCircle.getRadius(), TOLERANCE);
//        assertEquals(new Point(0, 0), myCircle.getCenter());
//        assertEquals(Color.BLACK, myCircle.getColor());
//    }

    /**
     * This method is to test the overloaded constructor with given value..
     */
    @Test
    public void testOverLoadConstructor() {
        myCircle = new Circle(10.0, new Point(20, 20), Color.BLACK);
        
        assertEquals(10.0, myCircle.getRadius(), TOLERANCE);
        assertEquals(new Point(20, 20), myCircle.getCenter());
        assertEquals(Color.BLACK, myCircle.getColor());
    }
    /**
     * This method is for the IllegalArgumentException 
     * for the radius passed in overloaded constructor.
     */
    @Test(expected = IllegalArgumentException.class)
    public void testOverLoadConstructorIllegal() {
        //try {
        myCircle = new Circle(-1.0, new Point(10, 10), Color.BLACK);
        //} catch (final IllegalArgumentException e) {
          //  System.out.println(e.getMessage());
        //}
    }
    
    /**
     * This method is for testing the OverLoaded constructor
     * with the null input for the center of circle.
     */
    //Tests the overloaded constructor for a negative radius.
    @Test(expected = NullPointerException.class)
    public void testConstructorNull() {
     //   try {
        myCircle = new Circle(1.0, new Point(null), Color.GREEN);
       // } catch (final NullPointerException e) {
         //   System.out.println(e.getMessage());
        //}
    }

    /**
     * This method is to set the radius of the circle.
     */
    @Test
    public void testSetRadius() {
        // setting the radius of circle passing through parameter,
        myCircle.setRadius(6.0);
        assertEquals(6.0, myCircle.getRadius(), TOLERANCE);
        
        
    }

    /**
     * This method is to check the IllegalArgumentException
     *  by giving illegal input for radius.
     */
    @Test (expected = IllegalArgumentException.class)
    public void testSetRadiusIllegal() {
        //passing the illegal parameter to setRadius method.
        myCircle.setRadius(-1);
       
        
    }
   
//    /**
//     * This method is to set the radius of the circle and will have assertion error.
//     */
//    @Test 
//    public void testSetRadiusError() {
//        // setting the radius of circle passing through parameter,
//        myCircle.setRadius(7.0);
//        // to catch the assertion error expectation 
//        try {
//            assertEquals(5.0, myCircle.getRadius(), TOLERANCE);
//        } catch (final AssertionError e) {
//            System.out.println(e.getMessage() 
//                               + "Assertion Error found in testSetRadiusError method ");
//        }
//    }
    /**
     * This method is to set the center of the circle.
     */
    @Test
    public void testSetCenter() {
        //setting the center of circle giving x and y value.
        myCircle.setCenter(new Point(12, 12));
        //to check the x and y value expected value.
        assertEquals("setLocation failed to set the x value correctly!",
                     12, myCircle.getCenter().getX(), TOLERANCE);
        assertEquals("setLocation failed to set the y value correctly!",
                     12, myCircle.getCenter().getY(), TOLERANCE);
    }
    
    /**
     * This method is to check the NUll input for the center input of circle.
     */
    @Test(expected = NullPointerException.class)
    public void testSetCenterNull() {
        // giving the null value as parameter.
        myCircle.setCenter(null);
        
    }
    

    /**
     * This method is to set the color of circle.
     */
    @Test
    public void testSetColor() {
        // setting the input value of Color as blue from setColor method.
        myCircle.setColor(Color.BLUE);
        
        assertEquals(Color.BLUE, myCircle.getColor());
    }
    
//    /**
//     * This method is to set the color of circle null.
//     */
//    @Test (expected = NullPointerException.class)
//    public void testSetColorNull() {
//        // setting the input value of Color as blue from setColor method.
//       
//        myCircle.setColor(null);
//        
//        
//    }

    /**
     * This method is to set Radius and 
     * check if it has same Radius or not.
     */
    @Test
    public void testGetRadius() {
        myCircle.setRadius(5.0);
        assertEquals(5.0, myCircle.getRadius(), TOLERANCE);
    }

    /**
     * TThis method is to set center of circle 
     * and check if it has same center or not.
     */
    @Test
    public void testGetCenter() {
        myCircle.setCenter(new Point(12, 12));
        
        assertEquals("setLocation failed to set the x value correctly!",
                     12, myCircle.getCenter().getX(), TOLERANCE);
        assertEquals("setLocation failed to set the y value correctly!",
                     12, myCircle.getCenter().getY(), TOLERANCE);
    }

    /**
     * TThis method is to set color and check if it has same color or not.
     */
    @Test
    public void testGetColor() {
        // setting the input value of Color as blue from setColor method.
        myCircle.setColor(Color.BLUE);
        
        assertEquals(Color.BLUE, myCircle.getColor());
    }

    /**
     * calculate the diameter of circle with the default value.
     */
    @Test
    public void testCalculateDiameterDefault() {
        assertEquals(myCircle.getRadius() * myCircle.getRadius(),
                     myCircle.calculateDiameter(), TOLERANCE);
        
    }
    
    /**
     * calculate the diameter of circle with the given value.
     */
    @Test
    public void testCalculateDiameter() {
        //set the radius value
        myCircle.setRadius(6.0);
        
        assertEquals(myCircle.getRadius() * myCircle.getRadius(),
                     myCircle.calculateDiameter(), TOLERANCE);
       
    }

    /**
     * Calculate the circumference of circle with the default value.
     */
    @Test
    public void testCalculateCircumferenceDefault() {
        assertEquals(Math.PI * myCircle.calculateDiameter(), 
                     myCircle.calculateCircumference(), TOLERANCE);
       
    }
    
    /**
     * Calculate the circumference of circle with the given value.
     */
    @Test
    public void testCalculateCircumference() {
      //set the radius value
        myCircle.setRadius(6.0);
        
        assertEquals(Math.PI * myCircle.calculateDiameter(), 
                     myCircle.calculateCircumference(), TOLERANCE);
        
    }
    
    /**
     * Calculate the area of circle with the default value.
     */
    @Test
    public void testCalculateAreaDefault() {
        final Double r = myCircle.getRadius();
        
        assertEquals(Math.PI * r * r, myCircle.calculateArea(), TOLERANCE);
        
    }
    
    /**
     * Calculate the area of circle with the given value.
     */
    @Test
    public void testCalculateArea() {
      //set the radius value
        myCircle.setRadius(6.0);
        
        final Double r = myCircle.getRadius();
        
        assertEquals(Math.PI * r * r, myCircle.calculateArea(), TOLERANCE);
        
    }

    /**
     * Test method for {@link shapes.Circle#toString()}.
     */
    @Test
    public void testToString() {
        assertEquals("Circle [radius=1.00, center=java.awt.Point[x=0,y=0], "
                     + "color=java.awt.Color[r=0,g=0,b=0]]", 
                     myCircle.toString());
    }

}
