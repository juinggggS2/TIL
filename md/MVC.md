# ๐ข MVC ๋?
> Spring ํ๋ ์์ํฌ๊ฐ ์ ๊ณตํ๋ Web์ผ๋ก 
Model-View-Controller ์ด๋ฃจ์ด์ ธ์๋ค.
ํ๋์ ์ ํ๋ฆฌ์ผ์ด์, ํ๋ก์ ํธ๋ฅผ ๊ตฌ์ฑํ  ๋ ๊ทธ ๊ตฌ์ฑ์์๋ฅผ ์ธ๊ฐ์ง์ ์ญํ ๋ก ๊ตฌ๋ถํ ํจํด์ด๋ค.
## :ONE: `Model` ์ด๋?
- ๋ฐ์ดํฐ๋ฒ ์ด์ค(DB)์์ ๋ฐ์ดํฐ๋ฅผ ๊ฐ์ง๊ณ  ์ฌ ์ ์๊ณ  ๋ฐ์ดํฐ๋ฅผ ๊ฐ์ง๊ณ  ์์ ์๋ ์๋ค.
- ๋ฐ์ดํฐ๋ฒ ์ด์ค์ ์ํตํ๋ค.
- ์ปจํธ๋กค๋ฌ์๊ฒ ๋ฐ์ดํฐ๋ฅผ ์ ๋ฌํ๋ค.
- ๋ชจ๋ธ์ด ๋ทฐ์ ์ง์  ์ํตํ๋ ์ผ์ ์๋ค.
    - Data Design์ ๋ด๋น
      - ์: ์ํ ๋ชฉ๋ก, ์ฃผ๋ฌธ ๋ด์ญ ๋ฑ

## :TWO: `View` ๋?
- ์ ์ ๊ฐ ๋ณด๋ ํ๋ฉด์ ๋ณด์ฌ์ฃผ๊ฒ ํ๋ ์ญํ ์ด๋ค. (HTML, CSS)
- ๋ฐ์ดํฐ๋ฅผ ๋ฐ๊ณ  ๊ทธ๋ฆฌ๋ ์ญํ ์ ์ํํ๋ค.
- ๋ชจ๋ธ์ด๋ ๋ฐ์ดํฐ๋ฒ ์ด์ค์๋ ์ํตํ์ง ์๊ณ  ์ปจํธ๋กค๋ฌ์๋ง ์ํตํ๋ค.
- ์ปจํธ๋กค๋ฌ์๊ฒ ์ก์์ด๋ ๋ฐ์ดํฐ๋ฅผ ์ ๋ฌ๋ง ํ๊ณ  ์ ๋ฌ ๋ฐ๊ธฐ๋ง ํ๋ค.
    - ์ค์ ๋ก ๋ ๋๋ง๋์ด ๋ณด์ด๋ Page ๋ด๋น
        - ์: jsp ๋ฑ
    
## :THREE: `Controller` ๋?
- ๋ทฐ์์ ์ก์๊ณผ ์ด๋ฒคํธ์ ๋ํ ์ธํ ๊ฐ์ ๋ฐ๋๋ค.
- ๋ทฐ์ ๋ชจ๋ธ ์ฌ์ด์ ์ธํฐํ์ด์ค ์ญํ ์ ํ๋ค.
- ๋ชจ๋ธ์ด ๋ฐ์ดํฐ๋ฅผ ์ด๋ป๊ฒ ์ฒ๋ฆฌํ ์ง ์๋ ค์ฃผ๊ณ  ๊ทธ ๊ฒฐ๊ณผ๋ฅผ ๋ทฐ์ ์ ๋ฌํด์ฃผ๋ ์ญํ 
- ๋ชจ๋ธ์๊ฒ ์ ๋ฌํด์ฃผ๊ธฐ ์ ์ ๋ฐ์ดํฐ๋ฅผ ๊ฐ๊ณตํ  ์ ์๋ค.
- ๋ทฐ์๊ฒ ๋ชจ๋ธ์๊ฒ ๋ฐ์ ๋ฐ์ดํฐ๋ฅผ ๊ฐ๊ณตํ  ์ ์๋ค.
  - ์ด์ฉ์์ ์์ฒญ์ ๋ฐ๊ณ , ์๋ต์ ์ฃผ๋ Logic ๋ด๋น
    - ์: HTTP Method GET, POST ๋ฑ์ URL Mapping
    <br/>
    
- Controller โ> (Service) โ> Dao โ> DB
 


#### Spring MVC Module์ ์ฌ์ฉํ์ฌ Back End Programming์ ๊ธฐ๋ณธ ํ๋ ์ ์ํฌ๋ฅผ์ก๋๋ค. WEB Server์ ํนํ๋์ด ๋ง๋ค์ด์ง ๋ชจ๋์ด๊ธฐ ๋๋ฌธ์ ๊ฐ๋ฐ์๊ฐ ๊ฐ๋ฐํด์ผ ํ  ์์ญ์ ๋ ์ ๊ฒ ๋ง๋ค์ด ์ฃผ๊ธฐ ๋๋ฌธ์ ์ด๊ฒ์ ์ฌ์ฉํ์ง ์์์ ๋ ๋ณด๋ค ๋ ๊น๋ํ๊ณ , ๊ฐํธํ๊ฒ ๊ฐ๋ฐ ํ  ์ ์๋ค.

