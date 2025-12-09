<section id="erm" class="section" style="padding-top: 0;">
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
</section>

