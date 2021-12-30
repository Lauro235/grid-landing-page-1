# grid-landing-page-1
A futuristic landing page utilising grid, a custom svg and a downloaded font

## Resources

The following are excellent resources I found as I developed this mini project.

Freecodecamp grid projects for beginners - https://www.freecodecamp.org/news/learn-css-grid-by-building-5-layouts/
Use downloaded fonts - https://www.youtube.com/watch?v=QhhYZJFOZnY&ab_channel=CalerEdwards
Font property (w3 schools) - https://www.w3schools.com/cssref/pr_font_font.asp

## Correctly Targeting Hover and focus states

Ever wondered how you could correctly style elements on hover and focus? I did, but today I got a little bit closer to understanding how it works...

Imagine we have the following items and we want to apply styling to them on hover and when tabbed (in focus state)

```
            <ul class="nav-list">
                <li class="nav-item"><a href="#">About</a></li>
                <li class="nav-item"><a href="#">Gallery</a></li>
                <li class="nav-item"><a href="#">Blog</a></li>
                <li class="nav-item"><a href="#">Portfolio</a></li>
                <li class="nav-item"><a href="#">Contact</a></li>
            </ul>

            <ul class="widget-list">
                <li class="widget-item"><a href="#"><i class="fab fa-facebook"></i></a></li>
                <li class="widget-item"><a href="#"><i class="fab fa-instagram"></i></a></li>
                <li class="widget-item"><a href="#"><i class="fab fa-twitter"></i></a></li>
                <li class="widget-item"><a href="#"><i class="fab fa-github"></i></a></li>
                <li class="widget-item"><a href="#"><i class="fab fa-free-code-camp"></i></a></li>
            </ul>
```

**a:hover, a:focus,**

The CSS above will only cover the nav-item anchors, It won’t be enough to cover the widget-item anchors.

The reason is that the smallest child in this situation is not the anchor, but actually the <i> tag.

**i:hover**

The i:hover works well. Hooray! Nice and easy, now I can just say i:focus right? No, unfortunately not... However it’s still possible to apply focus state styles to the child of an anchor.

The final bit of code is…

a:focus>i

We indicate that when the anchor is on focus, it’s child element <i> will be styled.
