# meme_classifier

There is a missing essential folder: "IMAGES". As its name suggests, it contains every image corresponding to the [quickmeme dataset](http://www.michelecoscia.com/?page_id=422). The dataset doesn't contain image data and the "scrape_image_bytes" when run downloads the corresponding images into an "IMAGES" directory.

The "neural_network_clustering" notebook focuses on devising a method to cluster related images into groups. Further explanation is in the notebook itself and below.

### Journal

My initial plan was to implement the algorithms described in the [MemeSequencer paper](https://arxiv.org/pdf/1802.04936.pdf). However after attempting to implement it, I found it to be way too expensive -even for small inputs. I wasn't sure if this was due to my own implementation or the algorithm itself. Regardless, I set out to classify memes into groups using a different method. I started with using perceptual hashing and machine learning to differentiate pairs of memes. I went through multiple models including logistic regression, gradient boosting trees, and random forests. However, a neural networked performed the best. With 98% precision and 98% recall, I was able to differentiate pairs of memes. I used this model to classify memes into multiple groups by iteratively asking the question: "Are these two memes the same?". The classification isn't perfect and can be improved.
