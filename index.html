import React, { useState, useEffect, useRef } from 'react';
import { Plus, X, ArrowLeft, ArrowRight, MapPin, Calendar, Heart, Loader2, Pencil, Trash2 } from 'lucide-react';

/* =========================================================
   STYLES — fonts, CSS variables, base layout
   ========================================================= */
const Styles = () => (
  <style>{`
    @import url('https://fonts.googleapis.com/css2?family=Markazi+Text:wght@400;500;600;700&family=Tajawal:wght@200;300;400;500;700;900&display=swap');

    :root {
      --cream: #F5EFE5;
      --cream-2: #EFE8DA;
      --cream-3: #FAF5EC;
      --ink: #1F1A14;
      --ink-soft: #4A413A;
      --ink-mute: #847B70;
      --terracotta: #B85C43;
      --terracotta-dark: #8E3F2C;
      --gold: #E8C547;
      --tan: #D4C8B5;
      --tan-2: #E2D8C5;
      --line: rgba(31,26,20,0.12);
    }

    * { box-sizing: border-box; }
    html, body, #root { background: var(--cream); }
    body { font-family: 'Tajawal', system-ui, sans-serif; color: var(--ink); }

    .display { font-family: 'Markazi Text', 'Amiri', serif; line-height: 1.15; letter-spacing: -0.005em; }
    .body { font-family: 'Tajawal', sans-serif; }

    .highlight-name {
      background-image: linear-gradient(180deg, transparent 55%, var(--gold) 55%, var(--gold) 92%, transparent 92%);
      padding: 0 4px;
    }

    .card-hover { transition: transform 0.35s cubic-bezier(.2,.7,.2,1), box-shadow 0.35s ease; }
    .card-hover:hover { transform: translateY(-4px); box-shadow: 0 18px 40px -20px rgba(31,26,20,0.25); }

    .nav-link { position: relative; transition: color .2s ease; }
    .nav-link::after {
      content: ''; position: absolute; right: 0; left: 0; bottom: -6px;
      height: 2px; background: var(--terracotta); transform: scaleX(0); transform-origin: right;
      transition: transform .3s ease;
    }
    .nav-link:hover::after, .nav-link.active::after { transform: scaleX(1); }

    .grain {
      background-image:
        radial-gradient(circle at 20% 25%, rgba(255,255,255,0.35) 0%, transparent 50%),
        radial-gradient(circle at 80% 75%, rgba(0,0,0,0.22) 0%, transparent 55%);
    }

    .timeline-line {
      background: linear-gradient(180deg, var(--terracotta) 0%, var(--gold) 50%, var(--tan) 100%);
    }

    .fade-in { animation: fadeIn .5s ease both; }
    @keyframes fadeIn { from { opacity: 0; transform: translateY(8px);} to { opacity: 1; transform: none;} }

    .btn-primary {
      background: var(--ink); color: var(--cream-3);
      transition: background .2s ease, transform .2s ease;
    }
    .btn-primary:hover { background: var(--terracotta); }
    .btn-primary:active { transform: translateY(1px); }

    .btn-ghost { color: var(--ink); transition: color .2s ease; }
    .btn-ghost:hover { color: var(--terracotta); }

    .input-field {
      background: var(--cream-3); border: 1px solid var(--line);
      color: var(--ink); font-family: 'Tajawal', sans-serif;
      padding: 10px 14px; border-radius: 6px; width: 100%;
      transition: border-color .2s ease, box-shadow .2s ease;
    }
    .input-field:focus { outline: none; border-color: var(--ink); box-shadow: 0 0 0 3px rgba(31,26,20,0.08); }

    .ornament { color: var(--terracotta); letter-spacing: 0.4em; }

    .scrollbar-hide::-webkit-scrollbar { display: none; }
    .scrollbar-hide { -ms-overflow-style: none; scrollbar-width: none; }

    @media (max-width: 640px) {
      .display-xl { font-size: 2.5rem !important; }
    }
  `}</style>
);

/* =========================================================
   PALETTES & MOTIFS — each trip cover is gradient + SVG
   ========================================================= */
const PALETTES = {
  warm:   { from: '#E8C547', to: '#B85C43', motif: '#3A1F10', text: '#1F1A14' },
  dusk:   { from: '#4A2C4A', to: '#B85C43', motif: '#F5EFE5', text: '#FAF5EC' },
  ocean:  { from: '#2C5F6F', to: '#83B0C2', motif: '#F5EFE5', text: '#FAF5EC' },
  rose:   { from: '#E8B4B4', to: '#8B4F58', motif: '#3A1F25', text: '#FAF5EC' },
  forest: { from: '#3F5F3F', to: '#9BB78A', motif: '#1A2A1A', text: '#FAF5EC' },
  sand:   { from: '#E5CDA8', to: '#9A7B4F', motif: '#3A2810', text: '#1F1A14' },
  night:  { from: '#1A2847', to: '#4A5F8E', motif: '#F5EFE5', text: '#FAF5EC' },
  spice:  { from: '#D85A2E', to: '#F0A858', motif: '#3A1810', text: '#1F1A14' },
  mist:   { from: '#A8B5B0', to: '#5C7068', motif: '#1A2520', text: '#FAF5EC' },
};

const Motif = ({ name, color }) => {
  const p = { fill: color, opacity: 0.9 };
  switch (name) {
    case 'mosque':
      return (
        <g {...p}>
          <rect x="14" y="38" width="3" height="55" />
          <circle cx="15.5" cy="36" r="3" />
          <path d="M14 30 L15.5 24 L17 30 Z" />
          <rect x="83" y="38" width="3" height="55" />
          <circle cx="84.5" cy="36" r="3" />
          <path d="M83 30 L84.5 24 L86 30 Z" />
          <path d="M28 93 L28 62 Q28 42 50 42 Q72 42 72 62 L72 93 Z" />
          <rect x="46" y="32" width="8" height="10" />
          <path d="M48 32 L50 26 L52 32 Z" />
          <rect x="8" y="91" width="84" height="3" />
        </g>
      );
    case 'temple':
      return (
        <g {...p}>
          <rect x="18" y="42" width="64" height="52" />
          <polygon points="14,42 50,18 86,42" />
          <rect x="46" y="20" width="8" height="22" opacity="0.5" fill={color} />
          <rect x="28" y="55" width="6" height="39" opacity="0.4" />
          <rect x="40" y="55" width="6" height="39" opacity="0.4" />
          <rect x="54" y="55" width="6" height="39" opacity="0.4" />
          <rect x="66" y="55" width="6" height="39" opacity="0.4" />
          <rect x="44" y="68" width="12" height="26" opacity="0.55" />
        </g>
      );
    case 'torii':
      return (
        <g {...p}>
          <rect x="14" y="30" width="72" height="6" />
          <rect x="18" y="36" width="64" height="3" />
          <rect x="22" y="39" width="6" height="58" />
          <rect x="72" y="39" width="6" height="58" />
          <rect x="40" y="50" width="20" height="4" />
        </g>
      );
    case 'mountain':
      return (
        <g {...p}>
          <polygon points="2,95 28,38 48,68 70,28 98,95" />
          <polygon points="36,95 56,58 78,82 95,95" opacity="0.55" />
          <circle cx="72" cy="22" r="6" opacity="0.7" />
        </g>
      );
    case 'pyramid':
      return (
        <g {...p}>
          <circle cx="76" cy="24" r="7" opacity="0.85" />
          <polygon points="50,18 5,92 95,92" />
          <polygon points="50,22 22,92 78,92" opacity="0.5" />
          <rect x="0" y="92" width="100" height="3" />
        </g>
      );
    case 'tree':
      return (
        <g {...p}>
          <rect x="46" y="58" width="8" height="35" />
          <circle cx="50" cy="42" r="24" />
          <circle cx="34" cy="50" r="14" opacity="0.85" />
          <circle cx="66" cy="50" r="14" opacity="0.85" />
          <circle cx="50" cy="28" r="10" opacity="0.7" />
          <rect x="0" y="92" width="100" height="2" />
        </g>
      );
    case 'ship':
      return (
        <g {...p}>
          <path d="M8 72 L92 72 L82 88 L18 88 Z" />
          <rect x="48" y="32" width="3" height="40" />
          <polygon points="51,34 78,55 51,55" />
          <polygon points="48,58 24,70 48,70" />
          <path d="M0 88 Q15 84 30 88 T60 88 T100 88 L100 95 L0 95 Z" opacity="0.4" />
        </g>
      );
    case 'cup':
      return (
        <g {...p}>
          <path d="M28 52 Q28 82 50 82 Q72 82 72 52 Z" />
          <ellipse cx="50" cy="52" rx="22" ry="3" />
          <path d="M72 58 Q86 58 86 68 Q86 78 72 78" fill="none" stroke={color} strokeWidth="3" />
          <path d="M40 38 Q40 30 46 28 M50 38 Q50 30 56 28 M60 38 Q60 30 66 28"
                fill="none" stroke={color} strokeWidth="2" opacity="0.55" strokeLinecap="round" />
          <rect x="20" y="84" width="60" height="3" />
        </g>
      );
    case 'lantern':
      return (
        <g {...p}>
          <rect x="48" y="8" width="4" height="14" />
          <ellipse cx="50" cy="50" rx="20" ry="28" />
          <rect x="28" y="22" width="44" height="3" />
          <rect x="28" y="78" width="44" height="3" />
          <path d="M50 30 L50 70" stroke={color} strokeWidth="1" opacity="0.4" fill="none" />
        </g>
      );
    case 'dune':
      return (
        <g {...p}>
          <path d="M0 78 Q25 60 50 72 T100 70 L100 100 L0 100 Z" />
          <path d="M0 88 Q30 75 60 85 T100 82 L100 100 L0 100 Z" opacity="0.55" />
          <circle cx="78" cy="28" r="9" opacity="0.85" />
        </g>
      );
    default:
      return <circle cx="50" cy="50" r="22" {...p} />;
  }
};

const Cover = ({ palette, motif, className = '', children, motifSize = 0.55 }) => {
  const p = PALETTES[palette] || PALETTES.warm;
  const inset = `${((1 - motifSize) / 2) * 100}%`;
  return (
    <div
      className={`relative overflow-hidden ${className}`}
      style={{ background: `linear-gradient(135deg, ${p.from} 0%, ${p.to} 100%)` }}
    >
      <div className="absolute inset-0 grain" />
      <svg
        viewBox="0 0 100 100"
        preserveAspectRatio="xMidYMid meet"
        className="absolute"
        style={{ inset, width: `${motifSize * 100}%`, height: `${motifSize * 100}%` }}
      >
        <Motif name={motif} color={p.motif} />
      </svg>
      {children}
    </div>
  );
};

/* =========================================================
   SAMPLE DATA
   ========================================================= */
const SAMPLE_TRIPS = [
  {
    id: 'istanbul_2026',
    title: 'أزقّة إسطنبول لا تَشيخ',
    subtitle: 'بين البوسفور والأذان، رحلةٌ في قلب المدينة التي تجمع قارّتين في نَفَسٍ واحد.',
    location: 'إسطنبول، تركيا',
    date: '15 مارس 2026',
    palette: 'spice',
    motif: 'mosque',
    featured: true,
    emoji: '🕌',
    accent: '✦',
    intro: 'حين تطأ قدمُك إسطنبول لأول مرة، تشعر أن المدينة تستقبلك بكل قرونها دفعةً واحدة؛ صوت الأذان من مئذنةٍ بعيدة، ورائحة الكستناء المشوية في الشتاء، ونوارس البوسفور التي تطير على مستوى نظرك. لم ندخل المدينة، بل تَسلَّلنا إليها.',
    timeline: [
      {
        id: 'ist_1',
        date: 'اليوم الأول · 15 مارس',
        title: 'أذان المغرب فوق السلطان أحمد',
        text: 'وقفنا في الميدان حين بدأ الأذان من جامع السلطان أحمد، ثم تَلاهُ أذانُ آيا صوفيا، فأذانٌ آخر من بعيد، حتى تحوّلت المدينة كلها إلى نداءٍ واحدٍ مُتعدِّد الأصوات. جلسنا على درجات الحجر، ولم نقُلْ شيئاً.',
        palette: 'dusk',
        motif: 'mosque',
      },
      {
        id: 'ist_2',
        date: 'اليوم الثاني · 16 مارس',
        title: 'قهوةٌ تركيةٌ في مقهى عتيق',
        text: 'في مقهى صغيرٍ في حيّ بَلَط، جلسنا أمام فناجين بنّيّة اللون، نشرب ببُطء، ونراقب القطط التي تسير في الأزقة كأنها صاحبةُ المكان. كان النادل يكلّمنا بالتركية ونردّ بالعربية، ومع ذلك فهمنا بعضنا.',
        palette: 'warm',
        motif: 'cup',
      },
      {
        id: 'ist_3',
        date: 'اليوم الثالث · 17 مارس',
        title: 'عبور البوسفور إلى آسيا',
        text: 'ركبنا العَبّارة من أوروبا إلى آسيا. الرحلة لا تستغرق أكثر من عشرين دقيقة، لكن الإحساس بأنك تعبر قارّتين بهذه السهولة يجعلك تبتسم في صمت. كان البحر متعَباً ذلك اليوم، والريحُ تَقصُّ علينا حكاياتٍ لا نَفهمها.',
        palette: 'ocean',
        motif: 'ship',
      },
    ],
  },
  {
    id: 'petra_2025',
    title: 'البَتراء: مدينةٌ ورديّة',
    subtitle: 'حين نَحَتَ الأنباطُ الجبلَ ليُصبح مدينة، نَحَتوا معه الزمن.',
    location: 'البتراء، الأردن',
    date: '8 نوفمبر 2025',
    palette: 'rose',
    motif: 'temple',
    emoji: '🌹',
    accent: '◆',
    intro: 'مشينا في السِّيق ساعةً كاملةً بين جدران الصخر العالية، ثم انفتحت الفجوة فجأةً على واجهة الخزنة، وكأن المدينة كانت تختبرُ صبرنا قبل أن تكشف نفسها.',
    timeline: [
      {
        id: 'pet_1',
        date: 'اليوم الأول · فجراً',
        title: 'دخول السّيق قبل الشروق',
        text: 'بدأنا المشي قبل شروق الشمس، الجوّ بارد، والصخورُ تَكتُمُ أصواتَ خطواتنا. الصمتُ في السّيق له وزن. حين خرجنا إلى الخزنة، كانت الشمس قد بدأت تَلمسها للتو، فبدا الحجر مشتعلاً بهدوء.',
        palette: 'sand',
        motif: 'mountain',
      },
      {
        id: 'pet_2',
        date: 'اليوم الثاني',
        title: 'صعود الدَّير',
        text: 'ثمانمائة درجةٍ حتى الوصول إلى الدير. حين وصلنا أخيراً، جلسنا أمام الواجهة الضخمة دون كلام، نَدَعُهُ يقول كلَّ شيء. كان البَدويُّ الذي يبيع الشاي يضحك من تعبِنا، فضحكنا معه.',
        palette: 'rose',
        motif: 'temple',
      },
    ],
  },
  {
    id: 'kyoto_2025',
    title: 'كيوتو حين تتفتَّحُ السّاكورا',
    subtitle: 'أسبوعٌ واحدٌ بين المعابد وأزهار الكرز، يكفي لتعرف لماذا يكتبون عنها الشعر.',
    location: 'كيوتو، اليابان',
    date: '2 أبريل 2025',
    palette: 'rose',
    motif: 'torii',
    emoji: '🌸',
    accent: '✿',
    intro: 'وصلنا إلى كيوتو في توقيتٍ مثالي. الساكورا في كل مكان، حتى في الأماكن التي لم نتوقّعها: على جانب الترام، فوق بِركةِ معبد صغير، في فناء بيتٍ تقليدي رأيناه صدفةً.',
    timeline: [
      {
        id: 'kyo_1',
        date: 'اليوم الأول',
        title: 'حديقة ماروياما',
        text: 'جلسنا تحت شجرة كرزٍ عملاقة مع أهل المدينة، نأكل وجبة الهانامي ونراقب البَتلات الورديّة تتساقط ببُطء. شعرنا أن الزمن نفسه يتساقط معها.',
        palette: 'rose',
        motif: 'tree',
      },
      {
        id: 'kyo_2',
        date: 'اليوم الثالث · فجراً',
        title: 'فوشيمي إيناري',
        text: 'مشينا في النفق الذي لا ينتهي من بوّابات التُّوري الحمراء. كنا وحدنا تقريباً عند الفجر. كل بوابةٍ تخفي البوابة التي بعدها، فظَنَّ كلٌّ منا أنه يمشي وحده، ثم نلتقي.',
        palette: 'spice',
        motif: 'torii',
      },
      {
        id: 'kyo_3',
        date: 'الليلة الأخيرة',
        title: 'فوانيس جيون',
        text: 'الحيّ القديم بعد المغرب، الفوانيس مُضاءة، والأزقّةُ خاويةٌ تقريباً. سمعنا صوت شامِيسِن من نافذةٍ مفتوحة، ووقفنا نُنصِت دون أن يدرينا أحد.',
        palette: 'night',
        motif: 'lantern',
      },
    ],
  },
  {
    id: 'salalah_2025',
    title: 'خَريفُ صَلالة',
    subtitle: 'حين يصبح الجنوبُ أخضر، ويُحوِّل الجبلَ إلى بحرٍ من الضباب.',
    location: 'صلالة، عُمان',
    date: '20 أغسطس 2025',
    palette: 'forest',
    motif: 'mountain',
    emoji: '🌿',
    accent: '❋',
    intro: 'الخريف في ظفار ليس فصلاً، إنه حالةٌ مزاجيّة للأرض كلها. القرى تختفي خلف الغيوم، والجبال تتنفّس، والنّاسُ يجلسون على الطرقات يَشربون الشاي وكأنهم في انتظار شيءٍ لا يأتي.',
    timeline: [
      {
        id: 'sal_1',
        date: 'اليوم الأول',
        title: 'جبل صَمحان في الضباب',
        text: 'صعدنا الجبل وقت الظهيرة، لكن الضبابَ كان كثيفاً حتى أننا فقدنا قدرتنا على رؤية السيارة أمامنا. توقّفنا على جانب الطريق، نَزَلنا، ومشينا قليلاً في غيمةٍ نازلة.',
        palette: 'mist',
        motif: 'mountain',
      },
      {
        id: 'sal_2',
        date: 'اليوم الثاني',
        title: 'عين رزات',
        text: 'الماء يَنبُع من الصخر ببساطةٍ مذهلة، يتجمّع في بِركةٍ صافية، ثم يجري إلى الوادي. الناس يأتون من كل مكان، يَملؤون قواريرَهم، ويذهبون.',
        palette: 'forest',
        motif: 'tree',
      },
    ],
  },
  {
    id: 'cairo_2024',
    title: 'صباحاتٌ في خان الخليلي',
    subtitle: 'القاهرة قبل أن تستيقظ، حين تكون لك وحدك.',
    location: 'القاهرة، مصر',
    date: '12 ديسمبر 2024',
    palette: 'sand',
    motif: 'pyramid',
    emoji: '☕',
    accent: '✧',
    intro: 'يقولون إنّ القاهرة لا تنام. لكنها تَخفُتُ في الفجر، تأخذ نَفَساً واحداً قبل صَخَب اليوم، وفي تلك اللحظة بالذات، إذا كنتَ مستيقظاً، تستطيع أن تسمعها تَهمس.',
    timeline: [
      {
        id: 'cai_1',
        date: 'الفجر · اليوم الأول',
        title: 'فطورٌ في فِشاوي',
        text: 'دخلنا مقهى الفِشاوي قبل أن يفتح بتمامه. النادل القديم يَعرف الزبائنَ من أصواتهم. شربنا الشاي بالنعناع، وقرأنا جريدةً قديمةً تُركَتْ على الطاولة المجاورة.',
        palette: 'warm',
        motif: 'cup',
      },
    ],
  },
];

/* =========================================================
   STORAGE HELPERS
   ========================================================= */
const STORAGE_KEY = 'all_trips_v1';

async function loadTripsFromStorage() {
  try {
    const result = await window.storage.get(STORAGE_KEY);
    if (result && result.value) {
      return JSON.parse(result.value);
    }
  } catch (e) {
    // key doesn't exist, fall through
  }
  // seed
  try {
    await window.storage.set(STORAGE_KEY, JSON.stringify(SAMPLE_TRIPS));
  } catch (e) {}
  return SAMPLE_TRIPS;
}

async function saveTripsToStorage(trips) {
  try {
    await window.storage.set(STORAGE_KEY, JSON.stringify(trips));
    return true;
  } catch (e) {
    console.error('Failed to save', e);
    return false;
  }
}

const newId = () => `t_${Date.now()}_${Math.random().toString(36).slice(2, 7)}`;

/* =========================================================
   COMPONENTS
   ========================================================= */

const TopNav = ({ onGoHome, currentView }) => (
  <header className="sticky top-0 z-30 backdrop-blur-md" style={{ background: 'rgba(245,239,229,0.85)', borderBottom: '1px solid var(--line)' }}>
    <div className="max-w-6xl mx-auto px-5 sm:px-8 py-4 flex items-center justify-between gap-4">
      {/* Logo on right (RTL) */}
      <button onClick={onGoHome} className="flex items-center gap-2 group">
        <span className="display text-2xl sm:text-3xl font-semibold" style={{ color: 'var(--ink)' }}>
          إسراء ومُعتَز
        </span>
        <span className="ornament text-sm hidden sm:inline" style={{ color: 'var(--terracotta)' }}>✦</span>
      </button>

      {/* Nav on left */}
      <nav className="flex items-center gap-5 sm:gap-7 text-[15px]" style={{ color: 'var(--ink-soft)' }}>
        <button onClick={onGoHome} className={`nav-link hidden sm:inline ${currentView === 'home' ? 'active' : ''}`}>الرئيسية</button>
        <button onClick={onGoHome} className="nav-link hidden md:inline">الرحلات</button>
        <a className="nav-link hidden md:inline">الوجهات</a>
        <a className="nav-link hidden md:inline">عنّا</a>
      </nav>
    </div>
  </header>
);

const Avatar = ({ name, palette = 'warm' }) => {
  const p = PALETTES[palette];
  return (
    <div
      className="w-9 h-9 rounded-full flex items-center justify-center display text-sm font-semibold shrink-0"
      style={{ background: `linear-gradient(135deg, ${p.from}, ${p.to})`, color: p.text }}
    >
      {name.slice(0, 1)}
    </div>
  );
};

const Byline = ({ date }) => (
  <div className="flex items-center gap-3 flex-wrap">
    <div className="flex items-center -space-x-2 space-x-reverse">
      <Avatar name="إ" palette="warm" />
      <Avatar name="م" palette="ocean" />
    </div>
    <div className="text-[15px]" style={{ color: 'var(--ink-soft)' }}>
      <span className="highlight-name display text-lg font-semibold" style={{ color: 'var(--ink)' }}>
        إسراء ومُعتَز
      </span>
      <span className="mx-2" style={{ color: 'var(--ink-mute)' }}>·</span>
      <span style={{ color: 'var(--ink-mute)' }}>{date}</span>
    </div>
  </div>
);

const FeaturedHero = ({ trip, onOpen }) => (
  <section className="max-w-6xl mx-auto px-5 sm:px-8 pt-10 pb-16 fade-in">
    <div className="flex items-center gap-3 mb-6 text-sm" style={{ color: 'var(--terracotta)' }}>
      <span style={{ letterSpacing: '0.3em' }}>الرحلة المُختارة</span>
      <span className="flex-1 h-px" style={{ background: 'var(--line)' }} />
    </div>

    <Cover
      palette={trip.palette}
      motif={trip.motif}
      motifSize={0.45}
      className="rounded-2xl aspect-[16/10] sm:aspect-[16/8] cursor-pointer card-hover"
    >
      <button onClick={() => onOpen(trip)} className="absolute inset-0" aria-label="فتح الرحلة" />
    </Cover>

    <div className="mt-10 text-center max-w-3xl mx-auto">
      <div className="ornament mb-5 text-base">{trip.accent || '✦'} &nbsp; {trip.location} &nbsp; {trip.accent || '✦'}</div>
      <h1 className="display display-xl text-5xl sm:text-6xl md:text-7xl font-semibold leading-[1.05] mb-5" style={{ color: 'var(--ink)' }}>
        <span className="inline-flex items-center gap-3 flex-wrap justify-center">
          <span className="text-3xl sm:text-4xl">{trip.emoji}</span>
          <span>{trip.title}</span>
        </span>
      </h1>
      <p className="text-lg sm:text-xl leading-relaxed mb-7" style={{ color: 'var(--ink-soft)' }}>
        {trip.subtitle}
      </p>
      <div className="flex justify-center mb-7">
        <Byline date={trip.date} />
      </div>
      <button
        onClick={() => onOpen(trip)}
        className="btn-primary inline-flex items-center gap-2 px-6 py-3 rounded-full text-[15px] font-medium"
      >
        <span>اقرأ الرحلة</span>
        <ArrowLeft className="w-4 h-4" />
      </button>
    </div>
  </section>
);

const TripCard = ({ trip, onOpen }) => (
  <article
    onClick={() => onOpen(trip)}
    className="card-hover cursor-pointer group"
  >
    <Cover palette={trip.palette} motif={trip.motif} motifSize={0.55} className="rounded-xl aspect-[4/3] mb-4" />
    <div className="px-1">
      <div className="text-xs mb-2 ornament" style={{ color: 'var(--terracotta)' }}>{trip.location}</div>
      <h3 className="display text-2xl sm:text-[1.7rem] font-semibold leading-tight mb-2" style={{ color: 'var(--ink)' }}>
        <span className="inline-flex items-baseline gap-2">
          <span className="text-base">{trip.emoji}</span>
          <span>{trip.title}</span>
        </span>
      </h3>
      <p className="text-[15px] leading-relaxed mb-3 line-clamp-2" style={{ color: 'var(--ink-soft)' }}>
        {trip.subtitle}
      </p>
      <div className="text-sm flex items-center gap-2" style={{ color: 'var(--ink-mute)' }}>
        <Calendar className="w-3.5 h-3.5" />
        <span>{trip.date}</span>
      </div>
    </div>
  </article>
);

const TripsGrid = ({ trips, onOpen, onAdd }) => (
  <section className="max-w-6xl mx-auto px-5 sm:px-8 pb-20">
    <div className="flex items-end justify-between gap-4 mb-10 pb-4" style={{ borderBottom: '1px solid var(--line)' }}>
      <div>
        <div className="ornament text-xs mb-2">دفتر الأسفار</div>
        <h2 className="display text-4xl sm:text-5xl font-semibold" style={{ color: 'var(--ink)' }}>
          كلُّ الرحلات
        </h2>
      </div>
      <button
        onClick={onAdd}
        className="btn-primary inline-flex items-center gap-2 px-5 py-2.5 rounded-full text-sm font-medium shrink-0"
      >
        <Plus className="w-4 h-4" />
        <span>رحلة جديدة</span>
      </button>
    </div>

    {trips.length === 0 ? (
      <div className="text-center py-16" style={{ color: 'var(--ink-mute)' }}>
        لا توجد رحلات بعد. ابدأ بإضافة واحدة.
      </div>
    ) : (
      <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10 gap-y-14">
        {trips.map((t) => (
          <TripCard key={t.id} trip={t} onOpen={onOpen} />
        ))}
      </div>
    )}
  </section>
);

const TripDetail = ({ trip, onBack, onAddMoment, onDeleteTrip, onDeleteMoment }) => (
  <article className="fade-in">
    {/* Cover */}
    <Cover palette={trip.palette} motif={trip.motif} motifSize={0.32} className="aspect-[16/9] sm:aspect-[16/7]" />

    <div className="max-w-3xl mx-auto px-5 sm:px-8 -mt-12 sm:-mt-16 relative">
      <div className="rounded-2xl p-7 sm:p-10" style={{ background: 'var(--cream-3)', boxShadow: '0 18px 50px -25px rgba(31,26,20,0.25)' }}>
        <button onClick={onBack} className="btn-ghost inline-flex items-center gap-2 text-sm mb-6">
          <ArrowRight className="w-4 h-4" />
          <span>عودة إلى الرحلات</span>
        </button>

        <div className="flex items-center gap-3 text-sm mb-4" style={{ color: 'var(--terracotta)' }}>
          <MapPin className="w-4 h-4" />
          <span style={{ letterSpacing: '0.05em' }}>{trip.location}</span>
        </div>

        <h1 className="display text-4xl sm:text-5xl md:text-6xl font-semibold leading-[1.1] mb-5" style={{ color: 'var(--ink)' }}>
          <span className="inline-flex items-baseline gap-3 flex-wrap">
            <span className="text-2xl sm:text-3xl">{trip.emoji}</span>
            <span>{trip.title}</span>
          </span>
        </h1>

        <p className="text-lg leading-relaxed mb-6" style={{ color: 'var(--ink-soft)' }}>
          {trip.subtitle}
        </p>

        <div className="flex items-center justify-between flex-wrap gap-4 pb-6 mb-7" style={{ borderBottom: '1px solid var(--line)' }}>
          <Byline date={trip.date} />
          <button
            onClick={() => onDeleteTrip(trip.id)}
            className="text-xs flex items-center gap-1.5 opacity-50 hover:opacity-100 transition-opacity"
            style={{ color: 'var(--ink-mute)' }}
          >
            <Trash2 className="w-3.5 h-3.5" />
            <span>حذف الرحلة</span>
          </button>
        </div>

        {trip.intro && (
          <p className="display text-xl sm:text-2xl leading-[1.6] mb-2" style={{ color: 'var(--ink)' }}>
            {trip.intro}
          </p>
        )}
      </div>
    </div>

    {/* Timeline */}
    <div className="max-w-3xl mx-auto px-5 sm:px-8 mt-16 pb-12">
      <div className="flex items-center gap-3 mb-10">
        <div className="ornament text-xs" style={{ color: 'var(--terracotta)' }}>الخط الزمني</div>
        <span className="flex-1 h-px" style={{ background: 'var(--line)' }} />
      </div>

      {trip.timeline.length === 0 ? (
        <div className="text-center py-10" style={{ color: 'var(--ink-mute)' }}>
          لا توجد لحظات بعد في هذه الرحلة.
        </div>
      ) : (
        <div className="relative pr-8 sm:pr-12">
          {/* vertical line */}
          <div className="absolute top-2 bottom-2 right-3 w-[2px] timeline-line rounded-full" />

          {trip.timeline.map((m, idx) => (
            <div key={m.id} className="relative mb-14 last:mb-0 fade-in">
              {/* dot */}
              <div
                className="absolute right-[-2px] top-2 w-4 h-4 rounded-full"
                style={{ background: PALETTES[m.palette]?.from || 'var(--terracotta)', border: '3px solid var(--cream)' }}
              />

              <div className="text-xs mb-2 ornament" style={{ color: 'var(--terracotta)' }}>
                {m.date}
              </div>

              <h3 className="display text-2xl sm:text-3xl font-semibold mb-4 leading-tight" style={{ color: 'var(--ink)' }}>
                {m.title}
              </h3>

              <Cover palette={m.palette} motif={m.motif} motifSize={0.5} className="rounded-xl aspect-[16/9] mb-5" />

              <p className="text-[17px] leading-[1.9]" style={{ color: 'var(--ink-soft)' }}>
                {m.text}
              </p>

              <button
                onClick={() => onDeleteMoment(trip.id, m.id)}
                className="mt-3 text-xs inline-flex items-center gap-1 opacity-40 hover:opacity-100 transition-opacity"
                style={{ color: 'var(--ink-mute)' }}
              >
                <Trash2 className="w-3 h-3" />
                <span>حذف</span>
              </button>
            </div>
          ))}
        </div>
      )}

      <div className="flex justify-center mt-10">
        <button
          onClick={() => onAddMoment(trip.id)}
          className="btn-primary inline-flex items-center gap-2 px-5 py-2.5 rounded-full text-sm font-medium"
        >
          <Plus className="w-4 h-4" />
          <span>أضف لحظة</span>
        </button>
      </div>
    </div>

    {/* End ornament */}
    <div className="text-center pb-20" style={{ color: 'var(--terracotta)', letterSpacing: '0.6em' }}>
      ✦ &nbsp; ✦ &nbsp; ✦
    </div>
  </article>
);

const Footer = () => (
  <footer className="py-12 text-center text-sm" style={{ borderTop: '1px solid var(--line)', color: 'var(--ink-mute)' }}>
    <div className="display text-2xl mb-2" style={{ color: 'var(--ink)' }}>إسراء ومُعتَز</div>
    <div>مذكّرات سفر · صُنِعَ بحُبٍّ على الطريق</div>
    <div className="mt-4 ornament" style={{ color: 'var(--terracotta)' }}>✦</div>
  </footer>
);

/* =========================================================
   MODALS — Add Trip & Add Moment
   ========================================================= */
const Modal = ({ open, onClose, title, children }) => {
  if (!open) return null;
  return (
    <div className="fixed inset-0 z-50 flex items-center justify-center p-4 fade-in" style={{ background: 'rgba(31,26,20,0.55)' }}>
      <div
        className="relative w-full max-w-lg rounded-2xl p-7 max-h-[90vh] overflow-y-auto"
        style={{ background: 'var(--cream-3)' }}
      >
        <button onClick={onClose} className="absolute top-4 left-4 btn-ghost" aria-label="إغلاق">
          <X className="w-5 h-5" />
        </button>
        <h3 className="display text-3xl font-semibold mb-6" style={{ color: 'var(--ink)' }}>{title}</h3>
        {children}
      </div>
    </div>
  );
};

const PaletteSelect = ({ value, onChange }) => (
  <div className="grid grid-cols-9 gap-2 mt-2">
    {Object.keys(PALETTES).map((key) => {
      const p = PALETTES[key];
      return (
        <button
          key={key}
          onClick={() => onChange(key)}
          className="aspect-square rounded-full transition-transform"
          style={{
            background: `linear-gradient(135deg, ${p.from}, ${p.to})`,
            transform: value === key ? 'scale(1.15)' : 'scale(1)',
            boxShadow: value === key ? '0 0 0 2px var(--ink)' : 'none',
          }}
          aria-label={key}
        />
      );
    })}
  </div>
);

const MotifSelect = ({ value, onChange }) => {
  const motifs = ['mosque', 'temple', 'torii', 'mountain', 'pyramid', 'tree', 'ship', 'cup', 'lantern', 'dune'];
  const labels = {
    mosque: 'مسجد', temple: 'معبد', torii: 'بوابة', mountain: 'جبل',
    pyramid: 'هرم', tree: 'شجرة', ship: 'سفينة', cup: 'فنجان',
    lantern: 'فانوس', dune: 'كثبان',
  };
  return (
    <div className="grid grid-cols-5 gap-2 mt-2">
      {motifs.map((m) => (
        <button
          key={m}
          onClick={() => onChange(m)}
          className="rounded-lg p-2 text-xs transition-all"
          style={{
            background: value === m ? 'var(--ink)' : 'var(--cream-2)',
            color: value === m ? 'var(--cream-3)' : 'var(--ink)',
          }}
        >
          {labels[m]}
        </button>
      ))}
    </div>
  );
};

const FieldLabel = ({ children }) => (
  <label className="text-sm block mb-1" style={{ color: 'var(--ink-soft)' }}>{children}</label>
);

const AddTripForm = ({ onSave, onCancel }) => {
  const [form, setForm] = useState({
    title: '', subtitle: '', location: '', date: '', intro: '',
    palette: 'warm', motif: 'mountain', emoji: '✈️', accent: '✦',
  });
  const update = (k, v) => setForm({ ...form, [k]: v });

  const handleSubmit = () => {
    if (!form.title.trim() || !form.location.trim()) return;
    onSave({
      id: newId(),
      ...form,
      featured: false,
      timeline: [],
    });
  };

  return (
    <div className="space-y-4">
      <Cover palette={form.palette} motif={form.motif} motifSize={0.5} className="rounded-lg aspect-[16/7]" />

      <div>
        <FieldLabel>العنوان</FieldLabel>
        <input className="input-field" value={form.title} onChange={(e) => update('title', e.target.value)}
               placeholder="مثلاً: ليالٍ في مَراكش" />
      </div>

      <div className="grid grid-cols-2 gap-3">
        <div>
          <FieldLabel>الوجهة</FieldLabel>
          <input className="input-field" value={form.location} onChange={(e) => update('location', e.target.value)}
                 placeholder="المدينة، البلد" />
        </div>
        <div>
          <FieldLabel>التاريخ</FieldLabel>
          <input className="input-field" value={form.date} onChange={(e) => update('date', e.target.value)}
                 placeholder="مثلاً: مايو 2026" />
        </div>
      </div>

      <div>
        <FieldLabel>الوصف</FieldLabel>
        <textarea className="input-field" rows="2" value={form.subtitle} onChange={(e) => update('subtitle', e.target.value)}
                  placeholder="سطرٌ يلخّص روح الرحلة" />
      </div>

      <div>
        <FieldLabel>المقدمة (اختياري)</FieldLabel>
        <textarea className="input-field" rows="3" value={form.intro} onChange={(e) => update('intro', e.target.value)}
                  placeholder="الفقرة الأولى من الرحلة" />
      </div>

      <div className="grid grid-cols-2 gap-3">
        <div>
          <FieldLabel>الرمز التعبيري</FieldLabel>
          <input className="input-field" value={form.emoji} onChange={(e) => update('emoji', e.target.value)} maxLength="3" />
        </div>
        <div>
          <FieldLabel>زخرفة</FieldLabel>
          <input className="input-field" value={form.accent} onChange={(e) => update('accent', e.target.value)} maxLength="2" />
        </div>
      </div>

      <div>
        <FieldLabel>لون الغلاف</FieldLabel>
        <PaletteSelect value={form.palette} onChange={(v) => update('palette', v)} />
      </div>

      <div>
        <FieldLabel>رمز الغلاف</FieldLabel>
        <MotifSelect value={form.motif} onChange={(v) => update('motif', v)} />
      </div>

      <div className="flex gap-3 pt-4">
        <button onClick={handleSubmit} className="btn-primary flex-1 py-3 rounded-full text-sm font-medium">
          حفظ الرحلة
        </button>
        <button onClick={onCancel} className="px-5 py-3 rounded-full text-sm" style={{ background: 'var(--cream-2)', color: 'var(--ink)' }}>
          إلغاء
        </button>
      </div>
    </div>
  );
};

const AddMomentForm = ({ onSave, onCancel }) => {
  const [form, setForm] = useState({
    date: '', title: '', text: '', palette: 'sand', motif: 'mountain',
  });
  const update = (k, v) => setForm({ ...form, [k]: v });

  const handleSubmit = () => {
    if (!form.title.trim()) return;
    onSave({ id: newId(), ...form });
  };

  return (
    <div className="space-y-4">
      <Cover palette={form.palette} motif={form.motif} motifSize={0.5} className="rounded-lg aspect-[16/7]" />

      <div>
        <FieldLabel>التاريخ / المرحلة</FieldLabel>
        <input className="input-field" value={form.date} onChange={(e) => update('date', e.target.value)}
               placeholder="مثلاً: اليوم الثاني · 16 مارس" />
      </div>

      <div>
        <FieldLabel>عنوان اللحظة</FieldLabel>
        <input className="input-field" value={form.title} onChange={(e) => update('title', e.target.value)}
               placeholder="مثلاً: صباحٌ في السوق القديم" />
      </div>

      <div>
        <FieldLabel>النص</FieldLabel>
        <textarea className="input-field" rows="5" value={form.text} onChange={(e) => update('text', e.target.value)}
                  placeholder="احكِ ما حدث، ما رأيت، وما شعرتَ به" />
      </div>

      <div>
        <FieldLabel>لون الغلاف</FieldLabel>
        <PaletteSelect value={form.palette} onChange={(v) => update('palette', v)} />
      </div>

      <div>
        <FieldLabel>رمز الغلاف</FieldLabel>
        <MotifSelect value={form.motif} onChange={(v) => update('motif', v)} />
      </div>

      <div className="flex gap-3 pt-4">
        <button onClick={handleSubmit} className="btn-primary flex-1 py-3 rounded-full text-sm font-medium">
          أضف اللحظة
        </button>
        <button onClick={onCancel} className="px-5 py-3 rounded-full text-sm" style={{ background: 'var(--cream-2)', color: 'var(--ink)' }}>
          إلغاء
        </button>
      </div>
    </div>
  );
};

/* =========================================================
   ROOT APP
   ========================================================= */
export default function App() {
  const [trips, setTrips] = useState([]);
  const [loading, setLoading] = useState(true);
  const [view, setView] = useState('home');
  const [currentTripId, setCurrentTripId] = useState(null);
  const [showAddTrip, setShowAddTrip] = useState(false);
  const [showAddMoment, setShowAddMoment] = useState(false);
  const [pendingMomentTripId, setPendingMomentTripId] = useState(null);
  const detailRef = useRef(null);

  useEffect(() => {
    (async () => {
      const loaded = await loadTripsFromStorage();
      setTrips(loaded);
      setLoading(false);
    })();
  }, []);

  const persist = async (newTrips) => {
    setTrips(newTrips);
    await saveTripsToStorage(newTrips);
  };

  const openTrip = (trip) => {
    setCurrentTripId(trip.id);
    setView('detail');
    window.scrollTo({ top: 0, behavior: 'smooth' });
  };

  const goHome = () => {
    setView('home');
    setCurrentTripId(null);
    window.scrollTo({ top: 0, behavior: 'smooth' });
  };

  const handleAddTrip = async (newTrip) => {
    const updated = [newTrip, ...trips];
    await persist(updated);
    setShowAddTrip(false);
    openTrip(newTrip);
  };

  const handleAddMoment = async (newMoment) => {
    const updated = trips.map((t) =>
      t.id === pendingMomentTripId ? { ...t, timeline: [...t.timeline, newMoment] } : t
    );
    await persist(updated);
    setShowAddMoment(false);
    setPendingMomentTripId(null);
  };

  const handleDeleteTrip = async (tripId) => {
    const updated = trips.filter((t) => t.id !== tripId);
    await persist(updated);
    goHome();
  };

  const handleDeleteMoment = async (tripId, momentId) => {
    const updated = trips.map((t) =>
      t.id === tripId ? { ...t, timeline: t.timeline.filter((m) => m.id !== momentId) } : t
    );
    await persist(updated);
  };

  if (loading) {
    return (
      <div dir="rtl" style={{ background: 'var(--cream)', minHeight: '100vh' }} className="flex items-center justify-center">
        <Styles />
        <Loader2 className="w-6 h-6 animate-spin" style={{ color: 'var(--terracotta)' }} />
      </div>
    );
  }

  const featured = trips.find((t) => t.featured) || trips[0];
  const rest = trips.filter((t) => t.id !== featured?.id);
  const currentTrip = trips.find((t) => t.id === currentTripId);

  return (
    <div dir="rtl" lang="ar" style={{ background: 'var(--cream)', minHeight: '100vh' }}>
      <Styles />

      <TopNav onGoHome={goHome} currentView={view} />

      {view === 'home' && (
        <main>
          {featured && <FeaturedHero trip={featured} onOpen={openTrip} />}
          <TripsGrid trips={rest} onOpen={openTrip} onAdd={() => setShowAddTrip(true)} />
        </main>
      )}

      {view === 'detail' && currentTrip && (
        <main ref={detailRef}>
          <TripDetail
            trip={currentTrip}
            onBack={goHome}
            onAddMoment={(id) => { setPendingMomentTripId(id); setShowAddMoment(true); }}
            onDeleteTrip={handleDeleteTrip}
            onDeleteMoment={handleDeleteMoment}
          />
        </main>
      )}

      <Footer />

      <Modal open={showAddTrip} onClose={() => setShowAddTrip(false)} title="رحلة جديدة">
        <AddTripForm onSave={handleAddTrip} onCancel={() => setShowAddTrip(false)} />
      </Modal>

      <Modal open={showAddMoment} onClose={() => setShowAddMoment(false)} title="لحظة جديدة">
        <AddMomentForm onSave={handleAddMoment} onCancel={() => setShowAddMoment(false)} />
      </Modal>
    </div>
  );
}
