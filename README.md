# Kotlin-Fragment
#  
## 참고 블로그
#### https://todaycode.tistory.com/131
##### ( 다른 분의 블로그로 문제가 되면 삭제하겠습니다 )
#  
#  
## Fragment 란?
### 한 Activity에 다른 여러 화면을 띄우면 관리가 힘들 뿐더러 코드가 길어진다.
### Fragment를 사용함으로 써 구성 화면을 여러개 띄울 수 있다.
#  
#  

## Fragment transcaton
### transacton.add( containerViewId, Fragment fragment )
#### 새로운 fragment를 화면에 추가한다.
#  
#  
### transacton.replace( containerViewId, Fragment fragment )
#### 추가된 fragment를 대체한다.
#  
#  
### transacton.remove( Fragment fragment )
#### 추가된 fragment를 제거한다.
#  
#  
### transacton.commit()
#### 화면에 적용한다.

#  
#  
## FragmentManager
        val fragmentManager: FragmentManager = supportFragmentManager
        val transacton: FragmentTransaction = fragmentManager.beginTransaction()
        val fragment = BlankFragment() // Fragment File Name

#
#

## Add Fragment Screen
        binding.button.setOnClickListener {
            transacton.add(R.id.framelayout, fragment) // add.(R.id.LayoutName, fragment)
            transacton.commit()
        }

#
