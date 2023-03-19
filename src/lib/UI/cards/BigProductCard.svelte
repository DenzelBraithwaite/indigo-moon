<script>
import { onMount } from 'svelte';

export let src;
export let alt;
export let title;
export let cost;
export let description;
export let bgColor;

onMount(() => {
    window.scrollTo({
    top: 0,
    left: 0,
  })
});
</script>

<div class="product-wrapper">
    <img class="product-img" {src} alt={alt}>
    <div class="product-wrapper-right">
      <h1>{title}</h1>
      <h2 class="cost">{cost}</h2>
      <p class="description">{description}</p>
      <a class="btn__buy {bgColor}"  href="mailto:tiffany@indigomoontarot.com">Buy Now</a>
    </div>
  </div>

  <style>
    .product-wrapper {
      position: relative;
      background-color: #ffffff;
      color: #444;
      margin: 8rem auto 5rem;
      max-width: 900px;
      text-align: center;
      box-shadow: 0px 2px 8px #0000001a;
      border-radius: 1rem;
      display: flex;
      justify-content: center;
      align-items: stretch;
      gap: 0;
      padding: 0;
    }

    .product-img {
    position: relative;
    width: 450px;
    height: 450px;
    border-radius: 1rem 0 0 1rem;
  }

  .product-wrapper-right {
    width: 550px;
    border-radius: 0 1rem 1rem 0;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
  }

  .description {
    width: 70%;
  }

  .cost {
    font-size: 3rem;
  }

  p {
      padding: 0;
      margin: 0;
  }

  .btn__buy:link,
  .btn__buy:visited {
    display: inline-block;
    transition: background-color 0.1s ease-in;
    text-decoration: none;
    border: none;
    color: #fff;
    width: 70%;
    text-align: center;
    font-size: 1.125rem;
    padding: 0.75rem 1rem;
    border-radius: 0.5rem;
    margin-bottom: 1.25rem;
    box-shadow: 0 2px 8px #0000001c; /* var(--secondary-purple), transparent*/
  }
  
  .btn__buy:active,
  .btn__buy:hover {
    box-shadow: 0 2px 10px #00000013; /* var(--secondary-purple), transparent*/
  }

  /* Button colors */
  .blue {
    background-color: #51a3e6;
  }

  .blue:hover,
  .blue:active {
    background-color: #60b2f5;
  }

  .orange {
    background-color: #D8690D;
  }

  .orange:hover,
  .orange:active {
    background-color: #fa892c;
  }

  .red {
    background-color: #c0381c;
  }

  .red:hover,
  .red:active {
    background-color: #e05034;
  }

  .green {
    background-color: #A3D53E;
  }

  .green:hover,
  .green:active {
    background-color: #b2e253;
  }

  .purple {
    background-color: #aa7bb1;
  }

  .purple:hover,
  .purple:active {
    background-color: #c695ce;
  }

  .yellow {
    background-color: #DCBA13;
  }

  .yellow:hover,
  .yellow:active {
    background-color: #f7db54;
  }

  .indigo {
    background-color: #5950A1;
  }

  .indigo:hover,
  .indigo:active {
    background-color: #7165c7;
  }

  .default {
    background-color: var(--secondary-purple);
  }

  .default:hover,
  .default:active {
    background-color: #95719b;
  }

  @media(max-width: 1000px) {
    .product-wrapper {
      margin: 10rem auto 5rem;
      min-width: 360px;
      max-width: 600px;
      width: 70%;

      flex-direction: column;
      justify-content: end;
    }

    .product-img {
      border-radius: 1rem 1rem 0 0;
      width: 100%;
    }

    .product-wrapper-right {
      border-radius: 0 0 1rem 1rem;
      background-color: #fff;
      width: 100%;

      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: space-between;
    }

    .btn__buy:link {
      margin: 1.5rem auto;
    }
  }

  @media (max-width: 450px) {
    .product-wrapper {
      margin: 3rem auto 5rem;
    }

    .cost {
      font-size: 2.5rem;
    }
  }
  </style>