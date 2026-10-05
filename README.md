Brain tumor diagnosis from magnetic resonance imaging (MRI) demands both
high classification accuracy and clinically interpretable predictions. Convolutional neural networks (CNNs) have demonstrated strong performance on this
task but inherently lack global context modelling due to their local receptive fields, while vanilla Vision Transformers (ViTs) trained from scratch on
small medical datasets suffer from data-efficiency problems. We present HViTDBSA, a Hierarchical Vision Transformer architecture that combines (i) a
pretrained ViT backbone for rich patch-level feature extraction, (ii) a transformer neck equipped with a novel Dual-Branch Spatial Attention (DBSA)
module that simultaneously models average-pooled and max-pooled channel
descriptors to produce a learned spatial gate, and (iii) a transformer-adapted
Layer-wise Relevance Propagation (LRP) explainability framework that
generates class-specific heatmaps from neck self-attention maps. To address the
well-documented distribution mismatch in the standard brain tumor MRI benchmark, we apply a stratified 70/15/15 train/validation/test split across the pooled
dataset. Two-phase training—frozen backbone followed by selective backbone
fine-tuning—yields a test accuracy of 92.4% and a macro-averaged F1-score
of 0.93 across four classes (glioma, meningioma, pituitary, no-tumor). Ablation
studies confirm that both DBSA and the correct data-split strategy are essential contributors to performance. LRP heatmaps demonstrate clinically coherent
attention to tumour boundaries, supporting deployability in a decision-support
context.
