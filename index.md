<!-- 🔤 Language Switcher -->
<div class="lang-switch" role="group" aria-label="Language switch">
  <button data-lang="en" class="active">English</button>
  <button data-lang="bn">বাংলা</button>
</div>

<style>

/* Restore strong heading sizes inside language sections */
.lang-section h1{ font-size:clamp(2rem,4vw,2.6rem); line-height:1.2; margin:1.2rem 0 .7rem; font-weight:800; }
.lang-section h2{ font-size:clamp(1.6rem,3vw,2rem); line-height:1.25; margin:1.1rem 0 .6rem; font-weight:750; }
.lang-section h3{ font-size:clamp(1.15rem,2vw,1.35rem); line-height:1.3; margin:.9rem 0 .45rem; font-weight:700; }

/* (Optional) hr spacing */
hr{ margin:1.4rem 0; }

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
<section class="welcome-note centered" style="margin-bottom:2rem;">
  <h3>Welcome to <span style="color:#8b0000;">Saha Bari's Kali Puja</span> Website</h3>
  <p>
    Click on the links below to listen to the songs containing the lines near the <em>mondop</em> and the <em>book stall</em>.
    This year, our prayer has been simple - that <strong>Maa</strong> may enter our lives and show us the
    path to Enlightenment. To guide us toward living each moment fully immersed in Her presence.
  </p>
</section>

<section class="video-tiles">
  <a class="video-tile" href="https://www.youtube.com/watch?v=sADh9yMDIHE&list=RDsADh9yMDIHE&index=1" target="_blank" rel="noopener">
    <div class="icon" aria-hidden="true">
      <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 3a9 9 0 00-9 9v6a3 3 0 003 3h1a2 2 0 002-2v-4a2 2 0 00-2-2H5v-1a7 7 0 0114 0v1h-2a2 2 0 00-2 2v4a2 2 0 002 2h1a3 3 0 003-3v-6a9 9 0 00-9-9z"></path></svg>
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

## Darshon E Maa Er Dorshon
Being the first of the ten [Mahavidyas](https://en.wikipedia.org/wiki/Mahavidya), [Maa Kali](https://en.wikipedia.org/wiki/Kali) is the epitome of [Shakti](https://en.wikipedia.org/wiki/Shakti). _Her_ iconography depicts _Her_ as "ugra" (fierce) - dark as the darkest [Kartik Amavasya](https://en.wikipedia.org/wiki/Amavasya) night sky, with three wide-open eyes that see past time, long tangled hair, a lolling crimson tongue, and a garland of countless skulls symbolizing the passing of time - innumerable births and deaths (*Kaal*). _She_ stands on [Lord Shiva](https://en.wikipedia.org/wiki/Shiva), in the cremation ground (*samshan*). In _Her_ left hands, _She_ holds a severed head and a *kharga* (scimitar), symbols of the destruction of [Ahamkara](https://en.wikipedia.org/wiki/Ahamkara) (ego, the “I” consciousness) and [Avidya](https://en.wikipedia.org/wiki/Avidy%C4%81_(Hinduism)) (ignorance). In _Her_ right hands, _She_ blesses and grants boons through the [Abhaya](https://en.wikipedia.org/wiki/Abhayamudra) and [Varada mudra](https://en.wikipedia.org/wiki/Varadamudra).
Despite this fierce iconography, we love and adore _Her_ in our own ways. For example, my sister, looking at our community's (*para*) Kali idol (*murti*), exclaimed, “Maa ke khub cute dekhte lagche” (Maa looks so cute). That's the magic of Kali - terrifying yet tender, destructive yet deeply loving.

_But who really is Maa Kali? What does She signify? **How can we see Her as Thakur Sri Ramakrishna saw Her?**_  
Let's take a journey together - to see Maa as the Mother, as Power, as the Primordial Energy, and as the Self within, each revealing a different facet of the same truth. Understanding each, we discover that how we see Maa depends on our *Bhava* - the inner feeling with which we approach Her.

<!-- 4 TILES (OVERVIEW) -->
<div class="tiles-4">
  <a class="tile" href="#aspect-1">
    <div class="tile-label">Bhava 1</div>
    <h3>Kali as The Divine Mother</h3>
  </a>
  <a class="tile" href="#aspect-2">
    <div class="tile-label">Bhava 2</div>
    <h3>Kali as The Power of Shiva</h3>
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

<hr />

### Bhava 1: Kali as the Divine Mother {#aspect-1}
At this level, Shakti appears in the form of Maa Kali, Maa Durga, Maa Saraswati, or any motherly power we worship. _She_ is external to us, our divine protector, our guide, our nurturer. We call out to _Her_ as we would to our earthly mother. Sometimes in love, sometimes in fear, but always in faith. _She_ destroys evil and removes obstacles, yet her destruction is compassionate, which clears the path for light to enter. _She_ blesses those who walk the path of [Dharma](https://en.wikipedia.org/wiki/Dharma), and gently corrects those who stray. Understanding _Her_ in this way is [Bhakti Yoga](https://en.wikipedia.org/wiki/Bhakti_yoga), the path of devotion. Here, the devotee and the Divine are two separate beings bound by love. It's a relationship of sweetness, surrender, and emotion - a [_Rasa_](https://en.wikipedia.org/wiki/Rasa_(theology)) (flavour) that fills the heart with bliss.

### Bhava 2: Kali as Shakti - The Power of Shiva {#aspect-2}
At a deeper level, Maa Kali is not merely someone outside who blesses us; _She_ is the very Power of the Absolute (Shiva). _She_ is Shiva's ardhangini - _His_ other half, _His_ pulse. Without _Her_, Shiva is _sava_ - motionless, pure stillness without expression. _She_ is _His_ expressive power, the one who makes consciousness move. As mentioned in the 6th mantra of the [Devi Sukta](https://en.wikipedia.org/wiki/Dev%C4%ABs%C5%ABkta) ([Ṛgveda: X.125](https://en.wikipedia.org/wiki/Rigveda)):

> **ahaṃ rudrāya dhanurā tanomi brahmadviṣe śarave hantavā u, ahaṃ janāya samadaṃ kṛṇomy-ahaṃ dyāvā-pṛthivī āviveśa ॥** 6
>_(Meaning: I bend the bow for Rudra to slay the demonic enemies of the noble. I battle the enemies of my devotees. Indeed, I pervade heaven and earth.)_

This is [Tantric](https://en.wikipedia.org/wiki/Tantra) [non-duality philosophy](https://en.wikipedia.org/wiki/Nondualism) (Shiva-Shakti tattva philosophy), where Shiva is pure, unchanging consciousness (Cit), and Shakti is the vibration, the movement (Spanda) of that consciousness. Together they form existence itself - the stillness and the dance. When Maa Kali dances, the universe comes alive; when _She_ stops, everything returns to stillness. Every breath, every heartbeat, every flash of thought is her movement within the vast silence of Shiva. In the Kali Tantra and Sakta texts, this union is described as a constant embrace, where Shiva, lying below, symbolizes the silent foundation of awareness, while Kali, standing upon _Him_, symbolizes energy rising and playing upon that awareness. When we recognize this, the image of Kali standing on Shiva is no longer "violent" but profoundly symbolic: consciousness and energy - two names for one Reality, forever entwined.

### Bhava 3: Kali as the Primordial Power that Flows through Us {#aspect-3}
At this level, Kali is no longer just an external goddess or even the power of Shiva. _She_ is the primordial pulse that keeps the universe alive. Shakti is the unseen rhythm of existence, the force by which the unmanifest becomes manifest. The rising sun, the beating of your heart, the birth and death of stars - all dance to _Her_ rhythm. The same energy that spins galaxies also hums within your spine as [Prana](https://en.wikipedia.org/wiki/Prana). Every thought that flashes across your mind, every surge of emotion, every act of creation or destruction - all are movements of Shakti. _She_ is the power that makes perception possible, the background vibration that turns pure consciousness into experience. When you feel inspired, when you love deeply, when you suffer and still rise again - that's _Her_ too. Shakti is not "out there"; _She_ is the current that flows through everything that is. According to [Samkhya Philosophy](https://en.wikipedia.org/wiki/Samkhya), _She_ is Mūla-Prakṛti, the first cause. In [Advaita Vedanta](https://en.wikipedia.org/wiki/Advaita_Vedanta), _She_ is [Maya-Shakti](https://en.wikipedia.org/wiki/Maya_(religion)#Hinduism), the dynamic nature of [Nirguna Brahman](https://www.bbc.co.uk/bitesize/guides/zrf6pbk/revision/2) - pure stillness appearing as motion. Kali is that very motion - timeless energy taking form as time itself. As mentioned in the 4th and 8th mantras of the Devi Sukta (Ṛgveda: X.125):
> **mayā so annam-atti yo vipaśyati yaḥ prāṇiti ya īṃ śṛṇotyuktam, amantavo māṃ ta upa kṣiyanti śrudhi-śruta śraddhivaṃ te vadāmi ॥** 4
>_(Meaning: He who eats food, sees, breathes, and hears that is spoken, does so through me. Those who are ignorant of me perish. You, who have ears, listen — I tell you that which is deserving of Śraddhā.)_
>
> **aham-eva vāta-iva pra vāmy-ārabhamāṇā bhuvanāni viśvā, paro divā para enā pṛthivyaitāvatī mahinā saṃ babhūva ॥** 8
> _(Meaning: Like the wind that blows, I set in motion all the created things. I am beyond the sky and the earth and I have become all this, in my own splendour.)_

### Bhava 4: Kali as Your Inner Being {#aspect-4}
Now come close. Ask yourself the question **"Who am I?"** Are you the body? The mind? If so, then point me to where in the body "you" reside? You might point towards your head and say, _"Here, in the brain"_. But, if I take an MRI of your brain, will I find you sitting there? No, right? The body is a tool, an instrument. The atma is subtler.

Then maybe you will say, _"I am the mind - my thoughts, feelings, memories"_. But think again. In deep sleep, the mind goes silent, and yet you remain! You wake and say, "I slept well". Someone clearly witnessed even that blankness. Or perhaps you will say, _"I am the social roles I play - as a parent, a child, a doctor, a friend, etc."_ - an idea which resonates among many cognitive scientists. But roles change every day. The daughter becomes a mother, the student becomes a teacher, the employee becomes the boss. Your knowledge, emotions, preferences, even your opinions, evolve with time - yet something constant watches it all. Who keeps track of all these changes? Who says, "I was different before"? That quiet witness - that awareness which notes change - is the real you.

Let's understand it deeper. If you observe the mind carefully in meditation, you will see thoughts rise and fall, emotions come and go, and even the feeling of "I" fades and returns. During moments of deep focus, such as reading, painting, or even watching a film, you forget time, body, and surroundings. Yet afterward, you know you were absorbed. That knowing is proof of the silent Witness - the [Sakshi](https://en.wikipedia.org/wiki/Sakshi_(witness)) that never sleeps. This Witness has no shape, no boundary, no birth. It is pure Awareness - [Sat-Cit-Ananda](https://en.wikipedia.org/wiki/Saccid%C4%81nanda), the essence of [Brahman](https://en.wikipedia.org/wiki/Brahman). At this level, Shiva and Shakti merge. Stillness and movement, energy and consciousness, they are not two - they are Advaita. Like wave and ocean, they differ only in name and form (nama and rupa).

**What is Brahman?**

Brahman is not a "cosmic thing". _It_ cannot be objectified, because _It_ is the very ground of knowing. Our language inevitably treats _It_ as an object, but _It_ is that by which even language shines. That's why the sages used the method of ["Neti Neti"](https://en.wikipedia.org/wiki/Neti_neti) (not this, not that) to point beyond words. Whatever you can describe is already within the light of Brahman. As [Swami Sarvapriyananda](https://www.vedantany.org/introductory-lectures) beautifully says, _"The subject can never be the object of experience"_. It's like [Gödel's Incompleteness Theorem](https://en.wikipedia.org/wiki/G%C3%B6del%27s_incompleteness_theorems) in spiritual form: within any system, there are truths that the system itself cannot prove. Likewise, within this finite body-mind system, we can't "know" Brahman as an object - because Brahman is the subject and this body-mind system is the object.

You might dejectedly wonder, **"Then can I never experience Brahman?"**

The paradox is, you already are experiencing _It_, always. Because, as the [Chandogya Upanishad](https://en.wikipedia.org/wiki/Chandogya_Upanishad) mentions, you are _It_. [**Tat tvam asi**](https://en.wikipedia.org/wiki/Mah%C4%81v%C4%81kyas) — You are That. Just as you infer the presence of light from the objects it reveals, you can infer Brahman from the very fact that you see, think, and feel. Objects in a room are not visible in the absence of light. Hence, seeing the objects is evidence of the presence of the illuminating light. Similarly, this entire existence is lit by That Consciousness. Every dream, every silence, every moment of awareness, every experience of yours is _Its_ evidence. Even the question "Can I experience Brahman?" arises within _Its_ light. Just like the ocean and its waves are nothing but water, you and Shakti are nothing but manifestations of Brahman.

This is the unchanging truth that death cannot touch. Your body will die, your mind and the sense of "I" will dissolve, but your Swarupa (your true essence) is eternal. It is infinite, unborn, and deathless. As Sri Krishna declares in the [Bhagavad Gita](https://www.holy-bhagavad-gita.org/index/) (2.17-2.25): the Self is indestructible; weapons cannot cut it, fire cannot burn it, water cannot wet it, wind cannot dry it.


As Sri Krishna declares in the [Bhagavad Gita](https://www.holy-bhagavad-gita.org/index/):

> **avināśhi tu tadviddhi yena sarvam idaṁ tatam, vināśham avyayasyāsya na kaśhchit kartum arhati ॥** (2.17)
> 
> **antavanta ime dehā nityasyoktāḥ śharīriṇaḥ, anāśhino ’prameyasya tasmād yudhyasva bhārata ॥** (2.18)
> 
> **ya enaṁ vetti hantāraṁ yaśh chainaṁ manyate hatam, ubhau tau na vijānīto nāyaṁ hanti na hanyate ॥** (2.19)
> 
> **na jāyate mriyate vā kadāchin, nāyaṁ bhūtvā bhavitā vā na bhūyaḥ, ajo nityaḥ śhāśhvato ’yaṁ purāṇo, na hanyate hanyamāne śharīre ॥** (2.20)
>
> **nainaṁ chhindanti śhastrāṇi nainaṁ dahati pāvakaḥ, na chainaṁ kledayantyāpo na śhoṣhayati mārutaḥ ॥** (2.23)
>
> **achchhedyo ’yam adāhyo ’yam akledyo ’śhoṣhya eva cha, nityaḥ sarva-gataḥ sthāṇur achalo ’yaṁ sanātanaḥ ॥** (2.24)
>
> **avyakto ’yam achintyo ’yam avikāryo ’yam uchyate, tasmādevaṁ viditvainaṁ nānuśhochitum arhasi ॥** (2.25)

So yes - **you are Shakti**, but not in the egoic sense of possessing power.
> You don't "have" Shakti; you are Shakti — localized for a while in this body, yet never limited by it.

When that insight dawns, all comparison dissolves. You no longer see "yourself" and "others"; you see Maa everywhere — the same infinite, ever-living consciousness shining as every form. You realize **Chidanada roopah Shivoham Shivoham**, as nicely sung in [Nirvana Shatakam.](https://www.youtube.com/watch?v=Ed_RsCvuPBQ&list=RDEd_RsCvuPBQ&start_radio=1)

### Conclusion
And thus, the journey completes. From worshipping _Her_ outside, to finding _Her_ within, to finally dissolving as _Her_. It's alright if we can't always "find" the Mother. She is Anondomoyee - ever-blissful, ever-revealing. She appears in whatever form you are ready to see. And if you truly long for Her, She will take the shape of your longing. As Thakur said, "Joto mot, toto poth" (As many faiths, so many paths). Truly, each heart has its own path to the Mother, and She expresses _Herself_ in each life in a unique way.

But here lies the real difficulty. Once the days of the festival pass, we tend to forget _Her_. "Life" rushes back in - work, family, deadlines, responsibilities. We become busy again: busy chasing science, progress, and success; busy offering our minds to the pleasures of the senses; busy living what we call "real life", while treating the philosophical side of life as mere theory - something to be discussed idly over a cup of tea (aantlami), but never actually lived. And in that busyness, the Mother becomes a faint memory - a quiet presence tucked away in some forgotten corner of the heart.

To truly find _Her_ again, we must, even for a moment, set aside these toys of worldly life and rekindle that yearning - that sacred restlessness (byakulata). As Thakur said, we must abandon our toys and call out for the Mother, just as a child cries only for Ma and is pacified by nothing else - not even their favorite playthings. Without that yearning, we remain content with the fleeting pleasures of a fleeting world, never truly happy, never truly fulfilled. Look around you - can you find a single person who says, "Yes, I am perfectly happy with my life. I want nothing more, no further achievement, no added comfort or pleasure."?

But when that longing for the Mother awakens, even for a single moment, you realize that _She_ was never gone. _She_ was there all along - in your breath, in your gaze, in your moments of joy and sorrow, in that silent awareness within you - the **Jyotir-o-Jyoti**.

### Acknowledgement
With deep gratitude, I thank [Swami Samarpanananda ji](https://en.wikipedia.org/wiki/Swami_Samarpanananda), [Swami Sarvapriyanada ji](https://en.wikipedia.org/wiki/Swami_Sarvapriyananda), and [Swami Vimalatmanada ji](https://belurmath.org/tentative-programme-of-srimat-swami-vimalatmananda-ji-maharaj/) for being three pillars in the form of gurus in my life. Whatever is clear or true in this article is due to them; any errors are mine alone. Swami Samarpanananda ji, a gifted teacher and acharya of Hindu spiritual texts. Many of the references to the Rig Veda Suktas and their interpretations are from his [Indian Spiritual Heritage](https://www.youtube.com/@IndianSpiritualHeritage) class notes. Swami Sarvapriyananda ji, for [his inspiring lectures](https://www.vedantany.org/lectures) on Vedantic inquiry into the Self and the Gita, which heavily influenced this article. [Swami Vimalatmananda ji](https://www.rkmyogodyan.org/), my diksha guru, my kandari.

</div>

<!-- =========================================================
     BENGALI VERSION
========================================================= -->
<div class="lang-section lang-bn" markdown="1">

<section class="welcome-note centered" style="margin-bottom:2rem;">
  <h3>স্বাগতম <span style="color:#8b0000;">সাহা বাড়ির কালীপূজা</span> ওয়েবসাইটে</h3>
  <p>
    নিচের লিঙ্কগুলোতে ক্লিক করে <em>মণ্ডপ</em> ও <em>বইয়ের স্টলের</em> কাছে গানের লাইনগুলির রেকর্ডিং শুনতে পারেন।
    এই বছর আমাদের প্রার্থনা খুবই সহজ। <strong>মা</strong> যেন আমাদের জীবনে প্রবেশ করে আমাদের <em>জ্ঞানার্জনের</em> পথ দেখায়। আমরা যেন মায়ের উপস্থিতি সর্বদা অনুভব করতে পারি।
  </p>
</section>

<section class="video-tiles">
  <a class="video-tile" href="https://www.youtube.com/watch?v=sADh9yMDIHE&list=RDsADh9yMDIHE&index=1" target="_blank" rel="noopener">
    <div class="icon" aria-hidden="true">
      <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 3a9 9 0 00-9 9v6a3 3 0 003 3h1a2 2 0 002-2v-4a2 2 0 00-2-2H5v-1a7 7 0 0114 0v1h-2a2 2 0 00-2 2v4a2 2 0 002 2h1a3 3 0 003-3v-6a9 9 0 00-9-9z"></path></svg>
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
    মা কালীকে বিভিন্নভাবে বিভিন্ন রূপে দেখা — এই বিষয়ে আমরা নিচে একটি ছোট্ট প্রবন্ধ লিখেছি। পড়ে দেখবেন। আপনি যেন মায়ের দর্শন পান, ঠিক যেমন করে আপনার মন চায়। <strong>জয় মা!</strong>
  </p>
</section>

<p align="center">
  <img src="{{ '/kali_pic_2024.png' | relative_url }}" alt="মা কালী"
       style="width:70%; max-width:600px; border-radius:14px;">
</p>

## মায়ের দার্শনিক দর্শন
দশ [মহাবিদ্যার](https://en.wikipedia.org/wiki/Mahavidya) প্রথম মহাবিদ্যা [মা কালী](https://en.wikipedia.org/wiki/Kali)। তিনি শক্তিরূপিণী। উগ্র তাঁর রূপ। তাঁর গায়ের রঙ কার্তিকী অমাবস্যার গভীর অন্ধকারের থেকেও কালো। তিনি ত্রিনয়নী - সময়-কাল-এর ঊর্ধ্বে। তাঁর জটার মতো লম্বা চুল, লাল জিহ্বা, আর গলায় অসংখ্য খুলি দিয়ে গাঁথা মালা, যা অনন্ত জন্ম আর মৃত্যু (কাল)-এর প্রতীক। তিনি স্বয়ং পশুপতির বুকে শ্মশানে বিরাজমান। তাঁর বাঁ হাতে কাটা মুণ্ডু আর খড়্গ - [অহংকার](https://en.wikipedia.org/wiki/Ahamkara) আর [অবিদ্যার](https://en.wikipedia.org/wiki/Avidy%C4%81_(Hinduism)) বিনাশের প্রতীক। তিনি এক ডান হাতে আশ্বাস দিচ্ছেন [অভয় মুদ্রায়](https://en.wikipedia.org/wiki/Abhayamudra), আবার আর এক ডান হাতে বরদান দিচ্ছেন [বরদা মুদ্রায়](https://en.wikipedia.org/wiki/Varadamudra)।
এই উগ্র রূপ হওয়া সত্ত্বেও আমরা ভয় না পেয়ে মাকে নিজ নিজ ভাবে স্নেহ করি আর ভালোবাসি। এই আগের দিন বোন পাড়ার কালীমূর্তি দেখে বলল, “মা-কে খুব কিউট দেখতে লাগছে।” এরকম অদ্ভুতই মায়ের টান - তিনি উগ্র হয়েও স্নেহময়ী।

তবে মা কালী কে? তিনি কিসের প্রতীক? **তাঁকে আমরা কীভাবে দেখতে পারি, ঠিক যেমন ঠাকুর রামকৃষ্ণ সবসময় দেখতেন?**
চলুন একসাথে এক যাত্রায়, যেখানে মাকে আমরা চার রূপে দেখব - মাতারূপে, শক্তিরূপে, আদ্যশক্তিরূপে, আর আমাদের অন্তঃসত্তারূপে। ঠিক যেমন ঠাকুর রামকৃষ্ণ বলেছেন, _"যত মত, তত পথ।"_ তেমনি প্রতিটি রূপ মা-কে দেখার নানা পথ। আমাদের ভাবানুযায়ী যে রূপে চাই, আমরা মাকে সর্বদাই দেখতে পারি।

<div class="tiles-4">
  <a class="tile" href="#aspect-1">
    <div class="tile-label">ভাব ১</div>
    <h3>দিব্য জননী</h3>
  </a>
  <a class="tile" href="#aspect-2">
    <div class="tile-label">ভাব ২</div>
    <h3>শিবের সচল শক্তি</h3>
  </a>
  <a class="tile" href="#aspect-3">
    <div class="tile-label">ভাব ৩</div>
    <h3>আদ্যশক্তি</h3>
  </a>
  <a class="tile" href="#aspect-4">
    <div class="tile-label">ভাব ৪</div>
    <h3>অন্তরের আমি</h3>
  </a>
</div>

<hr />

### ভাব ১: দিব্য জননী {#aspect-1}
শক্তি প্রকাশিত হন মা কালী, মা দুর্গা, মা সরস্বতী এবং নানান মাতৃশক্তিরূপে। তিনি আমাদের সৃষ্টি করেছেন, বিপদ থেকে রক্ষা করেন, আমাদের ভালো রাখেন। যেমন আমরা জন্মদাত্রী মাকে ডাকি, তেমনি শক্তিরূপে মাকেও ডাকি - ভালো-খারাপ দু’সময়েই। তিনি অধর্মের নাশ করেন, বাধা সরান, আমাদের [ধর্মের](https://en.wikipedia.org/wiki/Dharma) পথে চলতে শেখান। আর যখন আমরা অধর্মের দিকে ঝুঁকে পড়ি, তিনি মমতা-সহ আমাদের সংশোধন করেন। মাকে এই রূপে দেখা-ই [ভক্তিযোগ](https://en.wikipedia.org/wiki/Bhakti_yoga) - মাধুর্য, স্নেহ ও আন্তরিকতায় ভরা।

### ভাব ২: শিবের সচল শক্তি {#aspect-2}
আরও গভীরে গেলে মা কালী কেবল বাহিরের কোনো সত্তা নন; _তিনি_ **পরম সত্যের শক্তি (শিব)**। _তিনি_ শিবের *অর্ধাঙ্গিনী* - তাঁর স্পন্দন। শক্তি ছাড়া শিব *শব* - নিস্তরঙ্গ চৈতন্য। _তিনি_ সেই প্রকাশশক্তি, যিনি চৈতন্যকে গতিময় করেন। [দেবীসূক্ত](https://en.wikipedia.org/wiki/Dev%C4%ABs%C5%ABkta) (ঋগ্বেদ ১০.১২৫) বলে:

> **ahaṃ rudrāya… ॥ 6** - “আমি রুদ্রের ধনুক টানি… আকাশ-পাতাল ভেদ করে আমি বিরাজমান।”

এটাই [তন্ত্র](https://en.wikipedia.org/wiki/Tantra)-র **শিব–শক্তি তত্ত্ব**: শিব = চিত্ (নির্বিকার চৈতন্য), শক্তি = স্পন্দ (চৈতন্যের আন্দোলন)। দু’য়ে মিলে সৃষ্টিস্বরূপ - *নিঃস্তব্ধতা ও নৃত্য*। কালী নৃত্য করলে বিশ্ব জেগে ওঠে; থামলে সব নিস্তব্ধ। প্রতিটি নিঃশ্বাস, হৃদস্পন্দন, চিন্তার ঝলক - শিবের নিস্তব্ধতায় মায়েরই নৃত্য। তাই শিব-বক্ষে কালীমূর্তি কোনো হিংসা নয় - গভীর প্রতীক: চৈতন্য ও শক্তি - এক সত্যের দুই নাম।

### ভাব ৩: আদ্যশক্তি {#aspect-3}
এখানে কালী আর কেবল বাহ্য দেবী নন; _তিনি_ **আদ্যশক্তি** - মহাবিশ্বের প্রাণস্পন্দন। অদৃশ্য যে স্পন্দনে অপ্রকাশ্য প্রকাশ পায় - সেটাই শক্তি। সূর্যোদয়, হৃদস্পন্দন, নক্ষত্রের জন্ম-মৃত্যু - সবই তাঁর তালে। যে শক্তি আকাশগঙ্গাকে ঘোরায়, সেই শক্তিই মেরুদণ্ডে [প্রাণ](https://en.wikipedia.org/wiki/Prana) হয়ে সঞ্চারিত। ভাবনা, অনুভূতি, সৃষ্টি-লয় - সবই তাঁরই গতি। [সাংখ্য](https://en.wikipedia.org/wiki/Samkhya)-তে _তিনি_ **মূলপ্রকৃতি**; [অদ্বৈত বেদান্ত](https://en.wikipedia.org/wiki/Advaita_Vedanta)-এ **মায়া-শক্তি** - নির্বিকার ব্রহ্মণের গতিরূপ। দেবীসূক্ত (ঋগ্বেদ ১০.১২৫) আরও বলে:  
> **mayā so annam-atti… ॥ 4** - “যে খায়, দেখে, শ্বাস নেয়, শোনে - সবই আমার দ্বারাই।”  
> **aham-eva vāta-iva… ॥ 8** - “বাতাসের মতো আমি জগত্‌কে চালিত করি; আকাশ-পৃথিবীরও অতীতে আমি সৰ্ব্বত্র।”

### ভাব ৪: অন্তরের আমি {#aspect-4}
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
