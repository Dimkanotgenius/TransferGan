# TransferGan
Style Transfer using vgg16
Open this code on Kaggle.
Init labraries
install aiogram
Download labraries for work with aiogram and paste your token, which you got from BotFather
After that you will see block with ContentLoss, StyleLoss and Normalization. Init them.
Next Block is class TransferModel
                             args:content_layers - here you paste layers, where model will be calculate Content Loss.
                                    style_layers - here you paste layers, where model will be calculate Style Loss.
                                       num_steps - how many epoches you need  for train
                                  content_weight - factor how much content loss you want take from pictures
                                    style_weight - factor how much style loss you want take from pictures
In "forward" I give path, where you downloaded style_picture and content_picture(to this moment in handler you already has downloaded it), and image size, which you want
In the method get_photos model gets content image and style image, and transform them to Tensor

After this class you run code of bot (where you will see handlers)
The first handler greet and ask user to download the content image
The second handler ask user to download the style image
In the third handler model get images(path to this images and transform them to Tensor type) and return the 'result' tensor.After that, handler transform to PIL image
                                                                                                                                         and send this image to user.
        
                                                                                                                                        

