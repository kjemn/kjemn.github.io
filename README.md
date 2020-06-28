# 音声認識して文字起こしするWebサイト

Web Speech API の音声認識を利用して、マイク入力した音声の文字起こしをします。  
デバイスから発する音をループバック入力すれば、配信動画やビデオ会議の相手の音声を文字起こしすることもできます。
[Googleのサンプルコード](https://www.google.com/intl/en/chrome/demos/speech.html)を元に、筆者が次のような改修をおこないました。おもに、30分を越えるビデオ会議や動画配信に向けた安定動作を考慮しています。

- 最大5分で認識モードが自動解除されるAPIの仕様の対策
- 文字起こし済み文章が増大したときの処理負荷増大対策
- 同時通訳機能の追加（ベータ版）

## デモページ

[kjemn.github.io/speech-recognition/](https://kjemn.github.io/speech-recognition/)  
*PC版 Google Chromeのみ動作確認済

## 動作環境

筆者は一般的な動作環境のみ確認しています。

- PC版 Google Chrome
  - Windows 10 Pro 64-bit のみ確認済み
- 安定的に動作確認した言語
  - ドイツ語，英語（欧州英語は認識精度低め）

## Tips

### 相手の声（デバイスから発する音）を認識させる

フリーソフト等を使い、PC内部の再生音を仮想マイクとして入力する。  
参考（筆者が使用しているツール）：[Voicemeeter](https://www.vb-audio.com/Voicemeeter/)

## References

- [[Google] Web Speech API Demonstration](https://www.google.com/intl/ja/chrome/demos/speech.html)
- [[GitHub] Webカメラの映像に自動字幕を重ねるWebページ](https://github.com/1heisuzuki/speech-to-text-webcam-overlay)
- [[so-zou.jp] Google 翻訳 (Google Translate)](https://so-zou.jp/web-app/tech/search-engine/google/translate/)
- [[cman.jp] ON/OFFスイッチをCSSのみで実装
](https://webparts.cman.jp/button/onoff/)
