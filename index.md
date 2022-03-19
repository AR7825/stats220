## WELCOME
This is the meme I made using Rstudio and Magick 

### _Zuko Meme_
![my_meme](https://user-images.githubusercontent.com/101862073/159107727-a393b7cd-1f49-411a-90e5-5b63aad81358.png)



## Source Code of Meme 

``` 
library(magick)
# square one
url<-("https://i.pinimg.com/564x/f2/26/5e/f2265ee4310af731a033e5323c130aaa.jpg")
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
zuko_after <-image_read ("https://static.wikia.nocookie.net/avatar/images/c/ce/Complete_Team_Avatar_group_hug.png/revision/latest/scale-to-width-down/333?cb=20120723100718") %>% 
  image_scale(500)


# square four
zuko_aftertext <- image_blank (width = 500, 
                               height = 380,
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


