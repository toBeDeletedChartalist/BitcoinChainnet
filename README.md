
<img src="https://user-images.githubusercontent.com/6023331/36913973-4c09184c-1e11-11e8-83a2-18dfc6b1b938.png" width="72" height="72"/> &nbsp;&nbsp;&nbsp;&nbsp;
<img src="https://user-images.githubusercontent.com/6023331/36926816-47501caa-1e3f-11e8-8fa8-bee5cdff3dfe.png" width="72" height="72"/>


# CoinWorks

If you would like to extract chainlets from Bitcoin, please set up and use this simple project: https://github.com/cakcora/BitcoinParser


<h3>3. Chainnet (IEEE ICDM 2019)</h3>
  <p>Using persistent homology based ideas, we offer an elegant, easily extendable and computationally light approach for graph representation learning on Blockchain networks to predict cryptocurrency prices.</p>

 <h3>2. <a href = "http://cakcora.github.io/blockchain/576.pdf">Forecasting Bitcoin Price with Graph Chainlets </a> (PAKDD 2018) </h3>
  <p>We introduce a novel concept of chainlets, or Bitcoin subgraphs, which allows us to evaluate the local topological structure of the Bitcoin graph over time.</p>

  <h3>1. <a href = "http://cakcora.github.io/blockchain/blockchainsurvey1_1.pdf">Blockchain: A Graph Primer</a></h3>
  <p>Aug 2017 Version 1.1</p>
  <p>We offer a holistic view on Blockchain. Starting with a brief history, we give the building blocks of Blockchain,
and explain their interactions. As graph mining has become a major part its analysis, we elaborate on graph theoretical
aspects of the Blockchain technology.</p>


## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See the prerequisites that you need to deploy this project to your environment.

### Prerequisites

What things you need to install the software and how to install them

```
Python 3.5
Tensorflow r1.1
```

### Installing

Please visit the given links to install required software to run CoinWork project.

```
Python Installation     : https://www.python.org/downloads/
Tensorflow Installation : https://www.tensorflow.org/install/
```

Anaconda is recommended to be used for installation of both python and tensorflow. Anaconda is an open source distribution of Python and it simplifies package management and deployment. Please visit https://anaconda.org/ for more information.

## Authors
 - Nazmiye Ceren ABAY
 - Cuneyt Gurcan AKCORA

## Project Structure
Here, our project is divided into two main parts as data files and source codes written in Java and Python.

### Processed Data Files
Our processed data spans from 2009 to 2018 in each file:
<ul>
  <li> <a href="/data/dailyOccmatrices2009-2018.rar">Chainlet occurrence matrices (1MB)</a>: Each data file contains the matrix of the day. The file occ2009003.csv gives a 20x20 matrix of chainlet occcurences for year 2009 and day 003.</li>
  <li><a href="/data/dailyAmoMatrices2009-2018.rar">Chainlet amount matrices: (3.8MB)</a>: Each data file contains the matrix of the day. The file amo2009003.csv gives a 20x20 matrix of chainlet amounts for year 2009 and day 003.</li>
  <li> <a href="/data/feature.txt">Graeve's feature values(3.8MB)</a>: Extracted daily features</li>
  <li> Betti numbers <a href="/data/betti_0(100).csv">0</a> and <a href="/data/betti_1(100).csv">1</a> </li>
  <li> <a href="/data/filteredDailyOccMatrices.rar">Filtered occurence matrices</a></li>
  <li> <a href="/data/pricedBitcoin2009-2018.csv">Bitcoin prices</a></li>
</ul>

### Raw Data Files

Other than the processed data files, we also have raw input and output edges of transactions. This data is divided into yearly and monthly files. Each year's data is zipped together and contains 12 input edge files and 12 output edge files of transactions that were mined in the blocks of that year/month. 

Each line in the input edge file is tab separated with the format:
```
Unix time of transaction\thash of transaction\thash of first input transaction\tindex of output from first input transaction\thash of second input transaction\tindex of output from second input transaction\t(additional inputs, if exist)\r\n
```

Each line in the output edge file is tab separated with the format:
```
Unix time of transaction\thash of transaction\thash of first output address\tamount of first output bitcoins\thash of second output address\tamount of second output bitcoins\t(additional outputs, if exist)\r\n
```

<img src="https://user-images.githubusercontent.com/6596905/38154759-80cbf57a-3439-11e8-8d84-9706e5825d5c.png" width="50%"/> 

Consider the Bitcoin graph in the figure above, where transactions and addresses are shown with rectangles and circles, respectively. This graph would be given in two files: inputsYear_Month.txt and outputsYear_Month.txt. Files would include these lines:

```
-- inputsYear_Month.txt
UnixTimeOft_1	HashOft_1	HashOft_x1	0	HashOft_x2	8
UnixTimeOft_2	HashOft_1	HashOft_x3	1	HashOft_x4	3	HashOft_x5	0
UnixTimeOft_3	HashOft_1	1
UnixTimeOft_4	HashOft_3	2	HashOft_2	0
```

```

-- outputsYear_Month.txt
UnixTimeOft_1	HashOft_1	HashOfa_6	10^8	HashOfa_7	0.8^0.8
UnixTimeOft_2	HashOft_2	HashOfa_8	3.8*10^8
UnixTimeOft_3	HashOft_3 HashOfa_9	0.2*10^8	HashOfa_10	0.2*10^8	HashOfa_11	0.3*10^8
UnixTimeOft_4	HashOft_4 HashOfa_12	3.7*10^8	HashOfa_13	0.3*10^8
```

<ul>
  <li> <a href="https://utdallas.box.com/s/73i8q4g59ceoum9scc4kkbhi4ritmueg">2009 data (0.1MB)</a></li>
  <li> <a href="https://utdallas.box.com/s/6g2li4ls8zk2wfnf3tsl3gsr713r4pms">2010 data (15MB)</a></li>
  <li> <a href="https://utdallas.box.com/s/bu30643q4l0a79b4907c2a51tx31s16a">2011 data (300MB)</a></li>
   <li> <a href="https://utdallas.box.com/s/vb60kxanb2yifq2yaozviu6nsojnzm1c">2012 data (1.2GB)</a></li> 
   <li> <a href="https://utdallas.box.com/s/t2w1dc4xbds377lfgxulzk44sr6fwj1t">2013 data (3.2GB)</a></li>
   <li> <a href="https://utdallas.box.com/s/xrh9bw8ctmy0kuvx24h6b8v53tdwi127">2014 data (5.2GB)</a></li>
   <li> <a href="https://utdallas.box.com/s/zl1n1wh1dqgcicj59qvd8cmas2iz936y">2015 data (9.6GB)</a></li>
   <li> <a href="https://utdallas.box.com/s/vuog5rneci364h4m6w5f8eursk2ym786">2016 inputs (8.1GB)</a></li>
   <li> <a href="https://utdallas.box.com/s/9wozbdip3yjkfxgnqkf6x3jww9v5rm3m">2016 outputs (8.5GB)</a></li>
   <li> <a href="https://utdallas.box.com/s/atscqz8cle50rc5abvbc4ct20qdqoyhi">2017 data until August (13.2GB)</a></li>
</ul>



Please send your data related questions to cuneyt.akcora AT utdallas DOT edu.

Please cite one of the following works when using this data:
```
@inproceedings{abay2018,
  title={ChainNet: Learning on Blockchain Graphs with Topological Features},
  author={Abay, Nazmiye Ceren and Akcora, Cuneyt Gurcan and Gel, Yulia R. and Islambekov, Umar D. and Kantarcioglu, Murat and Thuraisingham, Bhavani},
  booktitle={under submission},
  pages={1-9},
  year={2018},
  organization={ACM}
}
```

```
@inproceedings{akcora2018pakdd,
  title={Forecasting Bitcoin Price with Graph Chainlets},
  author={Akcora, Cuneyt Gurcan and Dey, Asim Kumar and Gel, Yulia R. and Kantarcioglu, Murat},
  booktitle={Pacific-Asia conference on knowledge discovery and data mining},
  pages={1-12},
  year={2018},
  organization={Springer}
}
```
### Source Files


 * [src](./src)
    * [main](./src/main)
        * [python](./python)
            * [bitcoin_prediction](./bitcoin_prediction)
                * [bitcoin_tests](./bitcoin_tests)
                    * In this folder, we put bitcoin test files to predict log return of bitcoin with recursive neural network (RNN) and random forest algorithms.
                * [sliding](./sliding)
                    * [slided_regression.py](./sliding/slided_regression.py)
                        * This class can be used to predict bitcoin both for betti numbers and chainlets. It takes 3 file parameters to run prediction model bitcoin price file, chainlet file and result file.
                    * [filtration_regression.py](./sliding/filtration_regression.py)
                        * For given threshold values, chainlets are filtrated and fed into the prediction model. For each threshold, one model is constructed and output its prediction.
                    * [boosting_of_filtrated_regression.py](./sliding/boosting_of_filtrated_regression.py)
                        * This class takes the previously constructed models of filtration_regression.py and re-build the stronger deep learning model with them.
## Deep Learning Network Structure
In this project, for both slided and filtration techniques, regression of deep learning is used for constructing the model for prediction of Bitcoin system. While constructing deep learning, we have used 4 hidden layer with hyperbolic tangent activation function. To get better convergence of gradient descent, Xavier weight initialization technique is applied. For avoiding the overfitting of training bitcoin sets, dropout technique is used as a regularization technique and its value is 0.2 for each hidden layer.
