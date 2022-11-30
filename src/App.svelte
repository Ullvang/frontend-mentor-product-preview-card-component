<script>
  import Footer from "./lib/Footer.svelte";
</script>

<main>
  <picture>
    <source
      media="(max-width:700px)"
      srcset="/images/image-product-mobile.jpg"
    />
    <img src="/images/image-product-desktop.jpg" alt="chanel perfume" />
  </picture>
  <div id="text">
    <p id="overline">Perfume</p>
    <h1>Gabrielle Essence Eau De Parfum</h1>
    <p id="paragraph">
      A floral, solar and voluptuous interpretation composed by Olivier Polge,
      Perfumer-Creator for the House of CHANEL.
    </p>
    <p id="price">
      $149.99
      <span>$169.99</span>
    </p>
    <button> Add to Cart </button>
  </div>
</main>
<Footer />

<style>
  main {
    max-width: 600px;
    min-height: 450px;
    display: flex;
    background-color: var(--white);
    border-radius: 10px;
    overflow: hidden;
    margin: 28px 16px;
    grid-row-start: 2;
  }
  img,
  picture {
    max-width: 300px;
  }
  button {
    color: var(--white);
    background-color: var(--dark-cyan);
    border: none;
    border-radius: 8px;
    padding: 15px 62px 15px 63px;
    width: 100%;
  }
  button:hover {
    background-color: var(--deep-aquamaringe);
  }

  picture {
    max-height: 450px;
  }

  #text {
    padding: 32px 31.5px;
  }
  #overline {
    text-transform: uppercase;
    font-size: 12px;
    margin-bottom: 20px;
    letter-spacing: 5px;
  }
  #paragraph {
    line-height: 23px;
    margin-bottom: 29px;
  }
  #price {
    margin-bottom: 30px;
    font-size: 32px;
    font-family: var(--fraunces);
    font-weight: bold;
    color: var(--dark-cyan);
    line-height: 32px;
    display: flex;
    align-items: center;
  }
  span {
    text-decoration: line-through;
    color: var(--dark-grayish-blue);
    font-size: 13px;
    font-weight: 500;
    line-height: 23px;
    margin-left: 19px;
  }

  @media only screen and (max-width: 700px) {
    main {
      flex-direction: column;
      width: calc(100% - 32px);
      max-width: 343px;
      min-height: 611px;
      grid-row-start: 1;
    }
    img {
      max-width: 100%;
      height: 240px;
      object-fit: cover;
    }
    picture {
      height: 240px;
      max-width: 343px;
    }
    #text {
      padding: 24px;
    }
    #overline {
      margin-bottom: 12px;
    }
    h1 {
      margin-bottom: 16px;
    }
    #paragraph {
      margin-bottom: 24px;
    }
    #price {
      margin-bottom: 20px;
    }
  }
</style>
