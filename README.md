# Biomedical Lay Summarization Project

## 📖 Overview

This project explores the use of **Language Model (LM) based methods** to generate lay summaries of medical articles, focusing on **resource and cost-efficient approaches** to enhance accessibility for the general public. By converting complex biomedical literature into easily understandable summaries, this work bridges the gap between scientific research and public health literacy.

The project utilizes **state-of-the-art transformer models** including T5-Base, T5-Large, FlanT5-Base, BioGPT, Phi-2, and Falconsi-Medical_summarisation, all fine-tuned on **eLife and PLOS datasets**. A specific fine-tuning technique known as **LoRA (Low-Rank Adaptation of Large Language Models)** along with **PEFT (Parameter Efficient Fine-tuning)** was employed to improve model performance while maintaining computational efficiency.

## 🎯 Objectives

- Develop resource-efficient biomedical text summarization models for lay audiences
- Compare performance across multiple state-of-the-art language models
- Implement advanced fine-tuning techniques (LoRA + PEFT) for optimal performance
- Evaluate models on relevance, readability, and factuality metrics
- Identify the most efficient model in terms of size, performance, and resource utilization
- Enable better public access to biomedical research findings

## 🏗️ Model Architecture & Approach

### Language Models Explored
- **T5-Base** - Text-to-Text Transfer Transformer (Base variant)
- **T5-Large** - Text-to-Text Transfer Transformer (Large variant)
- **FlanT5-Base** - Instruction-tuned T5 model
- **BioGPT** - Biomedical domain-specific GPT model
- **Phi-2** - Microsoft's efficient language model
- **Falconsi-Medical_summarisation** - Specialized medical summarization model

### Fine-tuning Techniques
- **LoRA (Low-Rank Adaptation)**: Efficient adaptation method that reduces trainable parameters
- **PEFT (Parameter Efficient Fine-tuning)**: Advanced technique for resource-efficient model training

### Datasets
- **eLife**: Open-access biomedical research articles
- **PLOS**: Public Library of Science biomedical publications

## 📁 Project Structure

```
lays-bio-summery/
├── README.md                           # Project documentation
├── Model_training(biolaysumm).ipynb    # Model training with LoRA/PEFT
├── Evaluation.ipynb                    # Comprehensive model evaluation
├── requirements.txt                    # Python dependencies
├── CONTRIBUTING.md                     # Contribution guidelines
└── LICENSE                            # MIT License
```

## 📚 Notebooks Description

### 1. Model_training(biolaysumm).ipynb
- **Purpose**: Training biomedical summarization models with advanced fine-tuning
- **Contains**: 
  - Data preprocessing for eLife and PLOS datasets
  - Implementation of multiple transformer architectures
  - LoRA and PEFT fine-tuning implementation
  - Hyperparameter optimization
  - Model checkpointing and saving
  - Comparative training across all 6 models

### 2. Evaluation.ipynb
- **Purpose**: Comprehensive model evaluation and comparative analysis
- **Contains**:
  - Multi-dimensional evaluation metrics
  - Relevance, readability, and factuality assessments
  - Statistical analysis and model comparisons
  - Performance visualization and insights
  - Resource efficiency analysis

## 🛠️ Technologies Used

- **Python**: Primary programming language
- **TensorFlow**: Deep learning framework
- **PyTorch**: Deep learning framework
- **Hugging Face Transformers**: Pre-trained model library
- **LoRA**: Low-Rank Adaptation technique
- **PEFT**: Parameter Efficient Fine-tuning library
- **Jupyter Notebooks**: Development environment
- **Natural Language Processing**: Advanced text processing

## 📊 Evaluation Metrics

### Relevance Assessment
- **ROUGE (1, 2, L)**: Measures overlap between generated and reference summaries
- **BERTScore**: Semantic similarity assessment using contextualized embeddings
- **Coverage**: Assessment of main point preservation

### Readability Analysis
- **Flesch-Kincaid Grade Level (FKGL)**: Measures text complexity and grade level
- **Dale-Chall Readability Score (DCRS)**: Evaluates ease of understanding for lay readers

### Factuality Verification
- **BARTScore**: Ensures accuracy and consistency with original articles
- **Factual consistency**: Verification against source material

## 🏆 Key Findings & Results

### Model Performance Outcomes
- **Fine-tuned BioGPT and Phi-2** models significantly improved across all three dimensions: relevance, readability, and factuality
- **BioGPT and Falconsi** outperformed T5 models, highlighting the significant benefits of biomedical domain pre-training
- **Flan T5 models** demonstrated better readability but showed poorer performance in relevance and factuality metrics
- **Smaller Flan T5 variant** surprisingly outperformed its larger counterpart

### 🥇 Champion Model: Phi-2
**Phi-2 emerged as the most efficient model** when evaluated comprehensively across:
- ✅ **Model Size**: Compact and resource-friendly
- ✅ **Performance**: Superior across all evaluation metrics
- ✅ **Resource Utilization**: Optimal computational efficiency
- ✅ **Cost-effectiveness**: Best performance-to-resource ratio

## 🚀 Getting Started

### Prerequisites

```bash
# Install required dependencies
pip install -r requirements.txt

# Additional packages for advanced features
pip install transformers[torch] datasets evaluate
pip install peft accelerate bitsandbytes
```

### Running the Project

1. **Clone the repository**:
   ```bash
   git clone https://github.com/sank29mane/lays-bio-summery.git
   cd lays-bio-summery
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Launch Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```

4. **Run the notebooks in sequence**:
   - First: `Model_training(biolaysumm).ipynb` - Train models with LoRA/PEFT
   - Then: `Evaluation.ipynb` - Evaluate and compare all models

## 🔬 Use Cases & Applications

- **Patient Education**: Convert medical research into patient-friendly summaries
- **Healthcare Communication**: Bridge gap between medical professionals and patients
- **Public Health Literacy**: Make biomedical research accessible to general public
- **Medical Journalism**: Support science writers and health journalists
- **Educational Resources**: Create teaching materials for health education
- **Policy Making**: Provide accessible summaries for health policy decisions

## 📈 Future Enhancements

- [ ] **Multi-language Support**: Extend to non-English biomedical literature
- [ ] **Real-time API**: Deploy as a web service for instant summarization
- [ ] **Domain Expansion**: Include clinical trials and pharmaceutical research
- [ ] **Interactive Interface**: Web-based tool for researchers and educators
- [ ] **Advanced Evaluation**: Include human evaluation studies
- [ ] **Integration**: Connect with PubMed and other biomedical databases
- [ ] **Mobile Application**: Develop mobile app for on-the-go access

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on:
- Code contributions
- Bug reports
- Feature requests
- Documentation improvements

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🏅 Research Impact

This work contributes to:
- **Democratizing Medical Knowledge**: Making research accessible to all
- **Advancing NLP in Healthcare**: Pushing boundaries of medical text processing
- **Resource-Efficient AI**: Demonstrating effective use of LoRA and PEFT
- **Evaluation Methodology**: Comprehensive framework for summarization assessment

## 👨‍💻 Author

**Sanket Mane** - [@sank29mane](https://github.com/sank29mane)

*Researcher in Biomedical NLP and Efficient Language Models*

## 📞 Contact

For questions, collaborations, or research discussions:
- GitHub Issues: [Create an issue](https://github.com/sank29mane/lays-bio-summery/issues)
- Research Inquiries: Through GitHub profile

## 📚 Citation

If you use this work in your research, please consider citing:

```bibtex
@misc{mane2024biolaysumm,
  title={Resource-Efficient Biomedical Lay Summarization using LoRA and PEFT},
  author={Mane, Sanket},
  year={2024},
  url={https://github.com/sank29mane/lays-bio-summery}
}
```

---

⭐ **Star this repository if you find it useful!** ⭐

*Last updated: June 2025*