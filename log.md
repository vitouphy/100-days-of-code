# 100 Days Of Code - Log

### Day 0: June  28, 2020 

**Today's Progress**: Load "Topical Chat" dataset with dataloader for building a chatbot.

**Thoughts:** With Dataset and Dataloader package, it makes batching and shuffle a lot easier.

**Link to work:** [Chatbot Project](https://github.com/vitouphy/conv_agent)


### Day 1: June  29, 2020 

**Today's Progress**: Using PyTorch Vocab to get index for each token and start implementing GRU-based Seq2Seq

**Thoughts:** Using PyTorch Lightning framework with Seq2Seq is somewhat confusing just to consider which is to ouput from `forward` function.

**Link to work:** [Chatbot Project](https://github.com/vitouphy/conv_agent)


### Day 2: June  30, 2020 

**Today's Progress**: Implementing a simple GRU-based Seq2Seq with Greedy Decoding

**Thoughts:** Using `traning_step` instead of function `forward` makes things a lot easier.

**Link to work:** [Chatbot Project](https://github.com/vitouphy/conv_agent)


### Day 3: July  03, 2020 

**Today's Progress**: Implemented greedy and random sampling decoding

**Thoughts:** Does random sampling technique really work? Hmmmmmmmmm....


### Day 4: July  04, 2020 

**Today's Progress**: Implemented BeamSearch and n-Layers Bidrectional GRU (Seq2Seq)

**Thoughts:** It seems like beam-search tends to prefer short and generic response...

**Link to work:** [Chatbot Project](https://github.com/vitouphy/conv_agent)

### Day 5: July 05: 2020

**Today's Progress**: Implemented nucleus sampling

**Thoughts:** that concept of nucleus is pretty simple; yet seems to be quite robust.

**Link to work:** [Chatbot Project](https://github.com/vitouphy/conv_agent)


### Day 6: July 06: 2020

**Today's Progress**: Summary of the decoding strategies into a blog

**Thoughts:** Implementing is one thing, but putting them into words is another thing.

**Link to work:** Waiting to be approved [Toward DataScience](https://) 


### Day 7: July 07: 2020

**Today's Progress**: Refactor the code.

**Thoughts:** So far the code was done only in Jupyter Notebook, for simplicity. Now it is converted into many components.

**Link to work:** [Chatbot Project](https://github.com/vitouphy/conv_agent)


### Day 8: July 08: 2020

**Today's Progress**: Refactor the code further.

**Thoughts:** Using PyTorching Lightning to help with the process. It was easy to use. One confusing point is when the Lightning saves params passed to the model (including `vocab_path`); then, when loading its checkpoint, it uses the values from the checkpoint and it is hard to change that. 

**Link to work:** [Chatbot Project](https://github.com/vitouphy/conv_agent)

### Day 9: July 09: 2020

**Today's Progress**: Build a project to visualize each decoding strategy behaviour using VueJS.

**Thoughts:** So far, it's been fun. VueJS makes things easier; ChartJS adds interactive flavor on top of it. 

**Link to work:** [Decoding Visualizer Project](https://github.com/vitouphy/decoding_visualizer)


### Day 10: July 10: 2020

**Today's Progress**: Take a side quest, and learn to generate 🐕 images using GAN.

**Thoughts:** GAN takes a lot of time to training. Training for 200 epochs getting the following results. Also, Jupyter notebook on Kaggle, frequently, gets a timeout due to inactivity (I was waiting for the training to end 😭).

**Link to work:** [GAN](https://github.com/vitouphy/learning-deep-learning/tree/master/GAN)


### Day 11: July 11: 2020

**Today's Progress**: After training GAN for 500 epochs, the result is not much of a different from 200 epochs. I realized the model also suffers from `mode collapse` which the model no longer takes into account of latent variable z. Try GAN with loss fuction `Wasserstein`. The model is being experimenting. We however try to apply this WGAN to MNIST dataset; it performs horribly. What went wrong. Hmmmmmmm 

**Thoughts:** GAN is really hard to train especially with the mode collapse. Next time, I am gonna try DCGAN. 

**Link to work:** [GAN](https://github.com/vitouphy/learning-deep-learning/tree/master/GAN)


### Day 12: July 13: 2020

**Today's Progress**: Implementing Deep-Convolutional GAN (it just means using Conv for both generator and discriminator). It is claimed to combat with mode collapse well.

**Thoughts:** I am not sure what's going on here. After many epochs (30-ish), the generations are terrible. Maybe it needs more time?.

**Link to work:** [GAN](https://github.com/vitouphy/learning-deep-learning/tree/master/GAN)


### Day 13-15: July 15-17: 2020

**Today's Progress**: Tweaking, messing, breaking, ARRRGHHHHHHHH, but finally I got the GAN working.

**Thoughts:** Training GAN is painful. It's crazy. There is no way to know which setting works and which does not. Lots of hyper-parameter tuning. There is one interesting pattern though. The network does not train well if the discriminator is **too good** or **too bad**. When the discriminator is so good, generator has no chance to fool the discriminator. Thus, G only knows what is bad and has no idea on what is good. When D is **bad**, G can easily fool D with some weird pattern. 

**Things I found useful**:
- DCGAN can avoid `mode collapse` of GAN. 
- Use noise to add difficulty to discriminator and allow G to fool D from time to time
- Setting beta of Adam optimizer help 

**Link to work:** [GAN](https://github.com/vitouphy/learning-deep-learning/tree/master/GAN)

### Day 16: July 18: 2020

**Today's Progress**: I forgot to convert the output from [-1,1] to [0,1]. Now it's all better. Also implementing noise that reduces overtime.

**Thoughts:** GAN is tough to tweak. Different dataset might require different hyper-parameters.

**Things I found useful**:
- D loss should be around 0.7
- G loss should be > 1
- Do not forget to make sure the output is proper, or it's gonna be GG. 

**Link to work:** [GAN](https://github.com/vitouphy/learning-deep-learning/tree/master/GAN)

### Day 17: July 19: 2020

**Today's Progress**: Study the fundamental of CNN in detail on Coursera

**Things I found useful**:
- Classical CNN: Playing with convolution, padding, stride, and so on.
- ResNet: Using skip-connection (i.e. state at layer i is added to state at layer i+2) helps with deep network.
- InceptionNet: At each layer, 1x1, 3x3, 5x5, or pooling are used at the same time

### Day 18: July 20: 2020

**Today's Progress**: Study the further fundamental of CNN in detail on Coursera

**Things I found useful**:
- YOLO is roboust and fast.

### Day 19: July 29: 2020
**Today's Progress**: (i) Complete YOLO exercise on Coursera. (ii) Train GAN-based Text Generation with Gumbel Softmax.

**Things I found useful**:
- [YOLO] The idea of detecting the center of an object within a cell is very interesting.
- [GAN-Based] Currently, I notice that the mode collapse does not seem to affect much the training. However, the training is very inconsistent. The discriminator outperformsn generator very quickly

**Link to work:** [Chatbot Project](https://github.com/vitouphy/conv_agent)


