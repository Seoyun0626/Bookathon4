# π»2021 SKKU AI x Bookathon 4rdπ


## 1. Introduction
Book(μ±)κ³Ό Hackathon(ν΄μ»€ν€)μ ν©μ±μ΄λ‘ μΈκ°κ³Ό AIκ° νμνμ¬ κΈμ μ°λ λν

μ±κ· κ΄λνκ΅μμ μ£Όμ΅νλ AI x Bookathon λνλ‘ μΈκ³΅μ§λ₯ λͺ¨λΈμ μ¬μ©νμ¬ μ£Όμ κ° 'λλ΄ν'μΈ μνμ μμ±νλ κ²μ΄ λͺ©μ 


### π reward

π"6μμ νΌλ νλ ¨ν"λΌλ μ λͺ©μ κ°μ§ μνμ μμ±νμ¬ λ³Έμ μμ μ₯λ €μ μμ

[>> λ°νμλ£ λ³΄λ¬κ°κΈ°](./λΉλΉ!_λ°νμλ£.pdf)

[>> μ΅μ’μν λ³΄λ¬κ°κΈ°](./λΉλΉ!_6μμ%20νΌλ%20νλ ¨ν.pdf)


## 1μ°¨ μμ  -> μΈκ³΅μ§λ₯ κ΄λ ¨ μν
    2λ²μ μ¬μ κ΅μ‘κ³Όμ μ μνν ν  gptμ μ¬λ¬κ°μ§ aiμ κ΄λ ¨ν κ°κ΄μ, μ£Όκ΄μ, T/Fλ¬Έμ λ₯Ό νμ΄μ μμ ν΅κ³Ό
    λ€λ₯Έ νλ€μ λ΅λ³κ³Όμ μ°¨λ³μ±μ λκΈ°μν΄ λ΅λ³μ νλ¦° μ΄μ λ₯Ό κ·Όκ±°λ‘ μμ±νλ κ²κ³Ό μΆκ°μ€λͺμ μν κ·Έλ¦Όμ μ²¨λΆ
    μμ  κ³Όμ μ ν΅ν΄μ μ΄ λνμμ μ΄λ ν κ²μ νμ©νμ¬ μ΄λ ν κ²°κ³Όλ¬Όμ λμΆν΄μΌν μ§ μμ§νκ³  μ΄ν΄
    
    
## 2μ°¨ λ³Έμ 
    2μ°¨ λ³Έμ μ μ€ν 3μλΆν° μμνμ¬ λ€μλ  μ€μ 11μκΉμ§ μ΄ 21μκ°λμ λ¬΄λ° 2μΌλ‘ μ§ν
    μ±κ· κ΄ λνκ΅ μΌμ±νμ μ λ³΄κ΄μμ κ° νλ€μ΄ λͺ¨μ¬μ μ§ν
    μνμ ν€μλ λ°ν ν κ° νλ€μ΄ λͺ¨μ¬ μ΄λ ν μ£Όμ λ₯Ό λ°νν μ§ νμ ν κ° νλ§λ€ ν μκ° ν λ³Έκ²©μ μΈ μνμμ±μ μν νλ³ νλ μμ
    μ£Όμ  μ μ  ν μ΄μ κ΄λ ¨λ λ°μ΄ν°λ₯Ό μΆκ°μ μΌλ‘ ν¬λ‘€λ§ ν λ°μ΄ν° μ μ²λ¦¬ ν λͺ¨λΈμ μΆκ°μ μΌλ‘ νμ΅μμΌ μνλ λ¬Έμ₯μ΄ μμ±λ  μ μλλ‘ ν¨
    ν λͺμ΄ μλ²μ μ μνμ¬ κΈμ μ°κΈ°μλ μκ°μ΄ λΆμ‘±ν  κ²μ΄λΌκ³  νλ¨νμ¬ λͺ¨λΈμ΄ μΌλΆλ₯Ό freezingμμΌ GPUλ°μ΄ν° νλ³΄ νμ¬ μ¬λ¬ λͺμ΄ μλ²μ μ μνμ¬ κΈμ μΈ μ μλλ‘ ν¨


## 2. Data Preprocessing Strategy
    λν ν€μλλ₯Ό μκΈ° μ μλ λΈλ°μΉ(κ°μ± ESSAY), μ μΆλ¬Έμ, κΈν΄μμ ν¬λ‘€λ§ λν ν€μλλ₯Ό μκ³  λ νλ μ£Όμ μ μ ν©ν λ°μ΄ν° μΆκ°μ  ν¬λ‘€λ§
![λ°μ΄ν° μ μ²λ¦¬](https://user-images.githubusercontent.com/104416283/213635687-a417896e-7d07-4c11-a9d1-638900693540.jpg)

    ν¬λ‘€λ§ν λ°μ΄ν°(.txt)λ₯Ό νμΌ νμ λ³ν ν(.json) μ κ·ν ννμ μ΄μ©ν κΈ°κ³μ μ²λ¦¬ ν μΈλ°ν μ μ²λ¦¬λ₯Ό μν΄ μ¬λ μ μ²λ¦¬ κ³Όμ μ ν΅νμ¬ λ°μ΄ν° μ μ 
![μ μ΄μ¨ νμΌ μ ν](https://user-images.githubusercontent.com/104416283/213635678-afe14182-332c-4b01-b08f-131e4957f57f.jpg)

## 3. Model Training Strategy
    λ§μΈμ¦λ©μμ μ κ³΅νλ μ¬μ νμ΅λ GPT3 λͺ¨λΈμ μ¬μ©νλ λμ , EleutherAI/polyglot-ko-1.3b5λ₯Ό ν λ² λ μ¬μ νμ΅μ μ§νν ν 
    fine-tuning νλ λ°©λ²μΌλ‘ μμ± λͺ¨λΈμ νμ΅
![λͺ¨λΈ νμ΅](https://user-images.githubusercontent.com/104416283/213635688-2ef622fc-76f3-4f2a-9f29-f3cd9a93f599.jpg)

    GPU λ©λͺ¨λ¦¬ νλ³΄λ₯Ό μν μ λ΅
    1. Gradient Checkpointing
    2. 8-bit optimizer
    3. Gradient Accumulation
    4. Mixed/Half precision
![GPUλ©λͺ¨λ¦¬ νλ³΄ μ λ΅](https://user-images.githubusercontent.com/104416283/213635479-67c61aa8-ecf4-4dff-a370-3a116a777662.jpg)
    


## 4. Model Inference Strategy
    top-k sampling, top-p sampling, temperature λ°©λ²μ μ΄μ©νμ¬ λν μ‘°κ±΄μ λ§λ λ¬Έμ₯μ΄ μμ±λ μμλλ‘ νλΌλ―Έν° μ‘°μ 


# π ν μκ°-

    * **κΉμμ€** - *Data Preprocess + Writing* - (tjdbs0626@gmail.com)
    * **κΉν¨μ ** - *Data Crawling + Writing* - (hyojeong9888@gmail.com)
    * **μ΄μλ―Ό** - *Fine-Tuning + Model Training* - (l.alex6095@gmail.com)
    * **μ΄μ°½ν** - *Writing* - (rheasis0115@gmail.com)
    

## πββοΈμκ°
    μΈκ³΅μ§λ₯μ νμ΅μμΌ κΈμ μμ±νκ³  μ΅μμ κΈμ μ°κΈ° μν΄ μΈκ°μ κ°μμ΄ λ€μ΄κ° κ²°κ΅­ μΈκ°κ³Ό AIκ° νμνλ€λ κ²μ΄ ν₯λ―Έλ‘μ΄ κ²½νμ΄μλ€.
    
    
    μ²μμλ νμ νλͺμ΄ μλ²μ μ μνμ¬ κΈμ μ§μ€μ μΌλ‘ μμ±νκ³  λλ¨Έμ§λ λ€μ μμ λͺ©μ κ΅¬μ±νκ³  λ΄μ©μ κ΅¬μ±νμμ§λ§ 
    νμ νλͺλ§ μλ²μ μ μνλ©΄ 2λ§μλΌλ λΆλμ μ±μ°κΈ° νλ€ κ²μ΄λΌκ³  νλ¨νμ¬ λͺ¨λΈμ freezingμ μ¬μ©νμ¬ GPUνλ³΄ ν 
    νμ 3λͺμ΄μ κΈμ μμ±νκΈ°μ λΆλμ μ±μΈ μ μμλ€κ³  μκ°νκ³  μ΄ κ³Όμ μμ freezingν΄μΌκ² λ€λ νλ¨μ΄ μ€μνλ€κ³  μκ°νλ€.
    
    λν μ£Όμ κ° μ ν΄μ§ νμ μΈκ³΅μ§λ₯μ΄ νμμ μνλ λ΄μ©μ μμ±νκΈ° μν΄μ μΆκ°μ μ λ°μ΄ν°λ₯Ό μμ§ν΄μΌκ² λ€λ νλ¨μ νλλ°
    μ£Όμ μ κ΄λ ¨λ λ°μ΄ν°λ₯Ό μΆκ°μ μΌλ‘ μμ§νμ¬ νμ΅μμΌ°κΈ°λλ¬Έμ μΈκ³΅μ§λ₯μ΄ νμμ μκ΅¬νλ λ΄μ©μ λμΆν  μ μμλ€κ³  μκ°νμ¬
    μ΄ νλ¨μ΄ μ΅μμ κ²°κ³Όλ¬Όμ΄ λμ¬ μ μλ κ²°μ μ μΈ μ΄μ λΌκ³  μκ°νλ€.
    
    μ μ μμ§μκ³  λ°€μ νμ λͺ¨λκ° κΈμ μ°λλΌ λ§μ§λ§μλ νλ€μ΄νμ§λ§ μλ‘ μμνκ³  ν  μ μλ€κ³  κ³μ μκ°ν λλΆμ
    λ§μ§λ§κΉμ§ μ§μΉμ§μκ³  κΈμ μΈ μ μμλ€κ³  μκ°νλ€.
    
    μ₯λ €μμ μμν΄μ νλ³΅νκ³ , μ°λ¦¬ νμ λͺ¨λμκ² κ°μ¬νλ€β€β€!!






