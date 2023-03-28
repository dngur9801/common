# 자주쓰이는 자바스크립트 함수 및 객체 모음

### 날짜 포맷 
```js
const getDateFormat = (date: string) => {
  const KOREA_TIME_ZONE = new Date(date).getTime() - 3240 * 10000;

  const YYYY_MM_DD_HH_MM_SS = new Date(date)
    .toISOString()
    .replace("T", " ")
    .replace(/\..*/, "");

  const YYYY_MM_DD = new Date(date).toISOString().split("T")[0];
  const HH_MM_SS = new Date(KOREA_TIME_ZONE).toTimeString().split(" ")[0];

  return { YYYY_MM_DD_HH_MM_SS, YYYY_MM_DD, HH_MM_SS };
};

```
