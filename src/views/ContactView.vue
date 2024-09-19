<template>
  <div class="section">
    <div class="contact-content fade-in">
      <div class="container">
        <div class="row">
          <div class="contact-form slide-up">
            <form action="https://formspree.io/f/xyzgaeyn" method="POST">
              <div class="form-group">
                <div class="input-group">
                  <label for="first-name">First Name:</label>
                  <input type="text" name="first-name" id="first-name" required />
                </div>
                <div class="input-group">
                  <label for="last-name">Last Name:</label>
                  <input type="text" name="last-name" id="last-name" required />
                </div>
              </div>
              <div class="input-group">
                <label for="email">Email:</label>
                <input type="email" name="email" id="email" required />
              </div>
              <div class="input-group">
                <label for="message">Message:</label>
                <textarea name="message" id="message" rows="4"></textarea>
              </div>
              <button type="submit" class="submit-button scale-in">Send</button>
            </form>
          </div>
          <div class="contact-info slide-up">
            <div class="info-grid">
              <div class="info-item fade-in">
                <i class="bi bi-geo-alt-fill"></i>
                <h5>Address</h5>
                <p>Manenberg, Cape Town<br />Western Cape, 7764</p>
              </div>
              <div class="info-item fade-in">
                <i class="bi bi-telephone-fill"></i>
                <h5>Phone</h5>
                <p>0693527503</p>
              </div>
              <div class="info-item fade-in">
                <i class="bi bi-envelope-at-fill"></i>
                <h5>Email</h5>
                <p>amyj62450@gmail.com</p>
              </div>
              <div class="info-item fade-in">
                <i class="bi bi-hand-thumbs-up-fill"></i>
                <h5>Socials</h5>
                <div class="social-links">
                  <a href="https://www.linkedin.com/in/amy-johnson-5328b924a/" target="_blank">
                    <i class="bi bi-linkedin"></i>
                </a>
                  <a href="https://github.com/amyj0hn" target="_blank"
                    >
                    <i class="bi bi-github"></i>
                </a>
                </div>
              </div>
            </div>
          </div>

        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
/* CONTACT SECTION */
.contact-section {
  min-height: 80vh;
  display: flex;
  flex-direction: column;
  margin-top: 60px;
  padding: 2rem;
  text-align: center;
}

/* Fade-in Animation */
.fade-in {
  opacity: 0;
  animation: fadeIn 1s forwards;
}

@keyframes fadeIn {
  to {
    opacity: 1;
  }
}

.contact-header h1 {
  margin-bottom: 0.5rem;
  font-weight: bold;
}

.contact-header p {
  color: #666;
  margin-bottom: 2rem;
}

/* Slide-up Animation */
.slide-up {
  opacity: 0;
  transform: translateY(20px);
  animation: slideUp 1s forwards;
}

@keyframes slideUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.contact-content {
  display: flex;
  flex: 1;
  justify-content: center;
  align-items: center;
  margin-top: 2rem;
  height: 60vh;
}

.contact-form {
  flex: 1;
  max-width: 40%;
}

.contact-info {
  flex: 1;
  max-width: 50%;
}

.info-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 2rem;
}

.form-group {
  display: flex;
  justify-content: space-between;
}

.input-group {
  font-weight: bold;
  flex: 1;
  display: flex;
  flex-direction: column;
  margin-bottom: 1rem;
  padding: 0 1rem;
}

.input-group input,
.input-group textarea {
  padding: 0.5rem;
  border: 1px solid #000;
  width: 100%;
}

/* Scale-in Animation */
.scale-in {
  opacity: 0;
  transform: scale(0.9);
  animation: scaleIn 0.5s forwards;
}

@keyframes scaleIn {
  to {
    opacity: 1;
    transform: scale(1);
  }
}

.submit-button {
  padding: 0.5rem 1rem;
  background-color: #d2b48c;
  color: #fff;
  border: none;
  cursor: pointer;
  margin-top: 1rem;
}

.info-item {
  display: flex;
  align-items: flex-start;
  flex-direction: column;
}

.info-item h5 {
  font-size: 1rem;
  font-weight: bold;
  color: #333;
}

.info-item p {
  margin: 0;
  color: #666;
}

/* Social Links */
.social-links a {
 
  margin: 10rem 0.5rem;

}

.row {
  display: flex;
  justify-content: space-between;
}

.bi{
  color: #533E2D;
  font-size: 30px;
}

/* Media queries */
@media screen and (max-width: 768px) {
  .contact-content .row {
    flex-direction: column;
    align-items: center;
  }
  .contact-form .info-grid{
    width: 100%;
    margin-bottom: 20px;
  }
}
</style>