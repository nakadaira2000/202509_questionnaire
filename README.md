# 202509_questionnaire
202509～店舗アンケート
<!doctype html>
<html lang="ja">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Store Survey</title>
<style>
  body{font-family:system-ui,-apple-system,"Hiragino Kaku Gothic ProN",Meiryo,sans-serif;margin:0;background:#fafafa;}
  .wrap{max-width:720px;margin:24px auto;padding:16px;background:#fff;border-radius:12px;box-shadow:0 2px 8px rgba(0,0,0,.06)}
  h1{font-size:20px;margin:0 0 12px}
  label{display:block;margin:12px 0 6px}
  select,input[type="text"],textarea,input[type="number"],input[type="range"]{width:100%;padding:10px;border:1px solid #ddd;border-radius:8px;box-sizing:border-box}
  .row{display:grid;grid-template-columns:1fr 1fr;gap:12px}
  .chip{display:inline-block;margin:4px 8px 4px 0}
  .chip input{margin-right:6px}
  .btn{margin-top:16px;padding:12px 16px;border:0;border-radius:8px;background:#222;color:#fff;cursor:pointer}
  .note{color:#666;font-size:12px;margin-top:8px}
  .hidden{display:none}
</style>
</head>
<body>
<div class="wrap">
  <h1>店舗アンケート</h1>
  <p class="note">所要時間1〜2分。ご協力ありがとうございます。</p>

  <form id="f">
    <!-- 固定情報（自動入力） -->
    <input type="hidden" name="store" id="store" value="" />

    <label>言語 / Language</label>
    <select name="language" id="language" required>
      <option value="日本語">日本語</option>
      <option value="English">English</option>
      <option value="中文">中文</option>
      <option value="한국어">한국어</option>
    </select>

    <label>お住まいはどちらですか？</label>
    <select name="country" id="country" required>
      <option value="">選択してください</option>
      <option>日本</option>
      <option>アメリカ</option>
      <option>中国</option>
      <option>台湾</option>
      <option>香港</option>
      <option>韓国</option>
      <option>シンガポール</option>
      <option>その他</option>
    </select>

    <div id="prefWrap" class="hidden">
      <label>都道府県をお選びください（日本の方）</label>
      <select name="prefecture" id="prefecture">
        <option value="">選択してください</option>
        <option>北海道</option><option>青森県</option><option>岩手県</option><option>宮城県</option><option>秋田県</option><option>山形県</option><option>福島県</option>
        <option>茨城県</option><option>栃木県</option><option>群馬県</option><option>埼玉県</option><option>千葉県</option><option>東京都</option><option>神奈川県</option>
        <option>新潟県</option><option>富山県</option><option>石川県</option><option>福井県</option><option>山梨県</option><option>長野県</option>
        <option>岐阜県</option><option>静岡県</option><option>愛知県</option><option>三重県</option>
        <option>滋賀県</option><option>京都府</option><option>大阪府</option><option>兵庫県</option><option>奈良県</option><option>和歌山県</option>
        <option>鳥取県</option><option>島根県</option><option>岡山県</option><option>広島県</option><option>山口県</option>
        <option>徳島県</option><option>香川県</option><option>愛媛県</option><option>高知県</option>
        <option>福岡県</option><option>佐賀県</option><option>長崎県</option><option>熊本県</option><option>大分県</option><option>宮崎県</option><option>鹿児島県</option><option>沖縄県</option>
      </select>
    </div>

    <div class="row">
      <div>
        <label>何人でご来店されましたか？</label>
        <select name="party_size" required>
          <option value="">選択</option>
          <option>1</option><option>2</option><option>3</option><option>4</option><option>5</option>
          <option>6</option><option>7</option><option>8</option><option>9</option><option>10名以上</option>
        </select>
      </div>
      <div>
        <label>誰と来られましたか？</label>
        <select name="companion" required>
          <option value="">選択</option>
          <option>家族</option><option>友人</option><option>カップル</option><option>ビジネス</option><option>1人</option>
        </select>
      </div>
    </div>

    <label>当店を最初に知ったきっかけ（複数選択可）</label>
    <div>
      <!-- SNS -->
      <div class="chip"><label><input type="checkbox" name="discovery" value="[SNS] Instagram">Instagram</label></div>
      <div class="chip"><label><input type="checkbox" name="discovery" value="[SNS] X">X</label></div>
      <div class="chip"><label><input type="checkbox" name="discovery" value="[SNS] RED">RED</label></div>
      <div class="chip"><label><input type="checkbox" name="discovery" value="[SNS] Facebook">Facebook</label></div>
      <div class="chip"><label><input type="checkbox" name="discovery" value="[SNS] TikTok">TikTok</label></div>
      <div class="chip"><label><input type="checkbox" name="discovery" value="[SNS] YouTube">YouTube</label></div>
      <!-- メディア -->
      <div class="chip"><label><input type="checkbox" name="discovery" value="[メディア] テレビ">テレビ</label></div>
      <div class="chip"><label><input type="checkbox" name="discovery" value="[メディア] 雑誌">雑誌</label></div>
      <div class="chip"><label><input type="checkbox" name="discovery" value="[メディア] ラジオ">ラジオ</label></div>
      <div class="chip"><label><input type="checkbox" name="discovery" value="[メディア] Webニュース記事">Webニュース記事</label></div>
      <div class="chip"><label><input type="checkbox" name="discovery" value="[メディア] ブログ">ブログ</label></div>
      <div class="chip"><label><input type="checkbox" name="discovery" value="[メディア] ガイドブック">ガイドブック</label></div>
      <div class="chip"><label><input type="checkbox" name="discovery" value="[メディア] トラベルマガジン">トラベルマガジン</label></div>
      <!-- その他 -->
      <div class="chip"><label><input type="checkbox" name="discovery" value="[紹介] 知人の紹介">知人の紹介</label></div>
      <div class="chip"><label><input type="checkbox" name="discovery" value="[紹介] コンシェルジュの紹介">コンシェルジュの紹介</label></div>
      <div class="chip"><label><input type="checkbox" name="discovery" value="[その他] 通りがかり">通りがかり</label></div>
    </div>

    <label>来店検討時に参考にした情報源（複数選択可）</label>
    <div>
      <!-- SNS -->
      <div class="chip"><label><input type="checkbox" name="consideration" value="[SNS] Instagram">Instagram</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[SNS] X">X</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[SNS] RED">RED</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[SNS] Facebook">Facebook</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[SNS] TikTok">TikTok</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[SNS] YouTube">YouTube</label></div>
      <!-- グルメサイト -->
      <div class="chip"><label><input type="checkbox" name="consideration" value="[グルメサイト] 食べログ">食べログ</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[グルメサイト] TripAdvisor">TripAdvisor</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[グルメサイト] OpenTable">OpenTable</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[グルメサイト] ぐるなび">ぐるなび</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[グルメサイト] 一休.com">一休.com</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[グルメサイト] オズモール">オズモール</label></div>
      <!-- 検索 -->
      <div class="chip"><label><input type="checkbox" name="consideration" value="[検索] Google">Google</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[検索] Yahoo!">Yahoo!</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[検索] Bing">Bing</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[検索] GoogleMap">GoogleMap</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[検索] 公式HP">公式HP</label></div>
      <!-- メディア -->
      <div class="chip"><label><input type="checkbox" name="consideration" value="[メディア] テレビ">テレビ</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[メディア] 雑誌">雑誌</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[メディア] ラジオ">ラジオ</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[メディア] Webニュース記事">Webニュース記事</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[メディア] ブログ">ブログ</label></div>
      <!-- その他 -->
      <div class="chip"><label><input type="checkbox" name="consideration" value="[紹介] 知人の紹介">知人の紹介</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[紹介] コンシェルジュの紹介">コンシェルジュの紹介</label></div>
      <div class="chip"><label><input type="checkbox" name="consideration" value="[その他] 通りがかり">通りがかり</label></div>
    </div>

    <label>来店動機（複数選択可）</label>
    <div>
      <div class="chip"><label><input type="checkbox" name="motivation" value="店の雰囲気">店の雰囲気</label></div>
      <div class="chip"><label><input type="checkbox" name="motivation" value="有名店だから">有名店だから</label></div>
      <div class="chip"><label><input type="checkbox" name="motivation" value="口コミ評価">口コミ評価</label></div>
      <div class="chip"><label><input type="checkbox" name="motivation" value="特定のメニューを目当てに">特定のメニューを目当てに</label></div>
      <div class="chip"><label><input type="checkbox" name="motivation" value="立地">立地</label></div>
      <div class="chip"><label><input type="checkbox" name="motivation" value="言語対応が充実しているから">言語対応が充実しているから</label></div>
      <div class="chip"><label><input type="checkbox" name="motivation" value="価格（コスパ）">価格（コスパ）</label></div>
      <div class="chip"><label><input type="checkbox" name="motivation" value="以前に来たことがあって良かったから">以前に来たことがあって良かったから</label></div>
      <div class="chip"><label><input type="checkbox" name="motivation" value="系列店を利用していて当店も気になったから">系列店を利用していて当店も気になったから</label></div>
    </div>

    <label>当店を友人や家族におすすめしたいですか？（0〜10）</label>
    <input type="range" name="nps" min="0" max="10" value="8" oninput="npsOut.textContent=this.value">
    <div>現在の回答：<span id="npsOut">8</span></div>

    <label>ご意見・ご感想</label>
    <textarea name="comments" rows="4" placeholder="自由記述（任意）"></textarea>

    <button type="submit" class="btn">送信する</button>
    <div id="done" class="note hidden">送信ありがとうございました！</div>
  </form>
</div>

<script>
  // ▼ ここにGASのWebアプリURLを貼り付け
  const GAS_URL = "＜ここに貼る＞";

  // 店舗名をURL ?store=XXX から受け取り
  const params = new URLSearchParams(location.search);
  const store = params.get('store') || '';
  document.getElementById('store').value = store;

  // 日本を選んだら都道府県を表示
  const countrySel = document.getElementById('country');
  const prefWrap   = document.getElementById('prefWrap');
  countrySel.addEventListener('change', () => {
    prefWrap.classList.toggle('hidden', countrySel.value !== '日本');
  });

  // 送信
  const form = document.getElementById('f');
  form.addEventListener('submit', async (e) => {
    e.preventDefault();
    const fd = new FormData(form);
    // タイムスタンプとストア（念のため）
    fd.append('timestamp', new Date().toISOString());
    if (store) fd.append('store', store);

    try {
      // FormData送信（CORSプリフライト回避しやすい）
      const res = await fetch(GAS_URL, { method: 'POST', body: fd });
      // レスポンスは使わずOK（権限設定によってCORS制限が見える場合があるため）
      form.reset();
      document.getElementById('npsOut').textContent = '8';
      prefWrap.classList.add('hidden');
      document.getElementById('done').classList.remove('hidden');
    } catch (err) {
      alert('送信に失敗しました。ネットワークをご確認ください。');
    }
  });
</script>
</body>
</html>
