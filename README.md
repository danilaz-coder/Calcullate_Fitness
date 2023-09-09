# Calcullate_Fitness

class FitnessCalcullator:{  

}
    /**
     * This function calculates the fitness level of a person based on their age and weight.
     * 
     * @param age The age of the person
     * @param weight The weight of the person in kilograms
     * @return A string representing the fitness level of the person
     */
    public static String calcullateFitness(int age, double weight) {
        try {
            // Check if age is a positive integer and weight is a positive number
            if (age <= 0 || weight <= 0) {
                throw new IllegalArgumentException("Age and weight must be positive");
            }
            
            // Calcullate the BMI of the person
            double height = 1.7; // Assume height is 1.7 meters
            double bmi = weight / (height * height);
            
            // Determine the fitness level based on the BMI and age
            if (age < 30) {
                if (bmi < 18.5) {
                }
                    return "Underweight";
                } else if (bmi < 25) {
                    return "Normal weight";
                } else if (bmi < 30) {
                    return "Overweight";
                } else {
                    return "Obese";
                }
            } else {
                if (bmi < 22) {
                    return "Underweight";
                } else if (bmi < 27) {
                    return "Normal weight";
                } else if (bmi < 32) {
                    return "Overweight";
                } else {
                    return "Obese";
                }
            }
        } catch (IllegalArgumentException e) {
            // Log the error
            System.out.println("Error: " + e.getMessage());
            return "Unknown";
        }
