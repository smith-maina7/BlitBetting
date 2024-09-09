<script setup>
// const scrollToTop = () => {
//   window.scrollTo({
//     top: 0,
//     behavior: 'smooth'
//   })
// }
// Remember to work on smooth scrolling
</script>

<template>
  <footer class="site-footer">
    <div class="footer-content">
      <div class="back-to-top">
        <router-link to="/">&#94; <br />Back to Top</router-link>
        <hr class="top-divider" />
      </div>

      <div class="footer-columns">
        <div class="column">
          <h4>Our Apps</h4>
          <a href="https://apps.apple.com" target="blank">
            <img src="../assets/Images/Others/appstore-image.png" alt="Download on the App Store" />
          </a>
          <a href="https://play.google.com" target="blank">
            <img src="../assets/Images/Others/google-play-image.png" alt="Get it on Google Play" />
          </a>
        </div>
        <div class="column">
          <h4>Find Us</h4>
          <p>Phone: 123-456-7890</p>
          <p>Email: <a href="mailto:customer@example.com">customer@example.com</a></p>
          <a href="#">Your Feedback</a>
        </div>
        <div class="column">
          <h4>Credentials</h4>
          <p>We are regulated by the Betting Control and Licensing Board of Kenya.</p>
          <p>License No: 12345</p>
        </div>
      </div>
      <div class="social-media">
        <h4>Follow Us</h4>
        <hr class="divider" />
        <a href="#"><img src="../assets/Images/Socials/facebook.png" alt="Facebook" /></a>
        <a href="#"><img src="../assets/Images/Socials/x-logo.png" alt="Twitter" /></a>
        <a href="#"><img src="../assets/Images/Socials/instagram.jpeg" alt="Instagram" /></a>
      </div>
      <div class="footer-bottom">
        <p>&copy; 2024 Your Company Name. All rights reserved.</p>
      </div>
    </div>
  </footer>
</template>
