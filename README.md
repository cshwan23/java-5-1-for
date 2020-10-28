# java-5-1-for
반복문 for


	package com.daum.erp;

	public class Test_06 {
 
		public static void main(String[] args) {
	
			
//"사오정"이라는 문자 데이터를 9번 출력하기
			
// 무식한 방법으로 사오정 9번 출력하기	

		System.out.println("사오정");	
		System.out.println("사오정");	
		System.out.println("사오정");	
		System.out.println("사오정");	
		System.out.println("사오정");	
		System.out.println("사오정");	
		System.out.println("사오정");	
		System.out.println("사오정");	
		System.out.println("사오정");	
		System.out.println("사오정");	

// for 문 사용하여 "손오공"이란 문자 데이터9번 출력하기
		
//		for ( 초기값설정 ; 조건식 ; 증감식 ) { 실행구문; }
//		초기값이 조건식에 맞지않으면 한번도 실행 안될수도 있다.
//      증감식을 잘못 설정하면 무한반복에 걸릴 수도 있다.
//		조건식이 없을 경우(생략된 경우) 무한반복에 걸린다.
//		증감식이 없을 경우(생략된 경우) 무한반복에 걸린다.
//		언제끝나냐 조건식(조건식이 false여야 빠져나온다.)
//		마지막 실행되는건 조건식이다.(반복문의 마지막은 조건식이다.)
//		무한반복에 빠지지 않도록 프로그램을 잘 짜야한다.(조심해야된다.)

		int i=0;
		for( int i=0;  i<=9   ;   i++ ) {
			-------   -----       ---
			  <1>   <2><6><10>.. <5><9>..
//<1>0번부터 시작해라 (변수 초기화)			
//<2>조건식이 true일 때 안으로 들어간다(false이면 for문(반복문)을 빠져나간다. 			
//	

			System.out.println("손오공");
		    ---------------------------
			            <3><7><11>...
//<3>한번 출력	

	 	    }
       ---
     <4><8><12>...
  
//<4>빠져 나온다.
//<5>증감식에 들린다 i가 1이 증가한다 i가1이된다
//<6>조건 확인한다 트루이면 안으로 들어간다
//<7>실행구문을 실행한다.
//<8>빠져나온다
		
//		System.out.println(i);  // -> 에러난다.
//		for 문 () 안에서 선언된 변수는 for문 바깥에선 쓸 수가 없다.
//		for문 바깥으로 i 변수를 빼면 바깥에서도 사용가능하다.
		
		
//<문제1> *어렵다*다시볼것 *순서 확실히 기억*
//for 문 사용하여 1부터 5까지 더한 결과를 출력하기

		int tot = 0;
		
		for ( int i=1; i<6 ; i++) {
			
			tot = tot + i;
			
		}
		System.out.println("1부터 5까지의 합 : " + tot );
		
//변수안의 데이터가 계속 변한다
//변수추적능력 필요.
//		t   i 
//		0 + 1
//		1 + 2
//		3 + 3
//		6 + 4	
//		10+ 5	
		
		
//<문제2>*tot의 필요성*용도* for문이 어떻게 사용되는지 이제 적용/
//for 문을 사용하여 1부터 5까지 더하되 홀수만 골라 더한 결과를 출력하기
		
			
		tot = 0;
		
		for (int i=1 ; i<6  ; i+=2 ) {

			
			tot = tot + i;
      
 //			0 = 0 + 1
//			0 = 0 + 3 
			
			
		}
			
		System.out.println("1부터 5까지의 홀수의 합 : " + tot );
			
//<문제3> 
//		증감식을 i++를 건드리지말고 놔둔 상태에서 홀수의 합을 구해보기

		tot = 0;
		
		for (int i=1 ; i<6  ; i++ ) {

			
			if (i%2 == 1) {
						
				
			tot = tot + i;
			
//			1을 2로 나눈 나머지 값은 1, 3, 5, 7 ..홀수이다
//			0 = 0 + 1
//			0 = 0 + 3 

			}
			
		}
    
//<문제4> 
//for 문을 사용하여 1부터 60까지 더하되 40번대 숫자를 제외하고 더한 결과를 출력하시오.
		
		tot = 0;
		int tot1 = 0;
		
		
		for (int i=1 ; i<61 ; i++ ) {

			tot = tot + i;

		}
		
		for (int i=40 ; i<50 ; i++ ) {

			tot1 = tot1 + i;

		}
		
		int tot2 = tot - tot1;

		System.out.println("4)40번대를 제외한 1부터 60까지의 합 : " + tot2 );	
		
//<문제4-1> 
//for 문을 사용하여 1부터 60까지 더하되 40번대 숫자를 제외하고 더한 결과를 출력하시오.
				
				tot = 0;

				for (int i=1 ; i<61 ; i++ ) {

				if ((i >= 1 && i < 40) || ( i >= 50 && i <= 60)){
					
					tot = tot + i;
				}

				}


				System.out.println("4-1)40번대를 제외한 1부터 60까지의 합 : " + tot );	
	
//<문제4-2> 
//for 문을 사용하여 1부터 60까지 더하되 40번대 숫자를 제외하고 더한 결과를 출력하시오.
								
				tot = 0;

				for (int i=1 ; i<61 ; i++ ) {

					if (!(i>39 && i<50)){
          
// 					40번대를 잡아놓고 그 제외(!반전연산자)만 구하자 
						
						tot = tot + i;
					}

				}


				System.out.println("4-2)40번대를 제외한 1부터 60까지의 합 : " + tot );
		
//<문제5>
// 구구단 5단을 아래 처럼 출력하기
// 5 x 1 = 5
// 5 x 2 = 10
// 5 x 3 = 15

				int five = 5;
				tot = 0;
				int answer = 0;
				
				for ( int i=1 ;  i<11 ; i++ ) {
					
					
//					five 
//					5   1  5 
//					5   2  10
//					5   3  15
//					5   4  20
//					5   5  25
//					5   6  30
//					5   7  35
//					5   8  40
//					5   9  45
//					5   10 50

					tot = i; // 1 2 3 4 5 6 7 8 9 10
					answer = five * i;
					System.out.println( five + " x " + i + " = " + answer );

					
					}

			
//<문제 6-1>
//ocjp시험문제*

				int i = 1;
				int j = i++;
				if ( (i == ++j) | (i++ == j) ) {
					
					i = i + j;
					
				}
				
				System.out.println("i = " + i);
        
//<문제 6-2>
//ocjp시험문제*

				int i1 = 1;
				int j1 = i1++;
				if ( (i1 == ++j1) || (i1++ == j1) ) {
									
					i1 = i1 + j1;
									
				}
								
				System.out.println("i = " + i1);
								
							

	
				
				
				
				
	}
	

}
