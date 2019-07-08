# CSS Debug

## 引言

```
Someone: “What’s the best programming language?”
Donald Knuth: “Which one has the best debugger?”
 --- Donald Knuth(高德纳/唐纳德·尔文·克努斯) <<计算机程序设计艺术>>
```

## debugger

Don’t make the computer do what we don’t understand. I think there’s merit in this, but what I’m talking about here is revealing structure where it was otherwise invisible.
我明白不要让电脑干你不明白的事情,但这里我要揭示的是其它看不见的结构.

What can we do to see our website’s structure? Here are two solutions I’m aware of: we can make one-off CSS rules to emphasize(强调) an element, or we can use Chrome’s, Firefox’s, or Safari’s Debugger Tools. But that’s still more-or-less a one-off(一次性) solution. What we need is a general solution.

```css
* { outline: solid 0.25rem hsla(210, 100%, 100%, 0.5); }

// Yet the introduction of the * { … } was profound(意义深远) for me
* {
    color:                    hsla(210, 100%, 100%, 0.9) !important;
    background:               hsla(210, 100%,  50%, 0.5) !important;
    outline:    solid 0.25rem hsla(210, 100%, 100%, 0.5) !important;
}
// Much improved! Here we’ve created a schematic-like feel for our website
```

 I was careful to not use solid colors, but instead chose soft-colors or colors with an alpha channel so that nested elements appear deeper in color, with bluer blues and whiter whites. I also added !important because of the infamous(声名狼藉的) CSS [Specificity Wars](https://en.wikipedia.org/wiki/Cascading_style_sheets#specificity).

这个不太明白: What can sometimes feel like CSS screwing(拧紧/螺丝接合) with us is how and when the cascade(瀑布状) applies. That is, “How is it that styles are sometimes applied and sometimes not?”

This isn’t Schrodinger(薛定谔)'s CSS, it’s simple math. CSS uses a simple calculator to determine which rules are more specific, and the result determines whether or not CSS is applied.

###  !important

The mother of all specificity(特征) is !important, which overrides all inline, IDs, classes, and element rules.
It’s like the Death Star as compared to The Empire.
Despite(不管) the fact that the use of !important is discouraged in general, it’s perfect for a debugger — because we won’t ship our website with it “turned on.” Instead, we use the debugger just in the design and development of our website.

The more I used the debugger, the more I realized that using `*:not(path):noth(g)` as the selector was preferred(优先).
This way, I wouldn’t get extraneous(没有关联的) lines from vector graphics.
I also noticed that disabling box-shadow was cleaner, as the debugger doesn’t need a sense of depth(层次感).


### So, here’s the final debugger:
```css
*:not(path):not(g) {
    color:                    hsla(210, 100%, 100%, 0.9) !important;
    background:               hsla(210, 100%,  50%, 0.5) !important;
    outline:    solid 0.25rem hsla(210, 100%, 100%, 0.5) !important;
    box-shadow: none !important;
}
```

I think we humans hate what we don’t understand. And CSS is no exception. It’s mischaracterized(任意篡改) because it’s misunderstood. I propose: think of CSS as a double-edged sword. It can be used to both construct and deconstruct websites. Yes, CSS is not Photoshop, but that doesn’t mean it can’t do things that Photoshop can’t. Creating our own debugger is one thing we can do.

### How to use this debugger

+ 打开 https://zaydek.github.io/debug.css
+ 把 “Debug CSS” 拖到"书签页" ([source code here](https://gist.github.com/zaydek/6b2e55258734deabbd2b4a284321d6f6))
+ 打开要调试的页面,点击Debug css书签,就可以对当前网页进行调试了

## 引用

[Learn This One Weird 🙊 Trick To Debug CSS](https://medium.freecodecamp.org/heres-my-favorite-weird-trick-to-debug-css-88529aa5a6a3)






