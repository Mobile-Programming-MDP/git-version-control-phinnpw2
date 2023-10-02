//Implicit Interface

class Flyable{
  void fly(){}
}

class Animal{
  String name = "";
  int age = 6;
  double weight = 0;
  Animal(this.name, this.age, this.weight);
  void eat(){
    print("$name is eating.");
    weight = weight + 0.2;
  }
  void sleep(){
    print("$name is sleeping.");
  }
}

class Bird extends Animal implements Flyable{
  String featherColor;
  Bird(String name, int age, double weight, this.featherColor):super(name, age, weight);
  
  //Polymorphisme
  @override
  void fly(){
    print("$name is fly");
  }
  
}

void main(){
  var mdpBird = Bird("Gagak", 2, 0.7, "Black");
  mdpBird.fly();
  print("Berat Burung : ${mdpBird.weight}");
  mdpBird.eat();
  print("Berat Burung Sekarang : ${mdpBird.weight.toStringAsFixed(1)}");
}