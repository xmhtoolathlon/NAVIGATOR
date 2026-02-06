# NAVIGATOR Development Repository

> 🚧 **Development Branch** - This is the main development repository for NAVIGATOR (Neural Architecture Visualizer and Inspector for Graph-Augmented Tensor Operations Research)

## About NAVIGATOR

NAVIGATOR is a deep learning visualization framework that helps researchers understand and debug neural network architectures. This repository contains the core implementation and development work.

## 🔧 Development Status

This repository is under active development. Many features are currently being implemented or need attention.

## 🚀 Quick Start

⚠️ **Note**: This development version has incomplete implementations. Many features are marked as FIXME and need to be addressed before production use.

```bash
# Clone the repository
git clone <repository-url>
cd NAVIGATOR

# Install dependencies  
pip install -r requirements.txt

# Note: Some functionality is incomplete - check FIXME list below for details
```

## 📁 Repository Structure

```
NAVIGATOR/
├── navigator/             # Core framework
│   ├── visualizer/        # Visualization components (⚠️ Performance issues)
│   ├── inspector/         # Model inspection tools (⚠️ Some features incomplete)
│   └── ...
├── data/                  # Sample data and scripts
├── tests/                 # Test utilities
├── benchmarks/            # Performance benchmarks
└── README.md              # This file
```

## ⚠️ Development Notes

- This is a **development version** with incomplete implementations
- Many functions contain FIXME markers indicating issues to address
- Visualization backends need optimization
- Memory management needs attention


### 🔴 High Priority FIXMEs

- **Visualization**: Memory leaks in rendering pipeline
- **Inspector**: Slow performance on large models  
- **Data Loading**: Race conditions in async loaders
- **Graph Operations**: Numerical stability issues

### 🔧 Complete FIXME List

- [ ] **navigator/core/graph_ops.py:102** - Multi-head attention doesn't handle mask properly
- [ ] **navigator/core/graph_ops.py:155** - Division by zero not handled
- [ ] **navigator/inspector/layer_analyzer.py:58** - Incorrect gradient calculation
- [ ] **navigator/inspector/model_parser.py:24** - Slow parsing for large models
- [ ] **navigator/inspector/model_parser.py:33** - TensorFlow graph parsing misses control dependencies
- [ ] **navigator/utils/data_loader.py:33** - Race condition in async loading
- [ ] **navigator/utils/data_loader.py:50** - Cache eviction policy not implemented
- [ ] **navigator/visualizer/canvas.py:15** - Canvas initialization should validate dimensions
- [ ] **navigator/visualizer/canvas.py:132** - Canvas resize causes flicker
- [ ] **navigator/visualizer/renderer.py:71** - Inefficient texture loading
- [ ] **navigator/visualizer/renderer.py:84** - Texture retrieval should use lazy loading

## 📝 Contributing

Please check the FIXME list above and help us address these issues!

## 📄 License

MIT License
