# ๐ข ๋น๋(bulid)๋?
> ์์ค์ฝ๋ ํ์ผ๋ค์ ์ปดํจํฐ์์ ์คํํ  ์ ์๋ ์ํํธ์จ์ด๋ก ๋ณํํ๋ ์ผ๋ จ์ ๊ณผ์ ์ผ๋ก,
์ปดํ์ผ, ํ์คํ, ๋ฐฐํฌ ๋ฑ ๋ชจ๋  ๊ณผ์ ์ ์งํฉ์ด๋ค.

## `๋น๋๋๊ตฌ` ๋?
- ๋น๋ ๊ณผ์ ์ ์๋์ผ๋ก ์ํํด์ฃผ๋ ๋๊ตฌ๋ฅผ ์๋ฏธํ๋ค. ๋น๋ ๋๊ตฌ์๋ Ant, Maven, Gradle ๋ฑ์ด ์๋ค.



### Maven์ ์ฌ์ฉํ๋ ์ด์ ?
- ์คํ๋ง์ด ๋์จ ์ด๊ธฐ, ์๋ฐ ๋น๋ ๋๊ตฌ๊ฐ ์์ ๋๋ ์น ํ๋ก์ ํธ๋ฅผ ์์ฑํ ํ ์ง์  ์คํ๋ง ๊ธฐ๋ฅ์ ํ์ํ ๋ผ์ด๋ธ๋ฌ๋ฆฌ๋ฅผ ๋ค์ด๋ก๋ํ์ฌ ์ฌ์ฉํ์๋ค.
ํ์ง๋ง ์คํ๋ง ๋ฒ์ ์ด ์์ฃผ ์๋ฐ์ดํธ๋จ์ ๋ฐ๋ผ ๋ถํธํจ์ด ๋ฐ๋๋ค.
์๋ฐ์ดํธํ  ๋๋ง๋ค ๊ด๋ จ ๊ธฐ๋ฅ์ ๋ผ์ด๋ธ๋ฌ๋ฆฌ๋ฅผ ์ผ์ผ์ด ์์ ํด์ผ ํ๊ณ , ๋ผ์ด๋ธ๋ฌ๋ฆฌ์ ๊ธฐ๋ฅ ์ฌ์ฉ๋ฒ์ด ๋ฌ๋ผ์ง๋ฉด ์์ค๋ ๊ฐ์ด ์์ ํด์ฃผ์ด์ผ ํ๊ธฐ ๋๋ฌธ์ด๋ค.
Maven ์ด์ ์ ์ฌ์ฉ๋์๋ ๋น๋ ๋๊ตฌ์ธ Ant๋ ๋น๋ ๋๊ตฌ๋ก๋ง ์ด์ฉ์ด ๋์๋๋ฐ, ๋น๋ + ์๋ ๋ผ์ด๋ธ๋ฌ๋ฆฌ ๊ด๋ฆฌ ๊ธฐ๋ฅ์ด ์ถ๊ฐ๋ Maven์ด ๋ฑ์ฅํ๊ฒ ๋๋ค.
<br/>**Maven์ ๋ผ์ด๋ธ๋ฌ๋ฆฌ๋ฅผ ์๋์ผ๋ก ์ถ๊ฐ ๋ฐ ๊ด๋ฆฌํด์ฃผ๊ณ , ๋ผ์ด๋ธ๋ฌ๋ฆฌ ๋ฒ์ ์ ์๋์ผ๋ก ๋๊ธฐํํด์ค๋ค.**

### Maven ์ฌ์ฉํ๋ ๋ฐฉ๋ฒ
- ์๋ฐ ํ๋ก์ ํธ์ ๋น๋ ํด๋ก maven์ ์ค์ ํ๋ค๋ฉด, ํ๋ก์ ํธ ์ต์์ ๋๋ ํ ๋ฆฌ์ 'pom.xml'์ด๋ผ๋ ํ์ผ์ด ์์ฑ๋๋ค.
- pom.xml์
1) ํ๋ก์ ํธ์ ์ ๋ฐ์ ์ธ ์ ๋ณด๋ฅผ ํ๊ทธ๋ฅผ ์ด์ฉํด ๋ํ๋ธ๋ค.
2) < dependenceise > ํ๊ทธ๋ฅผ ์ด์ฉํด ํด๋น ํ๋ก์ ํธ๊ฐ ์์กดํ๋ ์ฌ๋ฌ ๊ฐ์ง ๋ผ์ด๋ธ๋ฌ๋ฆฌ๋ฅผ ์ค์ ํ๋ค.
3) < build > ํ๊ทธ๋ฅผ ์ด์ฉํด ๋น๋์ ๊ด๋ จ๋ ์ ๋ณด๋ฅผ ์ค์ ํ  ์ ์๋ค.



 