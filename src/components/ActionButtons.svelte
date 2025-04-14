<style>
  .buttons {
    background-color: #FFE900;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 1rem;
  }

  .btn {
    padding: 1.5rem;
    border: none;
    font-size: 1rem;
    cursor: pointer;
    border-radius: 8px;
    background: transparent;
    display: flex;
    align-items: center;
    gap: 0.5rem;
    text-decoration: none;
    color: #000;
  }

  .fliped{
    transform: scaleX(-1);
  }

</style>

<div class="buttons">
  <a class="btn" href="https://wa.me/5491122518844" target="_blank" aria-label="WhatsApp">
    <i class="fab fa-whatsapp"></i>
  </a>

  <a class="btn fliped" href="tel:+5491122518844" aria-label="Teléfono">
    <i class="fas fa-phone"></i>
  </a>

  <button class="btn" aria-label="Compartir">
    <i class="fas fa-share-alt"></i>
  </button>
</div>