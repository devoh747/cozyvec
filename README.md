# cozyvec

cozyvec is a terminal program for creating [plotter](https://en.wikipedia.org/wiki/Plotter) art (specifically via svg files) with minimal setup.

The library has been designed for brevity, so the code for a specific plot can be tweeted under the hashtag [#cozyvec](https://twitter.com/hashtag/cozyvec) (much like PICO-8's [#tweetcart](https://twitter.com/hashtag/tweetcart) and processing's [#つぶやきProcessing](https://twitter.com/hashtag/つぶやきProcessing)) by providing shortcut versions of most tokens that are 1-4 characters.

## Browser Version

Browser version available at: https://brubsby.github.io/cozyvec

![Image](https://github.com/brubsby/cozyvec/blob/master/resources/web_example.png)

However, the Electron experience is more polished (menu items).

## Install & Run

If you wish to use cozyvec inside of [Electron](https://electronjs.org/), follow these steps:

```
git clone https://github.com/brubsby/cozyvec.git
cd cozyvec/desktop/
npm install
npm start
```

Cross-platform build downloads to come soon

## Library

- `l2|lineTo(x,y)` draw line from last point
- `m2|moveTo(x,y)` move to point
- `clsp|closePath()` draw line to last move to point
- `ppr|paper(name[,orientation])` change paper to size in library
- `ppr|paper(w,h[,name[,orientation]])` custom paper in mm
- `pen(w)` pen width in mm
- `mbox|marginBox([a[,b[,c[,d]]]])` create bounding box with margins [x1,y1,x2,y2] default 40 mm, partial arguments follow css margin conventions
- `err|error(s)` error and quit
- `W|WIDTH` canvas width
- `H|HEIGHT` canvas height
- `PI` π
- `TAU|TWO_PI` 2*π
- `HPI|HALF_PI` π/2
- `QPI|QUARTER_PI` π/4
- `pow(a,b)` exponentiation
- `sqrt(a)` square root
- `sqr|square(a)` square number
- `cub|cube(a)` cube number
- `abs(a)` absolute value
- `ceil(a)` round up to nearest integer
- `flr|floor(a)` round down to nearest integer
- `sgn|sign(a)` return the sign of a number
- `sin(a)` sine
- `cos(a)` cosine
- `tan(a)` tangent
- `asin(a)` arcsine
- `acos(a)` arccosine
- `atan(a)` arctangent
- `at2|atan2(y,x)` arctangent2
- `min(...a)` minimum
- `max(...a)` maximum
- `mid(a,b,c)` clamp b to [a,c]
- `smid|smoothMid(a,b,c)` clamp b to [a,c] with [smoothing](https://en.wikipedia.org/wiki/Smoothstep)
- `dst|distance(x1,y1,x2,y2)` distance between points
- `rnd|random()` random \[0-1)
- `rnd|random(a)` random \[0-a)
- `rnd|random(a,b)` random \[a-b)
- `srnd|seedRandom()` seed rng with 0
- `srnd|seedRandom(s)` seed rng with s
- `nse|noise(pos)` [simplex noise](https://en.wikipedia.org/wiki/Simplex_noise) (pos can be a number or 1-4 numbers in a list)
- `nse|noise(pos,freq,amp)` simplex noise
- `nse|noise(pos,freq,amp,octaves,lacunarity,gain)` fractal simplex noise
