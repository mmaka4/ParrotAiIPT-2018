#  ParrotAiIPT-2018: Week 3 Progress Report
Hello guys. Today I would like to share with you things I have captured up for this week(3rd week).

For what I have discovered, if you have your problem and you would like to solve that by programming, it is better to get to know it’s theory before starting implementation. By doing so you will broad your understanding of that problem in deep and how to tackle it.
In my case I had a problem of how to extract text from an image, I had no idea how that is done so I decided to learn the theory behind of what is going on from when you input an image up to the final output of extracted text from that image. And the following is the brief of steps take place during Text extraction.

  ### IMAGE TO TEXT EXTRACTION STEPS 
1. Text detection

     To detect text from an image you may use character region methods or Sliding window methods.
   Example of character region methods are Stroke Width Transform (SWT), Extremal Region (Ers), Maximally Stable Extremal Regions (MSERs)/ substet of ERs.

     For sliding window features are extracted from an image such as Haar-like features, Histogram of Oriented Gradients (HOG) features which are used in character detection.

2. Localise/get location grids of that text after detecting it from the image. Such as by Hough lines detector.

3. Extracting/recognize those Text Regions.

	#### Character based recognition
    i) You may use SVM classifier to classify character regions, typographical model for disambiguate uppercase and lowercase characters then pairwise letter-based language model to choose the most probable recognized word estimate.\
    ii) You may use graphical model with unary terms from character classifiers acting on HOG features and hence pairwise terms incorporating spatial layout and scale similarity between neighbouring characters. This is done in the context of a lexicon, the lexicon word with the highest score is then taken as final recognition result.\
    iii) Also CNN(Convolutional Neural Network) is suitable for character recognition

    ####	Word Based Recognition
    i) You may use Fishers vactor to detect whole word instead of character\
    ii) RNN(Recurrent Neural Network) is suitable for recognizing multiple words.
    
    That's all I have covered on Image to Text extraction/recognition.
    
    ### END-TO-END LEARNING
    I also pass through this staff which it is also important to know. As we know some learning systems require multiple stages of processing. But end-to-end learning, the system instead takes all those multiple stages and replaces them with just a single neural network.

    It’s advantage:
    * Reduce complexity/less components needed
    * Fast processing

    It’s disadvantages:
    * For it to work well require lot of data.

    ### HOW TO LAYOUT AND MANAGE YOUR MACHINE LEARNING PROJECT
    And at last on weekend i have learned on how to arrange my Machine Learning project such as to structure files of my project to be cool. And it is as follows:
    * Data Directory\
      For keeping your scripts to download or generate data.
    * Figures Directory\
      For storing all generated graphics and figures to be used in reporting.
    * Logs\
      For keeping scores of your project, and any automatic logging.
    * Model Directory\
      Contain scripts for training your model(s) and then use trained model to make predictions.
    * Notebook Directory\
      This is where you keep your notebook of your whole project, it is for teaching purpose and helps one to understand your project easily by reading the notebook.
    * Results Directory\
      This is where you store your results obtained from your project/ after running your project.
    * Source/src Directory\
      Now this is place where you keep your source codes for processing your main project, also statistical analysis scripts can be kept here.
     
     
     Alright thank you for your attention, i hope this document will help you on your ML projects, let's wait for the next week and see what I have prepared for you.
