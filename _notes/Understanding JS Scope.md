---
title: Understanding JS Scope
---

While digging into JavaScript's fundamental, I found that one of the things I can't really explain is "scope".

I once read (I believe it's Feynmann's word) that if you can explain something in 'simple' words, it means that you don't really understand it.

---

So, the journey begans from "What's scope do?".

Scope helps us to look for variables. This statement seems not really helpful....... until I started to read someone code.

Let's say, I have this block

```javascript
let name = 'Dwi';

function sayHi() {
	let name = "Ibe";
	alert(`Hi ${name}!`);
}
```

The very first question that may occure is, "".