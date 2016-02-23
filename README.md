# Vehicle1
for java 

public class Vehicle {
	 	private String regNumber;
	    private String make;
	    private int yearMade;
	    private double value;

	    public Vehicle(String regNumberIn, String makeIn, int yearMadeIn, double valueIn)
	    {
	        regNumber = regNumberIn;
	        make = makeIn;
	        yearMade = yearMadeIn;
	        value = valueIn;
	    }

	    public void setValue(double valueIn)
	    {
	       value = valueIn;
	    }

	    public String getRegNumber()
	    {
	        return regNumber;
	    }

	    public String getMake()
	    {
	        return make;
	    }

	    public int getYear()
	    {
	        return yearMade;
	    }

	    public double getValue()
	    {
	        return value;
	    }

	    public int calculateAge(int currentYearIn)
	    {
	        return currentYearIn - yearMade;
	    }

}

secondhand vehicle commands


public class SecondHandVehicle extends Vehicle
	{
	private int numberOfOwners; // the attributes
	
	// the methods
	public SecondHandVehicle(String regln, String mln, int yln, double vln, int ownln)  // the constructor
	{
		super(regln, mln, yln, vln);
		numberOfOwners = ownln;
	}
	
// methods to read the attributes
	public int getNumberOfOwners()
	{
		return numberOfOwners;
	}

	public void sellVehicle(double sellValue){
	
		numberOfOwners = numberOfOwners +1;
		setValue(sellValue);
	
}

}

main SHV program to run


public class TestSHV {

	public static void main(String[] args) {
		SecondHandVehicle myCar = new SecondHandVehicle("CN4102", "UEL Motors", 2010, 4999, 2 );
		System.out.println("Registration: " +myCar.getRegNumber());
		System.out.println("Make:" +myCar.getMake());
		System.out.println("Year of manufacture: " +myCar.getYear());
		System.out.println("Value: " +myCar.getValue());
		System.out.println("Age: " +myCar.calculateAge(2016));
		System.out.println("number of owners: " +myCar.getNumberOfOwners());
		System.out.println("Car sold for: 2999");
		myCar.sellVehicle(2999);
		
		System.out.println("Value: " +myCar.getValue());
		System.out.println("number of owners: "+myCar.getNumberOfOwners());
		
		
	

	}

}

