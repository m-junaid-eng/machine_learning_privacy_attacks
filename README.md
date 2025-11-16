<section>
  <h1>ML Privacy Research: A Comprehensive Analysis</h1>
  <p><strong>Researcher:</strong> Muhammad Junaid</p>

  <p><strong>Focus:</strong> 14 Foundational Papers on Machine Learning Privacy Attacks</p>

  <h2>Project Overview</h2>
  <p>
    This repository provides a comprehensive analysis of how Machine Learning (ML)
    models leak sensitive data. By synthesizing 14 foundational research papers, this
    project categorizes vulnerabilities across the entire ML pipeline, from data
    poisoning during training to model extraction via public APIs.
  </p>

  <h2>Research Taxonomy</h2>

  <h3>1. Membership Inference Attacks (MIA)</h3>
  <p><strong>Objective:</strong> Determine if a specific individual's data was used to train the model.</p>
  <p><strong>Core Papers:</strong> Shokri et al. (2017), Choquette-Choo et al. (2021), Song &amp; Mittal (2020).</p>
  <p><strong>Key Finding:</strong> Overfitting is the strongest predictor of MIA success. Attacks are effective even with label-only access.</p>

  <h3>2. Model Inversion Attacks</h3>
  <p><strong>Objective:</strong> Reconstruct raw training samples (e.g., facial images) from model outputs.</p>
  <p><strong>Core Papers:</strong> Fredrikson et al. (2015), Zhang et al. (2020), Wang et al. (2021).</p>
  <p><strong>Key Finding:</strong> GAN-based and variational methods can reconstruct high-fidelity, recognizable private data.</p>

  <h3>3. Poisoning and Backdoor Attacks</h3>
  <p><strong>Objective:</strong> Manipulate the training set to control model behavior at a later stage.</p>
  <p><strong>Core Papers:</strong> Biggio et al. (2012), Gu et al. (2017).</p>
  <p><strong>Key Finding:</strong> Small triggers (BadNets) can be hidden in models that function normally until the trigger is present.</p>

  <h3>4. Model Extraction (Stealing)</h3>
  <p><strong>Objective:</strong> Clone the logic and parameters of a proprietary black-box model.</p>
  <p><strong>Core Papers:</strong> Tramèr et al. (2016), Orekondy et al. (2019).</p>
  <p><strong>Key Finding:</strong> Systematic API querying allows attackers to build knockoff networks that replicate model functionality.</p>

  <h3>5. Property and Generative Risks</h3>
  <p><strong>Objective:</strong> Extract aggregate dataset properties or training samples from GANs and VAEs.</p>
  <p><strong>Core Papers:</strong> Ganju et al. (2018), Song et al. (2022).</p>
  <p><strong>Key Finding:</strong> Generative models are significantly more prone to memorization than standard classifiers.</p>

  <h3>6. Meta-Surveys</h3>
  <p><strong>Core Papers:</strong> Jayaraman &amp; Evans (2019), Rigaki &amp; Garcia (2023).</p>
  <p>
    <strong>Summary:</strong> These papers provide the foundation for current defense
    strategies and modern attack taxonomies.
  </p>

  <h2>Key Research Findings</h2>
  <ul>
    <li><strong>The Overfitting Vulnerability:</strong> Models that do not generalize well are inherently less private.</li>
    <li><strong>Black-Box Sufficiency:</strong> Internal access is not required; most attacks succeed via standard API queries.</li>
    <li><strong>The Privacy-Utility Tradeoff:</strong> Defenses often lead to a slight reduction in model accuracy.</li>
  </ul>

  <h2>Mitigations and Defenses</h2>
  <ul>
    <li><strong>Differential Privacy (DP):</strong> Adding statistical noise (DP-SGD) to provide formal privacy guarantees.</li>
    <li><strong>Adversarial Training:</strong> Training models to recognize and resist inference attacks.</li>
    <li><strong>Rate Limiting:</strong> Restricting API access to prevent automated model extraction.</li>
    <li><strong>Privacy Auditing:</strong> Using tools such as Privacy Meter to evaluate model leakage before deployment.</li>
  </ul>

  <h2>References</h2>
  <p>
    This research is based on the full citations of the 14 papers listed above.
    For a detailed breakdown of each methodology, refer to the complete research report.
  </p>
</section>
