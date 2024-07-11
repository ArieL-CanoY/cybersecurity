```c#
//printing 
	Console.Write()  //print something but no new line
					 //needs arguments - char '' or string ""
	Console.WriteLine()  //print something and add new line
						 //does not need arguments

//variables
	//character - stores 1 character stored in single qoutes
		char answer = 'a';
		char symbol = '*';
		char num9 = '9';

	//string - stores sequence of characters stored in double qoutes
		string name = "John Clem";
		string friend_name = "Miggy Dimson";
		string letter = "Dead charo, I know you have been my disco, my disco";

	//boolean - stores true or false 
		bool isTrue = true;
		bool isMax = false;
		bool False = true;

	//int - stores whole numbers from -2,147,483,648 to 2,147,483,647
		int age  = 43;
		int totalPay = 120353;
		int totalClicked = 10;

	//long - stores whole numbers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807
		long allNetPay = 30039085084099L;
		long allShapeEdges = 9823948584854858;
		long allCharacters = 5474859578767455;

	//float - stores fractional numbers. Sufficient for storing 6 to 7 decimal digits
		float myGrade = 97.39F;
		float temp = 30.23F;
		float pi = 3.141592;

	//double - stores fractional numbers. Sufficient for storing 15 decimal digits
		double x = 9.8937249823894;
		double y = 9038450934.908957238457293405;
		double z = 984587.98345976813275

	//constant - it can never change
		const int PI = 3.14159;
		const int WEEK_DAYS = 7;
		const int ALLMONTHSCOUNT = 12;

//declaring variables
	datatype identifier;
	datatype identifier, identifier, identifier;
	datatype identifier = value;
	datatype identifier = value, identifier = value, identifier = value;
	
	//multiple
		int a, b, c;
		a = b = c = 10;

		//or like this
		int b, c;
		int a = b = c = 10;


//datatype conversion
	//implicit - small datatype to larger datatype, no need to convert (automatic convertion)
		char mychar = 'a';
		int myint = mychar;
		float myfloat = myint;
		double mydouble = myfloat;


	//explicit - larger datatype to small datatype, need to convert
		double mydouble = 1234.1234d;
		float myfloat = (float)mydouble;
		int myint = (int)myfloat;
		char mychar = (char)myint;




//arithmetic operators
	//addition
		int num1 = 4, num2 = 3;
		int sum = num1 + num2; //output 7

	//subtraction 
		int num1 = 4, num2 = 2;
		int different = num1 - num2; //2

	//multiplication
		int num1 = 4, num2 = 3;
		int product = num1 * num2; //12

	//division
		int num1 = 9, num2 = 3;
		int quotient = num1 / num2;  //3

	//modulus
		int num1 = 9, num2 = 2;
		int modulus = 9 % 2;  //1

	//increment
		int x = 1;
		x++; //2
		++x; //3

	//decrement
		int x = 2;
		x--; //1
		--x; //0

	//grouping - operators precendence
		/*
			Postfix             (), [], ++, --
			Multiplicative      *, /, %
			Additive            +, -    
		
		*/
		
		int z = 2 + 4 / 2 * 2;
		/*
			Evaluation:
				1st: 4 / 2 = 2 + 2 * 2
				2nd: 2 * 2 = 2 + 4
				3rd: 2 + 4 = 6
				z is 6
		*/
		
		int z = (2 + 4) / 2 + 2 * 2;
			/*
			Evaluation:
				1st: (2 + 4) = 6 / 2 + 2 * 2
				2nd: 6 / 2 = 3 + 2 * 2
				3rd: 2 * 2 = 3 + 4
				4th: 3 + 4 = 7
				z is 7
		*/

//assignment  operators
	// addition: +=
		int x = 12;
		x += x; //24
		x += 1; //25

	//subtraction: -=
		int x = 12;
		x -= 5; //7
		x -= x; //0

	//multiplication: *=
		int x = 3;
		x *= 2; //6
		x *= 3; //18

	//division: /=
		int x = 10;
		x /= 5; //2
		x /= x; //1

	//modulus: %=
		int x = 12;
		x %= 5; //2
		x %= 2; //0



//comparison operators
	//not equals - !=
		93 != 234 //true
	//less than - <
		9 > 32 //false
	//less than or equals - <=
		239 <= 239 //true
	//greater than - >
		923 > 93 //true
	//greater than or equals - >=
		923 >= 923 //true

//logical operators
	//AND - &&
		bool isBlack = True, isWhite = False;
		bool isBlackAndWhite = isBlack && isWhite;  //false
	//OR - ||
		bool isBlack = True, isWhite = False;
		bool isBlackAndWhite = isBlack || isWhite;  //false
	//NOT - !
		bool isBlack = True, isWhite = False;
		Console.WriteLine(!isBlack); //false
		Console.WriteLine(!isWhite); //true
	

//conditional statement
	//IF statement syntax
		int age = 18;
		if (age >= 18)
		{
			Console.WriteLine("You can enter the building");
		}

	//IF - ELSE statement syntax
		int age = 18;
		if (age >= 18)
		{
			Console.WriteLine("You can enter the building");
		}
		else
		{
			Console.WriteLine("You cannot enter the building");
		}

	//IF - ELSE IF - ELSE statement syntax
		int age = 18;
		if (age >= 18)
		{
			Console.WriteLine("You can enter the building");
		}
		else if (age >= 46)
		{
			Console.WriteLine("You are too old to enter the building");
		}
		else
		{
			Console.WriteLine("You cannot enter the building");
		}

//array
	//format
	datatype identifier = {val1, val2, val3};

	//declare and assign
	int[] numbers = new int[10];
	numbers[0] = 12;
	numbers[1] = 82;
	numbers[2] = 95;

	//declare with assign
		int[] names = {"harold", "clem", "Shyna"};

	//try this
		int[] num = new int[2];
		num = {12, 23};


//switch








