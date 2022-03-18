## WELCOME
This is the meme I made using Rstudio and Magick 

### _Zuko Meme_
![meme](https://user-images.githubusercontent.com/101862073/158961509-730164f8-adbd-4845-a240-87588e7e6cb8.png)


## Source Code of Meme 

``` 
library(magick)
# square one
url<-("https://user-images.githubusercontent.com/101681189/158502553-099745f1-9e1c-4872-ba6d-eb01d3b140bb.png")
zuko_before <-image_read(url) %>%
  image_scale(500)

# square two
zuko_beforetext <- image_blank(width = 500, 
                               height = 400, 
                               color= "black") %>% 
  image_annotate(text = "If you don't\nlove me at my",
                 color= "#FFFFFF",
                 size = 50,
                 font= "Impact",
                 location = "+100+100") 

# square three
zuko_after <-image_read ("https://user-images.githubusercontent.com/101681189/158505782-7d42a714-ac7d-41d9-9b1d-a9d332c8a4c2.jpeg") %>% 
  image_scale(500)


# square four
zuko_aftertext <- image_blank (width = 500, 
                               height = 350,
                               color = "black") %>% 
  image_annotate(text = "Then you don't\ndeserve me at my",
                 color = "#FFFFFF", 
                 size = 50,
                 font = "Impact", 
                 location = "+100+100")

# making each row
zuko_vector <- c(zuko_beforetext, zuko_before)
top_row <- image_append(zuko_vector)

# making bottom row
bottom_row <- image_append(c(zuko_aftertext, zuko_after))


# using another approach
my_meme <- c(top_row, bottom_row) %>%
  image_append(stack = TRUE) %>%
  image_scale(800)
image_write(my_meme, path = "meme.png", format = "png")
my_meme 
```



## Motivation Behind the Meme 
So you might be wondering what inspired me to make such an _interesting_ meme. I have always loved the show **Avatar the Last Airbender** and the redemtion 
arc and drastic change in the apperence of **Zuko** who is a character on the show. 

## How my meme is new/original 


## Image Sources

