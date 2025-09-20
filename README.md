<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>プロダクトアイデア評価シート</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Noto Sans JP', sans-serif;
        }
        .tab-btn.active {
            border-color: #3b82f6;
            background-color: #3b82f6;
            color: white;
        }
        .content-box {
            display: none;
        }
        .content-box.active {
            display: block;
        }
        /* Responsive table styles */
        @media (max-width: 768px) {
            .responsive-table thead {
                display: none;
            }
            .responsive-table, .responsive-table tbody, .responsive-table tr, .responsive-table td {
                display: block;
                width: 100%;
            }
            .responsive-table tr {
                margin-bottom: 1.5rem;
                border: 1px solid #e5e7eb;
                border-radius: 0.5rem;
                padding: 1rem;
                box-shadow: 0 1px 3px rgba(0,0,0,0.1);
            }
            .responsive-table td {
                padding-left: 50%;
                position: relative;
                text-align: right;
                border: none;
            }
            .responsive-table td::before {
                content: attr(data-label);
                position: absolute;
                left: 0.75rem;
                width: 45%;
                padding-right: 0.75rem;
                text-align: left;
                font-weight: 600;
                color: #1f2937;
            }
        }
        .rank-gold { background-color: #fffbeb; border-left-color: #f59e0b; }
        .rank-silver { background-color: #f9fafb; border-left-color: #9ca3af; }
        .rank-bronze { background-color: #fdf2f2; border-left-color: #cd7f32; }
    </style>
</head>
<body class="bg-slate-50 text-slate-800">

    <div class="container mx-auto p-4 sm:p-6 md:p-8">
        <header class="text-center mb-8">
            <h1 class="text-3xl md:text-4xl font-bold text-slate-900">プロダクトアイデア評価シート</h1>
            <p class="mt-2 text-slate-600">各アイデアの詳細、スコア、評価基準を切り替えて確認できます。</p>
        </header>

        <nav class="flex justify-center border-b border-slate-200 mb-8">
            <button class="tab-btn active text-lg font-semibold py-3 px-6 border-b-4" data-tab="ideas">アイデア一覧</button>
            <button class="tab-btn text-lg font-semibold py-3 px-6 border-b-4 border-transparent text-slate-500 hover:border-slate-300" data-tab="scoring">採点表</button>
            <button class="tab-btn text-lg font-semibold py-3 px-6 border-b-4 border-transparent text-slate-500 hover:border-slate-300" data-tab="criteria">採点基準</button>
        </nav>

        <main>
            <section id="ideas" class="content-box active space-y-6">
                <div class="bg-white p-6 rounded-lg shadow-sm border border-slate-200">
                    <h3 class="text-lg font-bold">A. 画面タッチで音楽を奏でるデバイス</h3>
                    <div class="mt-4 grid grid-cols-1 md:grid-cols-2 gap-x-8 gap-y-4 text-sm">
                        <div><strong class="text-slate-600">ターゲット顧客:</strong> 音楽経験はないが、手軽に自己表現をしたい若者</div>
                        <div><strong class="text-slate-600">根深い課題:</strong> 楽器演奏は習得が難しく、作曲は専門知識が必要でハードルが高い</div>
                        <div class="md:col-span-2"><strong class="text-slate-600">独自の価値提案(UVP):</strong> 楽譜も経験も不要。触れるだけで、プロが作ったような音楽を直感的に生み出せる魔法のキャンバス</div>
                        <div class="md:col-span-2"><strong class="text-slate-600">具体的なソリューション:</strong> 画面をタッチする場所や指の動きで音色やリズムが変化するパッド型デバイス。AIがユーザーの操作を解析し、音楽的に破綻しないようリアルタイムでアシストする。</div>
                        <div><strong class="text-slate-600">主要指標:</strong> 1日あたりの平均演奏時間、SNSでの作品シェア数</div>
                        <div><strong class="text-slate-600">技術的優位性:</strong> 触覚フィードバック技術、音源合成技術、AIによる音楽生成アルゴリズム</div>
                    </div>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-sm border border-slate-200">
                    <h3 class="text-lg font-bold">B. 子供の成長を記録し、才能を予測するAIカメラ</h3>
                    <div class="mt-4 grid grid-cols-1 md:grid-cols-2 gap-x-8 gap-y-4 text-sm">
                        <div><strong class="text-slate-600">ターゲット顧客:</strong> 子供の将来や教育に関心が高い30-40代の親</div>
                        <div><strong class="text-slate-600">根深い課題:</strong> 子供の何気ない日常の行動にどんな才能が隠れているか分からず、教育方針に迷う</div>
                        <div class="md:col-span-2"><strong class="text-slate-600">独自の価値提案(UVP):</strong> 日常を撮るだけで、AIが我が子の「隠れた得意」を見つけ出し、未来の可能性を教えてくれる子育てパートナー</div>
                        <div class="md:col-span-2"><strong class="text-slate-600">具体的なソリューション:</strong> 子供の行動（ブロック遊び、絵描き、運動など）を定点カメラで撮影。AIが画像解析で行動パターンを分類・分析し、「空間認識能力が高い」「集中力が持続する」などの特性を可視化し、レポートする。</div>
                        <div><strong class="text-slate-600">主要指標:</strong> 保護者のアプリ継続利用率、有料レポートの購入率</div>
                        <div><strong class="text-slate-600">技術的優位性:</strong> 高度な画像認識・行動分析AI、教育心理学に基づいた分析モデル</div>
                    </div>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-sm border border-slate-200">
                    <h3 class="text-lg font-bold">C. 没入感を究極に高めるVRライブ用ヘッドセット</h3>
                    <div class="mt-4 grid grid-cols-1 md:grid-cols-2 gap-x-8 gap-y-4 text-sm">
                        <div><strong class="text-slate-600">ターゲット顧客:</strong> 遠方に住んでいる、またはチケットが入手困難でライブに行けない音楽ファン</div>
                        <div><strong class="text-slate-600">根深い課題:</strong> ライブ配信は便利だが、会場の熱気や一体感がなく物足りない</div>
                        <div class="md:col-span-2"><strong class="text-slate-600">独自の価値提案(UVP):</strong> 自宅が最前列アリーナに変わる。アーティストの息遣いと会場の熱狂を全身で感じる、究極の没入型ライブ体験</div>
                        <div class="md:col-span-2"><strong class="text-slate-600">具体的なソリューション:</strong> 8K超高解像度映像、立体音響、微細な振動による触覚フィードバック機能を搭載した専用ヘッドセット。他の視聴者とアバターで交流できるソーシャル機能も備える。</div>
                        <div><strong class="text-slate-600">主要指標:</strong> 対応コンテンツの販売数、平均視聴時間</div>
                        <div><strong class="text-slate-600">技術的優位性:</strong> 映像・音響技術、高速・低遅延通信技術、小型化技術</div>
                    </div>
                </div>
            </section>

            <section id="scoring" class="content-box">
                 <div class="overflow-x-auto bg-white rounded-lg shadow-sm border border-slate-200">
                    <table class="responsive-table w-full text-sm text-left">
                        <thead class="bg-slate-100 text-slate-600 uppercase">
                            <tr>
                                <th class="p-4">No</th>
                                <th class="p-4">アイデア名</th>
                                <th class="p-4">市場性</th>
                                <th class="p-4">収益性</th>
                                <th class="p-4">ソニーらしさ</th>
                                <th class="p-4">技術実現性</th>
                                <th class="p-4">仮説検証容易さ</th>
                                <th class="p-4">Why Now</th>
                                <th class="p-4 font-bold">合計点</th>
                                <th class="p-4 font-bold">順位</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr class="border-b border-slate-200 border-l-8 rank-gold">
                                <td data-label="No" class="p-4 font-medium">A</td>
                                <td data-label="アイデア名" class="p-4 font-medium">画面タッチで音楽を奏でるデバイス</td>
                                <td data-label="市場性" class="p-4">4</td>
                                <td data-label="収益性" class="p-4">4</td>
                                <td data-label="ソニーらしさ" class="p-4">5</td>
                                <td data-label="技術実現性" class="p-4">4</td>
                                <td data-label="仮説検証容易さ" class="p-4">5</td>
                                <td data-label="Why Now" class="p-4">5</td>
                                <td data-label="合計点" class="p-4 font-bold text-lg">27</td>
                                <td data-label="順位" class="p-4 font-bold text-lg text-amber-500">1</td>
                            </tr>
                            <tr class="border-b border-slate-200 border-l-8 rank-silver">
                                <td data-label="No" class="p-4 font-medium">B</td>
                                <td data-label="アイデア名" class="p-4 font-medium">子供の成長を記録し、才能を予測するAIカメラ</td>
                                <td data-label="市場性" class="p-4">5</td>
                                <td data-label="収益性" class="p-4">3</td>
                                <td data-label="ソニーらしさ" class="p-4">4</td>
                                <td data-label="技術実現性" class="p-4">4</td>
                                <td data-label="仮説検証容易さ" class="p-4">3</td>
                                <td data-label="Why Now" class="p-4">4</td>
                                <td data-label="合計点" class="p-4 font-bold text-lg">23</td>
                                <td data-label="順位" class="p-4 font-bold text-lg text-slate-500">2</td>
                            </tr>
                            <tr class="border-b border-slate-200 border-l-8 rank-bronze">
                                <td data-label="No" class="p-4 font-medium">C</td>
                                <td data-label="アイデア名" class="p-4 font-medium">没入感を究極に高めるVRライブ用ヘッドセット</td>
                                <td data-label="市場性" class="p-4">3</td>
                                <td data-label="収益性" class="p-4">3</td>
                                <td data-label="ソニーらしさ" class="p-4">5</td>
                                <td data-label="技術実現性" class="p-4">3</td>
                                <td data-label="仮説検証容易さ" class="p-4">2</td>
                                <td data-label="Why Now" class="p-4">5</td>
                                <td data-label="合計点" class="p-4 font-bold text-lg">21</td>
                                <td data-label="順位" class="p-4 font-bold text-lg text-orange-700">3</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </section>

            <section id="criteria" class="content-box">
                <div class="space-y-4 text-sm">
                    <div class="bg-white p-4 rounded-lg shadow-sm border border-slate-200">
                        <h4 class="font-bold text-base text-slate-800">市場性</h4>
                        <p class="text-slate-600 mt-2"><strong class="w-12 inline-block">[5点]</strong> 既存市場を破壊、または巨大な新市場を創造する可能性</p>
                        <p class="text-slate-600 mt-1"><strong class="w-12 inline-block">[3点]</strong> 特定のセグメントで高いシェアを狙える</p>
                        <p class="text-slate-600 mt-1"><strong class="w-12 inline-block">[1点]</strong> ニッチ市場で、大きな成長は見込みにくい</p>
                    </div>
                    <div class="bg-white p-4 rounded-lg shadow-sm border border-slate-200">
                        <h4 class="font-bold text-base text-slate-800">収益性</h4>
                        <p class="text-slate-600 mt-2"><strong class="w-12 inline-block">[5点]</strong> 高い利益率が見込め、継続的な収益モデル（サブスク等）を構築可能</p>
                        <p class="text-slate-600 mt-1"><strong class="w-12 inline-block">[3点]</strong> 売り切りモデルだが、十分な利益が見込める</p>
                        <p class="text-slate-600 mt-1"><strong class="w-12 inline-block">[1点]</strong> マネタイズの具体案が不明確、または低利益率</p>
                    </div>
                    <div class="bg-white p-4 rounded-lg shadow-sm border border-slate-200">
                        <h4 class="font-bold text-base text-slate-800">ソニーらしさ</h4>
                        <p class="text-slate-600 mt-2"><strong class="w-12 inline-block">[5点]</strong> 技術・ブランド・顧客基盤など、自社の強みを最大限に活かせる</p>
                        <p class="text-slate-600 mt-1"><strong class="w-12 inline-block">[3点]</strong> 自社の既存事業とシナジーがある</p>
                        <p class="text-slate-600 mt-1"><strong class="w-12 inline-block">[1点]</strong> 自社でやる必然性が低い</p>
                    </div>
                    <div class="bg-white p-4 rounded-lg shadow-sm border border-slate-200">
                        <h4 class="font-bold text-base text-slate-800">技術的実現性</h4>
                        <p class="text-slate-600 mt-2"><strong class="w-12 inline-block">[5点]</strong> 既存技術の応用で実現可能。リスクは低い</p>
                        <p class="text-slate-600 mt-1"><strong class="w-12 inline-block">[3点]</strong> いくつか技術的課題はあるが、1-2年で解決可能</p>
                        <p class="text-slate-600 mt-1"><strong class="w-12 inline-block">[1点]</strong> 未知の技術要素が多く、実現にはブレークスルーが必要</p>
                    </div>
                </div>
            </section>
        </main>
        
        <footer class="mt-8 text-center text-sm text-slate-500">
             <a href="index.html" class="text-blue-600 hover:underline">← メインページに戻る</a>
        </footer>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const tabs = document.querySelectorAll('.tab-btn');
            const contents = document.querySelectorAll('.content-box');

            tabs.forEach(tab => {
                tab.addEventListener('click', () => {
                    // Deactivate all tabs and contents
                    tabs.forEach(t => t.classList.remove('active'));
                    contents.forEach(c => c.classList.remove('active'));

                    // Activate clicked tab and corresponding content
                    tab.classList.add('active');
                    document.getElementById(tab.dataset.tab).classList.add('active');
                });
            });
        });
    </script>

</body>
</html>
