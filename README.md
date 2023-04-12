# seq2seq_pytorch
learning pytorch by implementing seq2seq model

## 迭代版本:

### seq2seq_with_attention_tutorial.ipynb
参考pytorch seq2seq教程官方版本，https://pytorch.org/tutorials/intermediate/seq2seq_translation_tutorial.html 
但有改动：
- 在类AttDecoderGRU中改动了attention的计算方式，原来的计算方式有问题。

### seq2seq_with_attention_modify.ipynb
- 在前者的基础上，将encoder和decoder收归到Model类中，并定义了模型的forward，train_process，eval函数。
- train_process函数用于整个训练迭代过程，并在一定时间步之后调用eval函数计算test loss。
- 在train_process中调用self.train()，以及在eval中调用super.eval()，用于改变model的训练模式，即使这里并没有什么区别。
