# HCS2025-10-Yamada

・初期実験の実行手順  
Webブラウザ版のChatGPTを開き，新しいプロジェクトを作成する．  
作成したプロジェクトにTangramフォルダ内の画像ファイルをアップロードする．その際に順序効果を避けるため，画像ファイル名は「c32x.png」などの無造作なものに変更する．  
プロジェクト内に新しいチャットを作成し，HCS2025-10-FirstExperiment-Analytic.txtをプロンプトに入力しAnalyticな特徴の事前認知を行う．  
出力された内容を基にHCS2025-10-FirstExperiment-A-cost.txtとHCS2025-10-FirstExperiment-B-cost.txtを変更する．また，HCS2025-10-FirstExperiment-A-nocost.txtとHCS2025-10-FirstExperiment-B-nocost.txtは対話コストの内容を除いて変更する．  
プロジェクト内に新しく2つのチャットの作成する．このテキスト内ではそれぞれエージェントA，エージェントBと呼称する．  
「cost条件の実行」  
エージェントA、エージェントBそれぞれのプロンプトにHCS2025-10-FirstExperiment-Holistic-cost.txtを入力しHolisticな特徴の事前認知を行う．  
エージェントAのプロンプトにHCS2025-10-FirstExperiment-A-cost.txtを入力し，エージェントBのプロンプトにHCS2025-10-FirstExperiment-B-cost.txtを入力する．  
1.エージェントAから発話内容と内部状態が出力されるため，発話内容のみをエージェントBのプロンプトに入力する．  
2.エージェントBから発話内容と内部状態が出力されるため，発話内容のみをエージェントAのプロンプトに入力する．  
1,2の手順をタングラム命名課題が終了するまで繰り返す．  
タングラム命名課題が終了したら実験終了．  
「nocost条件の実行」  
cost条件の実行から，ファイル名のcostをnocostに置き換えたファイルに変更し，同様に実行する．  

・新規実験の実行手順  
ChatGPTのAPIキーを入手する．  
Tangramフォルダ内の画像URLを取得する．  
HCS2025-10-NewExperiment.ipynbを開く．  
先ほど取得したタングラムの画像URLをソースコード内に記入する．  
ソースコードを実行する．初回実行時にはAPIキーの入力が求められるので入力する．  
リアルタイムでエージェントAとエージェントBの対話が出力される．  
対話終了後，対話ログと内部状態ログがまとめて出力される．  
(環境定義はrequirements.txt参照)  
