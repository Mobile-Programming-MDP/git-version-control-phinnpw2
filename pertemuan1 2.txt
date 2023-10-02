void main() {
  String nama = "Samuel Effendi Pratama";
  int umur = 18;
  
  print("Hallo , Nama Saya $nama dan Umur Saya $umur tahun");
  print("Hallo , Nama Saya " + nama +" dan Umur Saya " + umur.toString() + " tahun");
  
  var alamat = "Jl. Karya Baru";
  var alamat2 = 'Jl. Karya Baru';
  print(alamat.runtimeType); // String
  print(alamat2.runtimeType);
  
  //Collection
  var numberlist = [1, 2, 3, 4]; // List
  var stringList = ["Hi", "Cun", "Ahu"];
  print(stringList);
  
  var dinamicList = [1, "MDP", true];
  print(dinamicList.runtimeType); //List<dynamic>
  
  //Set
  Set<int> mySet = new Set.from([1, 2, 3, 4, 2, 1]); //Menghapus Data Double
  print(mySet);
  
  var setA = {1, 2, 3};
  var setB = {1, 5, 7}; 
  
  //Tambahkan 4 ke dalam set A
  setA.add(4);
  print(setA); //1, 2, 3, 4
  
  //Hapus 7 dari set B
  setB.remove(7);
  print(setB); // 1, 5
  
  //Union Dan Intersection
  //Coba gunakan fungsi union dan intersection pada setA dan setB
  //Apa yang dihasilkan dari fungsi union?
  
  print(setA.union(setB)); //Gabungan
  
  print(setA.intersection(setB)); //Irisan
  
  print(setA.difference(setB)); 
  
  
  int angka1 = 10;
  
  var  primeNumber = [2, 3, 5, 7, 11, 13, 17, 19];
  
  var searchNumber = 13;
  
  for(int  i = 0 ; i<primeNumber.length ; i++)
  {
    if(searchNumber == primeNumber[i])
    {
      print( "$searchNumber adalah bilangan prima ke- ${i+1}");
      break;
    }
    print("$searchNumber != ${primeNumber[i]}");
  }
  
  }

