# quiz1
public class QBR {
	
	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		
		System.out.println("Enter passed attempts");
		double ATT = input.nextDouble();
		
		System.out.println("Enter completion number");
		double COMP = input.nextDouble();
		
		System.out.println("Enter passing yards points");
		double YDS = input.nextDouble();
		
		System.out.println("Enter touchdown passes");
		double TD = input.nextDouble();
		
		System.out.println("Enter interception");
		double INT = input.nextDouble();

		input.close();
		
		double a = ((COMP / ATT) - 0.3) * 5;
			if (a > 2.375){
				a = 2.375;			
			}
			
			if (a < 0){
				a = 0;
			}
		
		double b = ((YDS / ATT) - 3) * .25;
			if (b > 2.375){
				b = 2.375;			
			}
		
			if (b < 0){
				b = 0;
			}
		
		double c = (TD / ATT) * 20;
			if (c > 2.375){
				c = 2.375;			
			}
	
			if (c < 0){
				c = 0;
			}
			
		double d = 2.375 - ((INT / ATT) * 25);
			if (d > 2.375){
				d = 2.375;			
			}
	
			if (d < 0){
				d = 0;
			}
		
		double passerRating = (a + b + c + d) / 6 * 100;
		
		
		System.out.println("The passer rating is" + passerRating );
		
	}

}
