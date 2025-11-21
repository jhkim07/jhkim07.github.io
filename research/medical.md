---
layout: default
title: "Medical AI Projects"
---

<section class="section">
  <div class="container">
    <h2>Medical AI Projects</h2>
    <p class="section-text">
      This page summarizes ongoing and past projects in
      <strong>medical AI</strong>, with a particular focus on
      ophthalmology, retinal imaging, and trustworthy clinical decision
      support.
    </p>

    <h3>Key Themes</h3>
    <ul class="section-text">
      <li>Domain-specialized LLMs for ophthalmology (e.g., Ophtimus-V2-Tx)</li>
      <li>Noise-robust medical image analysis and quantification</li>
      <li>Reliable mapping from model outputs to clinical coding systems</li>
      <li>Evaluation frameworks for safety, robustness, and explainability</li>
    </ul>

    <h3>Selected Projects</h3>
    <ul class="section-text">
      <li>
        <a href="#ophtimus">
          <strong>Ophtimus-V2-Tx:</strong>
          An 8B-parameter ophthalmology LLM
          trained on case reports and evaluated with CliBench-based coding.
        </a>
      </li>
      <li>
        <a href="#erm">
          <strong>ERM Quantification:</strong>
          Low-cost and fast SD-OCT based
          epiretinal membrane detection and thickness quantification.
        </a>
      </li>
      <li>
        <strong>Trustworthy Clinical Support:</strong>
        Methods to validate and monitor LLM predictions
        before deployment in real clinical workflows.
      </li>
    </ul>

  </div>
</section>

<section id="ophtimus" class="section">
  <div class="container">

    <h2>Ophtimus: Ophthalmology-specific LLM</h2>

    <p class="section-text">
      <strong>Python · PyTorch · Transformers · LangChain · Streamlit · FastAPI</strong>
    </p>

    <!-- 대표 이미지 -->
    <div style="margin: 2rem 0;">
      <img 
        src="{{ '/assets/images/research/ophtimus/Ophtimus-Overall-Architecture.png' | relative_url }}" 
        alt="Ophtimus Overall Architecture"
        style="width:100%; max-width:900px; border-radius:0.75rem; border:1px solid #333;"
      >
    </div>

    <p class="section-text">
      🤗 <strong>Models and Datasets</strong> &nbsp;&nbsp;|&nbsp;&nbsp; 📕 <strong>AAAI 2025 Workshop Paper</strong>
    </p>

    <h3>Introduction</h3>
    <p class="section-text">
      Ophtimus is an open-source <strong>large language model (LLM)</strong> specialized in ophthalmology, 
      built with <strong>8 billion parameters</strong> based on the LLaMA architecture. It is trained on 
      carefully curated ophthalmology-specific data, including medical papers, textbooks, 
      and research reports. Through filtering, summarization, and preprocessing, only the 
      most relevant and high-quality information was retained.
    </p>
    <p class="section-text">
      Designed to be both <strong>lightweight</strong> and <strong>high-performing</strong>, Ophtimus is suitable for 
      real-world applications such as <strong>clinical decision support</strong>, <strong>medical education</strong>, and 
      <strong>patient communication</strong>. The model and its training pipeline are fully open-sourced, 
      providing a practical reference for developing similar domain-specific LLMs in other 
      areas of medicine.
    </p>

    <p class="section-text" style="margin-top:1.2rem;">
      <strong>Related GitHub Repositories</strong><br>
      • <a href="https://github.com/jinkimh/Ophtimus-Ophthalmology-LLM" target="_blank">
          Ophtimus-Ophthalmology-LLM
        </a><br>
      • <a href="https://github.com/jinkimh/SD-OCT-ERM-Quantification" target="_blank">
          SD-OCT-ERM-Quantification
        </a>
    </p>

    <hr style="margin:2.5rem 0; border:0.5px solid #333;">


    <!-- Dataset Details -->
    <h3>Dataset Details</h3>

    <p class="section-text">
      All datasets used for Ophtimus were either newly constructed or adapted for this project. 
      Pre-training datasets were curated from open-source ophthalmology materials, while 
      instruction-tuning and evaluation datasets were obtained by extracting only 
      <strong>ophthalmology-relevant samples</strong> from broader medical corpora.  
      All data underwent preprocessing steps, including <strong>deduplication</strong>, 
      <strong>English-only filtering</strong>, and removal of any <strong>personally identifiable information (PII)</strong>.
    </p>

    <div class="table-wrapper">
      <table class="degree-table">
        <thead>
          <tr>
            <th>Dataset name</th>
            <th>Source</th>
            <th>Size</th>
            <th>Purpose</th>
            <th>Key Features</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Ophthalmology-pubmed-corpus</td>
            <td>Ophthalmology papers</td>
            <td>18.4M Tokens</td>
            <td>Pre-Training</td>
            <td>
              • Map-reduce style summaries<br>
              • Broad ophthalmic keywords
            </td>
          </tr>
          <tr>
            <td>Ophthalmology-textbook-corpus</td>
            <td>Ophthalmology textbooks</td>
            <td>4M Tokens</td>
            <td>Pre-Training</td>
            <td>
              • Trusted medical sources<br>
              • Rich in diagnostic cases
            </td>
          </tr>
          <tr>
            <td>Ophthalmology MCQA Inst Dataset</td>
            <td>Ophthalmology documents</td>
            <td>51.7k QAs</td>
            <td>Instruction-Tuning</td>
            <td>
              • Diverse multiple-choice formats<br>
              • Reasoning included<br>
              • Various ophthalmic topics
            </td>
          </tr>
          <tr>
            <td>Ophthalmology EQA Inst Dataset</td>
            <td>Ophthalmology documents</td>
            <td>49.3k QAs</td>
            <td>Instruction-Tuning</td>
            <td>
              • Essay / explanation-style QA<br>
              • Variety of ophthalmic topics
            </td>
          </tr>
          <tr>
            <td>Ophtimus-Eval-Dataset</td>
            <td>Medical platform data</td>
            <td>2,153 QAs</td>
            <td>Evaluation</td>
            <td>
              • Expert-verified data<br>
              • Multi-choice QA dataset
            </td>
          </tr>
          <tr>
            <td>PubMedQA-ophthal-Dataset</td>
            <td>PubMedQA</td>
            <td>297 QAs</td>
            <td>Evaluation</td>
            <td>
              • Ophthalmology domain filtered<br>
              • True/False MCQA dataset
            </td>
          </tr>
          <tr>
            <td>MedMCQA-Ophthal-Dataset</td>
            <td>MedMCQA</td>
            <td>6,932 QAs</td>
            <td>Evaluation</td>
            <td>
              • Ophthalmology domain filtered<br>
              • Multi-choice QA dataset
            </td>
          </tr>
          <tr>
            <td>EQAEval-Dataset</td>
            <td>MedQuAD, others</td>
            <td>1,389 QAs</td>
            <td>Evaluation</td>
            <td>
              • Diverse open-source datasets<br>
              • Ophthalmology domain filtered<br>
              • Essay-style QA
            </td>
          </tr>
        </tbody>
      </table>
    </div>

    <hr style="margin:2.5rem 0; border:0.5px solid #333;">


    <!-- Model Details -->
    <h3>Model Details</h3>

    <p class="section-text">
      The <strong>pre-training</strong> and <strong>instruction-tuning</strong> columns below refer to the 
      training conducted in this project. The base models had already undergone their own 
      pre-training and/or fine-tuning, and Ophtimus was built using transfer learning on top of 
      these models.
    </p>

    <div class="table-wrapper">
      <table class="degree-table">
        <thead>
          <tr>
            <th>Model name</th>
            <th>Base model</th>
            <th>Parameters</th>
            <th>Pre-training</th>
            <th>Instruction-tuning</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Ophtimus-Base</td>
            <td>Llama-3.1-8B</td>
            <td>8B</td>
            <td>✅</td>
            <td>❌</td>
          </tr>
          <tr>
            <td>Ophtimus-Llama-1B</td>
            <td>Llama-3.2-1B-Instruct</td>
            <td>1B</td>
            <td>❌</td>
            <td>✅</td>
          </tr>
          <tr>
            <td>Ophtimus-Llama-3B</td>
            <td>Llama-3.2-3B-Instruct</td>
            <td>3B</td>
            <td>❌</td>
            <td>✅</td>
          </tr>
          <tr>
            <td>Ophtimus-Llama-8B</td>
            <td>Llama-3.1-8B-Instruct</td>
            <td>8B</td>
            <td>❌</td>
            <td>✅</td>
          </tr>
          <tr>
            <td>Ophtimus-Instruct-8B</td>
            <td>Ophtimus-Base</td>
            <td>8B</td>
            <td>✅</td>
            <td>✅</td>
          </tr>
        </tbody>
      </table>
    </div>

    <hr style="margin:2.5rem 0; border:0.5px solid #333;">


    <!-- Performance -->
    <h3>Performance</h3>

    <p class="section-text">
      <strong>Multi-Choice QA:</strong> Ophtimus-Eval, MedMCQA, PubMedQA (ophthalmology-subset)<br>
      <strong>Essay QA:</strong> MedQuAD, Medical Flashcards, Medical Wikidoc (ophthalmology-filtered)
    </p>
    <p class="section-text">
      Ophtimus-Eval is a proprietary dataset collected from a medical platform. 
      The other datasets are established medical benchmarks, from which only 
      <strong>ophthalmology-related QA pairs</strong> were extracted for evaluation.
    </p>

    <div class="table-wrapper">
      <table class="degree-table">
        <thead>
          <tr>
            <th rowspan="2">Model</th>
            <th colspan="3">Multi-Choice Question</th>
            <th colspan="4">Essay Question</th>
          </tr>
          <tr>
            <th>Ophtimus Eval</th>
            <th>MedMCQA (Ophth)</th>
            <th>PubMedQA (Ophth)</th>
            <th>RougeL</th>
            <th>BLEU</th>
            <th>METEOR</th>
            <th>SemScore</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>OpenAI GPT-4o</td>
            <td>71.95%</td>
            <td>81.95%</td>
            <td>89.90%</td>
            <td>0.193</td>
            <td>0.082</td>
            <td>0.341</td>
            <td>0.761</td>
          </tr>
          <tr>
            <td>Llama-3-8B-Instruct</td>
            <td>48.60%</td>
            <td>74.02%</td>
            <td>63.97%</td>
            <td>0.193</td>
            <td>0.064</td>
            <td>0.244</td>
            <td>0.684</td>
          </tr>
          <tr>
            <td>Llama-3.1-8B-Instruct</td>
            <td>39.78%</td>
            <td>57.96%</td>
            <td>83.84%</td>
            <td>0.177</td>
            <td>0.054</td>
            <td>0.215</td>
            <td>0.641</td>
          </tr>
          <tr>
            <td>Eye-Llama</td>
            <td>32.56%</td>
            <td>59.43%</td>
            <td>66.11%</td>
            <td>0.183</td>
            <td>0.062</td>
            <td>0.211</td>
            <td>0.686</td>
          </tr>
          <tr>
            <td>PMC-Llama-13B</td>
            <td>48.28%</td>
            <td>63.45%</td>
            <td>72.48%</td>
            <td>0.223</td>
            <td>0.082</td>
            <td>0.288</td>
            <td>0.714</td>
          </tr>
          <tr>
            <td>Ophtimus-Llama-1B</td>
            <td>41.45%</td>
            <td>45.74%</td>
            <td>61.95%</td>
            <td>0.219</td>
            <td>0.076</td>
            <td>0.217</td>
            <td>0.711</td>
          </tr>
          <tr>
            <td>Ophtimus-Llama-3B</td>
            <td>52.70%</td>
            <td>62.10%</td>
            <td>69.36%</td>
            <td>0.224</td>
            <td>0.077</td>
            <td>0.225</td>
            <td>0.726</td>
          </tr>
          <tr>
            <td>Ophtimus-Llama-8B</td>
            <td>60.78%</td>
            <td>68.25%</td>
            <td>69.70%</td>
            <td>0.226</td>
            <td>0.083</td>
            <td>0.230</td>
            <td>0.733</td>
          </tr>
          <tr>
            <td>Ophtimus-Instruct-8B</td>
            <td>63.85%</td>
            <td>71.51%</td>
            <td>72.73%</td>
            <td>0.222</td>
            <td>0.079</td>
            <td>0.224</td>
            <td>0.735</td>
          </tr>
        </tbody>
      </table>
    </div>

  </div>
</section>



<section id="erm" class="section">
  <div class="container">
    <h2>SD-OCT-based Epiretinal Membrane Diagnostic Assistant System</h2>

    <p class="section-text">
      <strong>Python · PyTorch · OpenCV · YOLO · Pillow</strong>
    </p>

    <!-- Architecture Image -->
    <div style="margin: 2rem 0; text-align:center;">
      <img src="{{ '/assets/images/research/erm/Architecture.png' | relative_url }}"
           alt="ERM System Architecture"
           style="max-width: 90%; border-radius: 0.5rem; border:1px solid #333;">
      <p style="color:#bdbdbd; font-size:0.9rem; margin-top:0.5rem;">
        Overall pipeline architecture for ERM detection & quantification
      </p>
    </div>

    <h3>Introduction</h3>
    <p class="section-text">
      This project presents a low-cost and efficient method for detecting and quantifying 
      Epiretinal Membranes (ERM) using Spectral-Domain OCT (SD-OCT). Using deep learning 
      techniques—particularly YOLO object detection—we generate en face 
      <strong>ERM Projection Images</strong> from B-scan data, enabling intuitive visualization and 
      accurate measurement of ERM lesions.
    </p>

    <p class="section-text">
      The proposed approach also quantifies the association between ERM severity and retinal 
      thickness, contributing toward enhanced clinical decision-making. This system aims to 
      reduce the diagnostic gap between SD-OCT and Swept-Source OCT (SS-OCT) while maintaining 
      accessibility and diagnostic performance.
    </p>

    <p class="section-text">
      <strong>GitHub repository:</strong>
      <a href="https://github.com/jinkimh/SD-OCT-ERM-Quantification" target="_blank">
        github.com/jinkimh/SD-OCT-ERM-Quantification
      </a>
    </p>

    <h3>YOLO Model Evaluation</h3>
    <p class="section-text">
      We evaluated YOLOv5, YOLOv8, and YOLOv11 models for ERM detection. Each model was 
      trained with two dataset scales (Full: 2200 images, Half: 1100 images) and tested on 
      650 expert-labeled OCT B-scans.
    </p>

    <div class="table-wrapper">
      <table class="degree-table">
        <thead>
          <tr>
            <th>Model</th><th>Size</th><th>Params (M)</th>
            <th>Precision</th><th>Recall</th>
            <th>mAP@50</th><th>mAP@50:95</th><th>Dataset</th>
          </tr>
        </thead>
        <tbody>

          <!-- YOLOv5 -->
          <tr><td>YOLOv5</td><td>S</td><td>7.02</td><td>0.752</td><td>0.703</td><td>0.722</td><td>0.423</td><td>Full</td></tr>
          <tr><td>YOLOv5</td><td>S</td><td>7.02</td><td>0.694</td><td>0.642</td><td>0.664</td><td>0.376</td><td>Half</td></tr>

          <tr><td>YOLOv5</td><td>M</td><td>20.87</td><td>0.783</td><td>0.734</td><td>0.752</td><td>0.444</td><td>Full</td></tr>
          <tr><td>YOLOv5</td><td>M</td><td>20.87</td><td>0.723</td><td>0.685</td><td>0.701</td><td>0.396</td><td>Half</td></tr>

          <tr><td>YOLOv5</td><td>L</td><td>46.14</td><td>0.813</td><td>0.762</td><td>0.784</td><td>0.463</td><td>Full</td></tr>
          <tr><td>YOLOv5</td><td>L</td><td>46.14</td><td>0.745</td><td>0.704</td><td>0.726</td><td>0.414</td><td>Half</td></tr>

          <tr><td>YOLOv5</td><td>X</td><td>86.22</td><td>0.836</td><td>0.784</td><td>0.802</td><td>0.485</td><td>Full</td></tr>
          <tr><td>YOLOv5</td><td>X</td><td>86.22</td><td>0.763</td><td>0.725</td><td>0.743</td><td>0.437</td><td>Half</td></tr>

          <!-- YOLOv8 -->
          <tr><td>YOLOv8</td><td>S</td><td>11.14</td><td>0.781</td><td>0.736</td><td>0.764</td><td>0.447</td><td>Full</td></tr>
          <tr><td>YOLOv8</td><td>S</td><td>11.14</td><td>0.723</td><td>0.676</td><td>0.701</td><td>0.393</td><td>Half</td></tr>

          <tr><td>YOLOv8</td><td>M</td><td>25.86</td><td>0.813</td><td>0.762</td><td>0.791</td><td>0.466</td><td>Full</td></tr>
          <tr><td>YOLOv8</td><td>M</td><td>25.86</td><td>0.748</td><td>0.705</td><td>0.724</td><td>0.412</td><td>Half</td></tr>

          <tr><td>YOLOv8</td><td>L</td><td>43.63</td><td>0.844</td><td>0.792</td><td>0.823</td><td>0.482</td><td>Full</td></tr>
          <tr><td>YOLOv8</td><td>L</td><td>43.63</td><td>0.774</td><td>0.731</td><td>0.754</td><td>0.436</td><td>Half</td></tr>

          <tr><td>YOLOv8</td><td>X</td><td>68.15</td><td>0.867</td><td>0.814</td><td>0.842</td><td>0.504</td><td>Full</td></tr>
          <tr><td>YOLOv8</td><td>X</td><td>68.15</td><td>0.793</td><td>0.752</td><td>0.772</td><td>0.454</td><td>Half</td></tr>

          <!-- YOLOv11 -->
          <tr><td>YOLOv11</td><td>S</td><td>9.43</td><td>0.804</td><td>0.752</td><td>0.783</td><td>0.468</td><td>Full</td></tr>
          <tr><td>YOLOv11</td><td>S</td><td>9.43</td><td>0.746</td><td>0.692</td><td>0.714</td><td>0.417</td><td>Half</td></tr>

          <tr><td>YOLOv11</td><td>M</td><td>20.05</td><td>0.846</td><td>0.794</td><td>0.821</td><td>0.493</td><td>Full</td></tr>
          <tr><td>YOLOv11</td><td>M</td><td>20.05</td><td>0.774</td><td>0.736</td><td>0.757</td><td>0.443</td><td>Half</td></tr>

          <tr><td>YOLOv11</td><td>L</td><td>25.31</td><td>0.873</td><td>0.823</td><td>0.854</td><td>0.524</td><td>Full</td></tr>
          <tr><td>YOLOv11</td><td>L</td><td>25.31</td><td>0.807</td><td>0.773</td><td>0.793</td><td>0.476</td><td>Half</td></tr>

          <tr><td>YOLOv11</td><td>X</td><td>56.87</td><td>0.902</td><td>0.857</td><td>0.882</td><td>0.556</td><td>Full</td></tr>
          <tr><td>YOLOv11</td><td>X</td><td>56.87</td><td>0.836</td><td>0.803</td><td>0.826</td><td>0.507</td><td>Half</td></tr>

        </tbody>
      </table>
    </div>

  </div>
</section>