The **Euclidean distance** between two vectors, often denoted as \(\|x - c\|\), is a measure of the straight-line distance between the points represented by those vectors in a Euclidean space (also known as a real coordinate space).

For two vectors \(x\) and \(c\) in a Euclidean space of \(n\) dimensions, the Euclidean distance is calculated as follows:

$$K(x, x') = \exp(-\gamma ||x - x'||^2)$$

where x and x′ are input vectors, <br>
∣∣⋅∣∣ denotes the Euclidean distance between the vectors, <br>
γ is a hyperparameter that controls the width of the kernel. <br>
The γ parameter controls the width of the RBF kernel, while the C parameter controls the trade-off between maximizing the margin and minimizing the classification error.<br>

对于较小的γ值，决策边界过于简单，欠拟合数据；对于较大的γ值，决策边界过于复杂，过拟合数据(underfits)。<br>
同样的，对于较小得到C值，间隔过大，欠拟合数据；而对于较大的C值，间隔过小，过拟合数据。<br>
When γ is too small, the decision boundary is too simple and underfits the data. This means that the model is not able to capture all the relevant information in the data, leading to poor performance on both training and test sets. <br>
On the other hand, when γ is too large, the decision boundary becomes too complex and overfits the data. This means that the model has learned to fit to noise in the training set, leading to poor performance on test sets.<br>
Similarly, when C is too small, the margin is too large and underfits the data. This means that the model is not able to capture all relevant information in the data, leading to poor performance on both training and test sets. On the other hand, when C is too large, the margin is too small and overfits the data. This means that the model has learned to fit to noise in the training set, leading to poor performance on test sets. <br>

In other words, to compute the Euclidean distance, you take the square root of the sum of the squared differences between corresponding components of the two vectors. This calculation effectively measures the length of the straight line connecting the points represented by vectors \(x\) and \(c\).

In the context of the Radial Basis Function (RBF) equation:

\[
RBF(x, c) = \exp\left(-\frac{\|x - c\|^2}{2\sigma^2}\right)
\]

The Euclidean distance \(\|x - c\|\) represents how far the input vector \(x\) is from the center vector \(c\) in the high-dimensional space. The RBF assigns higher values when this distance is small (i.e., when \(x\) is close to \(c\)) and lower values when the distance is large (i.e., when \(x\) is far from \(c\)), as controlled by the spread parameter \(\sigma\).
