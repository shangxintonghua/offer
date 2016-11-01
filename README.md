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





