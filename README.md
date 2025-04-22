# Special-dracopelta
Re action

![buh](https://github.com/nicolasbaez/Special-dracopelta/blob/main/xp047.gif)
```javascript
setup = (_) => createCanvas((w = 500), w, WEBGL);
k = 0;
s = 66;
c = (x, y, z) => {
  stroke(255);
  noFill();
  push();
  translate(x, y, z);
  box(s);
  r = random(-4, 4);
  translate(r, r);
  sphere(4);
  pop();
};
draw = (_) => {
  rotateY(k);
  clear();
  for (i = -s; i <= s; i += s)
    for (j = -s; j <= s; j += s) for (l = -s; l <= s; l += s) c(i, j, l);
  if (k == 0) saveGif("xp047.gif", 628, { delay: 0, units: "frames" });
  k += 0.01;
};
