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
  
  /* Vertical stack layout for full-width images */
  .project-images.vertical-stack {
    display: flex;
    flex-direction: column;
    gap: 2rem;
  }

  .vertical-stack img {
    width: 100%;
    height: auto;
    max-width: 800px;
    margin: 0 auto;
  }
  
  /* Special class for larger images */
  .project-images.large-images {
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
  }

  .large-images img {
    width: 100%;
    height: auto;
    transform: scale(1.5);
    margin: 4rem 0;
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
  
  /* For projects with mixed media (4 images + 1 video) */
  .project-mixed-media-5 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: auto auto auto;
    gap: 1rem;
    margin-bottom: 1rem;
  }
  
  .project-mixed-media-5 video {
    grid-column: 1 / -1;
    width: 100%;
    height: auto;
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
  
  .main-header img {
    max-width: 60%;
    height: auto;
    display: block;
    margin: 0 auto;
  }
  
  .main-header h1 {
    font-size: 3.5rem;
    color: #80EAFF; /* Lighter bright blue */
    margin-bottom: 1rem;
    font-weight: bold;
    letter-spacing: 2px;
    font-family: Arial, sans-serif;
    text-transform: uppercase;
  }
  
  p {
    color: #80EAFF; /* Lighter bright blue text */
    margin-top: 0.5rem;
    margin-bottom: 2rem;
    font-weight: 400;
  }
  
  .grid-item h2 {
    color:hsl(323, 90.20%, 51.80%) !important;
    margin-top: 0.5rem !important;
    margin-bottom: 1rem !important;
    font-size: 1.5rem;
    letter-spacing: 1px;
    border-bottom: none !important;
    padding-bottom: 0 !important;
    text-decoration: none !important;
    border: none !important;
    box-shadow: none !important;
  }
  
  /* Style for links */
  a {
    color: hsl(323, 90.20%, 51.80%);
    text-decoration: none;
  }

  a:hover {
    text-decoration: underline;
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

  .bottom-image {
    width: 100%;
    text-align: center;
    margin-top: 2rem;
  }

  .bottom-image img {
    max-width: 100%;
    height: auto;
    display: block;
    margin: 0 auto;
  }

  /* Image and Video popup styles */
  .popup-overlay {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.8);
    backdrop-filter: blur(5px);
    z-index: 1000;
    cursor: pointer;
  }

  .popup-content {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    max-width: 90%;
    max-height: 90vh;
    z-index: 1001;
  }

  .popup-content img, .popup-content video {
    max-width: 100%;
    max-height: 90vh;
    object-fit: contain;
    border: 2px solid hsl(323, 90.20%, 51.80%);
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
  }

  /* Make images and videos clickable */
  .grid-item img, .project-images img,
  .grid-item video, .project-videos video {
    cursor: pointer;
    transition: transform 0.2s ease;
  }

  .grid-item img:hover, .project-images img:hover,
  .grid-item video:hover, .project-videos video:hover {
    transform: scale(1.02);
  }

  /* Style for grid items with many images */
  .grid-item.full-width {
    grid-column: 1 / -1;
    max-width: 100%;
  }

  .grid-item.full-width .project-images {
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
  }

  .grid-item.full-width .project-images img {
    width: 100%;
    height: auto;
    transform: scale(1.1);
  }

  /* Style for small centered header */
  .small-header {
    text-align: center;
    max-width: 800px;
    margin: 2rem auto 1rem auto;
    padding: 0 2rem;
  }

  .small-header img {
    max-width: 300px;
    height: auto;
  }

  /* Style for the introduction section */
  .introduction {
    text-align: center;
    max-width: 800px;
    margin: 1rem auto 2rem auto;
    padding: 0 2rem;
  }

  .introduction p {
    font-size: 1rem;
    line-height: 1.6;
    margin-bottom: 1rem;
  }

  .introduction a {
    color: hsl(323, 90.20%, 51.80%);
    text-decoration: none;
    transition: opacity 0.2s ease;
  }

  .introduction a:hover {
    opacity: 0.8;
  }

  .highlight {
    color: hsl(323, 90.20%, 51.80%);
  }

  /* Style for signature header */
  .signature-header {
    text-align: right;
    max-width: 800px;
    margin: 0 auto 4rem auto;
    padding: 0 2rem;
  }

  .signature-header img {
    max-width: 200px;
    height: auto;
    margin-left: auto;
  }

  /* Style for large video grid items */
  .grid-item.large-videos {
    width: 100%;
  }

  .grid-item.large-videos .project-videos {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
  }

  .grid-item.large-videos video {
    width: 100%;
    height: auto;
    transform: scale(1.05);
  }

  /* Style for text selection */
  ::selection {
    background-color: hsl(323, 90.20%, 51.80%);
    color: white;
  }
  
  ::-moz-selection {
    background-color: hsl(323, 90.20%, 51.80%);
    color: white;
  }
</style>

<div class="content-wrapper">

  <div class="introduction">
    <p>Hi! My name is Balin Balinov, currently doing a masters in Engineering and ICT@NTNU in Trondheim. These days im spending most of my time building a racecar for <a href="https://www.revolve.no" target="_blank">REVOLVE NTNU</a> Throughout the years i have tipped my toes in design and engineering projects, here are some ;)
    </p>
  </div>


  <div class="grid-container">
    <!-- R25 Telemetry System Project -->
    <div class="grid-item">
      <h2>2025 R25 Telemetry System</h2>
      <div class="project-images vertical-stack">
        <img src="{{ site.baseurl }}/assets/images/RevolveNTNU-Telemetry/telemetry-system.png" alt="R25 Telemetry System">
        <img src="{{ site.baseurl }}/assets/images/RevolveNTNU-Telemetry/telemetry-interface.png" alt="Telemetry System Interface">
      </div>
      <p>I was responsible for leading a team of developers to create a racecar telemetry system for monitoring safety critcal data, and analyzing data post testing. As the leader of the group i have had a hand in the develoopment of the complete system archtecture, for better or worse. When i came to the frontend i made sure to put an artisic touch to it. </p>
    </div>

    <!-- Last Shannanigans Club Event -->
    <div class="grid-item">
      <h2>2025 LAST SHANNANIGANS - club event</h2>
      <div class="project-videos">
        <video autoplay loop muted>
          <source src="{{ site.baseurl }}/assets/images/UnofficialUnion/uu-black-solid.mp4" type="video/mp4">
        </video>
        <video autoplay loop muted>
          <source src="{{ site.baseurl }}/assets/images/UnofficialUnion/uu-record-eye.mp4" type="video/mp4">
        </video>
      </div>
      <p>Designed and animated instagram post, to promote a event hosted by the UNOFFICIAL UNION.</p>
    </div>

    <!-- R24 Rear Wing Project -->
    <div class="grid-item">
      <h2>2024 R24 REAR WING</h2>
      <div class="project-images vertical-stack">
        <img src="{{ site.baseurl }}/assets/images/RevolveNTNU-Aerodynamics/revolve-car-render.png" alt="Revolve NTNU Race Car">
        <img src="{{ site.baseurl }}/assets/images/RevolveNTNU-Aerodynamics/revolve-wing-design.png" alt="R24 Rear Wing Design">
        <img src="{{ site.baseurl }}/assets/images/RevolveNTNU-Aerodynamics/revolve-wing-render.png" alt="R24 Rear Wing Visualization">
      </div>
      <p>Designed and manufactured rear wing for HERA, Revolve NTNUs first overall winning car in Formula Student Team. Did about 200 CFD simulations, ended up with this design. Together with my team we spent the better part of spring 2024 manufacturing the complete areodynamic package in carbon fibre.
      
      The 3D designs where done using SolidWorks</p>
    </div>

    <!-- 2022 Rumpe Ristern Project -->
    <div class="grid-item">
      <h2>2022 RUMPE RISTERN</h2>
      <div class="project-mixed-media-5">
        <img src="{{ site.baseurl }}/assets/images/RR/rr-cover.png" alt="Rumpe Ristern Cover">
        <img src="{{ site.baseurl }}/assets/images/RR/rr-blue-canvas.png" alt="Rumpe Ristern Blue Canvas">
        <img src="{{ site.baseurl }}/assets/images/RR/rr-green-canvas.png" alt="Rumpe Ristern Green Canvas">
        <img src="{{ site.baseurl }}/assets/images/RR/rr-orange-canvas.png" alt="Rumpe Ristern Orange Canvas">
        <video autoplay loop muted>
          <source src="{{ site.baseurl }}/assets/images/RR/rr-animation.mp4" type="video/mp4">
        </video>
        <video autoplay loop muted>
          <source src="{{ site.baseurl }}/assets/images/RR/HENK.mp4" type="video/mp4">
        </video>
      </div>
      <p>Where i am from it is typical for many friend groups to create a Concept upon graduating from high school. Usually a group orders their own merch, and releases songs associted with the concept. In regards to this i designed the covers for some of our songs, and design some of the Spotify Canvases used.</p>
    </div>

    <!-- Spotify Canvases -->
    <div class="grid-item large-videos">
      <h2>2022 Spotify Canvases</h2>
      <div class="project-videos">
        <video autoplay loop muted>
          <source src="{{ site.baseurl }}/assets/images/Canvas/pigeland-animation.mp4" type="video/mp4">
        </video>
        <video autoplay loop muted>
          <source src="{{ site.baseurl }}/assets/images/Canvas/Sunroaad.mp4" type="video/mp4">
        </video>
      </div>
      <p>In 2022 i did a couple of spotify canvases. Some are animated using After Effects, and some using Procreate. Here is a commision for a spotifyCanvas animation for Pigeland 2022</p>
    </div>

    <!-- Hybrida Student Union Project -->
    <div class="grid-item">
      <h2>2022 20th Anneversary Hybrida Student Union</h2>
      <div class="project-images vertical-stack">
        <img src="{{ site.baseurl }}/assets/images/Hybrida/hybrida-crewneck-v1.jpg" alt="Hybrida Crewneck Design 1">
        <img src="{{ site.baseurl }}/assets/images/Hybrida/hybrida-crewneck-v2.jpg" alt="Hybrida Crewneck Design 2">
      </div>
      <video autoplay loop muted width="100%">
        <source src="{{ site.baseurl }}/assets/images/Hybrida/hybrida-warehouse-anniversary.mp4" type="video/mp4">
      </video>
      <p>Some design iterations for a crewneck design used for the merch for the 20th jubeleum of the student union Hybrida. In addition i did a render which was used as a background animation at the closing party for the week long event.</p>
    </div>

    <!-- Original Graphics -->
    <div class="grid-item full-width">
      <h2>2021 Original Graphics</h2>
      <div class="project-images">
        <img src="{{ site.baseurl }}/assets/images/OriginalGraphics/og-many-kisses.png" alt="Many Kisses Artwork">
        <img src="{{ site.baseurl }}/assets/images/OriginalGraphics/og-abstract-1.png" alt="Original Artwork">
      </div>
      <p>Enjoy playing around with graphics, here are some...</p>
    </div>

    <!-- Black Sketches -->
    <div class="grid-item full-width">
      <h2>Black Sketches</h2>
      <div class="project-images">
        <img src="{{ site.baseurl }}/assets/images/BlackScetches/bs-daily-1.png" alt="Daily Sketch 1">
        <img src="{{ site.baseurl }}/assets/images/BlackScetches/bs-sketch-1.png" alt="Black Sketch 1">
        <img src="{{ site.baseurl }}/assets/images/BlackScetches/bs-sketch-2.png" alt="Black Sketch 2">
        <img src="{{ site.baseurl }}/assets/images/BlackScetches/bs-sketch-3.png" alt="Black Sketch 3">
        <img src="{{ site.baseurl }}/assets/images/BlackScetches/bs-sketch-4.png" alt="Black Sketch 4">
        <img src="{{ site.baseurl }}/assets/images/BlackScetches/bs-sketch-5.png" alt="Black Sketch 5">
      </div>
      <p>Collection of some fast scetches i have done throught, just for the sake of it':)'</p>
    </div>
  </div>

  <div class="bottom-image">
    <img src="{{ site.baseurl }}/assets/images/BOTTOM.png" alt="Bottom Image">
  </div>
</div>


  <div class="small-header">
    <img src="{{ site.baseurl }}/assets/images/HEADER.png" alt="Site Header">
  </div>


<!-- Media Popup Modal -->
<div class="popup-overlay" id="mediaPopup">
  <div class="popup-content">
    <img id="popupImage" src="" alt="Enlarged image" style="display: none;">
    <video id="popupVideo" controls autoplay loop style="display: none;">
      <source src="" type="video/mp4">
    </video>
  </div>
</div>

<script>
  document.addEventListener('DOMContentLoaded', function() {
    const popup = document.getElementById('mediaPopup');
    const popupImg = document.getElementById('popupImage');
    const popupVideo = document.getElementById('popupVideo');
    
    // Get all images and videos
    const images = document.querySelectorAll('.grid-item img, .project-images img');
    const videos = document.querySelectorAll('.grid-item video, .project-videos video');
    
    // Handle images
    images.forEach(img => {
      img.addEventListener('click', function(e) {
        e.stopPropagation();
        popup.style.display = 'block';
        popupImg.style.display = 'block';
        popupVideo.style.display = 'none';
        popupImg.src = this.src;
        document.body.style.overflow = 'hidden';
      });
    });
    
    // Handle videos
    videos.forEach(video => {
      video.addEventListener('click', function(e) {
        e.stopPropagation();
        popup.style.display = 'block';
        popupImg.style.display = 'none';
        popupVideo.style.display = 'block';
        
        // Get the source from the original video
        const originalSource = this.querySelector('source');
        popupVideo.querySelector('source').src = originalSource.src;
        popupVideo.load(); // Reload the video with new source
        document.body.style.overflow = 'hidden';
      });
    });
    
    // Close popup
    popup.addEventListener('click', function() {
      popup.style.display = 'none';
      document.body.style.overflow = '';
      popupVideo.pause(); // Pause video when closing
    });
    
    // Prevent closing when clicking the media itself
    popupImg.addEventListener('click', function(e) {
      e.stopPropagation();
    });
    
    popupVideo.addEventListener('click', function(e) {
      e.stopPropagation();
    });
    
    // Close on escape key
    document.addEventListener('keydown', function(e) {
      if (e.key === 'Escape') {
        popup.style.display = 'none';
        document.body.style.overflow = '';
        popupVideo.pause(); // Pause video when closing
      }
    });
  });
</script>


