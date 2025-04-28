# Flood Detection Using Satellite Imagery (U-Net Model)  

## 📌 **Key Points**  

### **Project Overview**  
- **Goal**: Detect flooded areas in satellite images using a **U-Net deep learning model**.  
- **Input**: Multi-spectral satellite images (`.tif`).  
- **Output**: Binary segmentation masks (flooded vs. non-flooded).  

### **Model & Training**  
- **Architecture**: U-Net with encoder-decoder + skip connections.  
- **Training**:  
  - Optimizer: **Adam** (LR=0.0001)  
  - Loss: **Binary cross-entropy**  
  - Batch size: **16**  
  - Early stopping (patience=5)  
- **Results**:  
  - **Accuracy**: **77.74%**  
  - **IoU**: **0.0** (needs improvement)  

### **Challenges & Next Steps**  
- **Limitations**:  
  - Small dataset (100 samples used for quick testing).  
  - Poor IoU indicates model may need tuning.  
- **Improvements**:  
  - More training data & augmentation.  
  - Hyperparameter optimization.  
  - Experiment with different architectures (e.g., DeepLab, ResUNet).  

### **How to Use**  
```python
model, history = train_model()  
evaluate_model(model, history)  
```

### **Requirements**  
```bash
pip install tensorflow rasterio numpy matplotlib scikit-learn  
```  

🔹 **Note**: The model is a baseline—further tuning needed for better segmentation. 🚀
