/ [Home](index.md)

# Learning Notes Template




```
1. For example, if your learning is about transformers, 
  the file should be in "transformers-usename.txt"

2. Each learning should be divided with this delimiter
    --------------------------------------/

3. Each learning shoud be like below:
  Title
  <Youtube_link or Article_link>
  
  1. Notes Line 1
  2. Notes Line 2
  3. Notes Line 3

```


### Sample learning notes:
```
Encoders and decoders
https://www.youtube.com/watch?v=0_4KEb08xrE

1. The encoder processes input words, creating numerical representations that capture 
sequence meaning.  These representations are then passed to the decoder, which 
generates an output sequence through an autoregressive process, predicting one word at a time.

2. A practical example is engilsh to french translation.The encoder understands 
the English sentence, and the decoder, using the feature vector, generates the corresponding French words.

3. The decoder continues generating words until a "stopping value" is encountered, 
indicating the completion of the sequence. The first word, denoting the start of 
the sequence, initiates the decoding process.

4. The encoder specializes in understanding the input sequence, while the decoder 
focuses on generating the output sequence. This architecture is versatile for 
various tasks like translation and summarization.

5. Users can choose specific encoders and decoders based on their proven 
effectiveness in handling specific tasks, providing adaptability and 
optimization for diverse applications.
```


