# BSc-Thesis-Project
#### A Deep Learning-Based Approach for Diagnosis of Schizophrenia using EEG brain recordings
### Datasets
A public dataset of SZ EEG recordings was utilized for this project <br>
[Dataset](http://brain.bio.msu.ru/eeg_schizophrenia.htm), a 16 channel EEG recording dataset of 84 individuals (45 Schizophernic, 39 Healthy Control) <br>
Dataset was divided into 5 second segments of 224x224 spectrogram images of EEG signal

### Methods
Two Neural Network architectures were used
#### Plain CNN VGG-16
A VGG-16 CNN architecture implemented in keras was utilized which obtained 96.3% accuracy on test data (100% on training data) <br>
each 5 second sepctrogram of size 224x224 was fed to this network as training data.
this method is based on the work of [Aslan, Akin](http://193.140.240.104/xmlui/handle/11468/7223)


#### Hybrid CNN-LSTM
This architecture consists of CNN followed by LSTM cells. inputs of the CNNs are spectrogram segments for one subject, which are fed to LSTM sequentially<br>
This method underperfomrs compared to the previous plain CNN method due to the lack of sufficient training data.<br>
<br>
<img src="https://github.com/mehrshad-sdtn/BSc-Thesis-Project/blob/master/resources/lstmcnn.jpg" width="400" height="290"/>

### Generative Data Augmentation
Deep Generative Techniques have been used in order to augment the spectrogram dataset and obtain better results.

##### DCGAN architecture
<img src="https://github.com/mehrshad-sdtn/BSc-Thesis-Project/blob/master/resources/dcgan.jpg" width="400" height="150"/>

##### Variational Autoencoder architecture
<img src="https://github.com/mehrshad-sdtn/BSc-Thesis-Project/blob/master/resources/vae.jpg" width="400" height="150"/>
The variational autoencoder achieved 0.5% accuracy improvement and 0.14 loss decrease.


