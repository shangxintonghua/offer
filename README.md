#《剑指offer》java实现
###issue#2 Singleton  
1.饿汉模式  
    public class Singleton{   
	  private static final Singleton singleton=new Singleton();  
	  private Singleton(){}  
	  public static Singleton getSingleton(){  
	   return  singleton;	  
}
}  
2.懒汉模式  
    public class Singleton{  
	  private static Singleton singleton;
	  private Singleton(){}  
	  private static synchronized Singleton getSingleton(){  
	    if(singleton==null){  
		    singleton=new Singleton();
       }	
}
}  
3.doublecheck  
    public class  Singleton{  
      private static Singleton singleton;  
      private Singleton(){}  
      private static Singleton getSingleton(){  
    	   if(singleton==null){  
    		synchronized(Singleton.class){  
    	 if(singleton==null){  
    		  singleton=new Singleton();  
}}}}}  
4.内部静态类  
	public class Singleton{  
	  private Singleton(){}  
	  public static Singleton getSingleton(){  
		return SingletonHolder.instance;  
}   
	private static class SingletonHolder{  
	 privaate static final Singleton instance=new Singleton();  
}

}
###issue#3二位数组查找
  在一个二维数组中，每一行都按照从左到右递增的顺序排序，每一列都按照从上到下递增的顺序排列。请完成一个函数，输入这样一个数组和一个整数，判断数组中是否含有该整数。  
	public boolean getTarget(int[] args,int target){   
	  int row=args.length;   
	  int column=args[0][].length;  
	  int i=0  
	  while(row>=0&&i<columm){     
		if(args[row][i]>target){  
			row--;   
}  
		else if(args[row][i]<target) {  
		   i++;   
}  
        else  
		   return true;

}  
           return false;  
}




