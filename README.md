# dvc_tutorial
This repository contains code for kick starting data version controlling using DVC.

# Please download the initial_setup.sh using the below command
wget -L https://gist.githubusercontent.com/VigneshBaskar/419d3df6a1fbca18b59536075f9a76df/raw/35281680e82fd27d729fec95ac2e1217df7556b9/initial_setup.sh

chmod +x ./initial_setup.sh

./initial_setup.sh

cd dvc_tutorial
cat data/evaluation.txt


## Specify ngram parameter in CountVectorizer (lines 50–53) and increase number of features to 6000:
nano code/featurization.py

bag_of_words = CountVectorizer(stop_words='english',
                               max_features=6000,
                               ngram_range=(1, 3))


git commit -am "Add bigram features"

dvc repro evaluation.txt.dvc

cat data/evaluation.txt




