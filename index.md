<!-- 🔤 Language Switcher -->
<div class="lang-switch" role="group" aria-label="Language switch">
  <button data-lang="en" class="active">English</button>
  <button data-lang="bn">বাংলা</button>
</div>

<style>
/* Language visibility */
.lang-section{ display:none; }
body.lang-en .lang-en{ display:block; }
body.lang-bn .lang-bn{ display:block; }

/* Switcher styles (theme-friendly) */
.lang-switch{
  display:inline-flex; gap:8px; margin:0 0 1rem 0; border:1px solid #e5e5e5; border-radius:10px; padding:4px;
}
.lang-switch button{
  appearance:none; border:0; background:#fafafa; padding:6px 10px; border-radius:8px; cursor:pointer; font-weight:600;
}
.lang-switch button.active{ background:#8b0000; color:#fff; }
@media(prefers-color-scheme:dark){
  .lang-switch{ border-color:#333; }
  .lang-switch button{ background:#181818; color:#ddd; }
  .lang-switch button.active{ background:#8b0000; color:#fff; }
}

/* Shared styles from your page */
:root{
  --tile-bg:#5a0000;      /* Crimson box background */
  --icon-color:#8B0000;   /* Deep blood red icon */
  --text-light:#fff;      /* Text color on crimson */
}
.video-tiles{
  display:grid;
  gap:14px;
  grid-template-columns:repeat(2,1fr);
  margin:1.2rem 0 1.8rem;
}
@media(max-width:600px){ .video-tiles{ grid-template-columns:1fr; } }

.video-tile{
  display:flex;
  flex-direction:column;
  align-items:center;
  justify-content:center;
  text-decoration:none;
  background:var(--tile-bg);
  color:var(--text-light);
  border-radius:10px;
  padding:14px 8px;
  transition:transform .15s ease, box-shadow .15s ease;
}
.video-tile:hover{
  transform:translateY(-2px);
  box-shadow:0 6px 18px rgba(0,0,0,.2);
}
.icon{
  color:var(--icon-color);
  margin-bottom:.25rem;
}
.icon svg{
  width:0.9rem; height:0.9rem; display:block;
}
.caption{
  text-align:center;
  font-size:.85rem;  /* smaller text */
  line-height:1.3;
}
.caption strong{
  display:block;
  font-size:.9rem;
  margin-bottom:.15rem;
}
.caption p{
  margin:0;
  font-size:.8rem;
  opacity:.9;
}

/* Double divider */
.double-divider{
  width:100%;
  text-align:center;
  margin:1.5rem 0 2rem;
  position:relative;
}
.double-divider::before,
.double-divider::after{
  content:"";
  display:block;
  width:60%;
  max-width:400px;
  height:2px;
  margin:0.4rem auto;
  background:#8B0000; border-radius:2px;
}
.double-divider::after{ width:40%; opacity:0.8; }

/* Overview tiles */
.tiles-4{
  display:grid;
  gap:14px;
  grid-template-columns:repeat(4,1fr);
  margin: 0 0 1rem 0;
}
@media (max-width: 960px){ .tiles-4{ grid-template-columns:repeat(2,1fr); } }
@media (max-width: 520px){ .tiles-4{ grid-template-columns:1fr; } }
.tile{
  display:block; text-decoration:none; color:inherit; background:#fff;
  border:1px solid #e8e8e8; border-radius:12px; padding:14px 14px 16px;
  transition:transform .15s ease, box-shadow .15s ease, border-color .15s ease;
}
.tile:hover{ transform:translateY(-2px); border-color:#ddd; box-shadow:0 6px 20px rgba(0,0,0,.06); }
.tile-label{
  display:inline-block; font-size:.72rem; letter-spacing:.3px; color:#777;
  border:1px solid #eee; padding:.18rem .5rem; border-radius:999px; margin-bottom:.45rem;
}
.tile h3{ margin:.1rem 0 .35rem; font-size:1.05rem; font-weight:700; }
.tile p{ margin:0; color:#555; line-height:1.4; font-size:.95rem; }
</style>

<script>
(function(){
  const saved = localStorage.getItem('lang') || 'en';
  document.body.classList.remove('lang-en','lang-bn');
  document.body.classList.add('lang-' + saved);

  const buttons = document.querySelectorAll('.lang-switch button');
  buttons.forEach(btn=>{
    if(btn.dataset.lang === saved) btn.classList.add('active');
    btn.addEventListener('click', ()=>{
      buttons.forEach(b=>b.classList.remove('active'));
      btn.classList.add('active');
      const lang = btn.dataset.lang;
      document.body.classList.remove('lang-en','lang-bn');
      document.body.classList.add('lang-' + lang);
      localStorage.setItem('lang', lang);
    });
  });
})();
</script>

<!-- =========================================================
     ENGLISH VERSION
========================================================= -->
<div class="lang-section lang-en" markdown="1">

<!--  WELCOME NOTE -->
<section class="welcome-note" style="margin-bottom:2rem;">
  <h2>Welcome to <span style="color:#8b0000;">Saha Bari's Kali Puja</span> Website</h2>
  <p>
    Click on the links below to listen to the songs containing the lines near the <em>mondop</em> and the <em>book stall</em>.
    This year, our prayer has been simple - that <strong>Maa</strong> may enter our lives and show us the
    path to Enlightenment. To guide us toward living each moment fully immersed in Her presence.
  </p>
</section>

<section class="video-tiles">
  <a class="video-tile" href="https://www.youtube.com/watch?v=sADh9yMDIHE&list=RDsADh9yMDIHE&index=1" target="_blank" rel="noopener">
    <div class="icon" aria-hidden="true">
      <svg viewBox="0 0 24 24" fill="currentColor"><path d="M8 5v14l11-7-11-7z"></path></svg>
    </div>
    <div class="caption">
      <strong>Esheche Notun Manush - Dekhbi Jodi Aye Chole</strong>
    </div>
  </a>

  <a class="video-tile" href="https://www.youtube.com/watch?v=v_NX7qdX-0U&list=RDv_NX7qdX-0U&start_radio=1" target="_blank" rel="noopener">
    <div class="icon" aria-hidden="true">
      <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 3a9 9 0 00-9 9v6a3 3 0 003 3h1a2 2 0 002-2v-4a2 2 0 00-2-2H5v-1a7 7 0 0114 0v1h-2a2 2 0 00-2 2v4a2 2 0 002 2h1a3 3 0 003-3v-6a9 9 0 00-9-9z"></path></svg>
    </div>
    <div class="caption">
      <strong>Ramakrishna Namer Jowar Elo</strong>
    </div>
  </a>
</section>

<!--  DOUBLE LINE DIVIDER -->
<div class="double-divider"></div>

<section class="additional-note" style="margin-bottom:2rem;">
  <p>
    We have also composed a short article below - a heartfelt reflection on Maa Kali and Her many forms.
    Do give it a read, and may you find <strong>Maa</strong> in the form your heart desires. <strong>Joy Maa!</strong>
  </p>
</section>

<!-- HERO IMAGE -->
<p align="center">
  <img src="{{ '/kali_pic_2024.png' | relative_url }}" alt="Maa Kali"
       style="width:70%; max-width:600px; border-radius:14px;">
</p>

# Darshon E Maa Er Dorshon

Being the first of the ten [Mahavidyas](https://en.wikipedia.org/wiki/Mahavidya), [Maa Kali](https://en.wikipedia.org/wiki/Kali) is the epitome of [Shakti](https://en.wikipedia.org/wiki/Shakti). _Her_ iconography depicts _Her_ as "ugra" (fierce) - dark as the darkest [Kartik Amavasya](https://en.wikipedia.org/wiki/Amavasya) night sky, with three wide-open eyes that see past time, long tangled hair, a lolling crimson tongue, and a garland of countless skulls symbolizing the passing of time - innumerable births and deaths (*Kaal*). _She_ stands on [Lord Shiva](https://en.wikipedia.org/wiki/Shiva), in the cremation ground (*samshan*). In _Her_ left hands, She holds a severed head and a *kharga* (scimitar), symbols of the destruction of [Ahamkara](https://en.wikipedia.org/wiki/Ahamkara) (ego, the “I” consciousness) and [Avidya](https://en.wikipedia.org/wiki/Avidy%C4%81_(Hinduism)) (ignorance). In _Her_ right hands, _She_ blesses and grants boons through the [Abhaya](https://en.wikipedia.org/wiki/Abhayamudra) and [Varada mudra](https://en.wikipedia.org/wiki/Varadamudra).
Despite this fierce iconography, we love and adore _Her_ in our own ways. For example, my sister, looking at our community's (*para*) Kali idol (*murti*), exclaimed, “Maa ke khub cute dekhte lagche” (Maa looks so cute). That's the magic of Kali - terrifying yet tender, destructive yet deeply loving.

_But who really is Maa Kali? What does She signify? **How can we see Her as Thakur Sri Ramakrishna saw Her?**_  
Let’s take a journey together - to see Maa as the Mother, as Power, as the Primordial Energy, and as the Self within. Each reveals a different facet of the same truth. Understanding each, we discover that how we see Maa depends on our *Bhava* - the inner feeling with which we approach Her.

<!-- 4 TILES (OVERVIEW) -->
<div class="tiles-4">
  <a class="tile" href="#aspect-1">
    <div class="tile-label">Bhava 1</div>
    <h3>Kali as the Divine Mother</h3>
  </a>
  <a class="tile" href="#aspect-2">
    <div class="tile-label">Bhava 2</div>
    <h3>Kali as Shakti - The Power of Shiva</h3>
  </a>
  <a class="tile" href="#aspect-3">
    <div class="tile-label">Bhava 3</div>
    <h3>Kali as Primordial Power</h3>
  </a>
  <a class="tile" href="#aspect-4">
    <div class="tile-label">Bhava 4</div>
    <h3>Kali as Your Inner Being</h3>
  </a>
</div>



### Bhava 1: Kali as the Divine Mother {#aspect-1}
At this level, Shakti appears in the form of Maa Kali, Maa Durga, Maa Saraswati, or any motherly power we worship. _She_ is external to us - our divine protector, our guide, our nurturer. We call out to _Her_ as we would to our earthly mother: sometimes in love, sometimes in fear, always in faith. _She_ destroys evil and removes obstacles, yet Her destruction is compassionate - it clears the path for light to enter. _She_ blesses those who walk the path of [Dharma](https://en.wikipedia.org/wiki/Dharma), and gently corrects those who stray. Understanding _Her_ in this way is [Bhakti Yoga](https://en.wikipedia.org/wiki/Bhakti_yoga) - the path of devotion. Here, the devotee and the Divine are two beings bound by love: a relationship of sweetness, surrender, and emotion - a [_rasa_](https://en.wikipedia.org/wiki/Rasa_(theology)) that fills the heart with bliss.

### Bhava 2: Kali as Shakti - The Power of Shiva {#aspect-2}
At a deeper level, Maa Kali is not merely someone outside who blesses us; _She_ is the very **Power of the Absolute (Shiva)**. _She_ is Shiva’s *ardhangini* - His other half, His pulse. Without _Her_, Shiva is *śava* - motionless, pure stillness without expression. _She_ is His expressive power, the one who makes consciousness move. As mentioned in the 6th mantra of the [Devi Sukta](https://en.wikipedia.org/wiki/Dev%C4%ABs%C5%ABkta) ([Ṛgveda X.125](https://en.wikipedia.org/wiki/Rigveda)):

> **ahaṃ rudrāya dhanurā tanomi brahmadviṣe śarave hantavā u, ahaṃ janāya samadaṃ kṛṇomy-ahaṃ dyāvā-pṛthivī āviveśa ॥ 6**  
> _(Meaning: I bend the bow for Rudra to slay the enemies of the noble. I battle the enemies of my devotees. Indeed, I pervade heaven and earth.)_

This is [Tantric](https://en.wikipedia.org/wiki/Tantra) [non-duality](https://en.wikipedia.org/wiki/Nondualism) - **Shiva–Shakti tattva**: Shiva is pure, unchanging consciousness (*Cit*), and Shakti is the vibration, the movement (*Spanda*) of that consciousness. Together they form existence itself - the stillness and the dance. When Maa Kali dances, the universe comes alive; when _She_ stops, everything returns to stillness. Every breath, heartbeat, and flash of thought is Her movement within the vast silence of Shiva. In the **Kali Tantra** and **Shakta** texts, this union is described as a constant embrace: Shiva lying below symbolizes the silent foundation of awareness, while Kali standing upon Him symbolizes energy rising and playing upon that awareness. When we recognize this, the image of Kali standing on Shiva is no longer “violent” but profoundly symbolic - consciousness and energy, two names for one Reality, forever entwined.

### Bhava 3: Kali as the Primordial Power that Flows through Us {#aspect-3}
At this level, Kali is no longer just an external goddess or even the power of Shiva. _She_ is the **primordial pulse** that keeps the universe alive. Shakti is the unseen rhythm of existence - the force by which the unmanifest becomes manifest. The rising sun, the beating of your heart, the birth and death of stars - all dance to _Her_ rhythm. The same energy that spins galaxies also hums within your spine as [Prana](https://en.wikipedia.org/wiki/Prana). Every thought that flashes across your mind, every surge of emotion, every act of creation or destruction - all are movements of Shakti. _She_ is the power that makes perception possible, the background vibration that turns pure consciousness into experience. When you feel inspired, when you love deeply, when you suffer and still rise again - that’s _Her_ too. Shakti is not “out there”; _She_ is the current that flows through everything that is. In [Samkhya](https://en.wikipedia.org/wiki/Samkhya), _She_ is **Mūla-Prakṛti**, the first cause. In [Advaita Vedanta](https://en.wikipedia.org/wiki/Advaita_Vedanta), _She_ is **Maya-Shakti**, the dynamic nature of [Nirguna Brahman](https://www.bbc.co.uk/bitesize/guides/zrf6pbk/revision/2) - pure stillness appearing as motion. Kali is that very motion - timeless energy taking form as time itself. As in the 4th and 8th mantras of the Devi Sukta (Ṛgveda X.125):
> **mayā so annam-atti yo vipaśyati yaḥ prāṇiti ya īṃ śṛṇotyuktam, amantavo māṃ ta upa kṣiyanti śrudhi-śruta śraddhivaṃ te vadāmi ॥ 4**  
> _(Meaning: He who eats, sees, breathes, and hears - does so through me… listen, I tell you that which deserves śraddhā.)_
>
> **aham-eva vāta-iva pravāmi ārabhamāṇā bhuvanāni viśvā, paro divā para enā pṛthivyaitāvatī mahinā saṃ babhūva ॥ 8**  
> _(Meaning: Like the wind, I set all worlds in motion. I am beyond sky and earth and have become all this in my own splendour.)_

### Bhava 4: Kali as Your Inner Being {#aspect-4}
Now come close. Ask: **“Who am I?”** Are you the body? the mind? If so, point to where “you” reside. If I scan your brain, will I find *you* there? The body is the instrument; the *ātma* is subtler.  
You may say, “I am my thoughts and feelings.” Yet in deep sleep the mind is silent, and still *you* remain - you wake and say, “I slept well.” Who witnessed that blankness?  
Or you may say, “I am my roles - parent, child, friend.” Roles change; something constant notes the change. That **witness** is the real you.

In meditation, thoughts rise and fall, emotions come and go, even the sense “I” fades and returns. After deep absorption you *know* you were absorbed - proof of the **Sākṣī**, the witness that never sleeps. The witness has no shape, boundary, or birth. It is pure **Awareness - Sat-Cit-Ānanda**, the essence of **Brahman**. Here **Śiva and Śakti merge**: stillness and movement are not two - **Advaita**. Like wave and ocean, they differ only in name and form.

**What is Brahman?**  
Not a “cosmic thing.” It cannot be objectified, because it is the ground of knowing. Hence **Neti Neti** - whatever you can point to is already within its light. As **Swami Sarvapriyananda** says: “The subject can never be the object of experience.” Like **Gödel’s theorem**, within a system some truths can’t be proven from within. Likewise, the finite body–mind cannot “know” Brahman as object - because Brahman is the subject.

**“Then can I never experience Brahman?”**  
Paradoxically, you already are. **Tat tvam asi - You are That.** As you infer light from illuminated objects, you infer Brahman from the very fact that you see, think, and feel. Every dream, silence, and moment of awareness is its evidence. Just as waves and ocean are water, you and Śakti are Brahman’s manifestations.

This is the unchanging truth that death cannot touch. The body will die, the “I”-sense will dissolve, but your *svarūpa* is eternal - infinite, unborn, deathless. As **Śrī Krishna** declares in the **Gītā (2.17–25)**: the Self is indestructible; weapons cannot cut it, fire cannot burn it, water cannot wet it, wind cannot dry it.

So yes - **you are Śakti**, not in the egoic sense of possessing power, but as Being itself:
> You don’t “have” Śakti; **you are** Śakti - localized for a while in this body, yet never limited by it.

When that insight dawns, all comparison dissolves. You no longer see “yourself” and “others”; you see **Maa everywhere** - the same infinite, ever-living consciousness shining as every form. You realize **Chidānanda-rūpaḥ Śivo’ham Śivo’ham**.

### Conclusion
And thus the journey completes: from worshipping Her outside, to finding Her within, to dissolving as Her. It’s alright if we can’t always “find” the Mother. She is **Ānandamayī** - ever-blissful, ever-revealing. She appears in whatever form you are ready to see. And if you truly long for Her, She will take the shape of your longing. As Thakur said, “**Joto mot, toto poth**” - as many faiths, so many paths.

But here lies the difficulty. After the festival days, we forget Her. Life returns - work, family, deadlines. We get busy: chasing science, progress, success; offering the mind to the senses; calling this the “real” life and treating philosophy as tea-time talk. In that busyness, the Mother becomes a faint memory, tucked away in a corner of the heart.

To truly find Her again, we must pause and rekindle **byākulatā** - sacred yearning. Like a child who cries for Ma and is pacified by nothing else, we must seek Her alone. Without that longing, we settle for the fleeting pleasures of a fleeting world. But when that yearning awakens, even for a moment, you see She was never gone - in your breath, your gaze, your joy and sorrow, in the silent awareness within you - **the Jyotir-o-Jyoti**, the Light behind every light.
</div>

<!-- =========================================================
     BENGALI VERSION
========================================================= -->
<div class="lang-section lang-bn" markdown="1">

<section class="welcome-note" style="margin-bottom:2rem;">
  <h2>স্বাগতম <span style="color:#8b0000;">সাহা বাড়ির কালীপূজা</span> ওয়েবসাইটে</h2>
  <p>
    নিচের লিঙ্কগুলোতে ক্লিক করে <em>মণ্ডপ</em> ও <em>বইয়ের স্টলের</em> কাছে বাজতে থাকা গানের লাইনগুলির রেকর্ডিং শুনতে পারেন।
    এ বছর আমাদের প্রার্থনা খুব সহজ - <strong>মা</strong> যেন আমাদের জীবনে প্রবেশ করেন এবং
    আমাদেরকে আলোর পথে চালিত করেন; যেন প্রতিটি মুহূর্তে আমরা তাঁর উপস্থিতিতে নিমগ্ন থাকতে শিখি।
  </p>
</section>

<section class="video-tiles">
  <a class="video-tile" href="https://www.youtube.com/watch?v=sADh9yMDIHE&list=RDsADh9yMDIHE&index=1" target="_blank" rel="noopener">
    <div class="icon" aria-hidden="true">
      <svg viewBox="0 0 24 24" fill="currentColor"><path d="M8 5v14l11-7-11-7z"></path></svg>
    </div>
    <div class="caption">
      <strong>এসেছে নতুন মানুষ - দেখবি যদি আয় চলে</strong>
    </div>
  </a>

  <a class="video-tile" href="https://www.youtube.com/watch?v=v_NX7qdX-0U&list=RDv_NX7qdX-0U&start_radio=1" target="_blank" rel="noopener">
    <div class="icon" aria-hidden="true">
      <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 3a9 9 0 00-9 9v6a3 3 0 003 3h1a2 2 0 002-2v-4a2 2 0 00-2-2H5v-1a7 7 0 0114 0v1h-2a2 2 0 00-2 2v4a2 2 0 002 2h1a3 3 0 003-3v-6a9 9 0 00-9-9z"></path></svg>
    </div>
    <div class="caption">
      <strong>রামকৃষ্ণ নামে জোয়ার এলো</strong>
    </div>
  </a>
</section>

<div class="double-divider"></div>

<section class="additional-note" style="margin-bottom:2rem;">
  <p>
    নীচে আমরা একটি ছোট্ট নিবন্ধ দিয়েছি - মা কালী ও তাঁর নানান রূপ নিয়ে হৃদয়ের কথা।
    পড়ে দেখবেন; আপনার হৃদয় যেমন করে চায়, সেভাবেই যেন <strong>মা</strong> ধরা দেন। <strong>জয় মা!</strong>
  </p>
</section>

<p align="center">
  <img src="{{ '/kali_pic_2024.png' | relative_url }}" alt="মা কালী"
       style="width:70%; max-width:600px; border-radius:14px;">
</p>

# দর্শনে মায়ের দর্শন

দশ মহাবিদ্যার মধ্যে প্রথম, [মা কালী](https://en.wikipedia.org/wiki/Kali) হলেন [শক্তি](https://en.wikipedia.org/wiki/Shakti)-রই মূর্ত প্রতীক। তাঁর আইকনোগ্রাফিতে _তাঁকে_ দেখা যায় **উগ্র** - [কার্তিকী অমাবস্যা](https://en.wikipedia.org/wiki/Amavasya)-র কৃষ্ণরাত্রির মতো কৃষ্ণবর্ণ, তিনটি বিস্ফারিত নয়ন যা সময়েরও ওপারে দেখে, এলোমেলো জটা, রক্তিম জিহ্বা, আর অনন্ত খুলি-মালায় সময়ের ধারাবাহিক জন্ম-মৃত্যুর (কাল) সংকেত। _তিনি_ [ভগবান শিব](https://en.wikipedia.org/wiki/Shiva)-ের বক্ষে [শ্মশানে] (সমশান) বিরাজমান। বামহস্তে কাটা মুণ্ডু ও *খড়্গ* - [অহংকার](https://en.wikipedia.org/wiki/Ahamkara) ও [অবিদ্যা](https://en.wikipedia.org/wiki/Avidy%C4%81_(Hinduism)) বিনাশের প্রতীক; ডানহাতে [অভয়](https://en.wikipedia.org/wiki/Abhayamudra) ও [বরদা](https://en.wikipedia.org/wiki/Varadamudra) মুদ্রা - আশীর্বাদ ও বরদান।  
তবু এই ভয়াল রূপের মধ্যেও আমরা তাঁকে আপন করে ভালবাসি। আমাদের পাড়ার কালীমূর্তি দেখে আমার বোন হেসে বলেছিল, “মা-কে খুব কিউট দেখাচ্ছে!” - এটাই কালী-মায়ের মাহাত্ম্য - ভয়ংকর অথচ স্নেহময়ী, বিধ্বংসী অথচ গভীর প্রেমময়ী।

_তবে মা কালী কে? তিনি কী বোঝান? **ঠাকুর শ্রী রামকৃষ্ণ যেমন করে দেখেছিলেন, আমরাও কি তেমন করে তাঁকে দেখতে পারি?**_  
চলুন চারভাবে দেখি - মা **মাতা** রূপে, **শক্তি** রূপে, **আদ্যশক্তি** রূপে, আর **অন্তঃসত্তা** রূপে। একেকটি দৃষ্টিভঙ্গি একেকটি সত্যের আভাস দেয়। কোন *ভাব*ে আপনি মাকে ডাকছেন, তাই-ই নির্ধারণ করে আপনার দর্শন।

<div class="tiles-4">
  <a class="tile" href="#aspect-1">
    <div class="tile-label">ভাব ১</div>
    <h3>মা - দিব্য জননী</h3>
  </a>
  <a class="tile" href="#aspect-2">
    <div class="tile-label">ভাব ২</div>
    <h3>শক্তি - শিবের সচল শক্তি</h3>
  </a>
  <a class="tile" href="#aspect-3">
    <div class="tile-label">ভাব ৩</div>
    <h3>আদ্যশক্তি - স্রষ্টা স্পন্দন</h3>
  </a>
  <a class="tile" href="#aspect-4">
    <div class="tile-label">ভাব ৪</div>
    <h3>অন্তরের আমি - মা</h3>
  </a>
</div>

<hr />

### ভাব ১: মা - দিব্য জননী {#aspect-1}
এই স্তরে শক্তি উপস্থিত হন মা কালী, মা দুর্গা, মা সরস্বতী বা যে কোনও মাতৃশক্তি-রূপে। _তিনি_ আপাতত বাহিরে - রক্ষিকা, পথপ্রদর্শিকা, পোষিকা। কখনও প্রেমে, কখনও ভয়ে, কিন্তু বিশ্বাসে - আমরা তাঁকে ডাকি। তিনি দুষ্ট-দমন ও বিঘ্ন-নাশ করেন, কিন্তু সেই বিনাশও করুণাময় - আলোর পথ খুলে দেয়। [ধর্ম](https://en.wikipedia.org/wiki/Dharma)-পথিকদের আশীর্বাদ করেন, পথভ্রষ্টদের মমতায় সুধরান। এই দর্শনই [ভক্তি যোগ](https://en.wikipedia.org/wiki/Bhakti_yoga) - যেখানে ভক্ত ও ঈশ্বর দু’জন, কিন্তু প্রেমে আবদ্ধ। এ এক মাধুর্য, আত্মসমর্পণ ও রসের সম্পর্ক - হৃদয় ভরে ওঠে *রসে*।

### ভাব ২: কালী - শক্তি, শিবের শক্তি {#aspect-2}
আরও গভীরে গেলে মা কালী কেবল বাহিরের কোনো সত্তা নন; _তিনি_ **পরম সত্যের শক্তি (শিব)**। _তিনি_ শিবের *অর্ধাঙ্গিনী* - তাঁর স্পন্দন। শক্তি ছাড়া শিব *শব* - নিস্তরঙ্গ চৈতন্য। _তিনি_ সেই প্রকাশশক্তি, যিনি চৈতন্যকে গতিময় করেন। [দেবীসূক্ত](https://en.wikipedia.org/wiki/Dev%C4%ABs%C5%ABkta) (ঋগ্বেদ ১০.১২৫) বলে:

> **ahaṃ rudrāya… ॥ 6** - “আমি রুদ্রের ধনুক টানি… আকাশ-পাতাল ভেদ করে আমি বিরাজমান।”

এটাই [তন্ত্র](https://en.wikipedia.org/wiki/Tantra)-র **শিব–শক্তি তত্ত্ব**: শিব = চিত্ (নির্বিকার চৈতন্য), শক্তি = স্পন্দ (চৈতন্যের আন্দোলন)। দু’য়ে মিলে সৃষ্টিস্বরূপ - *নিঃস্তব্ধতা ও নৃত্য*। কালী নৃত্য করলে বিশ্ব জেগে ওঠে; থামলে সব নিস্তব্ধ। প্রতিটি নিঃশ্বাস, হৃদস্পন্দন, চিন্তার ঝলক - শিবের নিস্তব্ধতায় মায়েরই নৃত্য। তাই শিব-বক্ষে কালীমূর্তি কোনো হিংসা নয় - গভীর প্রতীক: চৈতন্য ও শক্তি - এক সত্যের দুই নাম।

### ভাব ৩: কালী - আদ্যশক্তি, যে স্পন্দন স্রোত {#aspect-3}
এখানে কালী আর কেবল বাহ্য দেবী নন; _তিনি_ **আদ্যশক্তি** - মহাবিশ্বের প্রাণস্পন্দন। অদৃশ্য যে স্পন্দনে অপ্রকাশ্য প্রকাশ পায় - সেটাই শক্তি। সূর্যোদয়, হৃদস্পন্দন, নক্ষত্রের জন্ম-মৃত্যু - সবই তাঁর তালে। যে শক্তি আকাশগঙ্গাকে ঘোরায়, সেই শক্তিই মেরুদণ্ডে [প্রাণ](https://en.wikipedia.org/wiki/Prana) হয়ে সঞ্চারিত। ভাবনা, অনুভূতি, সৃষ্টি-লয় - সবই তাঁরই গতি। [সাংখ্য](https://en.wikipedia.org/wiki/Samkhya)-তে _তিনি_ **মূলপ্রকৃতি**; [অদ্বৈত বেদান্ত](https://en.wikipedia.org/wiki/Advaita_Vedanta)-এ **মায়া-শক্তি** - নির্বিকার ব্রহ্মণের গতিরূপ। দেবীসূক্ত (ঋগ্বেদ ১০.১২৫) আরও বলে:  
> **mayā so annam-atti… ॥ 4** - “যে খায়, দেখে, শ্বাস নেয়, শোনে - সবই আমার দ্বারাই।”  
> **aham-eva vāta-iva… ॥ 8** - “বাতাসের মতো আমি জগত্‌কে চালিত করি; আকাশ-পৃথিবীরও অতীতে আমি সৰ্ব্বত্র।”

### ভাব ৪: কালী - তোমার অন্তঃসত্তা {#aspect-4}
একটু কাছে এসো। জিজ্ঞেস করো - **“আমি কে?”** শরীর? মন? তাহলে “আমি” কোথায় থাকি? মস্তিষ্ক স্ক্যানে কি তোমাকে দেখা যাবে? দেহ যন্ত্র; *আত্মা* সূক্ষ্মতর।  
গভীর নিদ্রায় মন স্তব্ধ, তবু জেগে উঠে বলো, “ভালো ঘুম হয়েছে”- কে জানল?  
ভূমিকা বদলায় - কন্যা মা হয়, ছাত্র শিক্ষক হয় - কিন্তু কোনো স্থিতসত্তা সব দেখে। সেই **সাক্ষী**-ই সত্যিকারের তুমি।

ধ্যানে দেখবে, ভাবনা-অনুভূতি ওঠে-নেমে, এমনকি “আমি”-বোধও আসে-যায়। ডুবে থেকে উঠে *জানো* তুমি ডুবেছিলে - এ জ্ঞানই **সাক্ষী**-র প্রমাণ। সাক্ষীর আকার নেই, সীমানা নেই, জন্ম নেই। তিনি **সৎ–চিত্–আনন্দ** - **ব্রহ্মস্বরূপ**। এখানে **শিব–শক্তি অভেদ** - স্থিতি ও গতি, দুটি নয় - **অদ্বৈত**। ঢেউ–সাগর-জল এক; নাম-রূপে ভেদ।

**ব্রহ্ম কী?** কোনো “বস্তু” নয়; *জ্ঞান করার আধার* বলেই অবস্তুনিষ্ঠ। তাই **“নেতি নেতি”** - যেটা বলা যায়, সবই ব্রহ্ম-প্রকাশের মধ্যে। **স্বামী সর্বপ্রিয়ানন্দ** বলেন: “বিষয় কখনও অবলম্বনকে বস্তু করতে পারে না।” গ্যোডেলের মত - সিস্টেমের ভেতরে এমন সত্য থাকে যা সিস্টেম দিয়ে প্রমাণ হয় না। তেমনি দেহ-মন দিয়ে ব্রহ্মকে বস্তু করা যায় না - কারণ ব্রহ্মই বিষয়।

**“তাহলে ব্রহ্মকে কি কখনো অনুভব করা যাবে না?”**  
বিপরীত - সর্বক্ষণই তুমি *তাই*। **তত্ত্বমসि** - “তুই সেই।” যেমন আলোকিত বস্তু দেখে আলো বোঝা যায়, তেমনি দেখা–ভাবা–জানা - সবই ব্রহ্ম-প্রকাশ। প্রতিটি স্বপ্ন, নীরবতা, চৈতন্য-মুহূর্ত - তাঁরই প্রমাণ। ঢেউ–সাগর-জল যেমন এক, তেমনি তুমি–শক্তি–ব্রহ্ম এক সত্যের তিন দৃষ্টিভঙ্গি।

এই সত্য মৃত্যু স্পর্শ করতে পারে না। দেহ নশ্বর, “আমি”-বোধ ম্লান হয়, কিন্তু তোমার **স্বরূপ** নিত্য - অনাদি, অজ, অবিনশ্বর। **গীতায়** (২.১৭–২৫) শ্রীকৃষ্ণ ঘোষণা করেছেন - আত্মা অক্ষয়; অস্ত্র কাটতে পারে না, অগ্নি পোড়াতে পারে না, জল ভেজাতে পারে না, বায়ু শুকোতে পারে না।

অতএব - **তুমি শক্তি**, অহংকারে নয়, সত্তায়:
> তুমি শক্তিকে “ধরো” না; **তুমিই** শক্তি - অস্থায়ীভাবে দেহে সীমাবদ্ধ, কিন্তু দেহে কখনো সীমিত নও।

এই বোধ উদিত হলে তুলনা–ভেদ সব মিলিয়ে যায়। “আমি” ও “অন্য” বলে থাকে না; সর্বত্র **মা**-কেই দেখ - অনন্ত চৈতন্যে জ্যোতিষ্মত রূপ। উচ্চারিত হয় - **চিদানন্দরূপঃ শিবো’হম্ শিবো’হম্**।

### উপসংহার
বাহিরের পূজা থেকে অন্তরের ধ্যান, শেষে অভেদে লয় - এভাবেই যাত্রা পূর্ণ। “মা” না-পেলেও ক্ষতি নেই - তিনি **আনন্দময়ী**, সদা-প্রকাশময়ী। তুমি যেরূপে দেখতে চাও, সেই রূপেই ধরা দেন। সত্যিকার ব্যাকুলতা থাকলে - “যত মত, তত পথ।”  
কিন্তু সমস্যা - পূজার পর আমরা তাঁকে ভুলে যাই। জীবন ফিরে আসে - কাজ, পরিবার, সময়সীমা। বিজ্ঞান, প্রগতি, সফলতার পিছে ছুটি; ইন্দ্রিয়ভোগে মন বিলাই; দর্শনকে “টেবিল-টক” ভাবি। সেই ব্যস্ততায় মা মনের কোণে নিস্তব্ধ স্মৃতি হয়ে থাকেন।  
তাঁকে পেতে হলে এক মুহূর্ত খেলনা-জীবন ছেড়ে **ব্যাকুলতা** ফেরাতে হবে - যেমন শিশু কেবল *মা*কেই ডাকে, খেলনা শান্ত করতে পারে না। ব্যাকুলতা ছাড়া ক্ষণস্থায়ী জগতে ক্ষণিক সুখেই আটকে থাকি। আর যেই সেই তৃষ্ণা জাগে, বুঝে নিও - মা কোনোদিন দূরে ছিলেন না; নিঃশ্বাসে, দৃষ্টিতে, সুখ–দুঃখে, অন্তরের নীরব চৈতন্যে - **জ্যোতিরও জ্যোতি**, সকল আলোর অন্তরালোক।
</div>
