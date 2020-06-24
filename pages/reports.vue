<template>
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="max-w-3xl mx-auto pt-4">
      <p id="h.burq7g4gifo6" class="c12 title">
        <span class="c10 c19">Yelp Sense</span>
      </p>
      <p id="h.6d93jk14rj5o" class="c22 subtitle">
        <span class="c27">Sentiment</span>
      </p>
      <h2 id="h.68xddz318rjw" class="c3 c16">
        <span class="c15 c10"></span>
      </h2>
      <h2 id="h.lm5n9vxshl0s" class="c3">
        <span class="c15 c10">Problem:</span>
      </h2>
      <p class="c0">
        <span class="c1">
          The Yelp platform provides users the ability to review and rate
          businesses. They use the common &ldquo;star&rdquo; rating system,
          where users can select a rating from 1 to 5 stars, with 1 being the
          worst and 5 being the best. This system works well and by averaging
          out all the star ratings for a business users are able to get a quick
          snapshot of what most people think about a given business.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span class="c1">
          There are some issues with the way of doing things. Users are also
          able to write a review for a given business in addition to rate it.
          There are times however when the content of the text doesn&rsquo;t
          match what a reasonable person would say the rating would be. For
          instance a user reviewed an eye clinic:
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0 c13">
        <span class="c4">
          I&#39;ve gone to Dr. Glancy for over ten years for my eye exams and
          contact lenses. &nbsp;The prescription and fit have always been
          perfect and I&#39;ve learned not to take this for granted. &nbsp;One
          thing I really appreciate about Dr. Glancy is that he explains about
          how the eyes work as well as the contact lenses so that you understand
          the decisions he makes and why you need to take certain precautions to
          care for your eyes. &nbsp;He&#39;s very professional and personable
          and his staff is as well!
        </span>
      </p>
      <p class="c0 c7 c13">
        <span class="c4"></span>
      </p>
      <p class="c0">
        <span>
          From that review, I believe a reasonable person would assume that the
          reviewer was happy with the business and would have rated it as a
          five, or maybe a four. However, the user actually gave this business a
          one star review. This was most likely an honest mistake, but this
          particular business only has 3 reviews, so by making this simple
          mistake, it brought the business
        </span>
        <span>&rsquo;s</span>
        <span class="c1">
          &nbsp;average rating down to 2.5. Mistakes like this have real world
          consequences. If this review was rated correctly, this business would
          go from a 2.5 rating to 3.5.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span>
          Another issue with the star rating system is that ratings are
          subjective. I believe that most people tend to agree with the
          extremes, the one and five stars, but once you move inward there can
          be some discrepancies. For instance a user reviewed a
        </span>
        <span class="c1">Cracker Barrel Old Country Store:</span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0 c13">
        <span class="c4">
          Fireplace and breakfast anytime. Could not be happier. The place even
          had that wood burning campfire smell. Staff was friendly. I had a late
          breakfast and the eggs were perfect. The ham was fabulous.
        </span>
      </p>
      <p class="c0 c7 c13">
        <span class="c4"></span>
      </p>
      <p class="c0">
        <span>To me, I would assume that</span>
        <span>user</span>
        <span class="c1">
          &nbsp;would have rated that business with five stars. However they
          rated it four stars. It&rsquo;s not much of a difference but it just
          goes to show that there&rsquo;s a level of subjectivity to star
          ratings that can lead to confusion and problems.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span>
          My final issue is that stars are discrete. Some sites will allow users
          to rate in half step increments, &nbsp;but I believe that sentiment is
          more continuous than that. By using a regression technique, I hope to
          capture some of the subtle differences between a 4 and 5 star review
          for instance.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <h2 id="h.cj493rjd46jj" class="c3">
        <span class="c15 c10">Proposed Solution:</span>
      </h2>
      <p class="c0">
        <span>
          I propose using a modern Natural Language Processing (NLP) pipeline
          trained on a English Yelp review texts and star ratings to output a
          value between 0 and 1 that can then be used in place of the
          traditional user&rsquo;s star rating. I hope that by removing the
          ability to specify a rating, and instead opt to use the text,
          user&rsquo;s will be incentivised to provide better text reviews that
          offer more insights and information. I will also be using this
          sentiment value in a similar way to the star rating, allowing users to
          easily gauge the general sentiment of a business.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <h2 id="h.ieqedrh1azfk" class="c3">
        <span class="c15 c10">Research:</span>
      </h2>
      <p class="c0">
        <span class="c1">
          The field of Natural Language Processing is one of the oldest uses of
          &ldquo;machine learning&rdquo; and has advanced rapidly in the past
          several years. Some of the more simple techniques include using word
          counts and some type of linear regression, or &nbsp;using a naive
          Bayes approach. Some more modern solutions use deep learning
          techniques, such as using an LSTM model, a bag of words model, or more
          recently using an Transformer model, including Bert, XLNet, and Ernie.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span class="c1">
          Some of the most popular and promising libraries using these
          techniques include the FastText library from Facebook for the bag of
          words approach, and the Transformers library from Hugging Face for the
          Transformer models.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span class="c14 c10">FastText:</span>
      </p>
      <p class="c0">
        <span>FastText was first describe in the paper</span>
        <span
          >&ldquo;Bag of Tricks for Efficient Text Classification&rdquo;</span
        >
        <sup>
          <a id="ftnt_ref1" href="#ftnt1">[1]</a>
        </sup>
        <span class="c1">&nbsp;and released in 2016.</span>
      </p>
      <p class="c0">
        <span class="c1">From the abstract:</span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0 c13">
        <span class="c4">
          fastText is often on par with deep learning classifiers in terms of
          accuracy, and many orders of magnitude faster for training and
          evaluation. We can train fastText on more than one billion words in
          less than ten minutes using a standard multicore CPU, and classify
          half a million sentences among 312K classes in less than a minute.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span class="c1">
          Without getting too technical, fasttext works by learning where words
          lie in some vector space, and using a linear classifier trained on the
          average vector space of a sentence.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span>
          Some of the advantages are it&rsquo;s incredible speed while
          maintaining a reasonably similar level of accuracy. This approach also
          allows for (mostly) language agnostic training. It also uses a special
          technique known as
        </span>
        <span class="c1">
          hierarchical softmax, meaning that you can have a very large amount of
          classes and still train and infer very quickly. It can also be
          deployed on very cheap hardware, and be able to keep up with large
          demand. Overall it&rsquo;s definitely the cheapest, most bang for your
          buck way to do NLP.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span class="c1">
          One of the main disadvantages for me is that the fasttext library only
          currently allows for classification and not regression. I could
          implement a solution myself, but one of the reasons it&rsquo;s so fast
          is that it is highly optimized C++ code, and I&rsquo;m not confident
          enough in my C++ skill yet to take that on.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span class="c14 c10">Transformers:</span>
      </p>
      <p class="c0">
        <span class="c1">
          The Transformers is a library from Hugging Face. It uses both PyTorch
          and TensorFlow to implement some of the most common Transformer
          models, including BERT, and XLNet. They have also released some of
          their own models including DistilBERT, which is similar to BERT but
          offers the advantages of being both smaller and faster, while
          maintaining reasonably similar metrics.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span class="c1">
          The models are actually pre-trained Transformer models. Without
          getting too technical, the way you can think of it is these models are
          already trained on the English (or some other) language, and as such,
          can be trained on a specific task by only adding one layer.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span class="c1">
          Some advantages of Transformers is that it is currently the state of
          the art, and as such much research is currently being put into it. It
          currently offers the best metrics. The Hugging Face Transformers
          library also makes it incredibly easy to implement these complex
          models.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span class="c1">
          The main disadvantage is that the training and deployment costs will
          be much more than fasttext, but such models as DistilBERT offer great
          improvements over the standard BERT. Because we are using transfer
          learning however, we are able to train on much less data which means
          we can speed up training.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span>
          While the Transformers library makes it quite easy, I would most
          likely use a wrapper library such as
        </span>
        <span>simpletransformers</span>
        <span class="c1">
          &nbsp;or ktrain. These libraries offer some nice extra features, and
          make training essential a 3 line solution.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <h2 id="h.irwltd5kam92" class="c3">
        <span class="c15 c10">Experiments:</span>
      </h2>
      <p class="c0">
        <span class="c10 c14">FastText Experiments:</span>
      </p>
      <p class="c0">
        <span class="c1">
          Since fasttext is much faster and offers similar results, I&rsquo;ll
          be running more experiments using it, and extrapolating the results to
          the other models.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <ul class="c8 lst-kix_2uzjl7no0mi5-0 start">
        <li class="c0 c5">
          <span class="c1">Star Rating + NLTK + Standard Hyperparms</span>
        </li>
      </ul>
      <ul class="c8 lst-kix_2uzjl7no0mi5-1 start">
        <li class="c0 c11">
          <span class="c10">0.7104</span>
          <span class="c1">accuracy (Unbalanced Targets)</span>
        </li>
        <li class="c0 c11">
          <span class="c10">0.6815</span>
          <span class="c1">accuracy (Balanced Targets)</span>
        </li>
      </ul>
      <ul class="c8 lst-kix_2uzjl7no0mi5-0">
        <li class="c0 c5">
          <span class="c1"
            >Pos/Neg/Neutral + NLTK + &nbsp;Standard Hyperparms</span
          >
        </li>
      </ul>
      <ul class="c8 lst-kix_2uzjl7no0mi5-1 start">
        <li class="c0 c11">
          <span class="c10">0.8842</span>
          <span class="c1">accuracy (Unbalanced Targets)</span>
        </li>
        <li class="c0 c11">
          <span class="c10">0.8771</span>
          <span>accuracy (Balanced Targets)</span>
        </li>
      </ul>
      <ul class="c8 lst-kix_2uzjl7no0mi5-0">
        <li class="c0 c5">
          <span class="c1"
            >Pos/Neg (3 is Neg) + NLTK + &nbsp;Standard Hyperparms</span
          >
        </li>
      </ul>
      <ul class="c8 lst-kix_2uzjl7no0mi5-1 start">
        <li class="c0 c11">
          <span class="c10">0.9254</span>
          <span class="c1">accuracy (Unbalanced Targets)</span>
        </li>
        <li class="c0 c11">
          <span class="c10">0.9131</span>
          <span class="c1">&nbsp;accuracy (Balanced Targets)</span>
        </li>
      </ul>
      <ul class="c8 lst-kix_2uzjl7no0mi5-0">
        <li class="c0 c5">
          <span class="c1"
            >Pos/Neg (3 is Pos) + NLTK + &nbsp;Standard Hyperparms</span
          >
        </li>
      </ul>
      <ul class="c8 lst-kix_2uzjl7no0mi5-1 start">
        <li class="c0 c11">
          <span class="c10">0.9398</span>
          <span class="c1">&nbsp;accuracy (Unbalanced Targets)</span>
        </li>
        <li class="c0 c11">
          <span class="c10">0.9409</span>
          <span class="c10 c18">&nbsp;</span>
          <span class="c1">accuracy (Balanced Targets)</span>
        </li>
      </ul>
      <ul class="c8 lst-kix_2uzjl7no0mi5-0">
        <li class="c0 c5">
          <span class="c1">Hyperparameter Tuning</span>
        </li>
      </ul>
      <ul class="c8 lst-kix_2uzjl7no0mi5-1 start">
        <li class="c0 c11">
          <span class="c1">
            I used a Bayesian optimization technique to try out ~100 different
            hyperparameters and found the default ones worked best.
          </span>
        </li>
      </ul>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span class="c1">
          Anecdotal average training time: 5 minutes on ~318k rows + validation
          on 200k
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span class="c1">
          Based on these experiments I&rsquo;ve found that I&rsquo;m going to
          try and train similar classification models with DistilBERT and BERT
          using Positive/Negative (where 3 is positive) as the labels, and not
          balancing the data.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span class="c14 c10">Transformers Experiments:</span>
      </p>
      <ul class="c8 lst-kix_x5gleevo7av5-0 start">
        <li class="c0 c5">
          <span class="c1">DistilBERT</span>
        </li>
      </ul>
      <ul class="c8 lst-kix_x5gleevo7av5-1 start">
        <li class="c0 c11">
          <span class="c10">0.95</span>
          <span class="c1">&nbsp;accuracy</span>
        </li>
      </ul>
      <ul class="c8 lst-kix_x5gleevo7av5-0">
        <li class="c0 c5">
          <span class="c1">BERT</span>
        </li>
      </ul>
      <ul class="c8 lst-kix_x5gleevo7av5-1 start">
        <li class="c0 c11">
          <span class="c10">0.95</span>
          <span class="c1">&nbsp;accuracy</span>
        </li>
      </ul>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span class="c1">
          Anecdotal average training time: 5 hours on ~318k rows + validation on
          200k
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span class="c1">
          Based on this I&rsquo;m going to use DistilBERT to train a regression
          model.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span>DistilBERT Regression MAE:</span>
        <span class="c18 c24">&nbsp;</span>
        <span class="c9">0.3538</span>
      </p>
      <p class="c0 c7">
        <span class="c9"></span>
      </p>
      <p class="c0">
        <span class="c14 c10">Summarization Before:</span>
      </p>
      <p class="c0">
        <span class="c1">
          I also tried using a BART summarization model to summarize the text
          prior to inference, however summarization takes a while (~3 seconds
          per review depending on length, etc) So I was only able to test this
          on an unacceptable small dataset (200 random rows)
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span>Without summarization the fasttext model had an accuracy of</span>
        <span class="c9">0.935.</span>
      </p>
      <p class="c0">
        <span>With summarization the accuracy was</span>
        <span class="c9">0.92.</span>
      </p>
      <p class="c0 c7">
        <span class="c9"></span>
      </p>
      <p class="c0">
        <span class="c1">
          There are also summarization methods, such as the t5 model, however I
          did not get a change to experiment with that for this purpose.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span class="c1">
          I do think that with some work, I could label and fine tune a
          summarization model and the summarizations might offer a great
          feature, by itself, but also as a preprocessing step.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <h2 id="h.4w9xo4blheoi" class="c3">
        <span class="c15 c10">Final Model Choice:</span>
      </h2>
      <p class="c0">
        <span class="c1">
          For my final model I have chosen to use a DistilBERT regression model.
          I believe that regression is the right choice as opposed to
          classification and that DistilBERT offers comparable results to BERT
          and has the advantage of being able to train for more epochs and more
          data since it&rsquo;s faster and cheaper.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span class="c1">
          My final model was trained on 800k rows from the original dataset. I
          have chosen to only use 800k because I don&rsquo;t need that many rows
          to achieve good results, and because by using less data, I can speed
          up training.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <h2 id="h.7765sh6nfvan" class="c3 c16">
        <span class="c10 c15"></span>
      </h2>
      <h2 id="h.fabtmka9zlnc" class="c3">
        <span class="c15 c10">Final Model Evaluation:</span>
      </h2>
      <p class="c0">
        <span class="c1">
          My model took approximately 1 hour to preprocess the 800k rows using a
          2016 13&rdquo; MacBook Pro, and 3 hours to train on a ml.p3.16xlarge
          instance type. The estimated cost was $100, but could change by using
          multiprocessing for the preprocessing, and using half precision
          floating point for the training. The issue with that however is that
          the transformers tokenizer doesn&#39;t work well with python
          multiprocessing, and the model doesn&rsquo;t support fp16 easily.
          These can both be most likely addressed and worked around given enough
          time.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span>I was able to achieve a MAE of</span>
        <span class="c10">0.328</span>
        <span class="c1">on a validation set of ~640k rows.</span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span>
          I also average out the new business rating and compared it with the
          average star ratings for
        </span>
        <span>
          2027 business in my local area. The MAE for the new ratings vs the old
          ones is
        </span>
        <span class="c9">0.10.</span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <h2 id="h.eg2526saab3a" class="c3">
        <span class="c15 c10">Final Model Considerations:</span>
      </h2>
      <p class="c0">
        <span class="c1">
          One of the biggest considerations is the cost. This model was
          expensive to train, and will be expensive to deploy. I think that
          these costs are manageable and worth it however. We must also consider
          the limitations of the model. For instance on reviews like:
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0 c13">
        <span class="c4">
          While there is nothing fantastically different about this Walmart as
          compared to all the others, it successfully sucks the blood of our
          local businesses by importing half its goods from places where they
          pay 5-year-old girls 2 cents a day. Oh, but it&#39;s so cheap!
        </span>
      </p>
      <p class="c0 c7 c13">
        <span class="c4"></span>
      </p>
      <p class="c0">
        <span class="c1">
          This is clearly a negative review, but because of the text &ldquo;Oh,
          but it&rsquo;s so cheap!&rdquo;, the model thinks it&rsquo;s positive.
          By removing that one sentence, the model accurately predicts the
          sentiment. This is a common problem that tongue in cheek, sarcastic,
          or off topic reviews are difficult to predict. This is why I&rsquo;m
          interested to see how training a summarization model would influence
          the predictions.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <p class="c0">
        <span>
          We can also do testing with select users to test the accuracy of the
          reviews. We can use a fasttext classification model to also get
          prediction and if the inferences differ we can assume that there might
          be an issue and have someone look into it.
        </span>
      </p>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <h2 id="h.qzywkmqg8v80" class="c3">
        <span class="c21 c10">Final Model Deployment:</span>
      </h2>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <h2 id="h.2kd0lbqyya9r" class="c3">
        <span class="c15 c10">Final Model API Docs:</span>
      </h2>
      <p class="c0 c7">
        <span class="c1"></span>
      </p>
      <h2 id="h.i98ix5f0axgh" class="c3">
        <span class="c10 c21">Extra Thoughts:</span>
      </h2>
      <hr class="c23" />
      <div>
        <p class="c0">
          <a id="ftnt1" href="#ftnt_ref1">[1]</a>
          <span>&nbsp;</span>
          <span class="c17">
            <a
              class="c6"
              href="https://www.google.com/url?q=https://arxiv.org/abs/1607.01759&amp;sa=D&amp;ust=1592884005990000"
              >arXiv:1607.01759</a
            >
          </span>
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
@import url('https://themes.googleusercontent.com/fonts/css?kit=dpiI8CyVsrzWsJLBFKehGrO2quSjkmHyRpzYsazfOBscZWF3hAHMNYZRL0MY3y1z');

.lst-kix_x5gleevo7av5-8 > li::before {
  content: '\0025a0  ';
}

.lst-kix_x5gleevo7av5-7 > li::before {
  content: '\0025cb  ';
}

.lst-kix_x5gleevo7av5-4 > li::before {
  content: '\0025cb  ';
}

.lst-kix_x5gleevo7av5-3 > li::before {
  content: '\0025cf  ';
}

.lst-kix_x5gleevo7av5-5 > li::before {
  content: '\0025a0  ';
}

.lst-kix_x5gleevo7av5-2 > li::before {
  content: '\0025a0  ';
}

.lst-kix_x5gleevo7av5-6 > li::before {
  content: '\0025cf  ';
}

ul.lst-kix_x5gleevo7av5-8 {
  list-style-type: none;
}

ul.lst-kix_x5gleevo7av5-7 {
  list-style-type: none;
}

ul.lst-kix_x5gleevo7av5-6 {
  list-style-type: none;
}

.lst-kix_jrtcit2h24mi-8 > li::before {
  content: '\0025a0  ';
}

.lst-kix_2uzjl7no0mi5-6 > li::before {
  content: '\0025cf  ';
}

ul.lst-kix_x5gleevo7av5-5 {
  list-style-type: none;
}

.lst-kix_jrtcit2h24mi-7 > li::before {
  content: '\0025cb  ';
}

.lst-kix_2uzjl7no0mi5-5 > li::before {
  content: '\0025a0  ';
}

.lst-kix_x5gleevo7av5-0 > li::before {
  content: '\0025cf  ';
}

ul.lst-kix_x5gleevo7av5-0 {
  list-style-type: none;
}

.lst-kix_x5gleevo7av5-1 > li::before {
  content: '\0025cb  ';
}

.lst-kix_jrtcit2h24mi-4 > li::before {
  content: '\0025cb  ';
}

.lst-kix_jrtcit2h24mi-6 > li::before {
  content: '\0025cf  ';
}

.lst-kix_2uzjl7no0mi5-2 > li::before {
  content: '\0025a0  ';
}

.lst-kix_2uzjl7no0mi5-4 > li::before {
  content: '\0025cb  ';
}

ul.lst-kix_x5gleevo7av5-4 {
  list-style-type: none;
}

ul.lst-kix_x5gleevo7av5-3 {
  list-style-type: none;
}

ul.lst-kix_x5gleevo7av5-2 {
  list-style-type: none;
}

.lst-kix_jrtcit2h24mi-5 > li::before {
  content: '\0025a0  ';
}

.lst-kix_2uzjl7no0mi5-3 > li::before {
  content: '\0025cf  ';
}

ul.lst-kix_x5gleevo7av5-1 {
  list-style-type: none;
}

.lst-kix_2uzjl7no0mi5-0 > li::before {
  content: '\0025cf  ';
}

.lst-kix_2uzjl7no0mi5-1 > li::before {
  content: '\0025cb  ';
}

.lst-kix_jrtcit2h24mi-0 > li::before {
  content: '\0025cf  ';
}

.lst-kix_jrtcit2h24mi-2 > li::before {
  content: '\0025a0  ';
}

.lst-kix_jrtcit2h24mi-3 > li::before {
  content: '\0025cf  ';
}

.lst-kix_jrtcit2h24mi-1 > li::before {
  content: '\0025cb  ';
}

.lst-kix_2uzjl7no0mi5-7 > li::before {
  content: '\0025cb  ';
}

ul.lst-kix_2uzjl7no0mi5-5 {
  list-style-type: none;
}

ul.lst-kix_2uzjl7no0mi5-6 {
  list-style-type: none;
}

ul.lst-kix_2uzjl7no0mi5-7 {
  list-style-type: none;
}

.lst-kix_2uzjl7no0mi5-8 > li::before {
  content: '\0025a0  ';
}

ul.lst-kix_2uzjl7no0mi5-8 {
  list-style-type: none;
}

ul.lst-kix_2uzjl7no0mi5-1 {
  list-style-type: none;
}

ul.lst-kix_2uzjl7no0mi5-2 {
  list-style-type: none;
}

ul.lst-kix_2uzjl7no0mi5-3 {
  list-style-type: none;
}

ul.lst-kix_2uzjl7no0mi5-4 {
  list-style-type: none;
}

ul.lst-kix_2uzjl7no0mi5-0 {
  list-style-type: none;
}

ul.lst-kix_jrtcit2h24mi-0 {
  list-style-type: none;
}

ul.lst-kix_jrtcit2h24mi-2 {
  list-style-type: none;
}

ul.lst-kix_jrtcit2h24mi-1 {
  list-style-type: none;
}

ul.lst-kix_jrtcit2h24mi-8 {
  list-style-type: none;
}

ul.lst-kix_jrtcit2h24mi-7 {
  list-style-type: none;
}

ul.lst-kix_jrtcit2h24mi-4 {
  list-style-type: none;
}

ul.lst-kix_jrtcit2h24mi-3 {
  list-style-type: none;
}

ul.lst-kix_jrtcit2h24mi-6 {
  list-style-type: none;
}

ul.lst-kix_jrtcit2h24mi-5 {
  list-style-type: none;
}

ol {
  margin: 0;
  padding: 0;
}

table td,
table th {
  padding: 0;
}

.c4 {
  background-color: #efefef;
  color: #000;
  font-weight: 400;
  text-decoration: none;
  vertical-align: baseline;
  font-size: 13pt;
  font-family: 'Roboto Mono', monospace;
  font-style: normal;
}

.c14 {
  -webkit-text-decoration-skip: none;
  color: #000;
  text-decoration: underline;
  vertical-align: baseline;
  text-decoration-skip-ink: none;
  font-size: 14pt;
  font-family: Arial, sans-serif;
  font-style: normal;
}

.c15 {
  -webkit-text-decoration-skip: none;
  color: #000;
  text-decoration: underline;
  vertical-align: baseline;
  text-decoration-skip-ink: none;
  font-size: 22pt;
  font-family: Arial, sans-serif;
  font-style: normal;
}

.c22 {
  padding-top: 0;
  padding-bottom: 16pt;
  line-height: 1.15;
  page-break-after: avoid;
  orphans: 2;
  widows: 2;
  text-align: left;
}

.c27 {
  color: #666;
  font-weight: 400;
  text-decoration: none;
  vertical-align: baseline;
  font-size: 15pt;
  font-family: Arial, sans-serif;
  font-style: normal;
}

.c2 {
  color: #000;
  font-weight: 400;
  text-decoration: none;
  vertical-align: baseline;
  font-size: 22pt;
  font-family: Arial, sans-serif;
  font-style: normal;
}

.c1 {
  color: #000;
  font-weight: 400;
  text-decoration: none;
  vertical-align: baseline;
  font-size: 14pt;
  font-family: Arial, sans-serif;
  font-style: normal;
}

.c3 {
  padding-top: 18pt;
  padding-bottom: 6pt;
  line-height: 1.15;
  page-break-after: avoid;
  orphans: 2;
  widows: 2;
  text-align: left;
}

.c9 {
  color: #000;
  font-weight: 700;
  text-decoration: none;
  vertical-align: baseline;
  font-size: 14pt;
  font-family: Arial, sans-serif;
  font-style: normal;
}

.c12 {
  padding-top: 0;
  padding-bottom: 3pt;
  line-height: 1.15;
  page-break-after: avoid;
  orphans: 2;
  widows: 2;
  text-align: left;
}

.c25 {
  color: #b7b7b7;
  font-weight: 400;
  text-decoration: none;
  vertical-align: baseline;
  font-size: 14pt;
  font-family: Arial, sans-serif;
  font-style: normal;
}

.c19 {
  color: #000;
  text-decoration: none;
  vertical-align: baseline;
  font-size: 26pt;
  font-family: Arial, sans-serif;
  font-style: normal;
}

.c0 {
  padding-top: 0;
  padding-bottom: 0;
  line-height: 1.15;
  orphans: 2;
  widows: 2;
  text-align: left;
}

.c20 {
  padding-top: 0;
  padding-bottom: 0;
  line-height: 1.15;
  orphans: 2;
  widows: 2;
  text-align: right;
}

.c17 {
  text-decoration-skip-ink: none;
  -webkit-text-decoration-skip: none;
  color: #15c;
  text-decoration: underline;
}

.c26 {
  background-color: #fff;
  max-width: 540pt;
  padding: 36pt 36pt 36pt 36pt;
}

.c18 {
  font-size: 10.5pt;
  font-family: 'Roboto', serif;
  color: #172b4d;
}

.c21 {
  text-decoration-skip-ink: none;
  -webkit-text-decoration-skip: none;
  text-decoration: underline;
}

.c24 {
  background-color: #f4f5f7;
  font-weight: 400;
}

.c6 {
  color: inherit;
  text-decoration: inherit;
}

.c23 {
  width: 33%;
  height: 1px;
}

.c8 {
  padding: 0;
  margin: 0;
}

.c11 {
  margin-left: 72pt;
  padding-left: 0;
}

.c5 {
  margin-left: 36pt;
  padding-left: 0;
}

.c10 {
  font-weight: 700;
}

.c7 {
  height: 11pt;
}

.c16 {
  height: 16pt;
}

.c13 {
  margin-left: 36pt;
}

.title {
  padding-top: 0;
  color: #000;
  font-size: 26pt;
  padding-bottom: 3pt;
  font-family: Arial, sans-serif;
  line-height: 1.15;
  page-break-after: avoid;
  orphans: 2;
  widows: 2;
  text-align: left;
}

.subtitle {
  padding-top: 0;
  color: #666;
  font-size: 15pt;
  padding-bottom: 16pt;
  font-family: Arial, sans-serif;
  line-height: 1.15;
  page-break-after: avoid;
  orphans: 2;
  widows: 2;
  text-align: left;
}

li {
  color: #000;
  font-size: 14pt;
  font-family: Arial, sans-serif;
}

p {
  margin: 0;
  color: #000;
  font-size: 14pt;
  font-family: Arial, sans-serif;
}

h1 {
  padding-top: 20pt;
  color: #000;
  font-size: 20pt;
  padding-bottom: 6pt;
  font-family: Arial, sans-serif;
  line-height: 1.15;
  page-break-after: avoid;
  orphans: 2;
  widows: 2;
  text-align: left;
}

h2 {
  padding-top: 18pt;
  color: #000;
  font-size: 22pt;
  padding-bottom: 6pt;
  font-family: Arial, sans-serif;
  line-height: 1.15;
  page-break-after: avoid;
  orphans: 2;
  widows: 2;
  text-align: left;
}

h3 {
  padding-top: 16pt;
  color: #434343;
  font-size: 14pt;
  padding-bottom: 4pt;
  font-family: Arial, sans-serif;
  line-height: 1.15;
  page-break-after: avoid;
  orphans: 2;
  widows: 2;
  text-align: left;
}

h4 {
  padding-top: 14pt;
  color: #666;
  font-size: 12pt;
  padding-bottom: 4pt;
  font-family: Arial, sans-serif;
  line-height: 1.15;
  page-break-after: avoid;
  orphans: 2;
  widows: 2;
  text-align: left;
}

h5 {
  padding-top: 12pt;
  color: #666;
  font-size: 14pt;
  padding-bottom: 4pt;
  font-family: Arial, sans-serif;
  line-height: 1.15;
  page-break-after: avoid;
  orphans: 2;
  widows: 2;
  text-align: left;
}

h6 {
  padding-top: 12pt;
  color: #666;
  font-size: 14pt;
  padding-bottom: 4pt;
  font-family: Arial, sans-serif;
  line-height: 1.15;
  page-break-after: avoid;
  font-style: italic;
  orphans: 2;
  widows: 2;
  text-align: left;
}
</style>
