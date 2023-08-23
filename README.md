# Graphs-Homework

In this homework, you will explore a classification task using graphs, through an implementation of GraphSAGE, from [Inductive Representation Learning on Large Graphs](http://papers.nips.cc/paper/6703-inductive-representation-learning-on-large-graphs), on the Cora Dataset

## Part 1: Installation


## Part 2: Dataset exploration

In this homework, we will use the Cora dataset, a citation network consisting of 2708 scientific publications.

Give a brief statistical description of the dataset and answer the following questions.

**What do the nodes and edges represent? How many are there?**

**What features are used to describe each node?**

**Is the graph directed or undirected?**

**What is the task for this dataset? What metric is used to evaluate this task?**

Then, choose two datasets from the [Open Graph Benchmark](https://ogb.stanford.edu/) datasets that are used for a different task than the Cora dataset and give a brief description. 


### Installation:

To download the dataset, run:

wget https://linqs-data.soe.ucsc.edu/public/lbc/cora.tgz

This will download a .tgz file containing the relevant files. To unzip this file, run:

tar zxvf cora.tgz

Finally, you must specify the path to the dataset in the config.json file inside `src/`

## Part 3: Implementation

In this part, you will be implementing the GraphSAGE model for the defined task on the Cora dataset. For this purpose, you should initially dive into the code (all files) to get a general understanding of the model. The Cora dataset class is defined in the datasets/node_classification.py and the model implementation in the `src/` files. 

Based on the Cora dataset class, explain in your own words the difference between training a transductive and inductive model. What would you expect to give better results? 

Also, include in your report an explanation of the message passing algorithm that is implemented on the forward function in the model.py file. How are the messages being aggregated?  How many layers does the model initially have? 

To be able to run the code, you have to complete some missing lines of code in layers.py file. In this file, you will find the different aggregator architectures used in the original paper. You need to complete the mean aggregator and the pooling aggregator classes. Please only modify the code where you are asked to do so (#TODO).

Once the missing lines are completed, you are ready for the experimentation part!

## Part 4: Experimentation

To run the model with the default parameters, go to `src` and use the command: 

```python
python main.py
```

First, experiment with the aggregation arquitecture. You must run **4 experiments**, one for each of the available methods. Are your results as expected? Then, choose other tunable hyperparameters that you wish to explore and run at leat **6 extra experiments**. In the `src` directory, edit the `config.json` file to specify arguments and flags.

To have the complete points, you need to attach a table with all the experiments to your report. In addition, you should discuss how each of the hyperparameters that you modify affects the performance of the network.

## Part 5: 

Finally, you should choose the best model found in Part 4 and experiment with the number of layers in the model. You must perform at least 2 extra experiments. In the report attach the table with the results and discuss them.

# Report



