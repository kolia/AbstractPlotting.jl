```@eval
using CairoMakie
CairoMakie.activate!()
```

# Box

A simple rectangle poly that is layoutable. This can be useful to make boxes for
facet plots or when a rectangular placeholder is needed.

```@example
using CairoMakie
using ColorSchemes

fig = Figure(resolution = (1200, 900))

rects = fig[1:4, 1:6] = [
    Box(fig, color = c)
    for c in get.(Ref(ColorSchemes.rainbow), (0:23) ./ 23)]

save("example_lrect.svg", fig); nothing # hide
```

![example lrect](example_lrect.svg)