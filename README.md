# cs115_examples
working with array lists and reading in files in java ; using constructors, accessor & mutator methods 

public class Designer {  // this is where info about single designer, will be put into array
//can't take arguments anyways
  private String lName, fName, faveShow; 
  private double salary; 
  private int age;
  private char status; 
  
  public Designer (String lN, String fN, int a, double s, char stat, String fs) { // constructor
	  lName = lN; 
	  fName = fN; 
	  age = a; 
	  faveShow = fs; 
	  salary = s; 
	  status = stat; 
  }
  
  public String getLastName () {
	  return lName; 
  }
  public String getFirstName () {
	  return fName; 
  }
  public int getAge() {
	  return age;
  }
  public String getFaveShow () {
	  return faveShow; 
  }
  public double getSalary ()  {
	  return salary; 
  }
  public char getStat () {
	  return status; 
  }
  public void setLastName (String passedlName) {
	  lName = passedlName;  
  }
  public void setFirstName (String passedfName) {
	  fName = passedfName;	
  }
  public void setAge (int passedAge) {
	  if (passedAge >= 18 && passedAge < 75) 
		  age = passedAge; 
	  else 
		  System.out.println ("Invalid Entry");	  
  }
  public void setSalary (double passedsalary) {
	  if (passedsalary >= 100.00 && passedsalary <= 1000000.00 )
	  salary = passedsalary; 
  }
  public void setFaveShow (String passedfaveShow) {
	  faveShow = passedfaveShow; 
  }
  public void setStatus (char passedStatus) {
	  status = passedStatus; 
  }
}
// also add following: 
import java.util.*; 

public class Season_v3 {  
   private ArrayList <Designer> designers; 
   private String seasonNumber; 

	public Season_v3 (String sNumber) {
		seasonNumber = sNumber; 
		designers = new ArrayList <Designer>();
		// constructor method 
	}
	public ArrayList <Designer> getDesigners() {
		return designers;  // because this is variable 
	}
	public void add (Designer d) { //add designers into AL 
		designers.add(d); 
	}
} 

// created a new type that's allowed to behaves sim to AL 
// & keeps track season number
// this is java's class season - inside is the array of designers
// season v2 is my type
