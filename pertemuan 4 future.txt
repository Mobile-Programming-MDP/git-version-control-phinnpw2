void main() {
  
  final myFuture = Future(() { //Uncomplete
      print('Creating the future');
      return 12;
    }).then((value) {   //Complete with data
    print(value);
  }).catchError((error) {  //Complete with error
    print("Error $error");
  });
  
  print('main() done');
//   print(myFuture);
  
  getOrder().then((value) {
    print("You ordered : $value");
  }).catchError((error) {  //Complete with error
    print("Error $error");
  }).whenComplete(() {
    print("Thank You");
  });
  print("Getting your order .....");
}

Future<String> getOrder(){
  return Future.delayed(Duration( seconds: 3), () {
    var isStockAvailable = true;
    if(isStockAvailable)
    {
      return "Coffee Boba";
    }
    else 
    {
      throw "Out of Stock";
    }
  }); 
}
