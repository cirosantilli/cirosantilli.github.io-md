# Principal component analysis

↑ **Parent:** [Dimensionality reduction](dimensionality-reduction.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Principal_component_analysis)

Given a bunch of points in $n$ dimensions, PCA maps those points to a new $p$ dimensional space with $p \le n$.

$p$ is a [hyperparameter](hyperparameter.md), $p=1$ and $p=2$ are common choices when doing dataset exploration, as they can be easily visualized on a planar plot.

The mapping is done by projecting all points to a $p$ dimensional [hyperplane](hyperplane.md). PCA is an algorithm for choosing this hyperplane and the coordinate system within this hyperplane.

The hyperplane choice is done as follows:
- the [hyperplane](hyperplane.md) will have origin at the [mean](arithmetic-mean.md) point
- the first axis is picked along the direction of greatest [variance](variance.md), i.e. where points are the most spread out.

  Intuitively, if we pick an axis of small variation, that would be bad, because all the points are very close to one another on that axis, so it doesn't contain as much information that helps us differentiate the points.
- then we pick a second axis, orthogonal to the first one, and on the direction of second largest variance
- and so on until $p$ orthogonal axes are taken

[https://www.sartorius.com/en/knowledge/science-snippets/what-is-principal-component-analysis-pca-and-how-it-is-used-507186](https://www.sartorius.com/en/knowledge/science-snippets/what-is-principal-component-analysis-pca-and-how-it-is-used-507186) provides an OK-ish example with a concrete context. In there, each point is a country, and the input data is the consumption of different kinds of foods per year, e.g.:
- flour
- dry codfish
- olive oil
- sausage
so in this example, we would have input points in 4D.

The question is then: we want to be able to identify the country by what they eat.

Suppose that every country consumes the same amount of flour every year. Then, that number doesn't tell us much about which country each point represents (has the least [variance](variance.md)), and the first PCA axes would basically never point anywhere near that direction.

Another cool thing is that PCA seems to automatically account for linear dependencies in the data, so it skips selecting highly correlated axes multiple times. For example, suppose that dry codfish and olive oil consumption are very high in Portugal and Spain, but very low in Germany and Poland. Therefore, the variation is very high in those two parameters, and contains a lot of information.

However, suppose that dry codfish consumption is also directly proportional to olive oil consumption. Because of this, it would be kind of wasteful if we selected:
- dry codfish as the first axis
- olive oil as the second axis
since the information about codfish already tells us the olive oil. PCA apparently recognizes this, and instead picks the first axis at a 45 degree angle to both dry codfish and olive oil, and then moves on to something else for the second axis.

We can see that much like the rest of [machine learning](machine-learning-split.md), PCA can [be seen as a form of compression](machine-learning-as-a-form-of-data-compression.md).

## ↑ Ancestors (7)

1. [Dimensionality reduction](dimensionality-reduction.md)
2. [Machine learning](machine-learning-split.md)
3. [Computer](computer-split.md)
4. [Information technology](information-technology.md)
5. [Area of technology](area-of-technology.md)
6. [Technology](technology-split.md)
7. [Ciro Santilli's Homepage](split.md)
