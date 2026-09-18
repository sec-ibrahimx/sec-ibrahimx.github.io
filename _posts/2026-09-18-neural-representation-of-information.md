---
layout: post
title: "كيف يرى الدماغ المعلومة: من الكتلة الجامدة إلى تفكيك العناصر"
date: 2026-09-18 21:00:00 +0300
description: "تحليل لكيفية معالجة الدماغ للمفاهيم عبر تفكيكها لتقليل الحمل الإدراكي وبناء نماذج ذهنية متماسكة."
tags: [neuroscience, mental-models, learning]
category: blog
---

من الخطأ معاملة المعلومة كأنها مكوِّن واحد، المعلومة هي الاسم العام لعدد من العناصر المجزأة ساهمت في تشكيلها. 

على سبيل المثال: **"هذا الحاسب سريع"**، للوهلة الأولى نراها معلومة واحدة جامدة وتتمثل في كون الحاسب سريع، وهنا تقع المغالطة؛ فهذه المعلومة ساهم في تشكيلها عدة عناصر: نوع المعالج، وسرعة قراءة القرص الصلب، وحجم الذاكرة العشوائية، وحتى كفاءة التبريد وجودة التصنيع.

لا يمكننا التمكّن من أي معلومة إلا بتفكيكها إلى عناصرها الأساسية المساهمة واستيعابها. وتكمن فائدة التفكيك في تحويل المعلومة الواحدة الجامدة إلى أجزاء صغيرة. ما الفائدة من ذلك؟ أن نتعلّم المعلومة بالطريقة التي تشكلت بها أصلًا. هذه الطريقة التي يعمل بها دماغنا البشري، فهو لا يفضّل المعلومة المعقدة دفعة واحدة، بل يستوعبها مفككة إلى مكونات أصغر مما يقلل الحمل الإدراكي (Cognitive Load) ويسمح للدماغ ببناء روابط وتفرعات جديدة.

---

### محاكاة عصبية: كيف يتعامل الدماغ مع السيناريوهين؟

<div style="background:#0d1117; border:1px solid #30363d; border-radius:8px; padding:1.5rem; color:#c9d1d9; font-family:sans-serif; margin:2rem 0;">

  <!-- Scenario 1 -->
  <div style="margin-bottom:2.5rem;">
    <div style="display:flex; align-items:center; justify-content:space-between; margin-bottom:0.6rem;">
      <h4 style="margin:0; color:#f85149; font-size:1.1rem;">السيناريو الأول: استقبال المعلومة ككتلة واحدة جامدة</h4>
      <span style="font-size:0.75rem; background:#21262d; border:1px solid #f85149; color:#f85149; padding:2px 8px; border-radius:4px;">مسار هش / تقليم عصبي</span>
    </div>
    <p style="margin:0 0 0.8rem 0; font-size:0.88rem; color:#8b949e; line-height:1.5;">
      مسار أحادي ضعيف بين مفهومين مجردين دون تفاصيل داعمة. تيار الإشارات بطيء وعرضة للمحو والتلاشي السريع (Synaptic Pruning).
    </p>
    <canvas id="canvas-s1" width="700" height="180" style="width:100%; height:auto; background:#161b22; border-radius:6px; border:1px solid #21262d; display:block;"></canvas>
  </div>

  <hr style="border:0; border-top:1px dashed #30363d; margin:2rem 0;" />

  <!-- Scenario 2 -->
  <div>
    <div style="display:flex; align-items:center; justify-content:space-between; margin-bottom:0.6rem;">
      <h4 style="margin:0; color:#3fb950; font-size:1.1rem;">السيناريو الثاني: تفكيك المعلومة إلى عناصرها المستقلة</h4>
      <span style="font-size:0.75rem; background:#21262d; border:1px solid #3fb950; color:#3fb950; padding:2px 8px; border-radius:4px;">شبكة متماسكة / LTP</span>
    </div>
    <p style="margin:0 0 0.8rem 0; font-size:0.88rem; color:#8b949e; line-height:1.5;">
      استيعاب كل عنصر (معالج، ذاكرة، قرص، تبريد) يبني عقداً راسخة. ترابطها معاً يكوّن شبكة كثيفة ومسارات عصبية سريعة بفضل المَيْلَنَة والتأييد طويل الأمد.
    </p>
    <canvas id="canvas-s2" width="700" height="280" style="width:100%; height:auto; background:#161b22; border-radius:6px; border:1px solid #21262d; display:block;"></canvas>
  </div>

</div>

<script>
window.addEventListener('load', function() {
  const c1 = document.getElementById('canvas-s1');
  const c2 = document.getElementById('canvas-s2');

  if (!c1 || !c2) return;

  const ctx1 = c1.getContext('2d');
  const ctx2 = c2.getContext('2d');

  let step1 = 0;
  let step2 = 0;

  function drawNode(ctx, x, y, r, label, color) {
    ctx.beginPath();
    ctx.arc(x, y, r, 0, Math.PI * 2);
    ctx.fillStyle = '#0d1117';
    ctx.fill();
    ctx.lineWidth = 2;
    ctx.strokeStyle = color;
    ctx.stroke();

    ctx.fillStyle = '#ffffff';
    ctx.font = 'bold 12px sans-serif';
    ctx.textAlign = 'center';
    ctx.textBaseline = 'middle';
    ctx.fillText(label, x, y);
  }

  function drawPulse(ctx, x1, y1, x2, y2, progress, color, size) {
    const px = x1 + (x2 - x1) * progress;
    const py = y1 + (y2 - y1) * progress;
    ctx.beginPath();
    ctx.arc(px, py, size || 4, 0, Math.PI * 2);
    ctx.fillStyle = color;
    ctx.fill();
  }

  function renderScenario1() {
    ctx1.clearRect(0, 0, c1.width, c1.height);
    step1 = (step1 + 0.008) % 1;

    const x1 = 200, y1 = 90, x2 = 500, y2 = 90;

    ctx1.beginPath();
    ctx1.moveTo(x1, y1);
    ctx1.lineTo(x2, y2);
    ctx1.lineWidth = 1.5;
    ctx1.setLineDash([6, 6]);
    ctx1.strokeStyle = '#f85149';
    ctx1.stroke();
    ctx1.setLineDash([]);

    drawPulse(ctx1, x1, y1, x2, y2, step1, '#f85149', 3.5);
    drawNode(ctx1, x1, y1, 30, 'الحاسب', '#f85149');
    drawNode(ctx1, x2, y2, 30, 'سريع', '#f85149');
  }

  function renderScenario2() {
    ctx2.clearRect(0, 0, c2.width, c2.height);
    step2 = (step2 + 0.018) % 1;

    const center = { x: 350, y: 140 };
    const nodes = [
      { x: 160, y: 60, name: 'معالج CPU' },
      { x: 540, y: 60, name: 'ذاكرة RAM' },
      { x: 160, y: 220, name: 'قرص SSD' },
      { x: 540, y: 220, name: 'تبريد Thermal' }
    ];

    for (let i = 0; i < nodes.length; i++) {
      for (let j = i + 1; j < nodes.length; j++) {
        ctx2.beginPath();
        ctx2.moveTo(nodes[i].x, nodes[i].y);
        ctx2.lineTo(nodes[j].x, nodes[j].y);
        ctx2.lineWidth = 1;
        ctx2.strokeStyle = '#21262d';
        ctx2.stroke();
      }
    }

    nodes.forEach(function(n) {
      ctx2.beginPath();
      ctx2.moveTo(n.x, n.y);
      ctx2.lineTo(center.x, center.y);
      ctx2.lineWidth = 2.5;
      ctx2.strokeStyle = '#3fb950';
      ctx2.stroke();

      drawPulse(ctx2, n.x, n.y, center.x, center.y, step2, '#58a6ff', 4.5);
    });

    nodes.forEach(function(n) {
      drawNode(ctx2, n.x, n.y, 28, n.name, '#58a6ff');
    });

    drawNode(ctx2, center.x, center.y, 42, 'سرعة النظام', '#3fb950');
  }

  function loop() {
    renderScenario1();
    renderScenario2();
    requestAnimationFrame(loop);
  }

  loop();
});
</script>
