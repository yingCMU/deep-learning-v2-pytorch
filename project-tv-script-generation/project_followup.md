## Questions
 1. label is 1, output is vocab_size, why it still works
This is because criterion=nn.CrossEntropyLoss(), This criterion combines nn.LogSoftmax() and nn.NLLLoss() in one single class.
And nn.NLLLoss() is expecting:
  ```
  Input: (N, C) where C = number of classes
  Target: (N) 
  ```
 https://pytorch.org/docs/master/generated/torch.nn.NLLLoss.html
 
2. why need to reshape LSTM output,
3. why get the last layer of output
