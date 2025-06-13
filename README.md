# NLP Model Review: Evaluating Text Classification Techniques – RNNs Triumph Over Transformers

### Executive Summary

In the era of **Generative AI and transformative advancements in NLP**, transformer models have emerged as comprehensive reasoners of unstructured textual data, praised for their ability to capture **complex syntactic structures and contextual nuances**. With the remarkable success of models like Gemini, GPT-4.1, and their successors, it is natural to assume that transformers would be the optimal choice for classifying short-form questions from an online forum. 

However, contrary to initial expectations, this comprehensive model review reveals that **traditional methods, specifically RNN-based approaches, outperformed transformer models** in both accuracy and computational efficiency. Despite the inherent strengths of transformers, their **high processing demands and marginal performance gains** rendered them less suitable for this particular classification task. Instead, simpler RNN models like GRU and LSTM demonstrated **30-40% higher classification performance**, highlighting that sometimes **traditional methods can outperform cutting-edge techniques when matched appropriately to the problem's characteristics**.

---

#### Key Insights and Observations

1. **Data Characteristics and Preprocessing:**
   - The dataset exhibited **category imbalances**, prompting the use of **stratified sampling** for train-test splits to enhance model generalisation.
   - **Noise analysis** revealed that equations and technical terminology were often misclassified as irrelevant or noisy. Careful consideration was given to retain these elements since they were contextually significant.
   - Vocabulary analysis identified that **n-grams and word frequency alone were insufficient** for robust classification, emphasising the need for context-aware models.

2. **Model Selection and Evaluation:**
   - Despite the **promising potential of transformer models**, their **high computational cost and marginal improvement** over traditional techniques made them less suitable for short-form question classification. Transformer metrics showed limited enhancement even after fine-tuning, including:
     - **F1-Score:** 0.591 (initial), 0.540 (post-category changes)
     - **Precision:** 0.803 (initial), 0.800 (post-category changes)
     - **Recall:** 0.559 (initial), 0.516 (post-category changes)
     - **Accuracy:** 0.559 (initial), 0.516 (post-category changes)
   - On the other hand, **RNN-based models (GRU and LSTM)** delivered significantly higher and more consistent performance with:
     - **Accuracy:** 89.50%
     - **Average Precision:** 88.73%
     - **Average Recall:** 87.65%
     - **Average F1-Score:** 88.15%
   - These results indicate that **RNNs, particularly GRU models, outperform transformers** for short-form text classification, offering a balanced trade-off between performance and computational efficiency.

3. **Recommendations and Next Steps:**
   - Further tuning and optimisation of RNN models could be explored, including **regularisation techniques and hyperparameter adjustments** to maximise model performance.
   - Investigating **additional data sources** with richer contextual information may enhance feature representation and model accuracy. However, it is crucial to balance model complexity with data availability and processing constraints.
   - Emphasis on **efficient model evaluation strategies** should continue, as data complexity and diversity remain key challenges in classification accuracy.

---

#### Conclusion
This study demonstrates that, while **transformer models carry immense potential and hype due to their success in Generative AI applications**, they are not universally superior. For this specific problem of **short-form question classification**, **traditional RNN-based models proved to be more effective**. These findings challenge the assumption that the most advanced models are always the best fit and highlight the importance of **carefully matching model architecture to the problem context**. The practical implications include **enhanced classification performance and efficient deployment** for real-world applications.
