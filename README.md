@FunctionalInterface
interface Operator {
    double apply(double a, double b);
}

public class OperatorDemo {
    public static void main(String[] args) {
        Operator power = Math::pow;
        Operator subtract = (a, b) -> a - b;
        Operator divide = (a, b) -> b == 0 ? Double.NaN : a / b;

        System.out.println(power.apply(2, 3));
        System.out.println(subtract.apply(10, 4));
        System.out.println(divide.apply(20, 5));
    }
}
