# Personal-Project


/*Method 1 :basic way adding mulitples of 3 or 5*/             
 private int GetSumOfMultiples()
 {
     int sum = 0;      
     for (int i = 1; i < 1000; i++)
     {
         if (((i % 3) == 0) || ((i % 5) == 0))
         {
             sum += i;
         }
     }
             
  /*calling method 2 here */           
      sum = 0;
      sum = MultiplesofN(3, 999) + MultiplesofN(5, 999) - MultiplesofN(15, 999);
      return sum;   
  }

/*Method2 : using generic method for any number of multiples. We are taking out the multiples of 15 bcoz when we add the multiple of 3 "+" multiples of 5, there is a chancthat we are adding twice the common mutliples of 3 & 5.since these are LCF's for 15,we are taking out that sum.*/       
private int MultiplesofN(int n, int p)
{
    return n * (p / n) * ((p / n) + 1) / 2;
}

