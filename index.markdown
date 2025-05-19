---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: single
classes: wide
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Caveat:wght@700&display=swap');
  
  body {
    background-color: black;
    color: white;
    margin: 0;
    padding: 0;
    font-family: Arial, Helvetica, sans-serif;
    overflow-x: hidden;
  }
  
  h1, h2, h3, h4, h5, h6 {
    color: #ff69b4; /* Pink headers */
    font-weight: 700;
    font-family: Arial, Helvetica, sans-serif;
    text-transform: uppercase;
  }
  
  .grid-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    grid-gap: 2rem;
    margin-bottom: 2rem;
    padding: 1rem;
    max-width: 1200px;
    margin-left: auto;
    margin-right: auto;
  }
  
  .grid-item {
    overflow: hidden;
    margin-bottom: 1rem;
    width: 100%;
  }
  
  .grid-item img {
    width: 100%;
    height: auto;
    display: block;
    margin-bottom: 1rem;
    max-width: 100%;
  }
  
  .grid-item video {
    width: 100%;
    height: auto;
    display: block;
    margin-bottom: 1rem;
    max-width: 100%;
  }
  
  .project-images {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
    margin-bottom: 1rem;
  }
  
  .project-videos {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
    margin-bottom: 1rem;
  }
  
  /* For projects with 4 images */
  .project-images-4 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: auto auto;
    gap: 1rem;
    margin-bottom: 1rem;
  }
  
  /* Remove site header and footer */
  .masthead, .page__footer {
    display: none !important;
  }
  
  /* Remove article styling */
  .page__content {
    margin: 0;
    padding: 0;
    max-width: 100%;
    overflow-x: hidden;
  }
  
  .page {
    padding-right: 0;
    padding-left: 0;
    width: 100%;
    max-width: 100%;
    overflow-x: hidden;
  }
  
  /* Full width layout */
  .page__inner-wrap {
    max-width: 100% !important;
    margin: 0 !important;
    overflow-x: hidden;
  }
  
  /* New styles for bright blue text */
  .main-header {
    text-align: center;
    padding: 3rem 1rem;
    margin-bottom: 1rem;
    width: 100%;
  }
  
  .main-header h1 {
    font-size: 3.5rem;
    color: #80EAFF; /* Lighter bright blue */
    margin-bottom: 1rem;
    font-weight: 700;
    letter-spacing: 2px;
    font-family: 'Caveat', cursive;
    text-transform: none;
  }
  
  p {
    color: #80EAFF; /* Lighter bright blue text */
    margin-top: 0.5rem;
    margin-bottom: 2rem;
    font-weight: 400;
  }
  
  h2 {
    color: #80EAFF !important; /* Override the pink headers for h2 with lighter blue */
    margin-top: 0.5rem;
    font-size: 1.5rem;
    letter-spacing: 1px;
  }
  
  .single-project {
    margin-bottom: 3rem;
  }
  
  /* Center all content */
  .content-wrapper {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1rem;
    box-sizing: border-box;
  }
</style>

<div class="content-wrapper">
  <div class="main-header">
    <h1>BALIN BALINOV</h1>
  </div>

  <div class="grid-container">
    <!-- 2023 Rumpe Ristern Project -->
    <div class="grid-item">
      <h2>2023 RUMPE RISTERN</h2>
      <div class="project-images-4">
        <img src="{{ site.baseurl }}/assets/images/Screenshot 2025-05-19 at 19.36.49.png" alt="Rumpe Ristern Screenshot 1">
        <img src="{{ site.baseurl }}/assets/images/Screenshot 2025-05-19 at 19.37.12.png" alt="Rumpe Ristern Screenshot 2">
        <img src="{{ site.baseurl }}/assets/images/image copy.png" alt="Rumpe Ristern Image 1">
        <img src="{{ site.baseurl }}/assets/images/image copy 2.png" alt="Rumpe Ristern Image 2">
      </div>
      <p>Design and development for the 2023 Rumpe Ristern event, including visual identity, promotional materials, and digital assets.</p>
    </div>

    <!-- Hybrida Student Union Project -->
    <div class="grid-item">
      <h2>20- Anneversary Hybrida Student Union</h2>
      <div class="project-images">
        <img src="{{ site.baseurl }}/assets/images/19_balinV1.jpg" alt="Hybrida Crewneck Design 1">
        <img src="{{ site.baseurl }}/assets/images/19_balinV2.jpg" alt="Hybrida Crewneck Design 2">
      </div>
      <video controls width="100%">
        <source src="{{ site.baseurl }}/assets/images/warehousejub.mp4" type="video/mp4">
      </video>
      <p>Crew Neck design iteration on a crewneck designed for the 20th anneversary of NTNU student union Hybrida</p>
    </div>
    
    <!-- R24 Rear Wing Project -->
    <div class="grid-item">
      <h2>R24 REAR WING</h2>
      <img src="{{ site.baseurl }}/assets/images/image.png" alt="R24 Rear Wing">
      <p>Designed and manufactured rear wing for Revolve NTNU Formula Student Team <href>https://www.revolve.no</href></p>
    </div>
    
    <!-- R25 Telemetry System Project -->
    <div class="grid-item">
      <h2>R25 Telemetry System</h2>
      <img src="{{ site.baseurl }}/assets/images/Screenshot 2025-05-19 at 18.22.48.png" alt="R25 Telemetry System">
      <p>Responsible for the design and development a full racecar telemetry system for Revolve NTNU Formula Student Teams</p>
    </div>
    
    <!-- Last Shannanigans Club Event -->
    <div class="grid-item">
      <h2>LAST SHANNANIGANS - club event</h2>
      <div class="project-videos">
        <video controls>
          <source src="{{ site.baseurl }}/assets/images/Black Solid 2.mp4" type="video/mp4">
        </video>
        <video controls>
          <source src="{{ site.baseurl }}/assets/images/Grey-Black-RecordEye@UU.mp4" type="video/mp4">
        </video>
      </div>
      <p>Designed and animated instagram post, to promote a event hosted by the UNOFFICIAL UNION 1.mai.</p>
    </div>
  </div>
</div>


