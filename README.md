# sumit-fancy-store
Official website for Sumit Fancy Store — luxury accessories &amp; cosmetics.  Online shopping site for Sumit Fancy Store.  Elegant black &amp; gold themed e-commerce homepage for Sumit Fancy Store.
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Sumit Fancy Store — Home</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600;700&family=Inter:wght@300;400;600&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#0b0b0b; /* near black */
      --gold:#d4af37; /* classic gold */
      --muted:#bdbdbd;
      --card:#121212;
      --glass: rgba(255,255,255,0.03);
    }

    *{box-sizing:border-box}
    html,body{height:100%;margin:0;font-family:Inter,system-ui,-apple-system,"Segoe UI",Roboto,"Helvetica Neue",Arial;background:linear-gradient(180deg,var(--bg),#050505);color:#fff}
    a{color:inherit;text-decoration:none}

    /* Header */
    header{display:flex;align-items:center;justify-content:space-between;padding:18px 28px;background:transparent;position:sticky;top:0;z-index:40}
    .logo{display:flex;align-items:center;gap:12px}
    .logo svg{height:56px;width:auto}
    .nav{display:flex;gap:18px;align-items:center}
    .nav a{font-weight:600;color:var(--muted)}
    .btn{background:var(--gold);color:#0b0b0b;padding:10px 14px;border-radius:12px;font-weight:700;display:inline-flex;align-items:center;gap:8px}

    /* Hero */
    .hero{display:grid;grid-template-columns:1fr 420px;gap:28px;padding:40px 28px;align-items:center}
    .hero-left{max-width:780px}
    h1{font-family:'Playfair Display', serif;font-size:44px;margin:0 0 12px;line-height:1.02;color:var(--gold)}
    p.lead{margin:0 0 20px;color:var(--muted);font-size:16px}
    .cta-row{display:flex;gap:12px;align-items:center}
    .search{background:var(--card);padding:12px;border-radius:14px;display:flex;gap:8px;align-items:center;width:420px}
    .search input{background:transparent;border:0;outline:0;color:#fff;font-size:15px;width:100%}

    /* Categories */
    .cats{display:flex;gap:12px;margin-top:18px}
    .chip{background:var(--glass);padding:10px 12px;border-radius:999px;font-weight:600;color:var(--muted)}

    /* Featured */
    .featured{padding:28px;}
    .grid{display:grid;grid-template-columns:repeat(4,1fr);gap:18px}
    .card{background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);padding:12px;border-radius:14px;border:1px solid rgba(255,255,255,0.03);}
    .card img{width:100%;height:200px;object-fit:cover;border-radius:10px}
    .card h3{margin:10px 0 6px;font-size:16px;color:#fff}
    .price{font-weight:700;color:var(--gold)}
    .card .meta{display:flex;justify-content:space-between;align-items:center}
    .add{background:transparent;border:1px solid var(--gold);padding:8px 10px;border-radius:10px;color:var(--gold);font-weight:700;cursor:pointer}

    /* Cart Modal */
    .cart-btn{position:relative}
    .cart-count{position:absolute;top:-6px;right:-8px;background:var(--gold);color:#0b0b0b;border-radius:999px;padding:4px 8px;font-weight:700;font-size:12px}
    .cart-panel{position:fixed;right:20px;top:80px;width:360px;max-height:70vh;background:#070707;border-radius:14px;padding:16px;border:1px solid rgba(255,255,255,0.04);box-shadow:0 10px 30px rgba(0,0,0,0.6);overflow:auto;display:none;z-index:80}
    .cart-item{display:flex;gap:12px;align-items:center;padding:10px 0;border-bottom:1px solid rgba(255,255,255,0.03)}
    .cart-item img{width:64px;height:64px;object-fit:cover;border-radius:8px}

    /* Footer */
    footer{padding:28px;border-top:1px solid rgba(255,255,255,0.03);display:flex;justify-content:space-between;align-items:center}

    /* Responsive */
    @media (max-width:1000px){
      .hero{grid-template-columns:1fr;}
      .grid{grid-template-columns:repeat(2,1fr)}
      .search{width:100%}
    }
    @media (max-width:560px){
      h1{font-size:32px}
      .grid{grid-template-columns:1fr}
      header{padding:12px}
      .logo svg{height:44px}
      .hero{padding:20px 12px}
    }
  </style>
</head>
<body>

<header>
  <div class="logo">
    <!-- Simple SVG text logo in gold -->
    <svg viewBox="0 0 500 80" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
      <defs>
        <linearGradient id="g1" x1="0" x2="1">
          <stop offset="0" stop-color="#f5df8a" />
          <stop offset="1" stop-color="#d4af37" />
        </linearGradient>
      </defs>
      <text x="0" y="52" font-family="'Playfair Display', serif" font-weight="700" font-size="42" fill="url(#g1)">Sumit</text>
      <text x="160" y="52" font-family="Inter, sans-serif" font-weight="600" font-size="22" fill="#d4af37">Fancy Store</text>
    </svg>
  </div>

  <nav class="nav">
    <a href="#featured">Featured</a>
    <a href="#shop">Shop</a>
    <a href="#about">About</a>
    <button class="btn cart-btn" id="open-cart"><span>Cart</span><span class="cart-count" id="cart-count">0</span></button>
  </nav>
</header>

<main>
  <section class="hero">
    <div class="hero-left">
      <h1>Luxury accessories. Everyday prices.</h1>
      <p class="lead">Discover elegant hair pieces, jewellery, cosmetics and small gifts — curated for style with a golden touch.</p>

      <div class="cta-row">
        <div class="search" role="search">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="none" aria-hidden><path d="M21 21l-4.35-4.35" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
          <input id="search" placeholder="Search products, e.g. bangles or lip gloss" />
        </div>
        <a class="btn" id="shop-now">Shop Now</a>
      </div>

      <div class="cats" aria-hidden>
        <div class="chip">Jewellery</div>
        <div class="chip">Hair Accessories</div>
        <div class="chip">Cosmetics</div>
        <div class="chip">Gifts</div>
      </div>
    </div>

    <div class="hero-right" aria-hidden>
      <img src="data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='420' height='320'><rect width='100%' height='100%' rx='18' fill='%23070b0b'/><text x='40' y='120' font-family='Playfair Display' font-size='34' fill='%23d4af37'>Elegance</text><text x='40' y='160' font-family='Inter' font-size='18' fill='%23bdbdbd'>New arrivals ready</text></svg>" alt="hero" style="width:100%;border-radius:12px;max-width:420px;"/>
    </div>
  </section>

  <section id="featured" class="featured">
    <h2 style="font-family:'Playfair Display', serif;color:var(--gold);margin:0 0 14px;font-size:28px">Featured products</h2>
    <div class="grid" id="product-grid">
      <!-- Product cards injected by JS -->
    </div>
  </section>

</main>

<!-- Cart panel -->
<div class="cart-panel" id="cart-panel" aria-hidden="true">
  <h3 style="margin:0 0 10px;font-family:'Playfair Display', serif;color:var(--gold)">Your Cart</h3>
  <div id="cart-items"></div>
  <div style="padding-top:12px;display:flex;justify-content:space-between;align-items:center">
    <div style="font-weight:700">Total: <span id="cart-total">₹0</span></div>
    <button class="btn" id="checkout">Checkout</button>
  </div>
</div>

<!-- Simple checkout modal (inline) -->
<div id="checkout-modal" style="display:none;position:fixed;inset:0;background:rgba(0,0,0,0.6);align-items:center;justify-content:center;z-index:120">
  <div style="background:#0b0b0b;padding:18px;border-radius:12px;max-width:480px;width:92%;border:1px solid rgba(255,255,255,0.03)">
    <h3 style="margin:0 0 10px;font-family:'Playfair Display', serif;color:var(--gold)">Checkout</h3>
    <form id="checkout-form">
      <div style="display:flex;flex-direction:column;gap:8px">
        <input name="name" placeholder="Full name" required style="padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:#fff" />
        <input name="phone" placeholder="Phone / WhatsApp" required style="padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:#fff" />
        <input name="address" placeholder="Delivery address" required style="padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:#fff" />
      </div>
      <div style="display:flex;gap:8px;justify-content:flex-end;margin-top:12px">
        <button type="button" id="cancel-checkout" style="background:transparent;border:0;padding:8px 12px;border-radius:8px">Cancel</button>
        <button class="btn" type="submit">Place order</button>
      </div>
    </form>
  </div>
</div>

<footer>
  <div>
    <strong>Sumit Fancy Store</strong><br>
    <small style="color:var(--muted)">Handpicked accessories • Fast delivery</small>
  </div>
  <div style="text-align:right;color:var(--muted)">
    <div>Contact: +91 98765 43210</div>
    <div style="margin-top:6px">Follow us: Instagram • WhatsApp</div>
  </div>
</footer>

<script>
// Sample products — replace with your real catalog when ready
const PRODUCTS = [
  {id:1,name:'Golden Pearl Hair Clip',price:249,img:'https://images.unsplash.com/photo-1529626455594-4ff0802cfb7e?auto=format&fit=crop&w=600&q=60'},
  {id:2,name:'Delicate Bangle Set',price:599,img:'https://images.unsplash.com/photo-1548953787-c3b8a8b9f1c6?auto=format&fit=crop&w=600&q=60'},
  {id:3,name:'Velvet Lipstick - Ruby',price:199,img:'https://images.unsplash.com/photo-1580910051076-17c6f8b0a8d8?auto=format&fit=crop&w=600&q=60'},
  {id:4,name:'Crystal Stud Earrings',price:349,img:'https://images.unsplash.com/photo-1617692837766-3b4b0b8ab9c1?auto=format&fit=crop&w=600&q=60'},
  {id:5,name:'Silk Scrunchie (pack)',price:159,img:'https://images.unsplash.com/photo-1572276596237-6f7d6f5a1f1c?auto=format&fit=crop&w=600&q=60'},
  {id:6,name:'Mini Gift Box - Gold',price:89,img:'https://images.unsplash.com/photo-1523206489230-c012d6a34f67?auto=format&fit=crop&w=600&q=60'},
  {id:7,name:'Nail Art Kit',price:299,img:'https://images.unsplash.com/photo-1522335789203-aabd1fc54bc9?auto=format&fit=crop&w=600&q=60'},
  {id:8,name:'Statement Hair Band',price:399,img:'https://images.unsplash.com/photo-1600180758895-7b80a7e36f5b?auto=format&fit=crop&w=600&q=60'}
];

// Render product cards
const grid = document.getElementById('product-grid');
function renderProducts(list){
  grid.innerHTML='';
  list.forEach(p=>{
    const el = document.createElement('article');
    el.className='card';
    el.innerHTML = `
      <img src="${p.img}" alt="${p.name}" loading="lazy" />
      <h3>${p.name}</h3>
      <div class="meta"><div class="price">₹${p.price}</div><button class="add" data-id="${p.id}">Add</button></div>
    `;
    grid.appendChild(el);
  })
}
renderProducts(PRODUCTS);

// Simple cart stored in localStorage
const CART_KEY = 'sfs_cart_v1';
function getCart(){return JSON.parse(localStorage.getItem(CART_KEY) || '[]')}
function saveCart(c){localStorage.setItem(CART_KEY,JSON.stringify(c))}
function addToCart(id){
  const p = PRODUCTS.find(x=>x.id===+id);
  if(!p) return;
  const c = getCart();
  const existing = c.find(i=>i.id===p.id);
  if(existing) existing.qty++;
  else c.push({id:p.id,name:p.name,price:p.price,img:p.img,qty:1});
  saveCart(c); updateCartUI();
}

// Wire add buttons
document.addEventListener('click',e=>{
  if(e.target.matches('.add')) addToCart(e.target.dataset.id);
});

// Cart UI
const cartPanel = document.getElementById('cart-panel');
const cartCount = document.getElementById('cart-count');
function updateCartUI(){
  const c = getCart();
  cartCount.textContent = c.reduce((s,i)=>s+i.qty,0);
  const container = document.getElementById('cart-items');
  container.innerHTML='';
  if(c.length===0){ container.innerHTML='<div style="color:var(--muted);padding:12px">Your cart is empty.</div>'; document.getElementById('cart-total').textContent='₹0'; return }
  let total=0;
  c.forEach(item=>{
    total += item.price * item.qty;
    const div = document.createElement('div'); div.className='cart-item';
    div.innerHTML = `
      <img src="${item.img}" alt="${item.name}"/>
      <div style="flex:1">
        <div style="font-weight:700">${item.name}</div>
        <div style="color:var(--muted);font-size:13px">₹${item.price} × ${item.qty}</div>
      </div>
      <div style="display:flex;flex-direction:column;gap:6px;align-items:flex-end">
        <button data-id="${item.id}" class="add">+</button>
        <button data-remove="${item.id}" style="background:transparent;border:0;color:var(--muted)">Remove</button>
      </div>
    `;
    container.appendChild(div);
  });
  document.getElementById('cart-total').textContent = '₹'+total;
}
updateCartUI();

// open/close cart
document.getElementById('open-cart').addEventListener('click',()=>{
  cartPanel.style.display = cartPanel.style.display==='block' ? 'none' : 'block';
});

// cart quantity and remove
document.getElementById('cart-panel').addEventListener('click',e=>{
  if(e.target.matches('[data-id]')){
    const id = +e.target.dataset.id; const c = getCart(); const it = c.find(x=>x.id===id); if(it){ it.qty++; saveCart(c); updateCartUI(); }
  }
  if(e.target.matches('[data-remove]')){
    const id = +e.target.dataset.remove; let c = getCart(); c = c.filter(x=>x.id!==id); saveCart(c); updateCartUI();
  }
});

// Checkout flow
const checkoutModal = document.getElementById('checkout-modal');
document.getElementById('checkout').addEventListener('click',()=>{
  checkoutModal.style.display='flex';
});
document.getElementById('cancel-checkout').addEventListener('click',()=>{checkoutModal.style.display='none'});

document.getElementById('checkout-form').addEventListener('submit',e=>{
  e.preventDefault();
  const c = getCart(); if(c.length===0){ alert('Your cart is empty.'); return }
  // simulate order placement
  const form = new FormData(e.target);
  const order = {customer:Object.fromEntries(form.entries()),items:c,total:c.reduce((s,i)=>s+i.price*i.qty,0),id: 'ORD'+Date.now()};
  // here you'd send order to your backend or payment gateway
  console.log('Order placed',order);
  // clear cart
  localStorage.removeItem(CART_KEY);
  updateCartUI();
  checkoutModal.style.display='none';
  cartPanel.style.display='none';
  alert('Thanks! Your order '+order.id+' has been placed. We will contact you on ' + order.customer.phone);
});

// Search
document.getElementById('search').addEventListener('input',e=>{
  const q = e.target.value.trim().toLowerCase();
  if(!q) return renderProducts(PRODUCTS);
  renderProducts(PRODUCTS.filter(p=>p.name.toLowerCase().includes(q)));
});

// Shop Now => scroll
document.getElementById('shop-now').addEventListener('click',()=>{ document.getElementById('featured').scrollIntoView({behavior:'smooth'}); });

</script>
</body>
</html>
