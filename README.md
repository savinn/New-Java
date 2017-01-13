package com.javafortesters.chap009arraysanditeration.examples;

import org.junit.Test;

import static org.junit.Assert.assertEquals;

/**
 * Created by robert.hope on 10/01/2017.
 */
public class Examples {

    String[] gymdays = {"monday", "tuesday", "thursday", "friday"};


    @Test
    public void simpleArrayExample() {
        String[] numbers0123 = {"zero", "one", "two", "three"};
        for (String numberText : numbers0123) {
            System.out.println(numberText);
        }
        assertEquals("zero", numbers0123[0]);
        assertEquals("three", numbers0123[3]);
    }

    @Test
    public void arrayDeclarations() {
        //declare arrays of a fixed size
        int[] array1 = new int[10];
        int[] array2 = new int[10];
        /* it is possible to use square braces after the name
         declaration like so.....
          */
        int array3[] = new int[10];
        String array4[] = new String[5];


        //assign values to a fixed length array
        array4 [0] = new String("rob");
        array4 [1] = new String("is");
        array4 [2] = new String("learning");
        array4 [3] = new String("java");
        array4 [4] = new String ("for testing");




        //declare an array with actual values
        int[] array5 = {1, 2, 3, 4, 5};

        /* declaring the array like this sets the size of the array int he declarartion*/

        // declare array of zero length
        int[] array6 = {};
        //or
        int[] array7 = new int[0];

        // you can declare and array with the name only, and then initialise it later on in the code like this

        int[] array8;
        //....
        // ....
        array8 = new int[10];
        //or create an anonymous array and allocate it to an existing variable like this
        array8 = new int[]{100, 200, 300};

        // access array items using the [i] notation where i is the array index position you want to access like this

        System.out.println(array5[3]);
//or this
        assertEquals("monday is a gym day", "monday", gymdays[0]);
        assertEquals("friday is a gym day", "friday", gymdays[3]);

        String pr4 ="";
        for (String printa4 : array4){
            pr4 = (pr4 + " " + printa4);
            /*System.out.println(pr4);*/
            /*DONT PUT YOUR PRINT STATEMENT HERE! IF YOU DO YOU WILL
            GET AN OUTPUT SPANNING MULTIPLE LINES FOR EACH ARRAY INDEX. IF YOU NEED A SINGLE LINE
            OUTPUT MAKE SURE THE PRINT STATEMENT IS OUTSIDE THE CURLY BRACE. THE SAME GOES FOR ANY
            ASSERT STATMENTS AND STUFF*/
        }
        // MAKE SURE TO PUT PRINTSD AND ASSERTS HERE
        System.out.println(pr4);
    }



@Test
        public void forEachLoop(){
        String days="";
        for(String gymday : gymdays) {
            days = days + "|" +  gymday;


        }
    //assertEquals("|monday|tuesday|thursday|friday", days);
    System.out.println(days);
}

@Test
    public void forLoop(){
    String days = "";
    for(int i =0; i<4; i++){
        days = days + "|" + gymdays[i];
    }
    System.out.println(days);
}

@ Test
    public void forLoopUsingIndexFixedCondition(){
    String days ="";
    for (int i = 0; i<4; i++){
        //using variable i in the output string allows me to have an index count against each string item in the output
        days = days + "|" + i + "-" + gymdays[i];
    }
    System.out.println(days);

    }



}







