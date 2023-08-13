<script>
  // components

  // stores
  import { URL, companyName, industry, cityAndState, pages, services } from "$lib/config"
  import { page } from "$app/stores"
  // styles
  import "$styles/home.less"

  // logic
  const thisPage = pages.find((p) => p.path === $page.route.id)
</script>

<svelte:head>
  <!-- preload hero imgs -->
  <!-- <link rel="preload" as="image" href="/heromobile.webp" />
  <link rel="preload" as="image" href="/hero.webp" /> -->
  <meta property="og:title" content="" />
  <link rel="canonical" href={URL} />
  <meta property="og:url" content={URL} />
  <meta name="description" content={thisPage?.metaDescription} />
  <meta property="og:description" content={thisPage?.metaDescription} />
  <title>{companyName} | {industry} | {cityAndState}</title>
</svelte:head>

<section id="landing">
  <picture>
    <source media="(max-width: 767px)" srcset="/hero-mobile.jpg" />
    <source media="(min-width: 768px)" srcset="/hero.jpg" />
    <img aria-hidden="true" decoding="async" src="/hero.jpg" alt="hero" width="800" height="450" />
  </picture>
  <div class="content">
    <span>Highest Rated Dealer</span>
    <h1>Car Dealership in Tulsa, Ok</h1>
    <p>
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Voluptates adipisci et magni
      laborum, voluptatibus omnis soluta numquam neque eaque inventore.
    </p>
    <a href="/" class="cta">Explore Vehicles</a>
  </div>
</section>
