<html lang="zh-CN"><head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IQ测试 - 挑战你的智力</title>
    <!-- 微信分享配置（已全部帮你填好） -->
    <meta property="og:title" content="智商测试" />
    <meta property="og:description" content="10道题测出你的真实智商，快来挑战一下！" />
    <meta property="og:image" content="https://p3-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/391d006fcaad446e93e57302b5a74038.jpg" />
    <meta property="og:url" content="当前页面网址" />
    <meta property="og:type" content="website" />

    
    <!-- Tailwind CSS v3 -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome -->
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    <!-- 统一的 Tailwind 配置 -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#3b82f6',
                        secondary: '#10b981',
                        accent: '#8b5cf6',
                        neutral: '#6b7280',
                        'neutral-light': '#f3f4f6',
                        'neutral-dark': '#1f2937'
                    },
                    fontFamily: {
                        sans: ['Inter', 'system-ui', 'sans-serif'],
                    },
                    animation: {
                        'fade-in': 'fadeIn 0.5s ease-in-out',
                        'slide-in': 'slideIn 0.5s ease-in-out',
                        'bounce-in': 'bounceIn 0.5s ease-in-out',
                        'pulse-slow': 'pulse 3s infinite'
                    },
                    keyframes: {
                        fadeIn: {
                            '0%': { opacity: '0' },
                            '100%': { opacity: '1' }
                        },
                        slideIn: {
                            '0%': { transform: 'translateY(20px)', opacity: '0' },
                            '100%': { transform: 'translateY(0)', opacity: '1' }
                        },
                        bounceIn: {
                            '0%': { transform: 'scale(0.8)', opacity: '0' },
                            '70%': { transform: 'scale(1.05)', opacity: '1' },
                            '100%': { transform: 'scale(1)', opacity: '1' }
                        }
                    }
                }
            }
        }
    </script>
    <style type="text/tailwindcss">
        @layer utilities {
            .content-auto {
                content-visibility: auto;
            }
            .glass-effect {
                @apply bg-white bg-opacity-20 backdrop-blur-lg;
            }
            .card-hover {
                @apply transition-all duration-300 hover:shadow-lg hover:-translate-y-1;
            }
            .btn-primary {
                @apply bg-primary text-white font-medium py-2 px-4 rounded-lg hover:bg-blue-600 transition-colors duration-300 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-opacity-50;
            }
            .btn-secondary {
                @apply bg-secondary text-white font-medium py-2 px-4 rounded-lg hover:bg-green-600 transition-colors duration-300 focus:outline-none focus:ring-2 focus:ring-green-500 focus:ring-opacity-50;
            }
            .btn-outline {
                @apply border border-primary text-primary font-medium py-2 px-4 rounded-lg hover:bg-primary hover:text-white transition-colors duration-300 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-opacity-50;
            }
            .input-radio {
                @apply h-4 w-4 text-primary focus:ring-primary border-gray-300 rounded;
            }
            .progress-bar {
                @apply h-2 bg-gray-200 rounded-full overflow-hidden;
            }
            .progress-value {
                @apply h-full bg-primary transition-all duration-300 ease-out;
            }
        }
    </style>
</head>
<body class="bg-gradient-to-br from-blue-50 to-indigo-100 min-h-screen">
    <!-- 导航栏 -->
    <nav class="bg-white shadow-md">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <i class="fa fa-brain text-primary text-2xl"></i>
                <span class="text-xl font-bold text-gray-800">IQ测试</span>
            </div>
            <div class="flex items-center space-x-4">
                <button id="helpBtn" class="text-gray-600 hover:text-primary transition-colors">
                    <i class="fa fa-question-circle text-lg"></i>
                </button>
                <button id="restartBtn" class="text-gray-600 hover:text-primary transition-colors">
                    <i class="fa fa-refresh text-lg"></i>
                </button>
            </div>
        </div>
    </nav>

    <!-- 主要内容 -->
    <main class="container mx-auto px-4 py-8">
        <!-- 开始页面 -->
        <section id="startSection" class="max-w-2xl mx-auto bg-white rounded-xl shadow-lg p-8 animate-fade-in">
            <div class="text-center mb-8">
                <h1 class="text-4xl font-bold text-gray-800 mb-4">欢迎参加IQ测试</h1>
                <p class="text-lg text-gray-600">这个测试包含10道选择题，测试你的逻辑思维、数学能力和空间想象能力。</p>
            </div>
            <div class="mb-8">
                <h2 class="text-xl font-semibold text-gray-800 mb-4">测试说明：</h2>
                <ul class="space-y-2 text-gray-700">
                    <li class="flex items-start">
                        <i class="fa fa-check-circle text-primary mt-1 mr-2"></i>
                        <span>共有10道题目，每道题有4个选项</span>
                    </li>
                    <li class="flex items-start">
                        <i class="fa fa-check-circle text-primary mt-1 mr-2"></i>
                        <span>选择你认为正确的答案，然后点击"下一题"</span>
                    </li>
                    <li class="flex items-start">
                        <i class="fa fa-check-circle text-primary mt-1 mr-2"></i>
                        <span>完成所有题目后，你将看到测试结果</span>
                    </li>
                    <li class="flex items-start">
                        <i class="fa fa-check-circle text-primary mt-1 mr-2"></i>
                        <span>测试没有时间限制，请仔细思考每一道题</span>
                    </li>
                </ul>
            </div>
            <div class="text-center">
                <button id="startTestBtn" class="btn-primary text-lg px-8 py-3">
                    开始测试
                    <i class="fa fa-arrow-right ml-2"></i>
                </button>
            </div>
        </section>

        <!-- 测试页面 -->
        <section id="testSection" class="max-w-2xl mx-auto bg-white rounded-xl shadow-lg p-8 hidden">
            <!-- 进度条 -->
            <div class="mb-6">
                <div class="flex justify-between items-center mb-2">
                    <span class="text-sm font-medium text-gray-700">进度：<span id="progressText">1/10</span></span>
                    <span class="text-sm font-medium text-gray-700">题目 <span id="currentQuestionNum">1</span>/10</span>
                </div>
                <div class="progress-bar">
                    <div id="progressValue" class="progress-value" style="width: 10%"></div>
                </div>
            </div>

            <!-- 题目 -->
            <div id="questionContainer" class="mb-8 animate-slide-in">
                <h2 id="questionText" class="text-2xl font-bold text-gray-800 mb-6">题目加载中...</h2>
                <div id="optionsContainer" class="space-y-4">
                    <!-- 选项将通过JavaScript动态添加 -->
                </div>
            </div>

            <!-- 导航按钮 -->
            <div class="flex justify-between">
                <button id="prevBtn" class="btn-outline opacity-50 cursor-not-allowed" disabled="">
                    <i class="fa fa-arrow-left mr-2"></i>
                    上一题
                </button>
                <button id="nextBtn" class="btn-primary">
                    下一题
                    <i class="fa fa-arrow-right ml-2"></i>
                </button>
            </div>
        </section>

        <!-- 结果页面 -->
        <section id="resultSection" class="max-w-2xl mx-auto bg-white rounded-xl shadow-lg p-8 hidden animate-bounce-in">
            <div class="text-center mb-8">
                <h1 class="text-4xl font-bold text-gray-800 mb-4">恭喜你完成了IQ测试！</h1>
                <p class="text-lg text-gray-600">你已经成功完成了所有题目，扫码支付9.9元获取你的测试结果。</p>
            </div>
            
            <div class="flex justify-center mb-8">
                <img src="https://p3-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/391d006fcaad446e93e57302b5a74038.jpg~tplv-a9rns2rl98-24:720:720.image?lk3s=8e244e95&rcl=20260211170407844DE89A3427A930320E&rrcfp=8a172a1a&x-expires=1771405447&x-signature=88WDp8DqGnyN%2B1LaX8BtFIrckIw%3D" alt="IQ测试完成" class="w-64 h-64 object-contain animate-pulse-slow">
            </div>
            
            <div class="bg-blue-50 rounded-lg p-6 mb-8">
                <div class="flex justify-between items-center mb-4">
                    <h2 class="text-xl font-semibold text-gray-800">你的得分</h2>
                    <span id="scoreDisplay" class="text-3xl font-bold text-primary">
                        <span id="userScore">***</span>
                    </span>
                </div>
                <div class="progress-bar" style="display: none;">
                    <div id="scoreProgress" class="progress-value bg-secondary" style="width: 0%"></div>
                </div>
            </div>
            
            <div class="mb-8">
                <h2 class="text-xl font-semibold text-gray-800 mb-4">IQ水平评估</h2>
                <div id="iqLevelDescription" class="text-gray-700 p-4 bg-neutral-light rounded-lg">
                    <p class="text-center text-gray-500 italic">评估结果已隐藏</p>
                </div>
            </div>
            
            <div class="text-center space-x-4">
                <button id="viewAnswersBtn" class="btn-outline opacity-50 cursor-not-allowed" disabled>
                    <i class="fa fa-lock mr-2"></i>
                    查看答案
                </button>
                <button id="restartTestBtn" class="btn-primary">
                    <i class="fa fa-refresh mr-2"></i>
                    重新测试
                </button>
            </div>
        </section>

        <!-- 答案页面 -->
        <section id="answersSection" class="max-w-2xl mx-auto bg-white rounded-xl shadow-lg p-8 hidden animate-fade-in">
            <div class="flex justify-between items-center mb-6">
                <h2 class="text-2xl font-bold text-gray-800">测试答案</h2>
                <button id="backToResultBtn" class="btn-outline text-sm">
                    <i class="fa fa-arrow-left mr-1"></i>
                    返回结果
                </button>
            </div>
            
            <div id="answersContainer" class="space-y-6">
                <!-- 答案将通过JavaScript动态添加 -->
            </div>
        </section>
    </main>

    <!-- 帮助模态框 -->
    <div id="helpModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden">
        <div class="bg-white rounded-xl shadow-xl p-6 max-w-md w-full mx-4 animate-slide-in">
            <div class="flex justify-between items-center mb-4">
                <h3 class="text-xl font-bold text-gray-800">测试帮助</h3>
                <button id="closeHelpBtn" class="text-gray-500 hover:text-gray-700">
                    <i class="fa fa-times text-xl"></i>
                </button>
            </div>
            <div class="text-gray-700 space-y-4">
                <p>本IQ测试包含10道选择题，旨在评估你的逻辑思维、数学能力和空间想象能力。</p>
                <p>测试流程：</p>
                <ol class="list-decimal pl-5 space-y-2">
                    <li>点击"开始测试"按钮进入测试</li>
                    <li>阅读题目，从四个选项中选择一个你认为正确的答案</li>
                    <li>点击"下一题"按钮进入下一题</li>
                    <li>完成所有题目后，系统会自动计算你的得分并显示结果</li>
                </ol>
                <p>测试没有时间限制，请仔细思考每一道题。</p>
                <p>如果你想重新开始测试，可以随时点击右上角的刷新按钮。</p>
            </div>
            <div class="mt-6 text-center">
                <button id="gotItBtn" class="btn-primary">
                    我知道了
                </button>
            </div>
        </div>
    </div>

    <!-- JavaScript -->
    <script>
        // 题目数据
        const questions = [
            {
                question: "以下哪个数字与其他数字不属于同一类别？",
                options: ["2", "5", "7", "9"],
                answer: 3, // 索引从0开始，9是第4个选项，索引为3
                explanation: "2、5、7 是质数，9 不是质数。"
            },
            {
                question: "如果\"苹果\"对应\"水果\"，那么\"汽车\"对应：",
                options: ["交通工具", "道路", "司机", "工厂"],
                answer: 0,
                explanation: "苹果是水果的一种，汽车是交通工具的一种。"
            },
            {
                question: "观察数列：2，4，6，8，下一个数字应该是：",
                options: ["9", "10", "11", "12"],
                answer: 1,
                explanation: "该数列是公差为 2 的等差数列，8 加 2 为 10。"
            },
            {
                question: "从镜子里看一个时钟显示为 3 点，实际时间是：",
                options: ["3 点", "9 点", "6 点", "12 点"],
                answer: 1,
                explanation: "镜子里的时钟和实际时间关于 6 点和 12 点的连线对称，镜子里 3 点实际是 9 点。"
            },
            {
                question: "下列哪个图形与其他图形不同？",
                options: ["圆形", "三角形", "正方形", "梯形"],
                answer: 0,
                explanation: "圆形是曲线图形，其他是直线图形。"
            },
            {
                question: "假如所有的 A 都是 B，有些 B 是 C，那么有些 A 是 C 这个说法：",
                options: ["一定正确", "一定错误", "不一定正确", "无法判断"],
                answer: 2,
                explanation: "虽然所有 A 是 B，但有些 B 是 C 不能必然推出有些 A 是 C。"
            },
            {
                question: "有一个人在跑步，他跑过了第二名，他现在是第几名？",
                options: ["第一名", "第二名", "第三名", "第四名"],
                answer: 1,
                explanation: "跑过第二名就取代了第二名的位置。"
            },
            {
                question: "以下哪个单词与其他单词不同类？",
                options: ["猫", "狗", "鸟", "树"],
                answer: 3,
                explanation: "树是植物，其他是动物。"
            },
            {
                question: "一个立方体有几个面？",
                options: ["4 个", "6 个", "8 个", "12 个"],
                answer: 1,
                explanation: "立方体有 6 个面。"
            },
            {
                question: "如果 3 只猫在 3 分钟内捉了 3 只老鼠，那么多少只猫在 100 分钟内捉 100 只老鼠？",
                options: ["3 只", "10 只", "30 只", "100 只"],
                answer: 0,
                explanation: "3 只猫 1 分钟捉 1 只老鼠，100 分钟捉 100 只老鼠还是 3 只猫。"
            }
        ];

        // DOM 元素
        const startSection = document.getElementById('startSection');
        const testSection = document.getElementById('testSection');
        const resultSection = document.getElementById('resultSection');
        const answersSection = document.getElementById('answersSection');
        const helpModal = document.getElementById('helpModal');

        const startTestBtn = document.getElementById('startTestBtn');
        const restartBtn = document.getElementById('restartBtn');
        const helpBtn = document.getElementById('helpBtn');
        const closeHelpBtn = document.getElementById('closeHelpBtn');
        const gotItBtn = document.getElementById('gotItBtn');
        const prevBtn = document.getElementById('prevBtn');
        const nextBtn = document.getElementById('nextBtn');
        const viewAnswersBtn = document.getElementById('viewAnswersBtn');
        const restartTestBtn = document.getElementById('restartTestBtn');
        const backToResultBtn = document.getElementById('backToResultBtn');

        const questionText = document.getElementById('questionText');
        const optionsContainer = document.getElementById('optionsContainer');
        const progressText = document.getElementById('progressText');
        const currentQuestionNum = document.getElementById('currentQuestionNum');
        const progressValue = document.getElementById('progressValue');
        const scoreDisplay = document.getElementById('scoreDisplay');
        const scoreProgress = document.getElementById('scoreProgress');
        const iqLevelDescription = document.getElementById('iqLevelDescription');
        const answersContainer = document.getElementById('answersContainer');

        // 测试状态
        let currentQuestionIndex = 0;
        const userAnswers = new Array(questions.length).fill(null);

        // 事件监听器
        startTestBtn.addEventListener('click', startTest);
        restartBtn.addEventListener('click', restartTest);
        helpBtn.addEventListener('click', showHelp);
        closeHelpBtn.addEventListener('click', hideHelp);
        gotItBtn.addEventListener('click', hideHelp);
        prevBtn.addEventListener('click', goToPreviousQuestion);
        nextBtn.addEventListener('click', goToNextQuestion);
        // 查看答案按钮已禁用，不再添加事件监听器
        // viewAnswersBtn.addEventListener('click', showAnswers);
        restartTestBtn.addEventListener('click', restartTest);
        backToResultBtn.addEventListener('click', showResult);

        // 开始测试
        function startTest() {
            startSection.classList.add('hidden');
            testSection.classList.remove('hidden');
            showQuestion(0);
        }

        // 显示问题
        function showQuestion(index) {
            const question = questions[index];
            questionText.textContent = `${index + 1}. ${question.question}`;
            
            // 清空选项容器
            optionsContainer.innerHTML = '';
            
            // 添加选项
            question.options.forEach((option, optionIndex) => {
                const optionDiv = document.createElement('div');
                optionDiv.className = 'flex items-center';
                
                const radioInput = document.createElement('input');
                radioInput.type = 'radio';
                radioInput.id = `option${optionIndex}`;
                radioInput.name = 'answer';
                radioInput.value = optionIndex;
                radioInput.className = 'input-radio';
                radioInput.checked = userAnswers[index] === optionIndex;
                
                radioInput.addEventListener('change', () => {
                    userAnswers[currentQuestionIndex] = optionIndex;
                });
                
                const label = document.createElement('label');
                label.htmlFor = `option${optionIndex}`;
                label.className = 'ml-3 text-gray-700 cursor-pointer hover:text-primary transition-colors';
                label.textContent = option;
                
                optionDiv.appendChild(radioInput);
                optionDiv.appendChild(label);
                optionsContainer.appendChild(optionDiv);
            });
            
            // 更新进度
            currentQuestionNum.textContent = index + 1;
            progressText.textContent = `${index + 1}/${questions.length}`;
            progressValue.style.width = `${(index + 1) / questions.length * 100}%`;
            
            // 更新导航按钮状态
            prevBtn.disabled = index === 0;
            prevBtn.classList.toggle('opacity-50', index === 0);
            prevBtn.classList.toggle('cursor-not-allowed', index === 0);
            
            if (index === questions.length - 1) {
                nextBtn.textContent = '完成测试';
                nextBtn.innerHTML = '完成测试 <i class="fa fa-check ml-2"></i>';
            } else {
                nextBtn.textContent = '下一题';
                nextBtn.innerHTML = '下一题 <i class="fa fa-arrow-right ml-2"></i>';
            }
        }

        // 上一题
        function goToPreviousQuestion() {
            if (currentQuestionIndex > 0) {
                currentQuestionIndex--;
                showQuestion(currentQuestionIndex);
            }
        }

        // 下一题
        function goToNextQuestion() {
            // 如果当前题没有选择答案，提示用户
            if (userAnswers[currentQuestionIndex] === null) {
                alert('请选择一个答案');
                return;
            }
            
            if (currentQuestionIndex < questions.length - 1) {
                currentQuestionIndex++;
                showQuestion(currentQuestionIndex);
            } else {
                // 完成测试
                showResult();
            }
        }

        // 显示结果
        function showResult() {
            testSection.classList.add('hidden');
            resultSection.classList.remove('hidden');
            
            // 计算得分但不显示，保持固定显示***
            const score = userAnswers.filter((answer, index) => answer === questions[index].answer).length;
            // 不再更新userScore，保持固定显示***
            // 不再更新分数条和IQ水平评估
        }

        // 显示答案
        function showAnswers() {
            resultSection.classList.add('hidden');
            answersSection.classList.remove('hidden');
            
            // 清空答案容器
            answersContainer.innerHTML = '';
            
            // 添加答案
            questions.forEach((question, index) => {
                const isCorrect = userAnswers[index] === question.answer;
                const answerDiv = document.createElement('div');
                answerDiv.className = `p-4 rounded-lg ${isCorrect ? 'bg-green-50 border border-green-200' : 'bg-red-50 border border-red-200'}`;
                
                const questionTitle = document.createElement('h3');
                questionTitle.className = 'text-lg font-semibold text-gray-800 mb-2';
                questionTitle.textContent = `${index + 1}. ${question.question}`;
                
                const optionsList = document.createElement('ul');
                optionsList.className = 'space-y-2 mb-3';
                
                question.options.forEach((option, optionIndex) => {
                    const optionItem = document.createElement('li');
                    optionItem.className = 'flex items-center';
                    
                    const optionText = document.createElement('span');
                    optionText.className = `ml-2 ${optionIndex === question.answer ? 'font-semibold text-green-600' : ''} ${optionIndex === userAnswers[index] && optionIndex !== question.answer ? 'font-semibold text-red-600' : ''}`;
                    optionText.textContent = option;
                    
                    const icon = document.createElement('i');
                    if (optionIndex === question.answer) {
                        icon.className = 'fa fa-check-circle text-green-500';
                    } else if (optionIndex === userAnswers[index]) {
                        icon.className = 'fa fa-times-circle text-red-500';
                    } else {
                        icon.className = 'fa fa-circle-o text-gray-400';
                    }
                    
                    optionItem.appendChild(icon);
                    optionItem.appendChild(optionText);
                    optionsList.appendChild(optionItem);
                });
                
                const explanation = document.createElement('p');
                explanation.className = 'text-sm text-gray-600 italic';
                explanation.textContent = `解释：${question.explanation}`;
                
                answerDiv.appendChild(questionTitle);
                answerDiv.appendChild(optionsList);
                answerDiv.appendChild(explanation);
                answersContainer.appendChild(answerDiv);
            });
        }

        // 重新开始测试
        function restartTest() {
            currentQuestionIndex = 0;
            userAnswers.fill(null);
            resultSection.classList.add('hidden');
            answersSection.classList.add('hidden');
            startSection.classList.remove('hidden');
        }

        // 显示帮助
        function showHelp() {
            helpModal.classList.remove('hidden');
        }

        // 隐藏帮助
        function hideHelp() {
            helpModal.classList.add('hidden');
        }

        // 点击模态框外部关闭
        helpModal.addEventListener('click', (e) => {
            if (e.target === helpModal) {
                hideHelp();
            }
        });
    </script>

</body></html>
