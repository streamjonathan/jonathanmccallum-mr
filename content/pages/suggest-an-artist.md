---
title: "एखाद्या कलाकाराची शिफारस करा"
slug: suggest-an-artist
---

यीशूचे अनुसरण करणाऱ्या संगीतकारांबद्दल आणि कलाकारांबद्दल ऐकायला मला खूप आवडतं. मी ज्यांच्याबद्दल लिहावं, ज्यांची मुलाखत घ्यावी किंवा ज्यांच्याबद्दल प्रतिक्रिया व्हिडिओ करावा असं तुम्हाला वाटतं अशी एखादी व्यक्ती तुम्हाला माहीत असेल, तर इथे मला सांगा.

एक नाव आणि एक दुवा पुरेसा आहे — आणि का ती व्यक्ती, हे काही शब्दांत सांगा. येणारं सगळं मी वाचतो. खूप खूप धन्यवाद.

तुम्हाला कुणी माहीत आहे का? त्यांच्या फोटोला स्पर्श करा, फॉर्म आपोआप भरेल — मग का ती व्यक्ती हे काही शब्दांत जोडा आणि पाठवा.

<div class="suggest-carousel" role="list" aria-label="तुम्ही शिफारस करू शकता असे संगीतकार आणि कलाकार">
{% for artist in suggest_carousel %}
  <button type="button" class="suggest-pick" role="listitem" data-artist="{{ artist.name }}" data-link="{{ artist.profile }}" title="{{ artist.name }} यांची शिफारस करा">
    <img src="{{ artist.img }}" alt="{{ artist.name }}" loading="lazy" width="150" height="150">
    <span class="suggest-pick__name">{{ artist.name }}</span>
    <span class="suggest-pick__note">{{ artist.note }}</span>
  </button>
{% endfor %}
</div>

<p class="suggest-carousel__more">किंवा खाली नवीन व्यक्तीची शिफारस करा — मला ज्यांच्याबद्दल ऐकायला हवं असं तुम्हाला वाटतं ती कोणतीही व्यक्ती.</p>

ही साइट १८ वर्षांखालील व्यक्तींसाठी नाही.

<form id="suggest-form" class="suggest-form">
  <label for="suggest-artist">कलाकाराचं नाव</label>
  <input id="suggest-artist" name="artist" type="text" maxlength="200" placeholder="मी कुणाकडे पाहावं?" required>

  <label for="suggest-link">सोशल मीडिया प्रोफाइलचा दुवा</label>
  <input id="suggest-link" name="link" type="url" maxlength="500" placeholder="https://www.instagram.com/…" required>

  <fieldset class="suggest-kinds">
    <legend>मी त्यांच्यासोबत काय करू?</legend>
    <label><input type="checkbox" name="kind" value="write"> त्यांच्याबद्दल लिहा</label>
    <label><input type="checkbox" name="kind" value="interview"> त्यांची मुलाखत घ्या</label>
    <label><input type="checkbox" name="kind" value="reaction"> त्यांच्याबद्दल प्रतिक्रिया व्हिडिओ करा</label>
  </fieldset>

  <label for="suggest-why">का ती व्यक्ती?</label>
  <textarea id="suggest-why" name="why" rows="3" maxlength="500" placeholder="काही शब्द पुरेसे आहेत…"></textarea>

  <label for="suggest-name">तुमचं नाव <span class="optional">(ऐच्छिक)</span></label>
  <input id="suggest-name" name="fromName" type="text" maxlength="100" placeholder="जेणेकरून मी आभार मानू शकेन">

  <label for="suggest-from-link">तुमच्या सोशल मीडिया प्रोफाइलचा दुवा <span class="optional">(ऐच्छिक)</span></label>
  <input id="suggest-from-link" name="fromLink" type="url" maxlength="500" placeholder="https://www.instagram.com/…">

  <button id="suggest-button" type="button">शिफारस पाठवा</button>

  <p id="suggest-result" aria-live="polite"></p>
</form>
