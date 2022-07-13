# TransferGan
Style Transfer using vgg16<br />
<br />
Open this code on Kaggle.<br />
Init labraries <br />
install aiogram <br />
![image](https://user-images.githubusercontent.com/109117419/178713057-ffe33423-cf29-4e91-9240-8639ff59aa3f.png)


Download labraries for work with aiogram and paste your token, which you got from BotFather  <br />

![image](https://user-images.githubusercontent.com/109117419/178716233-394a789f-5e78-4911-9b4e-ec9cdfa3f559.png)

<br />
<br />
After that you will see block with ContentLoss, StyleLoss and Normalization. Init them.     <br />

![image](https://user-images.githubusercontent.com/109117419/178716477-84d41ee7-3485-4b6e-a6c5-3ce9efc8e890.png)

 <br />
 <br />
 <br />
Next Block is class TransferModel <br />

                       args: <br /> - content_layers - here you paste layers, where model will be calculate Content Loss. <br />
                                    - style_layers - here you paste layers, where model will be calculate Style Loss. <br />
                                    -   num_steps - how many epoches you need  for train <br />
                                    - content_weight - factor how much content loss you want take from pictures <br />
                                    - style_weight - factor how much style loss you want take from pictures <br />
In "forward" I give path, where you downloaded style_picture and content_picture(to this moment in handler you already has downloaded it), and image size, which you want <br />
In the method get_photos model gets content image and style image, and transform them to Tensor
![image](https://user-images.githubusercontent.com/109117419/178716802-4d076e39-c58b-42c5-94fd-c0c6d50ad881.png)


<br />
<br />
<br />
-------------------------------------------------------------------------------------------
After this class you run code of bot (where you will see handlers) <br />

<br />

The first handler greet and ask user to download the content image <br />
![image](https://user-images.githubusercontent.com/109117419/178718805-0678eb25-48b9-4b50-976f-9011391aecfe.png)
<br />
<br />
-------------------------------------------------------------------------------------------
The second handler ask user to download the style image <br />

![image](https://user-images.githubusercontent.com/109117419/178719548-7dde7044-d8c6-46cd-8203-8ab04d85797e.png)
<br />
<br />
-------------------------------------------------------------------------------------------

In the third handler model get images(path to this images and transform them to Tensor type) and return the 'result' tensor.After that, handler transform to PIL image
                                                                                                                                         and send this image to user.  <br />
![image](https://user-images.githubusercontent.com/109117419/178721314-12314508-c19c-42ba-814c-c31fd7b82231.png)

<br />
And registrate handlers <br />

![image](https://user-images.githubusercontent.com/109117419/178721737-f5606faa-9e3d-4a20-b3be-4ae0c787c667.png)


        
                                                                                                                                        



