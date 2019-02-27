# 자료형

## primitive type (기본형)
  자바에서 기본적으로 제공하는 데이터형
  - 숫자형
    + 정수형
      * byte 8bits -2^7 ~ 2^7-1  
        byte b1 = 126 => Success  
        byte b = 128 => Error   
        => -128에서 127의 범위를 벗어나면 오버플로우 발생  
      * short 16bits -2^15 ~ 2^15-1
      * int 32bits -2^31 ~ 2^31-1
      * long 64bits -2^63 ~ 2^63-1 
      * char 16bits -2^15 ~ 2^15-1
    + 부동소수형    
        실수형 상수는 기본적으로 double의 성격을 가진다.
      * float  
        float f = 6.24 => Error  
        float f1 = 6.24f => Success  
      * double  
        double d = 6.24L  
  - 불리언형  
    + boolean 1bit true false  
        boolean check = true => Success  
        => boolean 값은 true와 false의 값을 가진다.  
        boolean check1 = 0 => Error  
        => boolean이 가질 수 있는 값은 ture와 false이여만 한다.  
 
## reference type (참조형)
  보통은 class를 의미
  - reference 
    + class type
        * String Class  
            이 클래스는 참조형이지만 기본형처럼 사용한다.  
            불변 하는 객체이기도 하다.   
            => 값을 특정 메모리에 저장 함으로써 주소를 이용하여 값을 가지고 오는 형태  
            String str = "스트링은 객체이다"  
            String str1 = new String("스트링은 객체이다")  
        * Wrapper Class  
            기본형을 클래스로 감싼 형태  
            - byte => Byte
            - short => Short
            - int => Integer
            - long => Long
            - float => Float
            - double => Double
            - char => Char
            - boolean => Boolean  
            Integer wrapperInteger = new Integer(10)  
            int wrapperInteger = new Integer(10)  
        * Class  
        유사한 특징을 지닌 객체들의 속성을 묶어 놓은 집합체이다.    
        ```java
        class MyObject{
            private int index;
            MyObject(int index) {
                this.index = index;
            }
            public int getIndex() {
                return index;
            }
            public void setIndex(int index) {
                this.index = index;
            }
        }
        public class ClassType {
            public static void main(String[] args) {
                MyObject a = new MyObject(2);
                MyObject b = new MyObject(4);
                System.out.println(a.getIndex()); // "a" result is 2.
                a = b;
                System.out.println(a.getIndex()); // "a" result is 4.
                b.setIndex(6);
                System.out.println(a.getIndex()); // "a" result is 6.
            }
        }
        ```
        + interface type  
        클래스들이 구현해야 하는 동작을 지정하는데 사용되는 추상형이다.
        ```java
        interface MyInterface<T> {
            void add(T value);
        }
        
        public class ClassType implements MyIterface {
            public static void main(String[] args) {
                
            }
        }
        ```
        + array type  
        같은 타입의 변수들의 모임이며 배열은 하나의 이름을 공유한다.
        ```java
        public class ArrayType {
            public static void main(String[] args) {
                int [] i = new int[2];
                Long [] l = new Long[2];
                Object[][] o = null;
            }
        }
        ```
