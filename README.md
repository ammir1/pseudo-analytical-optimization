# **Code for: \[GPU acceleration and memory optimization of acoustic wave equation using pseudo-analytical method\]**

This repository contains the code to reproduce the figures and results presented in the paper: "\[Your Publication Title\]" by \[Your Name(s)\].

## **Repository Structure**

The repository is organized as follows:

.  
├── LICENSE  
├── README.md  
├── requirements.txt  
├── src/  
│   ├── compute.cu  
│   └── utils.py  
├── figures/  
│   ├── figure1/  
│   │   ├── run\_figure1.sh  
│   │   ├── create\_args.py  
│   │   ├── plot\_results.py  
│   │   └── output/  
│   └── figure2/  
│       ├── ...  
├── data/  
│   └── (Your data files)  
└── results/  
    └── (Raw results from experiments)

* **src/**: Contains the core CUDA (.cu) and Python utility (.py) files used across different experiments.  
* **figures/**: Contains subdirectories for each figure in the paper. Each subdirectory has scripts to reproduce that specific figure.  
* **data/**: Should contain any necessary data files to run the code.  
* **results/**: Is the default location for the raw output of the scripts.  
* **requirements.txt**: A list of all Python packages required to run the code.  
* **LICENSE**: The license for the code.

## **Installation**

1. **Clone the repository:**  
   git clone \[https://github.com/your-username/your-repo-name.git\](https://github.com/your-username/your-repo-name.git)  
   cd your-repo-name

2. **Create a virtual environment (recommended):**  
   python \-m venv venv  
   source venv/bin/activate  \# On Windows use \`venv\\Scripts\\activate\`

3. **Install the required Python packages:**  
   pip install \-r requirements.txt

4. Compile the CUDA code:  
   You will need the CUDA toolkit installed. You can compile the .cu file using nvcc, the NVIDIA CUDA Compiler.  
   nvcc src/compute.cu \-o src/compute

## **Reproducing the Figures**

To reproduce a specific figure, navigate to its directory and run the corresponding shell script. For example, to reproduce Figure 1:

cd figures/figure1  
bash run\_figure1.sh

This script will:

1. Run create\_args.py to generate the necessary input/argument files.  
2. Execute the compiled CUDA code (src/compute).  
3. Run plot\_results.py to generate the figure from the results.

The final plot will be saved in the figures/figure1/output/ directory.

## **Citation**

If you use this code in your research, please cite our paper:

\[Your BibTeX citation here\]  
