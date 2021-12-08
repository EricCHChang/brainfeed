# brainfeed
A tool for domain experts to find recent and relevant public discourse on topics they are familiar with

## Project overview

### Motivation

The increasing accessibility of scientific articles and surrounding public discourse is generally beneficial to society. A tradeoff to this increased public consumption of knowledge (in formats traditionally meant for domain experts) is the rise of misinformation. Articles in scientific journals often describe specific facts and precise outcomes under specific conditions, and their validity and generalizability are usually only understood by a few experts. On the other hand, social media such as Reddit and Twitter allow anyone (often anonymously) to post articles and comment about their contents, and it is in these forums that wrong information is conveyed and spread. The wide audience of these forums, coupled with increased public interest on scientific topics (for example, in relation to the Covid-19 pandemic), has made it imperative that experts be able to find and engage such posts.

This project, pitched for [Brainhack Toronto 2021](https://brainhackto.github.io/global-toronto-12-2021/), seeks to create a live feed of active and relevant public discussions on widely used social media forums. While the initial focus of this project is to detect discussions that revolve around brain imaging, the tools to be developed here should in principle be useful for other scientific fields.

### Implementation



### Project communications

For Brainhack Toronto 2021, we'll communicate through a [Brainhack Toronto discord](https://discord.gg/HC7fumm79B) channel.

## Project goals

For **Brainhack 2021**:

- [ ] Post and comment detection on Reddit via Reddit API
- [ ] Abstract and keyword detection based via Crossref API
- [ ] Classification of posts relevancy based on abstract keywords
- [ ] Post data to central repository (Firebase)
- [ ] Web application to view recent posts

Future ideas:

- [ ] Extend to other forums (Twitter?)
- [ ] Sentiment detection of discussions
- [ ] Mobile applications to display discussion feed
- [ ] Analysis of scientific information spread across social networks



## Contributing

Contributors of all backgrounds and experiences are welcome.

### Requirements

- Python

    For simplicity and consistency, you can create a conda environment using the following command:

    ```bash
    conda create \
    --name brainfeed \
    python=3.7
    ```

    After creating the environment, you can activate it by running `conda activate brainfeed`.

- Packages

    You will need the following packages:

    - `habanero` (for Crossref)
    - `PRAW` (for Reddit)
    - `spyder` (optional, a Python IDE)

    You can install the required packages with this command, after activating the conda environment:

    ```bash
    conda install spyder=5.1.5
    pip install habanero==1.0.0 praw==7.5.0
    ```

- A Reddit account

    Setup a Reddit account, and create a script app by clicking the "Create app" button [here](https://old.reddit.com/prefs/apps/).
    More details on this can be found at: [https://github.com/reddit-archive/reddit/wiki/OAuth2](https://github.com/reddit-archive/reddit/wiki/OAuth2)


### Setup

1. Clone this repository

`git clone git@github.com:yohanyee/brainfeed.git`

2. Activate the conda environment

`conda activate brainfeed`

3. Copy the `praw.ini` file to your config directory (see [https://praw.readthedocs.io/en/stable/getting_started/configuration/prawini.html](https://praw.readthedocs.io/en/stable/getting_started/configuration/prawini.html)) and then fill in the information.
Make sure to *not* have this publicly visible.


### Helpful links

- Reddit API: [https://www.reddit.com/dev/api](https://www.reddit.com/dev/api)

    - Python API for Reddit (PRAW): [https://praw.readthedocs.io/en/stable/index.html](https://praw.readthedocs.io/en/stable/index.html)

- Twitter API: [https://developer.twitter.com/en/docs/twitter-api](https://developer.twitter.com/en/docs/twitter-api)

- Crossref API: [https://www.crossref.org/documentation/retrieve-metadata/](https://www.crossref.org/documentation/retrieve-metadata/)

    - Python API for Crossref (Habanero): [https://github.com/sckott/habanero](https://github.com/sckott/habanero)

- Altmetric API: [https://www.altmetric.com/products/altmetric-api/](https://www.altmetric.com/products/altmetric-api/)

- Firebase documentation: [https://firebase.google.com/docs](https://firebase.google.com/docs)

    - SDK for Firebase (Firebase Admin SDK): [https://firebase.google.com/docs/reference/admin](https://firebase.google.com/docs/reference/admin)
