<script>
  import '../styles/global.css'
  import Navbar from '../components/Navbar.svelte';
  import HeroImage from '../components/HeroImage.svelte';
  import ActionButtons from '../components/ActionButtons.svelte';
  import MenuAccordion from '../components/MenuAccordion.svelte';

  const menu = [
    {
      title:'Destacados',
      sub_title:null,
      recipes:[
        {
          recipe_title:'Pinta de cerveza',
          image:'https://placehold.co/64x64/golden/white',
          ingredientes:'473ml',
          precio:[
            { price_title:'IPA', price:6000 },
            { price_title:'APA', price:6000 },
            { price_title:'BLONDE', price:6000 },
            { price_title:'HONEY', price:6000 }
          ]
        },
        {
          recipe_title:'Promo Jarra',
          image:'https://placehold.co/64x64/golden/white',
          ingredientes:'1 litro',
          precio:[
            { price_title:'Jarra de Fernet', price:19000 },
            { price_title:'Jarra de Campari', price:19000 },
            { price_title:'Jarra de Destornillador', price:19000 }
          ]
        },
          ]
    },
    {
      title:'Hamburguesas',
      sub_title:'Todas incluyen papas',
      recipes:[
        {
          recipe_title:'hamburguesa clasica',
          image:'https://placehold.co/64x64/golden/white',
          ingredientes:'Hamburguesa de res 120 grs. Sola o con queso. Acompañada con papas y coleslaw.',
          precio:[ { price_title:'Para 1', price:13000 } ]
        },
        {
          recipe_title:'hamburguesa clasica Doble',
          image:'https://placehold.co/64x64/golden/white',
          ingredientes:'Doble medallón de res de 120gr c/u. Opcional queso. Acompañada con papas y coleslaw.',
          precio:[ { price_title:'Para 1', price:14500 } ]
        },
        {
          recipe_title:'hamburguesa Popeye',
          image:'https://placehold.co/64x64/golden/white',
          ingredientes:'Doble hambrguesa de res de 120 grs c/u, cebolla caramelizada, panceta, rúcula, y queso pategrás. Acompañadas de papas rústicas y coleslaw.',
          precio:[ { price_title:'Para 1', price:15500 } ]
        },
      ]
    },
    {
      title:'Pizzas',
      sub_title:'Estilo Napolitano',
      recipes:[
        {
          recipe_title:'PIZZA MUZZARELLA',
          image:'https://placehold.co/64x64/golden/white',
          ingredientes:'Salsa de tomate, muzzarella y orégano.',
          precio:[
            { price_title:'Para 2', price:18000 },
            { price_title:'Para 3', price:21000 },
            { price_title:'Para 4', price:24000 },
          ]
        },
        {
          recipe_title:'Pizza Tex Mex',
          image:'https://placehold.co/64x64/golden/white',
          ingredientes:'Salsa de tomate, muzzarella, salchichas, barbacoa y nachos.',
          precio:[
            { price_title:'Para 2', price:18000 },
            { price_title:'Para 3', price:21000 },
            { price_title:'Para 4', price:24000 },
          ]
        },
        {
          recipe_title:'Pizza Verde',
          image:'https://placehold.co/64x64/golden/white',
          ingredientes:'Salsa de tomate, muzzarella, rúcula, parmesano rallado, aceite de oliva.',
          precio:[
            { price_title:'Para 2', price:18000 },
            { price_title:'Para 3', price:21000 },
            { price_title:'Para 4', price:24000 },
          ]
        },
      ]
    },
    {
      title:'Picadas',
      sub_title:null,
      recipes:[
        {
          recipe_title:'Picada de la casa',
          image:'https://placehold.co/64x64/golden/white',
          ingredientes:'Jamón, salame, panceta, queso fontina, queso azul, albóndigas de carne, salchichas, papas fritas, nuggets de pollo, aceitunas verdes, pepinillos, tomatitos cherry y nueces.',
          precio:[
            { price_title:'Para 2', price:18000 },
            { price_title:'Para 3', price:21000 },
            { price_title:'Para 4', price:24000 },
          ]
        },
      ]
    },
  ];


</script>

<style>
  *{
    margin: 0;
    padding: 0;
  }
  .om_body {
    margin: 0;
    font-family: sans-serif;
  }
</style>

<div class="om_body">
  <Navbar />
  <HeroImage />
  <ActionButtons />
  <MenuAccordion {menu} />

</div>