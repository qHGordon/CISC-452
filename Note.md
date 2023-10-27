The **Euclidean distance** between two vectors, often denoted as \|x - c\|, is a measure of the straight-line distance between the points represented by those vectors in a Euclidean space (also known as a real coordinate space).

For two vectors \(x\) and \(c\) in a Euclidean space of \(n\) dimensions, the Euclidean distance is calculated as follows:

\[
\|x - c\| = \sqrt{\sum_{i=1}^{n} (x_i - c_i)^2}
\]

Where:
- \(x_i\) and \(c_i\) are the components (coordinates) of vectors \(x\) and \(c\) in the \(i\)-th dimension.
- The summation runs from \(i = 1\) to \(n\), covering all dimensions.

In other words, to compute the Euclidean distance, you take the square root of the sum of the squared differences between corresponding components of the two vectors. This calculation effectively measures the length of the straight line connecting the points represented by vectors \(x\) and \(c\).

In the context of the Radial Basis Function (RBF) equation:

\[
RBF(x, c) = \exp\left(-\frac{\|x - c\|^2}{2\sigma^2}\right)
\]

The Euclidean distance \|x - c\| represents how far the input vector \(x\) is from the center vector \(c\) in the high-dimensional space. The RBF assigns higher values when this distance is small (i.e., when \(x\) is close to \(c\)) and lower values when the distance is large (i.e., when \(x\) is far from \(c\)), as controlled by the spread parameter \(\sigma\).
