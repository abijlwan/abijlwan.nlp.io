<!DOCTYPE html>
<html lang="en-US">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>NLP Class Project | Spring 2025 CSCI 5541 | University of Minnesota</title>

  <link rel="stylesheet" href="style.css">
  <link rel="stylesheet" href="./files/bulma.min.css">
  <link rel="stylesheet" href="./files/styles.css">
  <link rel="preconnect" href="https://fonts.gstatic.com/">
  <link href="./files/css2" rel="stylesheet">
  <link href="./files/css" rel="stylesheet">
  <base href="." target="_blank">
</head>
<body>
  <div class="wrapper">
    <h1 style="font-family: 'Lato', sans-serif;">Minority Languages: Sourashtra</h1>
    <h4 style="font-family: 'Lato', sans-serif;">Spring 2025 CSCI 5541 NLP: Class Project - University of Minnesota</h4>
    <h4 style="font-family: 'Lato', sans-serif;">Audi Quattro</h4>

    <div class="authors-wrapper">
      <div class="author-container">
        <div class="author-image"><img src="" alt="Amoligha Timma"></div>
        <p>Amoligha Timma</p>
      </div>
      <div class="author-container">
        <div class="author-image"><img src="" alt="Gehad Abdelrahman"></div>
        <p>Gehad Abdelrahman</p>
      </div>
      <div class="author-container">
        <div class="author-image"><img src="" alt="Malak Raafat"></div>
        <p>Malak Raafat</p>
      </div>
      <div class="author-container">
        <div class="author-image"><img src="" alt="Abhi Bijlwan"></div>
        <p>Abhi Bijlwan</p>
      </div>
    </div>

    <div class="publication-links">
      <span class="link-block">
        <a href="" target="_blank" class="external-link button is-normal is-rounded is-dark is-outlined">
          <span>Final Report</span>
        </a>
      </span>
      <span class="link-block">
        <a href="" target="_blank" class="external-link button is-normal is-rounded is-dark is-outlined">
          <span>Code</span>
        </a>
      </span>
      <span class="link-block">
        <a href="" target="_blank" class="external-link button is-normal is-rounded is-dark is-outlined">
          <span>Model Weights</span>
        </a>
      </span>
    </div>
  </div>

  <div class="wrapper">
    <hr>
    <h2 id="abstract">Abstract</h2>
    <p>
      Advances in generative AI and large-scale language models have largely benefited widely spoken languages, leaving minority languages like Sourashtra underserved. We curated a custom sentiment dataset of 250 balanced Sourashtra samples and evaluated cross-lingual transfer from both Indo-Aryan (Gujarati, Marathi, Hindi) and Dravidian (Tamil, Telugu, Malayalam) languages using XLM-RoBERTa. Initial fine-tuning on related Indo-Aryan languages yielded modest gains (~53% ensemble accuracy), while Dravidian transfer showed minimal improvement (~50.8%). Exclusive fine-tuning on Sourashtra reached 64.0% accuracy. Augmenting Indo-Aryan fine-tuning with just 10 in-language examples boosted individual models to 65.4–69.2%, and an augmented Indo-Aryan ensemble achieved 67.08% accuracy. Our work highlights targeted fine-tuning and minimal data augmentation as effective strategies for low-resource NLP and provides a replicable framework for underrepresented languages.
    </p>
    <hr>

    <h2 id="introduction">Introduction</h2>
    <p>
      Languages play an important role in preserving cultural identity. Yet minority languages like Sourashtra remain vastly underrepresented in NLP research and applications due to limited digital resources. As a result, essential NLP tasks such as sentiment analysis and translation remain inaccessible to Sourashtra speakers. To bridge this gap, we fine-tune a multilingual transformer (XLM-RoBERTa) on linguistically related Indian languages and adapt it with a custom Sourashtra dataset to improve cross-lingual transfer.
    </p>
    <hr>

    <h2 id="approach">Approach</h2>
    <p><strong>Methodology:</strong> We first fine-tuned XLM-RoBERTa on large-scale Gujarati, Marathi, and Hindi datasets to capture Indo-Aryan linguistic patterns. Separately, we fine-tuned on Dravidian languages (Tamil, Telugu, Malayalam) to compare transfer effects. Next, we fine-tuned on our 250-sentence Sourashtra corpus to establish a low-resource baseline. Finally, we augmented each Indo-Aryan fine-tuned model with 10 Sourashtra examples and combined them in an ensemble. This two-stage strategy leverages related languages and minimal in-language data to enhance sentiment classification for Sourashtra.
    </p>
    <hr>

    <h2 id="results">Results</h2>

    <section id="baseline-results">
      <h3>Baseline (No Fine-Tuning)</h3>
      <p><strong>Accuracy:</strong> 50.0%</p>
    </section>

    <section id="single-language-results">
      <h3>Single-Language Fine-Tuned Models</h3>
      <ul>
        <li>Gujarati: 50.4%</li>
        <li>Marathi: 56.8%</li>
        <li>Hindi: 52.4%</li>
        <li>Tamil: 50.0%</li>
        <li>Telugu: 56.8%</li>
        <li>Malayalam: 49.6%</li>
      </ul>
    </section>

    <section id="ensemble-results">
      <h3>Ensemble Models</h3>
      <p><strong>Indo-Aryan Ensemble (Gujarati, Marathi, Hindi):</strong> 53.2%</p>
      <p><strong>Dravidian Ensemble (Tamil, Telugu, Malayalam):</strong> 50.8%</p>
    </section>

    <section id="sourashtra-only-results">
      <h3>Sourashtra-Only Fine-Tuned</h3>
      <p><strong>Accuracy:</strong> 64.0%</p>
    </section>

    <section id="augmented-results">
      <h3>Augmented Indo-Aryan Fine-Tuned Models</h3>
      <ul>
        <li>Gujarati + 10 Sourashtra: 65.4%</li>
        <li>Marathi + 10 Sourashtra: 66.3%</li>
        <li>Hindi + 10 Sourashtra: 69.2%</li>
        <li><strong>Augmented Indo-Aryan Ensemble:</strong> 67.08%</li>
      </ul>
    </section>
    <hr>

    <h2 id="conclusion">Conclusion and Future Work</h2>
    <p>
      Our experiments demonstrate that targeted cross-lingual transfer from related Indo-Aryan languages, combined with minimal in-language data augmentation, substantially improves sentiment analysis for Sourashtra. The augmented Indo-Aryan ensemble model achieved the highest accuracy (67.08%), confirming the value of linguistic similarity and few-shot adaptation. For future work, we plan to:
      <ul>
        <li>Incorporate Dravidian languages historically influencing Sourashtra.</li>
        <li>Expand and diversify the Sourashtra dataset, including code-mixed and domain-specific examples.</li>
        <li>Explore data selection strategies to identify the most informative samples for augmentation.</li>
        <li>Apply syntactic and contrastive learning techniques to better handle negation and idiomatic expressions.</li>
      </ul>
    </p>
    <hr>
  </div>
</body>
</html>
