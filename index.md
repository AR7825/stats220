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
My motivation behind the meme was the fact that my skills of making a meme and the meme itself were being assessed thus I wanted to create a meme where I could show off the skills I learnt and create a meme that resounded with me. So you might be wondering what inspired me to make such an _interesting_ meme. I have always loved the show **Avatar the Last Airbender** and the redemtion arc and drastic change in the apperence of **Zuko** who is a character on the show.  

## How my meme is new/original 
- My meme is mostly orignal but uses the same format as the [**If you don't like me at my/then you don't deserve me at my meme**](https://knowyourmeme.com/memes/if-you-cant-handle-me-at-my-worst). 
- I added **Avatar the Last Airbender** pictures to add a touch of my own flair 😂 to this meme. 
- I added an orignal touch to the meme as I flipped the words and pictures so they'd be laying on the side as it's easier to read and understand. 
- I added a black background colour and white text for the words to pop out more
- If you want to create a meme like I have, download R-studio to your desktop using this website https://www.rstudio.com/products/rstudio/download/. 

## Image Sources
- https://www.pinterest.nz/pin/220465344248683770/ 
- https://avatar.fandom.com/wiki/Fanon:Reunion_(Story) 

## Other Avatar memes and If you don't like me at my/then you don't deserve me at my, memes used for inspo
![image](https://user-images.githubusercontent.com/101862073/159097042-46048319-32b7-4a51-9e44-b1fd6f7e5729.png)
![image](https://user-images.githubusercontent.com/101862073/159097064-e3a760d8-0111-484c-8425-4692e33c5ad2.png)


