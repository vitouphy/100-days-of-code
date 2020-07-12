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


