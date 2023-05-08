Download Link: https://assignmentchef.com/product/solved-solvedstatcalc
<br>
The following class StatCalc defines a series of methods for computing statistics for a group of numbers.

/*

* An object of class StatCalc can be used to compute several simple statistics

* for a set of numbers. Numbers are entered into the dataset using

* the enter(double) method. Methods are provided to return the following

* statistics for the set of numbers that have been entered: The number

* of items, the sum of the items, the average, and the standard deviation

*/

public class StatCalc {

private int count; // Number of numbers that have been entered.

private double sum; // The sum of all the items that have been entered.

private double squareSum; // The sum of the squares of all the items.

/**

* Add a number to the dataset. The statistics will be computed for all

* the numbers that have been added to the dataset using this method.

*/

public void enter(double num) {

count++;

sum += num;

squareSum += num*num;

}

/**

* Return the number of items that have been entered into the dataset.

*/

public int getCount() {

return count;

}

/**

* Return the sum of all the numbers that have been entered.

*/

public double getSum() {

return sum;

}

/**

* Return the average of all the items that have been entered.

* The return value is Double.NaN if no numbers have been entered.

*/

public double getMean() {

return sum / count;

}

/**

* Return the standard deviation of all the items that have been entered.

* The return value is Double.NaN if no numbers have been entered.

*/

public double getStandardDeviation() {

double mean = getMean();

return Math.sqrt( squareSum/count – mean*mean );

}

} // end class StatCalc

Using the StatCalc class, write a program that calculates and then displays as output to the console, the following statistics against the set of numbers given below.

Statistics that must be calculated:

Count – Quantity of numbers in the data set.Mean – The mean or average of the numbers in the data set.Standard Deviation – The measure of variance (or dispersion) from the mean.The set of numbers that you must use is as follows:

5 7 12 23 3 2 8 14 10 5 9 13

You must create a program with a main method that defines the StatCalc class and instantiates an instance of StatCalc called myStatCalc. Your program should instantiate the instance of the StatCalc using a statement similar to the following:

StatCalc myStatCalc;

myStatCalc = new StatCalc();