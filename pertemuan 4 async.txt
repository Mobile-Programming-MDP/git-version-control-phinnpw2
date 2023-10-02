void main() async {
  
  print("Getting Your Order .....");
  var order = await getOrder();
  try {
    print("Your Order : $order");
  } catch (error){
    print("error $error");
  } finally {
    print("Thank You");
  }
  
}

Future<String> getOrder() {
  return Future.delayed(Duration(seconds: 3), () {
    var isStockAvailable = true;
    if(isStockAvailable){
      return "Coffee Boba";
    }else{
      throw "Out Of Stock";
    }
  });
}