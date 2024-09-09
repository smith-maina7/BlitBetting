<script setup></script>

<template>
  <main>
    <section class="hero">
      <img
        src="../assets/Images/Others/background hero.avif"
        alt="background image"
        class="hero-image"
      />
      <div class="hero-content">
        <h1>Revolutionized Betting</h1>
        <p>Best online odds</p>
        <p>Fastest Cashout</p>
        <p>Highest payout</p>
        <div class="promo">
          <p>Bet Shs100 and get 1000 in bonus bets</p>
        </div>
        <router-link to="/"> <button class="cta-button">Sign Up Now</button></router-link>
      </div>
    </section>
    <section class="app-info">
      <div class="app-img">
        <img src="../assets/Images/Others/blitz mobile.jpg" alt="mobile image" />
      </div>
      <div class="app-msg">
        <h4>The Betting World At Your Fingertips</h4>

        <p>
          The Betting Blitz app provides the definitive betting experience on your mobile or tablet.
          Get quick prices on thousands of markets and be in the thick of the action with live
          streaming and advanced in-play scoreboards. Bet, watch, cash out, and more - wherever and
          whenever you choose!
        </p>
        <div class="download-buttons">
          <a href="https://apps.apple.com" target="_blank" class="app-store">
            <!-- remember to replace the download link with the correct path -->
            <img src="../assets/Images/Others/appstore-image.png" alt="Download on the App Store" />
          </a>
          <a href="https://play.google.com" target="_blank" class="google-play">
            <!-- remember to replace the download link with the correct path -->
            <img src="../assets/Images/Others/google-play-image.png" alt="Get it on Google Play" />
          </a>
        </div>
      </div>
    </section>
    <section class="online-betting">
      <div class="online-img">
        <img src="../assets/Images/Others/online-community.png" alt="online market" />
      </div>
      <div class="online-msg">
        <h4>Online Betting Community</h4>
        <p>
          Join the world's largest and most popular online betting community. Engage with thousands
          of players, share your favorite sports, and trade bets with friends and family. Create and
          manage your own betting accounts, track your progress, and enjoy the best of sports while
          making lots of money
        </p>
        <router-link to="/"> <button class="cta-button">Sign Up Now</button></router-link>
      </div>
    </section>
    <section class="customer-care">
      <div class="cc-img">
        <img src="../assets/Images/Others/customer-care.png" alt="Our customer department" />
      </div>
      <div class="cc-msg">
        <h4>Customer Care</h4>
        <p>
          We are here to help you with any questions, concerns, or issues you might have. Contact
          our customer support team by phone, email, or live chat. We're always here to help you
          find the best odds, manage your bets, and enjoy the best of sports
        </p>
        <button class="phone-number">123-456-7890</button>
        <button class="email-link">customer@example.com</button>
      </div>
    </section>
  </main>
</template>
