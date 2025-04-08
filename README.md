
<link rel="stylesheet" href="style.css">
<!-- saved from url=(0014)about:internet -->
<html lang=" en-US"><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
  
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>NLP Class Project | Spring 2025 CSCI 5541 | University of Minnesota</title>

  <link rel="stylesheet" href="./files/bulma.min.css" />

  <link rel="stylesheet" href="./files/styles.css">
  <link rel="preconnect" href="https://fonts.gstatic.com/">
  <link href="./files/css2" rel="stylesheet">
  <link href="./files/css" rel="stylesheet">


  <base href="." target="_blank"></head>


<body>
  <div>
    <div class="wrapper">
      <h1 style="font-family: &#39;Lato&#39;, sans-serif;">Minority Languages: Sourashtra</h1>
      <h4 style="font-family: &#39;Lato&#39;, sans-serif; ">Spring 2025 CSCI 5541 NLP: Class Project - University of Minnesota</h4>
      <h4 style="font-family: &#39;Lato&#39;, sans-serif; ">Audi Quattro</h4>

      <div class="authors-wrapper">
        
        <div class="author-container">
          <div class="author-image">
                        
              <img src="">
            
          </div>
          <p>    
              Amoligha Timma
            
          </p>
        </div>
        
        <div class="author-container">
          <div class="author-image">
            
            <img src="">
            
          </div>
          <p>
            
            Gehad Abdelrahman
            
          </p>
        </div>
        
        <div class="author-container">
          <div class="author-image">
            
              <img src="">            
            
          </div>
          <p>
              Malak Raafat
          </p>
        </div>
        
        <div class="author-container">
          <div class="author-image">
                        
              <img src="">
            
          </div>
          <p>
            Abhi Bijlwan
          </p>
        </div>
        
      </div>

      <br/>

      <div class="authors-wrapper">
        <div class="publication-links">
          <!-- Github link -->
          <span class="link-block">
            <a
              href=""
              target="_blank"
              class="external-link button is-normal is-rounded is-dark is-outlined"
            >
            <span>Final Report</span>
            </a>
          </span>
          <span class="link-block">
            <a
              href=""
              target="_blank"
              class="external-link button is-normal is-rounded is-dark is-outlined"
            >
            <span>Code</span>
            </a>
          </span>      
          <span class="link-block">
            <a
              href=""
              target="_blank"
              class="external-link button is-normal is-rounded is-dark is-outlined"
            >
            <span>Model Weights</span>
            </a>
          </span>              
        </div>
      </div>


    </div>
  </div>

  <div class="wrapper">
    <hr>
    
    <h2 id="abstract">Abstract</h2>

<p>Minority languages like Sourashtra are largely

    underrepresented in Natural Language Processing (NLP), making tasks like sentiment analysis challenging due to limited training data.
    
    Since multilingual transformer models such
    as BERT and XLM-RoBERTa rely on large
    datasets, they often struggle with low resource
    
    languages. This project explores whether finetuning XLM-RoBERTa on linguistically related
    
    Indian languages (e.g., Gujarati, Marathi) improves sentiment classification for Sourashtra.
    
    To evaluate this, we create a new Sourashtra
    sentiment dataset and compare performance
    
    across models fine-tuned on related and unrelated languages. Our findings contribute to
    
    ongoing research in low-resource NLP, high-
    lighting the role of linguistic similarity in crosslingual transfer learning and providing a framework for improving NLP applications for underrepresented languages.
</p>

<hr>


<h2 id="introduction">Introduction</h2>

<p>
    Languages play an important role in preserving

and recognizing cultural identity. Yet minority languages like Sourashtra remain vastly underrepresented in Natural Language Processing research

and implementations. Due to limited amounts of
text based data, most popular models struggle to
process and understand minority languages. As
a result of this, key NLP tasks such as sentiment
analysis, translation, and text generation remain

inaccessible to communities that speak these languages.

The limited existence of Sourashtra (and similar minority languages) in the digital space creates

major challenges for computational language processes. Unlike widely spoken languages such as

English and Hindi, Sourashtra doesn’t have a large scale system for lingual data. This makes it difficult

to develop models that understand the language’s

unique grammar, phonetics, and sentiments. Existing pre-trained models such as BERT and mBERT,

perform poorly on minority languages in comparison to languages like Chinese. This is due to the

model’s reliance on large, diverse training datasets.
This exclusion not only limits NLP advancements

but also restricts accessibility for Sourashtra speakers in areas such as education, translations, and

even social media.

</p>
<p>
To bridge the gap between Sourashtra and large

LLMs, our project proposes to fine-tune a multilingual pre-trained model on influential Indian
languages such as Hindi, Gujarati, Marathi, Telugu, Tamil, and Malayalam. These languages have
had major influences on the Sourashtra language
and are thus vital for our training. By leveraging
these related languages with large datasets, we aim
to improve the cross-lingual transfer learning and
enhance sentiment classification for the language.
The model will then be evaluated and tested on a

custom-made dataset. This will be designed specifically for the Sourashtra language to assess its ability to generalize and adapt to minority vernaculars.
</p>

<hr>

<h2 id="approach">Approach</h2>

<p>
<b>What did you do exactly? How did you solve the problem? Why did you think it would be successful? Is anything new in your approach?</b>
We began by using the capable multilingual model XLM-RoBERTa to address the issue of limited data in minority languages like Sourashtra. 
First, we gathered large datasets in related Indian languages like Hindi, Gujarati, Marathi, Telugu, Tamil, and Malayalam that possess richer textual resources.
By fine-tuning the model on these languages, we enabled it to learn common linguistic and sentiment patterns that could be potentially transferred to or be seen in Sourashtra.

Next, we further fine-tuning the model on a custom-made Sourashtra sentiment dataset. 
Our strategy is rooted in the theory that linguistic similarities among the 6 popular Indian languages would allow the model to successfully capture the linguistic nuances of Sourashtra. 
The innovative aspect of our approach lies in a two method traing: first gathering abundant data from related languages and then adapting that knowledge to a low-resource language. 
This method not only improves sentiment classification accuracy for Sourashtra but also demonstrates a novel, scalable pathway for enhancing NLP applications in other minority languages.

</p>


<p>
<b>What problems did you anticipate? What problems did you encounter? Did the very first thing you tried work?</b>
One major problem that we anticipated and faced was retrieving a sufficient dataset for the Sourashtra language. Since it is a minority language, there are not many abundant resources/resources that
we could utilize. To overcome this, we had one of our group members create a custom datasheet, as they are a native speaker. This provided us with approximately 250 positive and negative sentiments 
that we fed to the pre-trained XLM-RoBERTa model. 
</p>


<hr>
<h2 id="results">Results</h2>

<!-- Baseline Results -->
<section id="baseline-results">
  <h3>Baseline Results</h3>
  <pre>
Baseline Accuracy  
Label 
1    125 
0    125 
Name: count, dtype: int64 
Baseline Accuracy: 0.5000 
Precision: 0.5000, Recall: 1.0000, F1-score: 0.6667
  </pre>
</section>

<!-- Gujarati Fine-tuned Model Results -->
<section id="gujarati-results">
  <h3>Gujarati Fine-tuned Model (3 Epochs)</h3>
  <p><strong>Accuracy on Sourashtra:</strong> 0.5040</p>
  <p><strong>Precision:</strong> 0.5021, <strong>Recall:</strong> 0.9680, <strong>F1-score:</strong> 0.6612</p>
  <pre>
training_args = TrainingArguments(
    output_dir="./results",
    evaluation_strategy="epoch",
    save_strategy="epoch",
    learning_rate=5e-5,
    per_device_train_batch_size=8,
    per_device_eval_batch_size=8,
    num_train_epochs=3,
    weight_decay=0.01,
    logging_dir="./logs",
    logging_steps=10,
    remove_unused_columns=False
)
  </pre>
</section>

<!-- Marathi Fine-tuned Model Results (3 Epochs) -->
<section id="marathi-3epochs">
  <h3>Marathi Fine-tuned Model (3 Epochs)</h3>
  <p><strong>Accuracy on Sourashtra:</strong> 0.5000</p>
  <p><strong>Precision:</strong> 0.5000, <strong>Recall:</strong> 1.0000, <strong>F1-score:</strong> 0.6667</p>
  
  <h4>Training Metrics</h4>
  <table>
    <thead>
      <tr>
        <th>Epoch</th>
        <th>Training Loss</th>
        <th>Validation Loss</th>
        <th>Accuracy</th>
        <th>Precision</th>
        <th>Recall</th>
        <th>F1</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>1</td>
        <td>0.711700</td>
        <td>0.693495</td>
        <td>0.500000</td>
        <td>1.000000</td>
        <td>0.000000</td>
        <td>0.000000</td>
      </tr>
      <tr>
        <td>2</td>
        <td>0.689700</td>
        <td>0.695169</td>
        <td>0.500000</td>
        <td>0.500000</td>
        <td>1.000000</td>
        <td>0.666667</td>
      </tr>
      <tr>
        <td>3</td>
        <td>0.688800</td>
        <td>0.693072</td>
        <td>0.500000</td>
        <td>0.500000</td>
        <td>1.000000</td>
        <td>0.666667</td>
      </tr>
    </tbody>
  </table>
  
  <pre>
training_args = TrainingArguments(
    output_dir="./results",
    evaluation_strategy="epoch",
    save_strategy="epoch",
    learning_rate=5e-5,
    per_device_train_batch_size=8,
    per_device_eval_batch_size=8,
    num_train_epochs=3,
    weight_decay=0.01,
    logging_dir="./logs",
    logging_steps=10,
    remove_unused_columns=False
)
  </pre>
</section>

<!-- Marathi Fine-tuned Model Results (7 Epochs) -->
<section id="marathi-7epochs">
  <h3>Marathi Fine-tuned Model (7 Epochs)</h3>
  <p><strong>Accuracy on Sourashtra:</strong> 0.5000</p>
  <p><strong>Precision:</strong> 0.5000, <strong>Recall:</strong> 1.0000, <strong>F1-score:</strong> 0.6667</p>
  
  <h4>Training Metrics</h4>
  <table>
    <thead>
      <tr>
        <th>Epoch</th>
        <th>Training Loss</th>
        <th>Validation Loss</th>
        <th>Accuracy</th>
        <th>Precision</th>
        <th>Recall</th>
        <th>F1</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>1</td>
        <td>0.696700</td>
        <td>0.694290</td>
        <td>0.500000</td>
        <td>1.000000</td>
        <td>0.000000</td>
        <td>0.000000</td>
      </tr>
      <tr>
        <td>2</td>
        <td>0.701500</td>
        <td>0.695057</td>
        <td>0.500000</td>
        <td>0.500000</td>
        <td>1.000000</td>
        <td>0.666667</td>
      </tr>
      <tr>
        <td>3</td>
        <td>0.699600</td>
        <td>0.693483</td>
        <td>0.500000</td>
        <td>1.000000</td>
        <td>0.000000</td>
        <td>0.000000</td>
      </tr>
      <tr>
        <td>4</td>
        <td>0.695200</td>
        <td>0.696917</td>
        <td>0.500000</td>
        <td>1.000000</td>
        <td>0.000000</td>
        <td>0.000000</td>
      </tr>
      <tr>
        <td>5</td>
        <td>0.695900</td>
        <td>0.693611</td>
        <td>0.500000</td>
        <td>1.000000</td>
        <td>0.000000</td>
        <td>0.000000</td>
      </tr>
      <tr>
        <td>6</td>
        <td>0.704400</td>
        <td>0.693242</td>
        <td>0.500000</td>
        <td>1.000000</td>
        <td>0.000000</td>
        <td>0.000000</td>
      </tr>
      <tr>
        <td>7</td>
        <td>0.686900</td>
        <td>0.693171</td>
        <td>0.500000</td>
        <td>0.500000</td>
        <td>1.000000</td>
        <td>0.666667</td>
      </tr>
      <!-- Include additional rows for epochs 2 to 7 as shown in your PDF -->
    </tbody>
  </table>
  
  <pre>
training_args = TrainingArguments(
    output_dir="./marathi_results",
    eval_strategy="epoch",
    save_strategy="epoch",
    learning_rate=5e-5,
    per_device_train_batch_size=8,
    per_device_eval_batch_size=8,
    num_train_epochs=7,
    weight_decay=0.01,
    logging_dir="./marathi_logs",
    logging_steps=10,
    remove_unused_columns=False,
    report_to="none"
)
  </pre>
</section>

<!-- Hindi Fine-tuned Model Results (3 & 7 Epochs) -->
<section id="hindi-results">
  <h3>Hindi Fine-tuned Model (3 Epochs)</h3>
  <p><strong>Accuracy on Sourashtra:</strong> 0.5000</p>
  <p><strong>Precision:</strong> 0.5000, <strong>Recall:</strong> 1.0000, <strong>F1-score:</strong> 0.6667</p>
  
  <h4>Training Metrics (3 Epochs)</h4>
  <table>
    <thead>
      <tr>
        <th>Epoch</th>
        <th>Training Loss</th>
        <th>Validation Loss</th>
        <th>Accuracy</th>
        <th>Precision</th>
        <th>Recall</th>
        <th>F1</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>1</td>
        <td>0.690900</td>
        <td>0.543022</td>
        <td>0.770000</td>
        <td>0.770000</td>
        <td>1.000000</td>
        <td>0.870056</td>
      </tr>
      <tr>
        <td>2</td>
        <td>0.779200</td>
        <td>0.546899</td>
        <td>0.770000</td>
        <td>0.770000</td>
        <td>1.000000</td>
        <td>0.870056</td>
      </tr>
      <tr>
        <td>3</td>
        <td>0.571900</td>
        <td>0.539649</td>
        <td>0.770000</td>
        <td>0.770000</td>
        <td>1.000000</td>
        <td>0.870056</td>
      </tr>
    </tbody>
  </table>
  
  <pre>
training_args = TrainingArguments(
    output_dir="./results",
    evaluation_strategy="epoch",
    save_strategy="epoch",
    learning_rate=5e-5,
    per_device_train_batch_size=8,
    per_device_eval_batch_size=8,
    num_train_epochs=3,
    weight_decay=0.01,
    logging_dir="./logs",
    logging_steps=10,
    remove_unused_columns=False
)
  </pre>
  
  <h3>Hindi Fine-tuned Model (7 Epochs)</h3>
  <p><strong>Accuracy on Sourashtra:</strong> 0.5000</p>
  <p><strong>Precision:</strong> 0.5000, <strong>Recall:</strong> 1.0000, <strong>F1-score:</strong> 0.6667</p>
  
  <h4>Training Metrics (7 Epochs)</h4>
  <table>
    <thead>
      <tr>
        <th>Epoch</th>
        <th>Training Loss</th>
        <th>Validation Loss</th>
        <th>Accuracy</th>
        <th>Precision</th>
        <th>Recall</th>
        <th>F1</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>1</td>
        <td>0.667500</td>
        <td>0.539256</td>
        <td>0.770000</td>
        <td>0.770000</td>
        <td>1.000000</td>
        <td>0.870056</td>
      </tr>
      <tr>
        <td>2</td>
        <td>0.793500</td>
        <td>0.545243</td>
        <td>0.770000</td>
        <td>0.770000</td>
        <td>1.000000</td>
        <td>0.870056</td>
      </tr>
      <tr>
        <td>3</td>
        <td>0.580100</td>
        <td>0.540899</td>
        <td>0.770000</td>
        <td>0.770000</td>
        <td>1.000000</td>
        <td>0.870056</td>
      </tr>
      <tr>
        <td>4</td>
        <td>0.498400</td>
        <td>0.539759</td>
        <td>0.770000</td>
        <td>0.770000</td>
        <td>1.000000</td>
        <td>0.870056</td>
      </tr>
      <tr>
        <td>5</td>
        <td>0.509900</td>
        <td>0.539628</td>
        <td>0.770000</td>
        <td>0.770000</td>
        <td>1.000000</td>
        <td>0.870056</td>
      </tr>
      <tr>
        <td>6</td>
        <td>0.517400</td>
        <td>0.540118</td>
        <td>0.770000</td>
        <td>0.770000</td>
        <td>1.000000</td>
        <td>0.870056</td>
      </tr>
      <tr>
        <td>7</td>
        <td>0.507500</td>
        <td>0.540586</td>
        <td>0.770000</td>
        <td>0.770000</td>
        <td>1.000000</td>
        <td>0.870056</td>
      </tr>
    </tbody>
  </table>
  
  <pre>
training_args = TrainingArguments(
    output_dir="./results",
    evaluation_strategy="epoch",
    save_strategy="epoch",
    learning_rate=5e-5,
    per_device_train_batch_size=8,
    per_device_eval_batch_size=8,
    num_train_epochs=7,
    weight_decay=0.01,
    logging_dir="./logs",
    logging_steps=10,
    remove_unused_columns=False
)
  </pre>
</section>

<hr>

<h2 id="conclusion">Conclusion and Future Work</h2>
<p>

    After running multiple epochs of training, so far our model is only able to get 50% accuracy with Hindi and Marathi. 
    Comparing against Gujarati, the accuracy was observed to be marginally better at 50.21%. In theory, this hints that Gujarati has 
    more influence on Sourashtra than the other 2 Indo-Aryan Languages. To expand on the project for the future, we plan to dive into the 
    3 Dravidian languages that have historically influenced Sourashtra with the current datasets we have. 
</p>

<p>
    Further development is still required for the model to learn and find better relationships between the Sourashtra and the 6 Indian languages 
    we are exploring. Although we were able to receieve results, it seems that the current approach does need modification as attaining exactly 50% accuracy is 
    unlikely. Another approach could be to have acquire more Sourashtra sentiment statements that could allow the model to have more data to test on which 
    potentially can have an impact on accuracy observed. Tuning the hyper parameters used in the model could further refine the accuracy perecentage outputted by the model. Experimenting with different model structures, such as adding additional neural layers, could be a determinant of the accuracy.
    The results that we were able to reproduce can be succesfully implemented in other work environments as long as the datasets and the pretrained models can be acquired. 

</p>
<hr>
  </div>

</body></html>
