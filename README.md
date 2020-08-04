# The Effect of Visual Cues on Accuracy Estimation in Immersive Scatterplots

Supplementary Materials

**Abstract** Immersive visualization in virtual reality (VR) allows us to exploit visual cues for perception in 3D space, yet few existing studies have measured the effects of using visual cues in data visualization. Across a desktop monitor and a head-mounted display (HMD), we assessed scatterplot designs that vary their use of visual cues—motion, shading, perspective (graphical projection), and dimensionality—on visualizations of two different sets of data. We conducted a user study with a realistic task in which 32 participants estimated the classification accuracy of an artificial neural network from the scatterplots. We find that no variable alone explains all the variance in estimation error; however, using an HMD, allowing motion, or showing a more complicated dataset leads to longer response times. Motion generally reduces participants’ estimation error; besides motion, using other cues may increase participants’ estimation error. The results also indicate the complexity of combining different visual cues and applying them to different data properties. Using an HMD generally results in slightly larger estimation errors than using a desktop monitor; however, using certain combinations of visual cues, a VR HMD performs as well as a desktop monitor. In summary, via studying participants as they interpret the output from a complicated machine learning model, we advance our understanding of the effects of visual cues for immersive analytics.

## Visual-Cues-in-VR.mp4
   - a short video to illustrate the experimental conditions

## literature review.pdf
   - our literature review document
   
## data
   - `metas.csv` : participants' answers to the open-ended questions and demographics information
      -  **familiarML**: self-rated familiarity with machine learning
      -  **familiarDR**: self-rated familiarity with dimension reduction techniques
      -  **familiarVIS**: self-rated familiarity with data visualization
      -  **familiarVR**: self-rated familiarity with virtual reality
      -  **Session{1,2,3,4}Q{1,2}**: participants answers to the two open-ended questions at the end of each estimation session
      -  **PostDataFamilarity**: the answer to the post-experiment question: familiarity with the datasets
      -  **PostComments**: free comments
      -  **PostGlasses**: the answer to the post-experiment question: if pariticpants used glasses, etc.
      - **PostSickness**: the answer to the post-experiment question: if pariticpants felt sick in the experiment.
      -  **the remaining columns**: time stamps

   - `trials.csv`
      -  **SessionIndex**: which estimation session
      -  **SessionStart**,**SessionEnd**,**PracticeStart**,**PracticeEnd**,**MainStart**,**MainEnd**,**QuestionStart**,**QuestionEnd**: these are timestamps
      -  **TrialStatus**: main or practice
      -  **TrialIndex**
      -  **TrialStart**,**TrialVisualizationStart**,**TrialVisualizationEnd**,**TrialAnswerStart**,**TrialAnswerEnd**,**TrialFeedbackStart**,**TrialEnd**: timestamps for each trial, the response time is the differentce between **TrialAnswerStart** and **TrialVisualizationStart**
      -  **TrialAnswer**: participants' answer to this trial
      -  **TrialIntAccuracy**: the true accuracy, rounded 
      -  **TrialSolution**: the true accuracy in decimal numbers
      -  **TrialDataset**: cifar-10 or babi, which data model
      -  **FactorStereo**,**FactorMotion**,**FactorPerspective**,**FactorShading**,**Dim**: each cue
      -  **Step**,**BinIndex**,**BinLower**,**BinUpper**,**File**: the refering to which file to use

## analysis
   - the analysis scripts for the Bayesian inference (they may take 10 - 30 minutes to run)

## python
#### generating participants
   - the script to randomize experimental variables and generate participants
   
#### machine learning
   - the scripts to train the two neural networks (they may take a few hours to run)
   - the scripts to compute t-SNE projections (they may take a day to run)
   - all saved intermediate neural networks (checkpoints)
   - the images of the projections generated by Python to check convergence

## experiment
   - the experiment system code based on Qt, OpenGL, SteamVR, etc.
   

