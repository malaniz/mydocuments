Styling
=======
This document will expose the points to figure out and decide how to style MUI custom
components. Because the components are based on material-ui library and the way to
style them is totally different that what we want, css-modules or a css based solution.

Material-ui (MUI)
-----------------
MUI is the library from Google Inc used to develop our own components
and the documentation for them. That's because we're studying how they solve
the styling and why they choose the JSS approach.

Actually, MUI choose differents paths based in its version.
1. **LESS Modules**. The older versions use a scss based solution. But because
their Design Material Guidelines, it wasn't a good option, it was very limited
to have all the features that they need.
2. **Inline Styles**. The actual _stable_ version is based on a inline style
and at the end they said that because the effort to maintain and to customize
it, it's still a bad solution.
3. **JSS or CSS in JSS**. The @next version (almost the stable one). Use this
solution. If you want to know why they make this, you can see [this repo](https://github.com/oliviertassinari/a-journey-toward-better-style)
or [this presentation](https://oliviertassinari.github.io/a-journey-toward-better-style/#/?_k=k15l78)

Our library is based on the @next version.

The problem
===========
The MUI library has some features as **theme nesting** and **dynamic styles**
that can only be can be used with JSS in our code. They specifically says this:

> Material-UI aims to provide strong foundations for building dynamic UIs. For
> the sake of simplicity we expose our internal styling solution to users. You
> can use it, but you don't have to. This styling solution is interoperable with
> other solutions like PostCSS, CSS modules, or styled-components.

But When you think about it, you can always use css with !important flag on it to
override the rules applied in one HTML component and then use CSS modules or
whatever solutions there are out there. The big problem with it, is:

> Material has so many behaviours for each components that you'll need to
> customize too many css rules

Take a look on the guidelines for colors and how they implement every color on
themes. If you want to follow the guidelines, you'll need to define a color palette.
And for each palette you'll need to define hue and shades.
[Check the color system here](https://material.io/guidelines/style/color.html#color-color-system) and they
even have a [tool](https://material.io/color/#!/?view.left=0&view.right=0) to
ensure your palette color meets accessibility standards, with sufficient
contrast between elements.

Summarizing, JSS in MUI is a good solution for themes and to make exactly what
they need to customize its components in a maintainable and performant way.
It can be used with another styling techniques but at the end you'll need to
customize the MUI components with JSS and maybe your layouts or html elements
or macro components with the other approach. If you don't make this, you'll
break a lot of new features that will come with the @next version.

Possible solution
=================
Right now, I just figure out 2 ways to make it:

1. A complete theme for material-UI following the MUI guidelines and customize
not MUI things with css-modules or another css based technique.

2. A totally JSS based solution. Maybe using dot jss files to make the styling
object there and simulating something like JSS modules.


| Point | Option 1 | Option 2 |
| ----- |:--------:|:--------:|
| Over Engineering | YES | NO |
| Good Performance on DEV | NO | YES |
| Optimized for production | YES | YES |
| Themeable | NO | YES |
|  | NO | YES |




