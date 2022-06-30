# **Video Virtual Try-On Capstone Project**
## Maygan Miguez (*TU '22*) and Jaclyn Wilson (*TU '22*)
## Faculty Mentor: Dr. Allan Ding

Video Virtual Try-On is our two-semester-long, senior year final capstone project. This project implements a virtual try-on solution that takes in a user's video input, runs the ACGPN model on the extracted video frames, and outputs a virtual try-on video that mimics a real-time virtual clothing try-on. 

        
**ACGPN Cited:**

Yang_2020_CVPR   
Yang, Han and Zhang, Ruimao and Guo, Xiaobao and Liu, Wei and Zuo, Wangmeng and Luo, Ping, *Towards Photo-Realistic Virtual Try-On by Adaptively Generating-Preserving Image Content*, IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), June 2020.
       
## Project Goal       
Our project aims to add a video component to the virtual try-on image-to-image method. This software allows the user to preview an article of clothing on their body using a video component to mimic how the garment would look in real-time. 
         
Our approach to virtual try-on enables the user to virtually view the garment on their body instead of their picture, so they can have a closer experience to actually trying on clothes in a brick-and-mortar store. This solution improves the current work done using the Adaptive Content Generating and Preserving Network (ACGPN). The ACGPN has never been adapted to work with video input. 
        
## The ACGPN      
The ACGPN has three primary modules, including a semantic generation module (SGM), clothes warping module (CWM), and a content fusion module (CFM). The SGM uses semantic segmentation of the reference image to create the desired semantic layout after try-on. Next, the CWM warps the clothing images according to the generated semantic layout, and a second-order difference constraint is used in the warping process during training. Third, the CFM integrates all of the information, including the reference image, semantic layout, and warped clothes, to produce each semantic part of the body
        
## Our Approach
This virtual try-on problem can be broken down into two parts: 
* Taking in a video input of the person trying on model clothing
* Running the ACGPN model on the video input to mimic a real-time virtual clothing try-on experience in a reasonable amount of time. 
           
Our approach takes in video input from the user and outputs a video of the user wearing the target clothing. Because the ACGPN model runs on single images, we must break down the video input into frames and run the model on each frame of the video. After running the model on the video frames, we compile the new try-on images back into a new video as output.
           
## Conclusion
Overall, our project had some unexpected turns throughout the year which enabled us to learn more about the virtual clothing try-on problem and the potential solutions that could be implemented to solve it. Given the time constraint of two semesters, we were able to research more about deep learning techniques and determine a realistic solution that we could implement to address the problem. However, a lot improvements we would like to make to the video virtual try-on would take a lot more time and research than we had this year. Therefore, if we had more time and resources there are a few improvements we would implement and continue to work on.
            
Regarding the model, we would work on improving the run time and the model in general. Because it takes a substantial amount of time to run the model frame by frame, we would look into developing a parallel computing solution that could decrease the program’s runtime. Moreover, we would utilize 3-dimensional instead of 2-dimensional key points, so we could improve on the skin preservation component to recognize when body parts are not being displayed and deformed. We also would require a face detection implementation to help identify different angles given a 360-degree input. The model currently does not function well with hair in the way and various obstructions. 
              
            

https://user-images.githubusercontent.com/60798398/176746437-073dfa8a-ac73-4d3f-a33f-95135fbbe334.mp4

The video above shows an example of our video virtual try-on solution.   

### View our Video Virtual Try-On solution [here]()!
