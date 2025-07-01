<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Drink Menu Grid</title>
  <style>
    /* Base styles */
    body {
      font-family: sans-serif;
      margin: 0;
      padding: 2rem;
      background-color: #f8f8f8;
      color: #00bfcf; /* Rebel Teal font color */
    }
    .search-container {
      position: relative;
      margin-bottom: 1rem;
      width: 100%;
    }
    #drink-search {
      width: 100%;
      padding: 0.5rem 1rem 0.5rem 2.5rem;
      font-size: 1rem;
      font-weight: bold;
      border: 2px solid #d9326f; /* Defiance Berry border */
      background-color: white;
      color: #00bfcf; /* Rebel Teal text */
      border-radius: 9999px;
      box-sizing: border-box;
    }
    #drink-search::placeholder {
      color: #d9326f; /* Defiance Berry placeholder */
      opacity: 0.7;
    }
    .search-container svg {
      position: absolute;
      top: 50%;
      left: 1rem;
      transform: translateY(-50%);
      fill: #d9326f; /* Defiance Berry icon */
      width: 1rem;
      height: 1rem;
      pointer-events: none;
    }
    #menu-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      gap: 1rem;
    }
    .drink.category.col {
      background: transparent;
      border-radius: 8px;
      overflow: visible;
      position: relative;
      text-align: center;
      padding: 0.5rem;
      cursor: pointer;
      transition: color 0.3s ease;
      color: #00bfcf; /* Rebel Teal font color */
    }
    .drink.category.col:hover h3 {
      color: #d9326f; /* Defiance Berry hover text */
    }
    .image-wrapper {
      position: relative;
      overflow: visible;
      z-index: 0;
    }
    .image-wrapper img {
      width: 100%;
      height: auto;
      display: block;
      transition: transform 0.3s ease;
      z-index: 0;
      border-radius: 8px;
    }
    .drink.category.col:hover .image-wrapper img {
      transform: scale(1.2);
    }
    .frame {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      box-shadow: inset 0 0 0 2px rgba(0, 0, 0, 0.05);
      border-radius: 8px;
      pointer-events: none;
    }
    h3 {
      margin: 0;
      padding: 1rem 0 0 0;
      font-size: 1rem;
      color: inherit; /* inherit font color */
      transition: color 0.3s ease;
    }
    .menu-item-link {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 1;
      text-indent: -9999px;
      overflow: hidden;
    }
    .section-heading.menu-page-title {
      text-align: center;
      margin-bottom: 2rem;
      color: #00bfcf; /* Rebel Teal */
    }
  </style>
</head>
<body>

  <div class="section-heading menu-page-title">
    <h1>MENU</h1>
  </div>

  <div class="search-container">
    <svg viewBox="0 0 24 24" aria-hidden="true" focusable="false">
      <path d="M15.5 14h-.79l-.28-.27A6.471 6.471 0 0016 9.5 6.5 6.5 0 109.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zM10 14a4 4 0 110-8 4 4 0 010 8z"/>
    </svg>
    <input 
      type="text" 
      id="drink-search" 
      placeholder="SEARCH BY NAME OR INGREDIENT" 
      class="form-text" 
      aria-label="SEARCH BY NAME OR INGREDIENT" />
  </div>

  <div id="menu-grid" class="dbros-drink-menu parent grid gap-xs">
    <!-- 25 cards with data attributes for juice, fruit, sorbet -->
    <div class="drink category col" 
         data-juice="Mango,Pineapple" 
         data-fruit="Mango,Pineapple" 
         data-sorbet="Passion">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/512px2/DB-MayJune_Updated_SectionImage_512.png" alt="Survivor" />
        <div class="frame"></div>
      </div>
      <h3>Survivor</h3>
      <a class="menu-item-link" title="Survivor" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Clementine" 
         data-fruit="Strawberry,Mango" 
         data-sorbet="Passion,Coconut">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/categories/Classics.png" alt="Captain" />
        <div class="frame"></div>
      </div>
      <h3>Captain</h3>
      <a class="menu-item-link" title="Captain" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Peach,Mango" 
         data-fruit="Peach,Mango" 
         data-sorbet="Passion,Coconut,Mango">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/512px2/Protein_Coffee_Digital_Batch1_SeasonalImage.png" alt="Explorer" />
        <div class="frame"></div>
      </div>
      <h3>Explorer</h3>
      <a class="menu-item-link" title="Explorer" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Strawberry,Watermelon" 
         data-fruit="Pineapple,Dragon" 
         data-sorbet="Dragon">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/512px2/h_bln_frz_PICTURE_PERFECT_chc_car_512.png" alt="Drifter" />
        <div class="frame"></div>
      </div>
      <h3>Drifter</h3>
      <a class="menu-item-link" title="Drifter" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Pineapple" 
         data-fruit="Pineapple" 
         data-sorbet="Coconut">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/512px2/DB-MayJune_Updated_SectionImage_512.png" alt="Nudist" />
        <div class="frame"></div>
      </div>
      <h3>Nudist</h3>
      <a class="menu-item-link" title="Nudist" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Peach" 
         data-fruit="Peach" 
         data-sorbet="Mango,Coconut">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/categories/Classics.png" alt="Peacekeeper" />
        <div class="frame"></div>
      </div>
      <h3>Peacekeeper</h3>
      <a class="menu-item-link" title="Peacekeeper" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Berry Patch,Clementine" 
         data-fruit="Cherries,Peach" 
         data-sorbet="Acai,Mango,Passion">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/512px2/Protein_Coffee_Digital_Batch1_SeasonalImage.png" alt="Creator" />
        <div class="frame"></div>
      </div>
      <h3>Creator</h3>
      <a class="menu-item-link" title="Creator" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Blackberry,Peach" 
         data-fruit="Cherries,Pomegranate" 
         data-sorbet="Acai,Passion">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/512px2/h_bln_frz_PICTURE_PERFECT_chc_car_512.png" alt="Lover" />
        <div class="frame"></div>
      </div>
      <h3>Lover</h3>
      <a class="menu-item-link" title="Lover" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Peach,Watermelon" 
         data-fruit="Peach,Pomegranate" 
         data-sorbet="Mango,Coconut">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/512px2/DB-MayJune_Updated_SectionImage_512.png" alt="Professor" />
        <div class="frame"></div>
      </div>
      <h3>Professor</h3>
      <a class="menu-item-link" title="Professor" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Berry Patch" 
         data-fruit="Peach,Pomegranate" 
         data-sorbet="Acai">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/categories/Classics.png" alt="Guardian" />
        <div class="frame"></div>
      </div>
      <h3>Guardian</h3>
      <a class="menu-item-link" title="Guardian" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Berry Patch" 
         data-fruit="Blueberry,Raspberry" 
         data-sorbet="Acai,Coconut">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/512px2/Protein_Coffee_Digital_Batch1_SeasonalImage.png" alt="Poet" />
        <div class="frame"></div>
      </div>
      <h3>Poet</h3>
      <a class="menu-item-link" title="Poet" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Strawberry,Blackberry" 
         data-fruit="Strawberry,Raspberry" 
         data-sorbet="Acai,Passion">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/512px2/h_bln_frz_PICTURE_PERFECT_chc_car_512.png" alt="Dreamer" />
        <div class="frame"></div>
      </div>
      <h3>Dreamer</h3>
      <a class="menu-item-link" title="Dreamer" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Berry Patch" 
         data-fruit="Strawberry,Blueberry" 
         data-sorbet="Passion">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/512px2/DB-MayJune_Updated_SectionImage_512.png" alt="Artisan" />
        <div class="frame"></div>
      </div>
      <h3>Artisan</h3>
      <a class="menu-item-link" title="Artisan" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Strawberry,Blackberry" 
         data-fruit="Dragon,Blueberry" 
         data-sorbet="Dragon,Acai">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/categories/Classics.png" alt="Dancer" />
        <div class="frame"></div>
      </div>
      <h3>Dancer</h3>
      <a class="menu-item-link" title="Dancer" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Berry Patch,Clementine" 
         data-fruit="Blue,Raspberry,Strawberry,Peach" 
         data-sorbet="Acai,Mango,Coconut">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/512px2/Protein_Coffee_Digital_Batch1_SeasonalImage.png" alt="Playwright" />
        <div class="frame"></div>
      </div>
      <h3>Playwright</h3>
      <a class="menu-item-link" title="Playwright" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Mango,Pineapple" 
         data-fruit="Mango,Pineapple" 
         data-sorbet="Passion">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/512px2/h_bln_frz_PICTURE_PERFECT_chc_car_512.png" alt="Rebel" />
        <div class="frame"></div>
      </div>
      <h3>Rebel</h3>
      <a class="menu-item-link" title="Rebel" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Clementine" 
         data-fruit="Raspberry" 
         data-sorbet="Mango,Dragon">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/512px2/DB-MayJune_Updated_SectionImage_512.png" alt="Activist" />
        <div class="frame"></div>
      </div>
      <h3>Activist</h3>
      <a class="menu-item-link" title="Activist" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Watermelon,Strawberry" 
         data-fruit="Cherry,Strawberry" 
         data-sorbet="Passion">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/categories/Classics.png" alt="Catalyst" />
        <div class="frame"></div>
      </div>
      <h3>Catalyst</h3>
      <a class="menu-item-link" title="Catalyst" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Blackberry,Clementine" 
         data-fruit="Dragon,Raspberry" 
         data-sorbet="Dragon,Passion">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/512px2/Protein_Coffee_Digital_Batch1_SeasonalImage.png" alt="Visionary" />
        <div class="frame"></div>
      </div>
      <h3>Visionary</h3>
      <a class="menu-item-link" title="Visionary" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Blackberry,Peach" 
         data-fruit="Pomegranate,Peach" 
         data-sorbet="Acai,Mango">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/512px2/h_bln_frz_PICTURE_PERFECT_chc_car_512.png" alt="Optimist" />
        <div class="frame"></div>
      </div>
      <h3>Optimist</h3>
      <a class="menu-item-link" title="Optimist" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Pineapple" 
         data-fruit="Pineapple,Mango" 
         data-sorbet="Matcha">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/512px2/DB-MayJune_Updated_SectionImage_512.png" alt="Stargazer" />
        <div class="frame"></div>
      </div>
      <h3>Stargazer</h3>
      <a class="menu-item-link" title="Stargazer" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Mango,Peach" 
         data-fruit="Pineapple,Peach" 
         data-sorbet="Matcha,Coconut">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/categories/Classics.png" alt="Palm Reader" />
        <div class="frame"></div>
      </div>
      <h3>Palm Reader</h3>
      <a class="menu-item-link" title="Palm Reader" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Pineapple,Watermelon" 
         data-fruit="Mango,Peach" 
         data-sorbet="Matcha,Passion">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/512px2/Protein_Coffee_Digital_Batch1_SeasonalImage.png" alt="Oracle" />
        <div class="frame"></div>
      </div>
      <h3>Oracle</h3>
      <a class="menu-item-link" title="Oracle" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Berry Patch" 
         data-fruit="Blueberry,Raspberry" 
         data-sorbet="Matcha,Acai">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/512px2/h_bln_frz_PICTURE_PERFECT_chc_car_512.png" alt="Philosopher" />
        <div class="frame"></div>
      </div>
      <h3>Philosopher</h3>
      <a class="menu-item-link" title="Philosopher" href="#"></a>
    </div>

    <div class="drink category col" 
         data-juice="Strawberry" 
         data-fruit="Blue,Raspberry,Strawberry,Cherry" 
         data-sorbet="Matcha,Acai,Dragon">
      <div class="image-wrapper">
        <img loading="lazy" src="https://files.dutchbros.com/website/menu/drink-images-v2/categories/Classics.png" alt="Yogi" />
        <div class="frame"></div>
      </div>
      <h3>Yogi</h3>
      <a class="menu-item-link" title="Yogi" href="#"></a>
    </div>
  </div>

  <script>
    const searchInput = document.getElementById('drink-search');
    const cards = document.querySelectorAll('#menu-grid .drink');

    searchInput.addEventListener('input', () => {
      const query = searchInput.value.trim().toLowerCase();

      cards.forEach(card => {
        const name = card.querySelector('h3').textContent.toLowerCase();
        const juice = card.dataset.juice.toLowerCase();
        const fruit = card.dataset.fruit.toLowerCase();
        const sorbet = card.dataset.sorbet.toLowerCase();

        const combined = name + " " + juice + " " + fruit + " " + sorbet;

        if (combined.includes(query)) {
          card.style.display = '';
        } else {
          card.style.display = 'none';
        }
      });
    });
  </script>

</body>
</html>
