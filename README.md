<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>اختبار الإنجليزية للأطفال</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #a8dadc, #457b9d); /* تدرج أزرق مريح وجذاب */
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            color: #333;
            overflow: auto; /* للسماح بالتمرير إذا كان المحتوى كبيرًا */
        }

        .quiz-container {
            background-color: #ffffff;
            padding: 35px;
            border-radius: 15px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.25); /* ظل أوضح وأكثر بروزًا */
            width: 95%;
            max-width: 680px; /* عرض أكبر قليلاً */
            text-align: center;
            direction: rtl;
            animation: fadeIn 1s ease-out; /* تأثير ظهور ناعم */
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        h1, h2 {
            color: #1d3557; /* لون أزرق داكن جذاب */
            margin-bottom: 25px;
            font-size: 2.2em; /* حجم أكبر للعناوين */
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1); /* ظل خفيف للنص */
        }

        p {
            font-size: 1.15em; /* خط أكبر قليلاً */
            line-height: 1.7;
            color: #333;
        }

        input[type="text"] {
            width: calc(100% - 22px);
            padding: 14px; /* حشوة أكبر */
            margin-bottom: 25px;
            border: 2px solid #457b9d; /* حدود أكثر وضوحًا */
            border-radius: 10px; /* زوايا دائرية أكثر */
            font-size: 1.2em; /* حجم خط أكبر */
            text-align: right;
            box-sizing: border-box;
            outline: none; /* إزالة الإطار الأزرق عند التركيز */
            transition: border-color 0.3s ease;
        }

        input[type="text"]:focus {
            border-color: #e63946; /* لون حدود عند التركيز */
        }

        button {
            background-color: #e63946; /* لون أحمر زاهي */
            color: white;
            padding: 15px 35px; /* حشوة أكبر */
            border: none;
            border-radius: 10px; /* زوايا دائرية أكثر */
            cursor: pointer;
            font-size: 1.25em; /* حجم أكبر للأزرار */
            font-weight: bold;
            transition: background-color 0.3s ease, transform 0.2s ease;
            margin-top: 15px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2); /* ظل للأزرار */
        }

        button:hover {
            background-color: #c92a3a; /* أحمر أغمق عند التمرير */
            transform: translateY(-4px); /* تأثير رفع أوضح */
        }

        .options-container {
            display: flex;
            flex-direction: column;
            gap: 15px; /* مسافات أكبر بين الخيارات */
            margin-top: 30px;
        }

        .option-btn {
            background-color: #f1faee; /* لون خلفية للخيارات (أبيض مصفر) */
            color: #1d3557;
            padding: 15px 25px; /* حشوة أكبر */
            border: 2px solid #a8dadc;
            border-radius: 10px;
            cursor: pointer;
            font-size: 1.15em;
            transition: background-color 0.2s ease, transform 0.1s ease, border-color 0.2s ease;
            text-align: right;
            font-weight: 500;
        }

        .option-btn:hover {
            background-color: #e0f2f7;
            transform: translateY(-2px);
            border-color: #457b9d;
        }

        .option-btn.selected {
            border: 3px solid #1d3557; /* حدود أسمك عند الاختيار */
            background-color: #cce5ff; /* أزرق فاتح جداً */
            color: #1d3557;
        }

        .option-btn.correct {
            background-color: #d4edda; /* أخضر فاتح */
            border-color: #28a745; /* أخضر داكن */
            color: #155724;
            font-weight: bold;
            animation: bounceIn 0.5s; /* تأثير ارتداد عند الإجابة الصحيحة */
        }

        .option-btn.incorrect {
            background-color: #f8d7da; /* أحمر فاتح */
            border-color: #dc3545; /* أحمر داكن */
            color: #721c24;
            font-weight: bold;
            animation: shake 0.5s; /* تأثير اهتزاز عند الإجابة الخاطئة */
        }

        /* Animations for feedback */
        @keyframes bounceIn {
            0%, 20%, 40%, 60%, 80%, 100% {
                -webkit-animation-timing-function: cubic-bezier(0.215, 0.610, 0.355, 1.000);
                animation-timing-function: cubic-bezier(0.215, 0.610, 0.355, 1.000);
            }
            0% { opacity: 0; transform: scale3d(0.3, 0.3, 0.3); }
            20% { transform: scale3d(1.1, 1.1, 1.1); }
            40% { transform: scale3d(0.9, 0.9, 0.9); }
            60% { opacity: 1; transform: scale3d(1.03, 1.03, 1.03); }
            80% { transform: scale3d(0.97, 0.97, 0.97); }
            100% { opacity: 1; transform: scale3d(1, 1, 1); }
        }

        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            10%, 30%, 50%, 70%, 90% { transform: translateX(-10px); }
            20%, 40%, 60%, 80% { transform: translateX(10px); }
        }


        #feedback {
            margin-top: 25px;
            font-weight: bold;
            font-size: 1.3em; /* حجم أكبر للملاحظات */
            color: #dc3545; /* لون أحمر افتراضي للخطأ */
            animation: fadeIn 0.8s ease-out;
        }
        #feedback.correct-feedback {
            color: #28a745; /* لون أخضر للصحيح */
        }

        .share-buttons {
            margin-top: 35px;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 18px; /* مسافات أكبر بين الأزرار */
        }

        .share-btn {
            text-decoration: none;
            padding: 13px 25px;
            border-radius: 10px;
            font-size: 1.15em;
            font-weight: bold;
            transition: background-color 0.3s ease, transform 0.2s ease;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            box-shadow: 0 3px 6px rgba(0,0,0,0.15);
        }

        .whatsapp-btn {
            background-color: #25D366;
            color: white;
        }

        .whatsapp-btn:hover {
            background-color: #1DA851;
            transform: translateY(-3px);
        }

        .arabic-meaning-hint {
            font-size: 1em;
            color: #555;
            margin-top: 15px;
            font-style: italic; /* خط مائل لتوضيح أنها معلومة إضافية */
        }
        #question-text {
            font-size: 1.6em; /* حجم أكبر للسؤال */
            margin-bottom: 10px;
            color: #1d3557;
            direction: ltr; /* اتجاه النص من اليسار لليمين للأسئلة الإنجليزية */
            text-align: left; /* محاذاة لليسار للأسئلة الإنجليزية */
        }
        #question-counter {
            font-size: 1.1em;
            color: #607d8b;
            margin-bottom: 5px;
        }

        #answer-summary {
            margin-top: 40px;
            text-align: right;
            border-top: 2px solid #a8dadc;
            padding-top: 20px;
        }

        #answer-summary h3 {
            color: #1d3557;
            font-size: 1.8em;
            margin-bottom: 20px;
        }

        .summary-item {
            background-color: #f1faee;
            border: 1px solid #a8dadc;
            border-radius: 10px;
            padding: 15px;
            margin-bottom: 15px;
            text-align: right;
            line-height: 1.8;
            box-shadow: 0 2px 4px rgba(0,0,0,0.08);
        }

        .summary-item p {
            margin: 5px 0;
            font-size: 1.05em;
        }

        .summary-question-text {
            font-weight: bold;
            color: #1d3557;
            direction: ltr; /* اتجاه لليسار للسؤال الإنجليزي في الملخص */
            text-align: left; /* محاذاة لليسار للسؤال الإنجليزي في الملخص */
        }

        .summary-user-answer {
            color: #e63946; /* أحمر للإجابات المختارة */
            font-weight: bold;
        }

        .summary-correct-answer {
            color: #28a745; /* أخضر للإجابات الصحيحة */
            font-weight: bold;
        }

        .summary-result.correct {
            color: #28a745;
            font-weight: bold;
        }

        .summary-result.incorrect {
            color: #dc3545;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="quiz-container">
        <h1>اختبار الإنجليزية للأطفال</h1>

        <div id="welcome-screen">
            <p>أهلاً بك في اختبار اللغة الإنجليزية! هيا نختبر معلوماتك.</p>
            <input type="text" id="student-name" placeholder="أدخل اسمك" required>
            <button id="start-quiz-btn">ابدأ الاختبار</button>
        </div>

        <div id="quiz-screen" style="display: none;">
            <p id="question-counter"></p>
            <h2 id="question-text"></h2>
            <p class="arabic-meaning-hint">معنى المفهوم الرئيسي: <span id="arabic-meaning-question"></span></p>
            <div id="options-container" class="options-container">
                </div>
            <p id="feedback"></p>
            <button id="next-question-btn" style="display: none;">السؤال التالي</button>
        </div>

        <div id="result-screen" style="display: none;">
            <h2>الاختبار انتهى!</h2>
            <p>اسم الطالب/ة: <span id="final-student-name"></span></p>
            <p>أجبت بشكل صحيح على <span id="correct-answers-count"></span> من <span id="total-questions-count"></span> سؤال.</p>
            <p>درجتك النهائية: <span id="final-score"></span> من 100.</p>

            <div id="answer-summary">
                <h3>ملخص الإجابات:</h3>
                </div>

            <div class="share-buttons">
                <a id="whatsapp-share-1" href="#" target="_blank" class="share-btn whatsapp-btn">شارك النتيجة (واتساب 1)</a>
                <a id="whatsapp-share-2" href="#" target="_blank" class="share-btn whatsapp-btn">شارك النتيجة (واتساب 2)</a>
            </div>
            <button id="restart-quiz-btn">ابدأ الاختبار من جديد</button>
        </div>
    </div>

    <script>
        // --- JavaScript Logic ---
        document.addEventListener('DOMContentLoaded', () => {
            const welcomeScreen = document.getElementById('welcome-screen');
            const quizScreen = document.getElementById('quiz-screen');
            const resultScreen = document.getElementById('result-screen');

            const studentNameInput = document.getElementById('student-name');
            const startQuizBtn = document.getElementById('start-quiz-btn');
            const questionCounter = document.getElementById('question-counter');
            const questionText = document.getElementById('question-text');
            const arabicMeaningQuestionSpan = document.getElementById('arabic-meaning-question');
            const optionsContainer = document.getElementById('options-container');
            const feedback = document.getElementById('feedback');
            const nextQuestionBtn = document.getElementById('next-question-btn');

            const finalStudentName = document.getElementById('final-student-name');
            const correctAnswersCountSpan = document.getElementById('correct-answers-count');
            const totalQuestionsCountSpan = document.getElementById('total-questions-count');
            const finalScoreSpan = document.getElementById('final-score');
            const whatsappShare1 = document.getElementById('whatsapp-share-1');
            const whatsappShare2 = document.getElementById('whatsapp-share-2');
            const restartQuizBtn = document.getElementById('restart-quiz-btn');
            const answerSummaryDiv = document.getElementById('answer-summary');

            let studentName = '';
            let currentQuestionIndex = 0;
            let score = 0;
            const totalQuestions = 50; // إجمالي عدد الأسئلة
            let quizResults = []; // لتخزين نتائج كل سؤال

            // --- بيانات الأسئلة باللغة الإنجليزية مع تنوع أكبر في الصياغة والخيارات ---
            // تم تعديل الخيارات لتكون مختلفة في الحروف الأولى لزيادة التحدي
            const verbToBeQuestions = [
                { q: "Choose the correct form of 'to be': I ____ happy.", options: ["am", "runs", "is"], correct: "am", qWordMeaning: "فعل يكون" },
                { q: "Fill in the blank: She ____ smart.", options: ["is", "jump", "are"], correct: "is", qWordMeaning: "فعل يكون" },
                { q: "Which verb is correct for 'They': They ____ playing.", options: ["are", "eats", "is"], correct: "are", qWordMeaning: "فعل يكون" },
                { q: "He ____ a good student. Select the correct verb.", options: ["is", "go", "are"], correct: "is", qWordMeaning: "فعل يكون" },
                { q: "We ____ close friends.", options: ["are", "sleep", "am"], correct: "are", qWordMeaning: "فعل يكون" },
                { q: "It ____ a cute cat. (for non-human)", options: ["is", "fly", "walk"], correct: "is", qWordMeaning: "فعل يكون" },
                { q: "You ____ a great teacher.", options: ["are", "sing", "is"], correct: "are", qWordMeaning: "فعل يكون" },
                { q: "The water ____ very cold.", options: ["is", "drink", "are"], correct: "is", qWordMeaning: "فعل يكون" },
                { q: "My parents ____ in the garden.", options: ["are", "read", "am"], correct: "are", qWordMeaning: "فعل يكون" },
                { q: "Choose the correct conjugation: I ____ tired today.", options: ["am", "drive", "is"], correct: "am", qWordMeaning: "فعل يكون" },
            ];

            const verbToDoQuestions = [
                { q: "Choose the correct form of 'to do': I ____ my homework every day.", options: ["do", "sings", "play"], correct: "do", qWordMeaning: "فعل يفعل" },
                { q: "She ____ not like chocolate.", options: ["does", "run", "jump"], correct: "does", qWordMeaning: "فعل يفعل" },
                { q: "Which verb is correct for 'They': They ____ not speak English.", options: ["do", "writes", "reads"], correct: "do", qWordMeaning: "فعل يفعل" },
                { q: "He ____ his work diligently.", options: ["does", "sleep", "walk"], correct: "does", qWordMeaning: "فعل يفعل" },
                { q: "We ____ our best.", options: ["do", "eats", "dances"], correct: "do", qWordMeaning: "فعل يفعل" },
                { q: "It ____ not make a difference.", options: ["does", "fly", "swim"], correct: "does", qWordMeaning: "فعل يفعل" },
                { q: "You ____ a good job.", options: ["do", "sit", "stand"], correct: "do", qWordMeaning: "فعل يفعل" },
                { q: "My brother ____ his school chores.", options: ["does", "talk", "listen"], correct: "does", qWordMeaning: "فعل يفعل" },
                { q: "____ you speak Arabic?", options: ["do", "sees", "hears"], correct: "do", qWordMeaning: "فعل يفعل" },
                { q: "What ____ she doing now?", options: ["does", "come", "go"], correct: "does", qWordMeaning: "فعل يفعل" },
            ];

            const verbToHaveQuestions = [
                { q: "Choose the correct form of 'to have': I ____ a blue pen.", options: ["have", "eat", "has"], correct: "have", qWordMeaning: "فعل يملك" },
                { q: "She ____ long hair.", options: ["has", "run", "have"], correct: "has", qWordMeaning: "فعل يملك" },
                { q: "Which verb is correct for 'They': They ____ many books.", options: ["have", "sings", "has"], correct: "have", qWordMeaning: "فعل يملك" },
                { q: "He ____ a new bicycle.", options: ["has", "play", "have"], correct: "has", qWordMeaning: "فعل يملك" },
                { q: "We ____ a pet.", options: ["have", "sleeps", "has"], correct: "have", qWordMeaning: "فعل يملك" },
                { q: "This house ____ a large garden.", options: ["has", "read", "have"], correct: "has", qWordMeaning: "فعل يملك" },
                { q: "____ you any questions?", options: ["have", "jumps", "has"], correct: "have", qWordMeaning: "فعل يملك" },
                { q: "My daughter ____ brown eyes.", options: ["has", "writes", "have"], correct: "has", qWordMeaning: "فعل يملك" },
                { q: "Birds ____ wings to fly.", options: ["have", "flies", "has"], correct: "have", qWordMeaning: "فعل يملك" },
                { q: "Choose the correct conjugation: I ____ a great idea!", options: ["have", "swims", "has"], correct: "have", qWordMeaning: "فعل يملك" },
            ];

            const heItIsQuestions = [
                { q: "Fill in the blank: ____ is my best friend.", options: ["He", "She", "It"], correct: "He", qWordMeaning: "هو (للمذكر العاقل)" },
                { q: "Fill in the blank: ____ is a small cat.", options: ["It", "He", "She"], correct: "It", qWordMeaning: "هو/هي (لغير العاقل)" },
                { q: "Fill in the blank: ____ is my doctor.", options: ["She", "He", "It"], correct: "She", qWordMeaning: "هي (للمؤنث العاقل)" },
                { q: "Fill in the blank: ____ is a very tall building.", options: ["It", "He", "She"], correct: "It", qWordMeaning: "هو/هي (لغير العاقل)" },
                { q: "Fill in the blank: ____ is my older brother.", options: ["He", "She", "It"], correct: "He", qWordMeaning: "هو (للمذكر العاقل)" },
                { q: "Fill in the blank: ____ is my new car.", options: ["It", "He", "She"], correct: "It", qWordMeaning: "هو/هي (لغير العاقل)" },
                { q: "Fill in the blank: ____ is a talented artist.", options: ["He", "She", "It"], correct: "He", qWordMeaning: "هو (للمذكر العاقل)" },
            ];

            const vocabularyQuestions = [
                { q: "Which word means 'a round red fruit'?", options: ["Apple", "Book", "Chair"], correct: "Apple", qWordMeaning: "تفاحة" },
                { q: "Choose the word that means 'something you read'.", options: ["Book", "Ball", "Dog"], correct: "Book", qWordMeaning: "كتاب" },
                { q: "Which word means 'a four-wheeled vehicle for transport'?", options: ["Car", "Cat", "Fish"], correct: "Car", qWordMeaning: "سيارة" },
                { q: "Choose the word that means 'a barking pet animal'.", options: ["Dog", "Bird", "Tree"], correct: "Dog", qWordMeaning: "كلب" },
                { q: "Which word means 'a round thing you eat for breakfast'?", options: ["Egg", "Eye", "Ear"], correct: "Egg", qWordMeaning: "بيضة" },
                { q: "Choose the word that means 'an animal that lives in water and swims'.", options: ["Fish", "Frog", "Hand"], correct: "Fish", qWordMeaning: "سمكة" },
                { q: "Which word means 'a young female human'?", options: ["Girl", "Glass", "Goat"], correct: "Girl", qWordMeaning: "فتاة" },
                { q: "Choose the word that means 'a place where we live'.", options: ["House", "Hat", "Moon"], correct: "House", qWordMeaning: "منزل" },
                { q: "Which word means 'a cold dessert eaten in summer'?", options: ["Ice Cream", "Ink", "Island"], correct: "Ice Cream", qWordMeaning: "آيس كريم" },
                { q: "Choose the word that means 'a drink made from fruit'.", options: ["Juice", "Jacket", "Jam"], correct: "Juice", qWordMeaning: "عصير" },
                { q: "Which word means 'a toy that flies in the sky with a string'?", options: ["Kite", "Key", "King"], correct: "Kite", qWordMeaning: "طائرة ورقية" },
                { q: "Choose the word that means 'a wild animal that lives in the jungle'.", options: ["Lion", "Lamp", "Leaf"], correct: "Lion", qWordMeaning: "أسد" },
                { q: "Which word means 'an animal with a long tail that loves bananas'?", options: ["Monkey", "Moon", "Milk"], correct: "Monkey", qWordMeaning: "قرد" },
                { q: "Choose the word that means 'a part of your face you use to smell'.", options: ["Nose", "Net", "Nest"], correct: "Nose", qWordMeaning: "أنف" },
                { q: "Which word means 'an orange-colored fruit'?", options: ["Orange", "Owl", "Onion"], correct: "Orange", qWordMeaning: "برتقالة" },
                { q: "Choose the word that means 'a tool for writing and drawing'.", options: ["Pencil", "Pen", "Pig"], correct: "Pencil", qWordMeaning: "قلم رصاص" },
                { q: "Which word means 'the wife of a king'?", options: ["Queen", "Quilt", "Quiet"], correct: "Queen", qWordMeaning: "ملكة" },
                { q: "Choose the word that means 'a pet animal with long ears'.", options: ["Rabbit", "Rain", "Robot"], correct: "Rabbit", qWordMeaning: "أرنب" },
                { q: "Which word means 'a bright star in the daytime'?", options: ["Sun", "Star", "Shoe"], correct: "Sun", qWordMeaning: "شمس" },
                { q: "Choose the word that means 'a tall woody plant with leaves'.", options: ["Tree", "Table", "Tiger"], correct: "Tree", qWordMeaning: "شجرة" },
                { q: "Which word means 'a tool that protects you from rain'?", options: ["Umbrella", "Uniform", "Up"], correct: "Umbrella", qWordMeaning: "مظلة" },
                { q: "Choose the word that means 'a small vehicle for transporting goods'.", options: ["Van", "Violin", "Vase"], correct: "Van", qWordMeaning: "شاحنة صغيرة" },
                { q: "Which word means 'a device to tell time worn on your wrist'?", options: ["Watch", "Water", "Window"], correct: "Watch", qWordMeaning: "ساعة يد" },
                { q: "Choose the word that means 'an internal body image of bones'.", options: ["X-ray", "Xylophone", "Fox"], correct: "X-ray", qWordMeaning: "أشعة سينية" },
                { q: "Which word means 'the color of a ripe banana'?", options: ["Yellow", "Yogurt", "Yawn"], correct: "Yellow", qWordMeaning: "أصفر" },
                { q: "Choose the word that means 'a striped black and white animal similar to a horse'.", options: ["Zebra", "Zoo", "Zip"], correct: "Zebra", qWordMeaning: "حمار وحشي" },
            ];

            // قاموس أوسع للمعاني العربية للخيارات
            const arabicMeaningMap = {
                "am": "أكون", "is": "يكون", "are": "يكونون", "runs": "يجري", "jump": "يقفز", "eats": "يأكل", "go": "يذهب", "sleep": "ينام", "fly": "يطير", "walk": "يمشي", "sing": "يغني", "drink": "يشرب", "read": "يقرأ", "drive": "يقود",
                "do": "يفعل", "does": "يفعل (للمفرد الغائب)", "did": "فعل (ماضي)", "sings": "يغني", "play": "يلعب", "writes": "يكتب", "reads": "يقرأ", "sleeps": "ينام", "jumps": "يقفز", "dances": "يرقص", "swim": "يسبح", "sit": "يجلس", "stand": "يقف", "talk": "يتحدث", "listen": "يستمع", "sees": "يرى", "hears": "يسمع", "come": "يأتي",
                "have": "يملك", "has": "يملك (للمفرد الغائب)", "had": "ملك (ماضي)", "eat": "يأكل", "run": "يجري", "flies": "يطير", "swims": "يسبح",
                "He": "هو (للمذكر العاقل)", "She": "هي (للمؤنث العاقل)", "It": "هو/هي (لغير العاقل)",
                "Apple": "تفاحة", "Ant": "نملة", "Airplane": "طائرة",
                "Book": "كتاب", "Ball": "كرة", "Dog": "كلب", "Bird": "طائر", "Banana": "موزة",
                "Car": "سيارة", "Cat": "قطة", "Cloud": "سحابة", "Chair": "كرسي",
                "Duck": "بطة", "Desk": "مكتب",
                "Egg": "بيضة", "Eye": "عين", "Ear": "أذن",
                "Fish": "سمكة", "Frog": "ضفدع", "Flower": "زهرة", "Fan": "مروحة",
                "Girl": "فتاة", "Grape": "عنب", "Glass": "كوب/زجاج", "Goat": "ماعز",
                "House": "منزل", "Hat": "قبعة", "Hand": "يد",
                "Ice Cream": "آيس كريم", "Ink": "حبر", "Island": "جزيرة",
                "Juice": "عصير", "Jacket": "سترة", "Jam": "مربى",
                "Kite": "طائرة ورقية", "Key": "مفتاح", "King": "ملك",
                "Lion": "أسد", "Lamp": "مصباح", "Leaf": "ورقة شجر",
                "Monkey": "قرد", "Moon": "قمر", "Milk": "حليب",
                "Nose": "أنف", "Net": "شبكة", "Nest": "عش",
                "Orange": "برتقالة", "Owl": "بومة", "Onion": "بصلة",
                "Pencil": "قلم رصاص", "Pen": "قلم حبر", "Pig": "خنزير", "Pineapple": "أناناس",
                "Queen": "ملكة", "Quilt": "لحاف", "Quiet": "هادئ",
                "Rabbit": "أرنب", "Rain": "مطر", "Robot": "روبوت",
                "Sun": "شمس", "Star": "نجمة", "Shoe": "حذاء",
                "Tree": "شجرة", "Table": "طاولة", "Tiger": "نمر",
                "Umbrella": "مظلة", "Unicorn": "وحيد القرن", "Uniform": "زي موحد", "Up": "فوق",
                "Van": "شاحنة صغيرة", "Violin": "كمان", "Vase": "مزهرية",
                "Water": "ماء", "Window": "نافذة", "Watch": "ساعة يد",
                "X-ray": "أشعة سينية", "Xylophone": "إكسيليفون", "Fox": "ثعلب",
                "Yellow": "أصفر", "Yogurt": "زبادي", "Yawn": "تثاؤب",
                "Zebra": "حمار وحشي", "Zoo": "حديقة حيوان", "Zip": "سحاب (ملابس)"
            };

            function getArabicMeaning(word) {
                return arabicMeaningMap[word] || "معنى غير متاح";
            }

            let allQuestions = [];

            // توليد وتوزيع الأسئلة
            function generateQuizQuestions() {
                const categories = {
                    'verb_to_be': shuffleArray([...verbToBeQuestions]).slice(0, 10), // 10 أسئلة
                    'verb_to_do': shuffleArray([...verbToDoQuestions]).slice(0, 10), // 10 أسئلة
                    'verb_to_have': shuffleArray([...verbToHaveQuestions]).slice(0, 10), // 10 أسئلة
                    'he_it_is': shuffleArray([...heItIsQuestions]).slice(0, 5), // 5 أسئلة
                    'vocabulary': shuffleArray([...vocabularyQuestions]).slice(0, 15) // 15 سؤال
                };

                allQuestions = [];
                for (const category in categories) {
                    allQuestions = allQuestions.concat(categories[category]);
                }
                allQuestions = shuffleArray(allQuestions); // خلط كل الأسئلة معًا
            }

            // دالة لخلط عناصر مصفوفة
            function shuffleArray(array) {
                for (let i = array.length - 1; i > 0; i--) {
                    const j = Math.floor(Math.random() * (i + 1));
                    [array[i], array[j]] = [array[j], array[i]];
                }
                return array;
            }

            // عرض السؤال الحالي
            function displayQuestion() {
                feedback.textContent = '';
                feedback.className = ''; // مسح أي كلاسات سابقة (مثل correct-feedback)
                nextQuestionBtn.style.display = 'none';
                optionsContainer.innerHTML = ''; // مسح الخيارات السابقة

                if (currentQuestionIndex < totalQuestions) {
                    const question = allQuestions[currentQuestionIndex];
                    questionCounter.textContent = `السؤال ${currentQuestionIndex + 1} من ${totalQuestions}`;
                    questionText.textContent = question.q;
                    arabicMeaningQuestionSpan.textContent = question.qWordMeaning;

                    // خلط خيارات السؤال الحالي
                    const shuffledOptions = shuffleArray([...question.options]);

                    shuffledOptions.forEach(option => {
                        const button = document.createElement('button');
                        button.classList.add('option-btn');
                        button.textContent = option;
                        // For English options, set direction to LTR
                        button.style.direction = 'ltr';
                        button.addEventListener('click', () => selectAnswer(button, option, question.correct, question.q));
                        optionsContainer.appendChild(button);
                    });
                } else {
                    showResultScreen(); // عرض شاشة النتائج عند الانتهاء
                }
            }

            // التعامل مع اختيار الإجابة
            function selectAnswer(selectedButton, selectedAnswer, correctAnswer, originalQuestionText) {
                // تعطيل جميع الخيارات بعد الاختيار
                Array.from(optionsContainer.children).forEach(button => {
                    button.disabled = true;
                    button.classList.remove('selected');
                });

                selectedButton.classList.add('selected');

                const selectedMeaning = getArabicMeaning(selectedAnswer);
                const correctMeaning = getArabicMeaning(correctAnswer);
                const isCorrect = (selectedAnswer === correctAnswer);

                // حفظ نتيجة هذا السؤال
                quizResults.push({
                    question: originalQuestionText,
                    chosenAnswer: selectedAnswer,
                    correctAnswer: correctAnswer,
                    isCorrect: isCorrect
                });

                if (isCorrect) {
                    feedback.textContent = `إجابة صحيحة! (اختيارك: ${selectedAnswer} - ${selectedMeaning})`;
                    feedback.classList.add('correct-feedback'); // إضافة كلاس لتغيير اللون للأخضر
                    selectedButton.classList.add('correct');
                    score++;
                } else {
                    feedback.textContent = `إجابة خاطئة. الإجابة الصحيحة كانت: ${correctAnswer} (${correctMeaning}). اختيارك: ${selectedAnswer} (${selectedMeaning})`;
                    feedback.classList.remove('correct-feedback'); // إزالة الكلاس في حالة الخطأ
                    selectedButton.classList.add('incorrect');
                    // تمييز الإجابة الصحيحة
                    Array.from(optionsContainer.children).forEach(button => {
                        if (button.textContent === correctAnswer) {
                            button.classList.add('correct');
                        }
                    });
                }
                nextQuestionBtn.style.display = 'block'; // إظهار زر "السؤال التالي"
            }

            // عرض شاشة النتائج النهائية
            function showResultScreen() {
                quizScreen.style.display = 'none';
                resultScreen.style.display = 'block';

                const finalScore = (score / totalQuestions) * 100;

                finalStudentName.textContent = studentName;
                correctAnswersCountSpan.textContent = score;
                totalQuestionsCountSpan.textContent = totalQuestions;
                finalScoreSpan.textContent = finalScore.toFixed(2); // تنسيق الرقم العشري

                displayAnswerSummary(); // عرض ملخص الإجابات

                // توليد روابط مشاركة واتساب
                let whatsappMessage = `مرحباً! ${studentName} أكمل/ت اختبار الإنجليزية وحصل/ت على ${finalScore.toFixed(2)} من 100.\n\n`;
                whatsappMessage += "ملخص الإجابات:\n";

                quizResults.forEach((result, index) => {
                    const status = result.isCorrect ? "صحيحة" : "خاطئة";
                    whatsappMessage += `\nالسؤال ${index + 1}: ${result.question}\n`;
                    whatsappMessage += `إجابتك: ${result.chosenAnswer} (${getArabicMeaning(result.chosenAnswer)})\n`;
                    whatsappMessage += `الإجابة الصحيحة: ${result.correctAnswer} (${getArabicMeaning(result.correctAnswer)})\n`;
                    whatsappMessage += `الحالة: ${status}\n`;
                });

                const encodedMessage = encodeURIComponent(whatsappMessage);

                whatsappShare1.href = `https://wa.me/201117112423?text=${encodedMessage}`;
                whatsappShare2.href = `https://wa.me/201019334526?text=${encodedMessage}`;
            }

            // عرض ملخص الإجابات في شاشة النتائج
            function displayAnswerSummary() {
                answerSummaryDiv.innerHTML = '<h3>ملخص الإجابات:</h3>'; // إعادة تهيئة القسم
                quizResults.forEach((result, index) => {
                    const itemDiv = document.createElement('div');
                    itemDiv.classList.add('summary-item');

                    const questionP = document.createElement('p');
                    questionP.classList.add('summary-question-text');
                    questionP.textContent = `السؤال ${index + 1}: ${result.question}`;
                    itemDiv.appendChild(questionP);

                    const userAnswerP = document.createElement('p');
                    userAnswerP.classList.add('summary-user-answer');
                    userAnswerP.textContent = `إجابتك: ${result.chosenAnswer} (${getArabicMeaning(result.chosenAnswer)})`;
                    itemDiv.appendChild(userAnswerP);

                    const correctAnswerP = document.createElement('p');
                    correctAnswerP.classList.add('summary-correct-answer');
                    correctAnswerP.textContent = `الإجابة الصحيحة: ${result.correctAnswer} (${getArabicMeaning(result.correctAnswer)})`;
                    itemDiv.appendChild(correctAnswerP);

                    const statusP = document.createElement('p');
                    statusP.classList.add('summary-result');
                    statusP.classList.add(result.isCorrect ? 'correct' : 'incorrect');
                    statusP.textContent = `الحالة: ${result.isCorrect ? 'صحيحة' : 'خاطئة'}`;
                    itemDiv.appendChild(statusP);

                    answerSummaryDiv.appendChild(itemDiv);
                });
            }

            // إعادة تعيين الاختبار
            function resetQuiz() {
                currentQuestionIndex = 0;
                score = 0;
                studentName = '';
                quizResults = []; // مسح النتائج المحفوظة
                studentNameInput.value = '';
                feedback.textContent = '';
                feedback.className = '';
                nextQuestionBtn.style.display = 'none';
                quizScreen.style.display = 'none';
                resultScreen.style.display = 'none';
                welcomeScreen.style.display = 'block';
            }

            // --- المستمعون للأحداث (Event Listeners) ---
            startQuizBtn.addEventListener('click', () => {
                studentName = studentNameInput.value.trim();
                if (studentName) {
                    welcomeScreen.style.display = 'none';
                    quizScreen.style.display = 'block';
                    generateQuizQuestions(); // توليد وخلط الأسئلة لكل جلسة اختبار جديدة
                    displayQuestion();
                } else {
                    alert('من فضلك، أدخل اسمك لبدء الاختبار!');
                }
            });

            nextQuestionBtn.addEventListener('click', () => {
                currentQuestionIndex++;
                displayQuestion();
            });

            restartQuizBtn.addEventListener('click', resetQuiz);

            // توجيه كتابة الاسم من اليمين لليسار
            studentNameInput.style.direction = 'rtl';
        });
    </script>
</body>
</html>
