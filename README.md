# MasterGraduateResearch
Study on Feeling Analysis based on House-Tree-Person Drawing Test with Deep Learning.   

## Quickly understanding
In this research, we aimed to analyze human feeling information with a new, interesting method. Actually, the existing method has been tested that they could be effectively used to detect human feeling information. But there are still some limitations that questions in those methods are a little privacy and could let test takers feel pressure to join test. So we want to propose a interesting method so that to overcome the psychological pressure and praise to get true feeling information.  

##  Research Process  
### Conduct a psychological experiment.   
We used a Chinese online system called [Wen JuanXing online system](https://www.wjx.cn)  to conduct this experiment.      
The contents including three sections:    
Basic information   
LSNS-6 questions    
House-Tree-Person Drawing Test      
![Test Contents](https://github.com/xiaoyiyi123/MasterGraduateResearch/blob/main/image/contents.png)        
After serveral weeks, we collected the test data and all the data are stored as an excel file.      
There are four sections: the first column is the answers of basic information, the second column is answers of LSNS-6 qeustions, the thrid column is the answers of HTP images here all those images are stored as url as a results of online address, and the last is the scores of LSNS-6 scale.
![Test data](https://github.com/xiaoyiyi123/MasterGraduateResearch/blob/main/image/data.png) 

### Process and Analyze the collect data.       
Firstly, remove useless data. Here useless data means the data missing meaningful HTP images. After that we got a total 74 useful data.     
Then, based on the scores of the LSNS-6 scale, we classified those HTP images into two groups. The HTP image with the score below 12 was put into the high social isolation risk group otherwise it was put into the low social isolation risk group.       
Next, we analyzed these two groups' images to find the similarities and differences and also refered to the related research about Huse-Tree-Person drawing test and finally we identified a set of socialty related features. And use these features as analyze pionts to analyze whether this guy are from social isolation risk or not.      
![Identified Features](https://github.com/xiaoyiyi123/MasterGraduateResearch/blob/main/image/Identified%20Features.png) 
    
### Use Object Detection Technique to Detect the identified features from HTP images

#### Train Object Detection model       
First we use the code shown in the folder as "object detection model.ipynb" [object detection model.ipynb](https://github.com/xiaoyiyi123/MasterGraduateResearch/blob/main/source%20code/object%20detection%20model.ipynb)to train the object detection mode through google colab.     
If you are not farmilar with how to train with google colab, you can click the following link to take as a reference.       
[Explaination on how to use google colab to train your Object detection model with your own dataset](https://www.youtube.com/watch?v=hTCmL3S4Obw)       
But if you don't want to train model again you can directly download my pre-trained weight file through [Pre-trained weight file](https://drive.google.com/file/d/1q7LUdfVVtwVgbnEE3HjgpiG9-HAc29XS/view?usp=sharing) then directly use it for detection part.      
Next, after got pre-trained weight file, you can take the code called ['Test.ipynb'](https://github.com/xiaoyiyi123/MasterGraduateResearch/blob/main/source%20code/Test.ipynb) to detect the object from HTP images.        
At the end of this step, you can calculate the scores of collected HTP images.
In my situation, I collected 74 useful data and the average score of HTP is calculated as 8.9. So here we assumed that the images with the score below 8.9 as high risk otherwise no risk.
[test results](https://github.com/xiaoyiyi123/MasterGraduateResearch/blob/main/data/testResultsAnalysis.xlsx)

### Analysis wether our assumption and classification results are reliable or not       
Do a stastical analysis through SPSS, you can download this software through [SPSS download address](https://www.ibm.com/analytics/spss-statistics-software). But it's only free for one month, I recomend you put the analysis step at the very end step after you got everything.     
If you are not farmilar with how to use SPSS you can click here [How to use SPSS to analyze data ](https://www.youtube.com/watch?v=Bku1p481z80) to learn how to use it.     

That's all the approach of my research.     
If you continue to do this research, you continue to collect more data, the more HTP images you collected, the results may be a little be difference. Since everyone draw in a different way.       
Final note: If you get more HTP images, you need to learn [Interpretation of HTP images](https://drive.google.com/file/d/1KpBB5WLclmdTfJ4GHTB8bD9d9g1bDxBU/view?usp=sharing), to check whether there is any other thing can be used to detect social isolation situation.






















     

