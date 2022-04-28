# ML_Class8
## Domain Adaptation
### 假設訓練資料跟測試資料有一點差異時，如何讓訓練結果更好？
1. 希望用測試資料所訓練出來的模型可以用在不一樣的domain上，所以我們在訓練的時候，就要對target domain有一些了解，隨著瞭解的程度不同，就有不同的domain adaptation的方法
2. 在target domain有大量未標注的資料，如何用這些資料來幫助我們在source domain上訓練一個模型且可以用在target domain上？
3. 如何找出feature extractor?
   把一個classifier的前幾層分類為feature extractor，後幾層分類為Label Predictor
4. 如何使用在target domain沒有標注的資料？
   把target data跟source data丟進去model，然後把feature extractor的output拿出來看，我們希望source data丟進去的feature跟target data的feature，兩者要分不出差異（要藉由
   domain adversarial training的技術）
5. domain adversarial training就很像是GAN！
6. Label Predictor：找一個theta(p)，使得L越小越好，也就是source domain的image分類越正確越好

   Domain Classifier：找一個theta(d)，使得L(d)越小越好，也就是domain的分類越正確越好

   Feature Extractor:站在Label Predictor那邊，與Domain Classifier抗衡

   
