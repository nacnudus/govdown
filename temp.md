---
title: "GOV.UK-style R Markdown Document"
author: ""
date: ""
output:
  govdown::govuk_document:
    keep_md: yes
---

# govuk header xl *italic* {caption="govuk caption xl"}


```r
library(tidyverse)

mtcars %>%
  ggplot(aes(cyl, mpg)) +
  geom_point()
```

![](temp_files/figure-html/unnamed-chunk-1-1.png)

::: {.lead-para}
This is a lead paragraph that appears in larger text than the rest of the body
text of the page.

Using multiple lead paragraphs is discouraged.
:::

This is a normal paragraph in normal size.

::: {.small-para}
If you're bored with writing in big letter and normal letters, then you can
write small letters too.
:::

Body *italic* **bold** ***bold and italic***

[normal hyperlink](https://design-system.service.gov.uk).

[hyperlink that doesn't turn purple](https://design-system.service.gov.uk){.govuk-link--no-visited-state}.

Next paragraph.

* First bullet
  * Nested bullets are available but ...
  * ... they look terrible because the GOV.UK Design System doesn't really support
    them.
* Second bullet
* Third bullet

Lists without bullets aren't supported because I don't know how to, so you
have to write the html yourself

<ul class="govuk-list">
  <li>
    <a>Unbulleted item one</a>
  </li>
  <li>
    <a>Unbulleted item two</a>
  </li>
  <li>
    <a>Unbullted item three</a>
  </li>
</ul>

1. Numbered list item
1. Second numbered list item
1. Third numbered list item

The default section break `---` is the largest.  For other sizes use the raw
HTML because pandoc doesn't support classes for this element.

---

> United wishes and good will cannot overcome brute facts.  Truth is
> incontrovertible. Panic may resent it. Ignorance may deride it. Malice may
> distort it. But there it is.


## govuk header l *italic* {caption="govuk caption l"}

Body text.

### govuk header m *italic* {caption="govuk caption m"}

Body text.

#### govuk header s *italic* {caption="govuk caption s"}

Body text.  There is no small caption.
