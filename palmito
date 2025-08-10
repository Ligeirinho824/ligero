<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Ligeirinho — Palmito</title>
  <style>
    :root{
      --accent:#2a9d8f;
      --muted:#666;
      --bg:#f7f7f8;
      --card:#fff;
      --radius:10px;
      --maxw:980px;
      font-family: "Inter", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      background:linear-gradient(180deg, #fbfdfe 0%, var(--bg) 100%);
      color:#122;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      padding:24px;
      display:flex;
      justify-content:center;
    }
    .wrap{
      width:100%;
      max-width:var(--maxw);
    }

    header{
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:16px;
      margin-bottom:18px;
    }
    .brand{
      font-weight:800;
      font-size:34px;
      color:#000; /* nome em preto conforme pedido */
      letter-spacing:0.6px;
    }
    .tagline{
      color:var(--muted);
      font-size:14px;
    }

    main{
      display:grid;
      grid-template-columns: 1fr 360px;
      gap:20px;
      align-items:start;
    }

    /* lista de produtos */
    .products{
      display:flex;
      flex-direction:column;
      gap:14px;
    }
    .card{
      background:var(--card);
      border-radius:var(--radius);
      padding:16px;
      box-shadow:0 6px 18px rgba(18,34,54,0.06);
      display:flex;
      gap:14px;
      align-items:center;
    }
    .thumb{
      width:120px;
      height:80px;
      border-radius:8px;
      background:linear-gradient(135deg,#e9f7f4,#f0fbfa);
      display:flex;
      align-items:center;
      justify-content:center;
      color:var(--muted);
      font-size:13px;
      flex-shrink:0;
    }
    .info{
      flex:1;
    }
    .title{
      font-weight:700;
      margin:0 0 6px 0;
    }
    .desc{
      margin:0;
      color:var(--muted);
      font-size:13px;
    }
    .price{
      font-weight:700;
      font-size:18px;
      margin-top:8px;
    }

    .controls{
      display:flex;
      align-items:center;
      gap:8px;
      margin-left:8px;
    }
    .qty{
      display:flex;
      align-items:center;
      gap:6px;
      background:#f3f6f5;
      padding:6px;
      border-radius:8px;
    }
    .qty button{
      border:0;
      background:transparent;
      font-size:18px;
      width:28px;
      height:28px;
      cursor:pointer;
    }
    .qty span{
      min-width:28px;
      text-align:center;
      font-weight:700;
    }

    /* carrinho */
    .cart{
      background:var(--card);
      border-radius:var(--radius);
      padding:18px;
      box-shadow:0 6px 18px rgba(18,34,54,0.06);
      position:sticky;
      top:24px;
      height:fit-content;
    }
    .cart h3{margin:0 0 8px 0}
    .cart-list{display:flex;flex-direction:column;gap:10px;margin:12px 0}
    .cart-item{display:flex;justify-content:space-between;color:var(--muted);font-size:14px}
    .total-row{display:flex;justify-content:space-between;align-items:center;margin-top:12px;font-weight:800;font-size:18px}
    .whatsapp-btn{
      display:inline-flex;
      align-items:center;
      gap:10px;
      background:linear-gradient(90deg,var(--accent),#1b9b8f);
      color:#fff;
      border:0;
      width:100%;
      padding:12px 14px;
      border-radius:10px;
      font-weight:700;
      cursor:pointer;
      margin-top:12px;
      text-decoration:none;
    }

    footer{
      margin-top:20px;
      text-align:center;
      color:var(--muted);
      font-size:14px;
    }

    /* responsivo */
    @media (max-width:880px){
      main{grid-template-columns:1fr; padding-bottom:60px}
      .thumb{width:100px;height:72px}
    }
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div>
        <div class="brand">Ligeirinho</div>
        <div class="tagline">Palmito fresco — venda direta</div>
      </div>
      <div class="tagline">Peça pelo WhatsApp: <strong>+55 18 99704-3604</strong></div>
    </header>

    <main>
      <section class="products" aria-label="Produtos">
        <!-- Produto 1: Caixa com 15 unidades -->
        <article class="card" data-id="box">
          <div class="thumb">Imagem</div>
          <div class="info">
            <h4 class="title">1 Caixa (15 unidades)</h4>
            <p class="desc">Caixa com 15 unidades de palmito — ideal para revenda ou consumo familiar.</p>
            <div class="price" data-price="230">R$ 230,00</div>
          </div>
          <div class="controls">
            <div class="qty" role="group" aria-label="Quantidade caixa">
              <button class="dec" aria-label="Diminuir">−</button>
              <span class="count" id="qty-box">0</span>
              <button class="inc" aria-label="Aumentar">+</button>
            </div>
          </div>
        </article>

        <!-- Produto 2: Unidade -->
        <article class="card" data-id="unit">
          <div class="thumb">Imagem</div>
          <div class="info">
            <h4 class="title">1 Unidade</h4>
            <p class="desc">Palmito por unidade — para pedidos pequenos.</p>
            <div class="price" data-price="15.5">R$ 15,50</div>
          </div>
          <div class="controls">
            <div class="qty" role="group" aria-label="Quantidade unidade">
              <button class="dec" aria-label="Diminuir">−</button>
              <span class="count" id="qty-unit">0</span>
              <button class="inc" aria-label="Aumentar">+</button>
            </div>
          </div>
        </article>

      </section>

      <aside class="cart" aria-label="Carrinho">
        <h3>Carrinho</h3>
        <div class="cart-list" id="cart-list">
          <div class="cart-item" id="cart-box">
            <div>Caixa (15 un.) x <span id="cart-box-qty">0</span></div>
            <div id="cart-box-price">R$ 0,00</div>
          </div>
          <div class="cart-item" id="cart-unit">
            <div>Unidade x <span id="cart-unit-qty">0</span></div>
            <div id="cart-unit-price">R$ 0,00</div>
          </div>
        </div>

        <div class="total-row">
          <div>Total</div>
          <div id="cart-total">R$ 0,00</div>
        </div>

        <a href="#" id="whatsapp-buy" class="whatsapp-btn" target="_blank" rel="noopener noreferrer">
          📲 Comprar via WhatsApp
        </a>

        <div style="font-size:13px;color:var(--muted);margin-top:8px">
          Entrega e pagamento por combinar via WhatsApp.
        </div>
      </aside>
    </main>

    <footer>
      <div>Telefone: <strong>+55 18 99704-3604</strong></div>
    </footer>
  </div>

  <script>
    // preços base
    const PRICE_BOX = 230.00;
    const PRICE_UNIT = 15.50;
    const PHONE = "+5518997043604"; // whatsapp sem sinais

    // elementos
    const qtyBoxEl = document.getElementById('qty-box');
    const qtyUnitEl = document.getElementById('qty-unit');

    const cartBoxQty = document.getElementById('cart-box-qty');
    const cartUnitQty = document.getElementById('cart-unit-qty');
    const cartBoxPrice = document.getElementById('cart-box-price');
    const cartUnitPrice = document.getElementById('cart-unit-price');
    const cartTotalEl = document.getElementById('cart-total');
    const whatsappBtn = document.getElementById('whatsapp-buy');

    // estado
    let qtyBox = 0;
    let qtyUnit = 0;

    // função utilitária de formatação BRL
    function brl(value){
      return value.toLocaleString('pt-BR', { style:'currency', currency:'BRL' });
    }

    // atualiza visual do carrinho
    function updateCart(){
      const totalBox = qtyBox * PRICE_BOX;
      const totalUnit = qtyUnit * PRICE_UNIT;
      const total = totalBox + totalUnit;

      qtyBoxEl.textContent = qtyBox;
      qtyUnitEl.textContent = qtyUnit;

      cartBoxQty.textContent = qtyBox;
      cartUnitQty.textContent = qtyUnit;

      cartBoxPrice.textContent = brl(totalBox);
      cartUnitPrice.textContent = brl(totalUnit);
      cartTotalEl.textContent = brl(total);

      // construir mensagem pré-preenchida para WhatsApp
      let lines = [];
      lines.push("Olá! Gostaria de fazer um pedido para Ligeirinho.");
      if(qtyBox > 0) lines.push(`- Caixas (15 un.) x ${qtyBox} = ${brl(totalBox)}`);
      if(qtyUnit > 0) lines.push(`- Unidades x ${qtyUnit} = ${brl(totalUnit)}`);
      lines.push(`Total: ${brl(total)}`);
      lines.push("");
      lines.push("Por favor, confirmar disponibilidade e forma de pagamento/entrega.");
      const message = encodeURIComponent(lines.join("\\n"));

      // wa.me link
      whatsappBtn.href = `https://wa.me/${PHONE}?text=${message}`;
    }

    // adicionar handlers para botões +/-
    document.querySelectorAll('.card').forEach(card => {
      const id = card.getAttribute('data-id');
      const inc = card.querySelector('.inc');
      const dec = card.querySelector('.dec');

      inc.addEventListener('click', ()=> {
        if(id === 'box'){ qtyBox++; }
        else if(id === 'unit'){ qtyUnit++; }
        updateCart();
      });

      dec.addEventListener('click', ()=> {
        if(id === 'box'){ qtyBox = Math.max(0, qtyBox-1); }
        else if(id === 'unit'){ qtyUnit = Math.max(0, qtyUnit-1); }
        updateCart();
      });
    });

    // inicializa
    updateCart();

    // acessibilidade: permitir teclado para botões com Enter/Space
    document.querySelectorAll('.qty button').forEach(btn=>{
      btn.addEventListener('keydown', (e)=>{
        if(e.key === 'Enter' || e.key === ' '){
          e.preventDefault();
          btn.click();
        }
      });
    });

    // dica: clique longo para zerar (mobile)
    document.querySelectorAll('.qty').forEach(q=>{
      let timer = null;
      q.addEventListener('touchstart', ()=>{ timer = setTimeout(()=>{
        // zerar a quantidade correspondente
        const parent = q.closest('.card');
        if(parent && parent.dataset.id === 'box'){ qtyBox = 0; }
        if(parent && parent.dataset.id === 'unit'){ qtyUnit = 0; }
        updateCart();
      }, 800);});
      q.addEventListener('touchend', ()=>{ clearTimeout(timer); });
    });

  </script>
</body>
</html>
