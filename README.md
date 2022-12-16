# android_lotto





  //로또 번호를 중복을 허용하고 생성하는 함수
    private fun getLottoNumber1() {
		val rnd = Random()
		val lotto = IntArray(6)
		for (i in lotto.indices) {
			lotto[i] = rnd.nextInt(45) + 1
		}
		lotto.sort()
		setTvNumber(lotto[0], binding.tvLotto1)
		setTvNumber(lotto[1], binding.tvLotto2)
		setTvNumber(lotto[2], binding.tvLotto3)
		setTvNumber(lotto[3], binding.tvLotto4)
		setTvNumber(lotto[4], binding.tvLotto5)
		setTvNumber(lotto[5], binding.tvLotto6)
  } 
  
  
  
  
  
  
    //로또 번호를 중복을 허용하지 않고 생성하는 함수
      	private fun getLottoNumber2() {
		val rnd = Random()
		val lotto = IntArray(6)
		while (true) {
			var isSame = false
			for (i in lotto.indices) {
				lotto[i] = rnd.nextInt(45) + 1
			}
			for (i in lotto.indices) {
				for (j in lotto.indices) {
					if (i != j) {
						if (lotto[i] == lotto[j]) {
							isSame = true
						}
					}
				}
			}
        //if( isSame == false) {
			if (!isSame) {
				break
			}
		}
		lotto.sort()
		setTvNumber(lotto[0], binding.tvLotto1)
		setTvNumber(lotto[1], binding.tvLotto2)
		setTvNumber(lotto[2], binding.tvLotto3)
		setTvNumber(lotto[3], binding.tvLotto4)
		setTvNumber(lotto[4], binding.tvLotto5)
		setTvNumber(lotto[5], binding.tvLotto6)
	}
  
  중복을 허용하지 않을 때의 화면
  
  ![image](https://user-images.githubusercontent.com/93520695/208101244-9fa71378-7411-4e51-8e05-f528c59f5800.png)
  
  
  중복을 허용 할 때의 화면
  
  ![image](https://user-images.githubusercontent.com/93520695/208101334-f73144de-6400-4129-942b-bf8daaad0d72.png)


저장버튼을 누른뒤 저장된 리스트를 볼수있는 화면

![image](https://user-images.githubusercontent.com/93520695/208101379-a31c5f52-536f-4886-b625-1a26638aab42.png)

