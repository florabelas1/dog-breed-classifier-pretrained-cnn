# Dog Breed Classifier Using Pre-trained CNN Models

**AWS AI Programming with Python Nanodegree - Final Project**

Image classification project using pre-trained Convolutional Neural Networks 
(VGG, AlexNet, ResNet) to identify dog breeds from images.

---

## 🎯 Project Objective

Develop a command-line application that:
1. Identifies whether an image contains a dog
2. Classifies the dog breed if present
3. Compares performance across three pre-trained CNN architectures
4. Evaluates accuracy and computational efficiency

---

## 🧠 Pre-trained Models Tested

| Model | Architecture | Performance | Speed |
|-------|--------------|-------------|-------|
| **VGG** | 16 layers | Highest accuracy | Slowest |
| **AlexNet** | 8 layers | Good balance | Fastest |
| **ResNet** | 50 layers | High accuracy | Moderate |

---

## 📊 Key Results

### Model Comparison on Pet Images Dataset

- **VGG-16**: Best overall performance for dog breed classification
- **AlexNet**: Fastest execution with acceptable accuracy
- **ResNet-50**: Good balance between accuracy and speed

### Classification Tasks
1. ✅ Dog vs Not-Dog identification
2. ✅ Breed classification for correct dog images
3. ✅ Handling of non-dog images (cats, wildlife, objects)

---

## 🛠️ Technologies

- **Python 3.x**
- **PyTorch** (torchvision pre-trained models)
- **PIL** (Image processing)
- **argparse** (Command-line interface)

---

## 📁 Project Structure

```
├── check_images.py              # Main application script
├── get_pet_labels.py            # Extract labels from filenames
├── classify_images.py           # Run CNN classification
├── adjust_results4_isadog.py    # Validate dog classifications
├── calculates_results_stats.py  # Compute performance metrics
├── print_results.py             # Display results
├── classifier.py                # CNN model wrapper
├── get_input_args.py            # Command-line argument parsing
├── dognames.txt                 # List of valid dog breeds
├── pet_images/                  # Sample pet images for testing
├── uploaded_images/             # Custom test images
├── run_models_batch.sh          # Batch execution script
└── *_pet-images.txt             # Results for each model
```

---

## 🚀 How to Run

### Basic Usage

```bash
python check_images.py --dir pet_images/ --arch vgg --dogfile dognames.txt
```

### Arguments

- `--dir`: Directory containing images (default: `pet_images/`)
- `--arch`: CNN model architecture (`vgg`, `alexnet`, `resnet`)
- `--dogfile`: Text file with dog breed names (default: `dognames.txt`)

### Batch Testing

```bash
sh run_models_batch.sh
```

Runs all three models and saves results to text files.

---

## 📈 Performance Metrics

The application calculates:

- **Accuracy**: Overall correct classifications
- **Precision**: True positives / (True positives + False positives)
- **Recall**: True positives / (True positives + False negatives)
- **Execution Time**: Model inference speed

### Sample Output

```
Model Architecture: VGG
Number of Images: 40
Number of Dog Images: 30
Number of "Not-a" Dog Images: 10

Percentage Correct Dogs: 100.0%
Percentage Correct Breed: 93.3%
Percentage Correct "Not-a" Dog: 100.0%
```

---

## 🎓 Project Context

**Program**: AWS AI Programming with Python Nanodegree  
**Provider**: Udacity  
**Focus**: Image Classification, Transfer Learning, Model Evaluation  
**Year**: 2024

### Learning Objectives Achieved

✅ Implement command-line applications in Python  
✅ Use pre-trained CNN models for transfer learning  
✅ Compare model architectures on classification tasks  
✅ Optimize for accuracy vs computational efficiency  
✅ Handle edge cases (non-dog images, ambiguous breeds)

---

## 🔍 Key Insights

1. **Transfer Learning Works**: Pre-trained models on ImageNet generalize 
   well to dog breed classification without additional training

2. **Architecture Trade-offs**: VGG provides highest accuracy but at the 
   cost of inference speed; AlexNet offers best speed/accuracy balance

3. **Label Quality Matters**: Filename-based labeling requires careful 
   preprocessing and validation

4. **Real-World Challenges**: Models can confuse similar-looking breeds 
   (e.g., different types of terriers)

---

## 📝 Sample Results

### Pet Images Dataset (40 images)
- **Dogs correctly identified**: 100%
- **Breeds correctly classified**: 90-100% (depending on model)
- **Non-dogs correctly rejected**: 100%

### Uploaded Images Dataset (custom)
- Tested with challenging cases (mixed breeds, unusual angles)
- Validated model robustness on unseen data

---

## 🔗 Resources

- [PyTorch Pre-trained Models](https://pytorch.org/vision/stable/models.html)
- [ImageNet Classes](http://www.image-net.org/)
- [AWS AI Programming Nanodegree](https://www.udacity.com/course/ai-programming-python-nanodegree--nd089)

---

## 🎯 Future Enhancements

- [ ] Add web interface for image upload
- [ ] Implement fine-tuning on specific dog breed dataset
- [ ] Support for video classification
- [ ] Real-time breed detection with webcam
- [ ] Mobile app deployment

---

*AWS AI Programming with Python Nanodegree - 2024*
