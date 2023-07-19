# AI LLM `Transformer` Model
- Widely used in AI applications such as Natural Language Processing (NLP), Computer Vision (CV), etc.
- Enormous computation workload becomes an obstacle to train large transformer models efficiently.
    - **Command**: `train(model, data, optimizer)`
- Some methods focus on reducing the computation workload during the training by skipping some layers.
    - **Command**: `skip_layers(model, layers_to_skip)`

## Sensitivity-Based Layer Dropping (SBLD)
- A novel method to accelerate training.
- Uses layer-wise sensitivity data to switch on/off transformer layers in proper order to keep high accuracy.
    - **Command**: `sbld(model, sensitivity_data)`
- Adjusts the probability of skipping transformer layers with a scheduler to accelerate training speed and get faster convergence.
    - **Command**: `adjust_probability(model, scheduler)`
- Can decrease end-to-end training time by 19.67% during training of GPT-3 Medium model, the same time increasing the accuracy by 1.65% w.r.t. baseline.

### Layer-Wise Sensitivity
- Every layer in the model has different impact on the overall model convergence.
- Layer-wise sensitivity can describe the importance of each layer more accurately.
    - **Command**: `calculate_sensitivity(model, layer)`

### Block/Allow Lists
- Further improve model accuracy by avoiding dropping the most sensitive layers.
- Layers are sorted with sensitivity value and put into Block/Allow lists.
    - **Command**: `create_block_allow_lists(sensitivity_data)`

### Variance-Based Scheduler
- Considers the training iteration as another factor when searching the optimal keep probability.
- Uses Poly-Weighted Exponential Gamma Distribution (PWEGD) to fit the change curve of variance between baseline and layer dropping over training time.
    - **Command**: `create_variance_based_scheduler(training_data)`

### Update Keep Probability
- Combines the base layer-wise sensitivity and the optimal keep probability of the whole model for each training iteration to get the keep probability list.
    - **Command**: `update_keep_probability(sensitivity_data, optimal_keep_probability)`

# Experiments
- SBLD method outperforms existing methods on various Transformer models.
- Improves training throughput and model accuracy.
- Can be used for pre-training and fine-tuning of all transformer-based models such as language transformers, vision transformers and other transformers.

# The comparison between Transformer, RNN, CNN, and Attention:

- "Deep learning model-transformer based wind power forecasting approach" by Sheng Huang, Chang Yan, Yinpeng Qu. This paper discusses the use of Transformer, a neural network architecture based on the attention mechanism, in wind power forecasting. It highlights the differences between Transformer and other deep learning models such as CNN and RNN1.

- "Intelligent Tool-Wear Prediction Based on Informer Encoder and Bi-Directional Long Short-Term Memory" by Xingang Xie, Min Huang, Yue Liu, Qi An. This paper introduces a new deep learning network, the IE-Bi-LSTM, based on an informer encoder and bi-directional long short-term memory. It discusses how this model can achieve remote feature extraction and the parallel computation of long-sequence-dependent features, different from methods using CNN and RNN2.

- "Modern Approaches in Natural Language Processing" by T. Quan. This paper provides a roadmap of modern approaches in NLP, including their ideas, theories, and applications. It discusses the evolution of NLP models from Word Embedding techniques to attention-enhanced BiLSTM, Transformer, and BERT3.

- "ConvRNN-T: Convolutional Augmented Recurrent Neural Network Transducers for Streaming Speech Recognition" by Martin H. Radfar, Rohit Barnwal, R. Swaminathan, Feng-Ju Chang, Grant P. Strimel, Nathan Susanj, A. Mouchtaris. This paper introduces a new streaming ASR model, ConvRNN-T, which augments the LSTM-based RNN-T with a novel convolutional frontend. It shows that ConvRNN-T outperforms RNN-T, Conformer, and ContextNet4.
