# 📝 Medical Thesis LaTeX Files

Welcome to the repository containing the LaTeX source files for my **Medical Thesis** in hematology entitled **Prognostic Impact of Machine Learning-Predicted Minimal Residual Disease for Autologous Stem Cell Transplant Eligible Myeloma Patients**, written as part of my medical studies at University of Burgundy. These files are structured to facilitate editing, compilation, and customization of the final thesis document. 🩺📚

This is a slightly modified version of [Bashimao's](https://github.com/bashimao/ltu-thesis) La Trobe latex template based on the classicthesis thesis template by [André Miede](https://bitbucket.org/amiede/classicthesis).
I've made slight changes so that the margins meet the requirements of my medicine school. I've changed the language to French et add miniTOCs. I've also added an acronym page and appendices.

## 📂 Repository Structure

- **`thesis.tex`**: The main LaTeX file that compiles the entire thesis.
- **`text/`**: Directory containing individual `.tex` files for each chapter. 📄
- **`figures/`**: Directory containing images and figures used in the thesis. 🖼️
- **`tables/`**: Directory containing tables used in the thesis. 🖼️
- **`library.bib`**: The BibTeX file containing references. 📚

## 🚀 How to Compile

To compile the thesis document, you can use a local LaTeX environment or an online LaTeX editor like [Overleaf](https://www.overleaf.com/). 

### Using Overleaf
1. Go to [Overleaf](https://www.overleaf.com/) and create a new project.
2. Upload all the files from this repository to the Overleaf project.
3. Overleaf will automatically compile the `thesis.tex` file and generate a PDF.

### Using a Local Environment
1. Clone the repository:
    ```bash
    git clone https://github.com/haematool/MDthesis.git
    cd MDthesis
    ```

2. Compile the `thesis.tex` file with:
    ```bash
    pdflatex thesis.tex
    bibtex thesis
    pdflatex thesis.tex
    pdflatex thesis.tex
    ```

This will generate the `thesis.pdf` document containing your complete thesis. 🎉

## 🔧 Customization

- ✏️ You can modify individual chapters in the `text/` directory.
- 🖼️ Figures  can be added to the `images/` directory and included in the thesis using standard LaTeX commands.
- 📚 The bibliography is managed with BibTeX in the `library.bib` file. Add new references following the BibTeX format and compile with `bibtex`.

## 🚧 Future Work

I will continue to update this repository as the thesis progresses. If you notice any issues or have suggestions, feel free to open an issue or submit a pull request. 💡

## ⚖️ License

This repository is licensed under the [MIT License](LICENSE), meaning you are free to use the structure, but the content of the thesis itself is proprietary. 📜

## 📬 Contact

For any questions or issues related to the thesis, please contact me via email at [emmanuelsleiman@gmail.com]. 📧
