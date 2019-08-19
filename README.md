d = 1;
a= new Promise(res => setTimeout(() => res(1), 1000));
b= new Promise(res => setTimeout(() => res(2 + d), 999));


async function c() {
  await a;
  d = 2;
  console.log(await b);
}

c();

1. How to make console 4 ? Without changing timeout time and initial d value ?
2. If 
