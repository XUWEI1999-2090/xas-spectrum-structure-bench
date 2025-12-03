# XAS Spectrum–Structure Benchmark

This project provides structured and AI-ready XAS (X-ray Absorption Spectroscopy) datasets along with processed and visualization files.

### Data Processing Workflow

1. **Raw Data**: All experimental spectra are sourced from [XASLIB](https://docs.xrayabsorption.org/xaslib/), stored in the `raw` folder (total 215 spectra). We acknowledge:  
   > "At this point, if you wish to cite the collection as a whole, simply use the URL https://xaslib.xrayabsorption.org and reference the work as belonging to the International X-ray Absorption Society. We will explore generating a DOI for the collection as a whole."

2. **Processing**: Background subtraction is applied using the `mbk` module of the [Larch Python library](https://github.com/LMGuo/larch), with results stored in the `processed` folder.

3. **Structure Labeling**: All samples have known chemical formulas, enabling derivation of local structure information such as central atom, oxidation state, and coordination number. This metadata is stored in `x_os_cn.csv`.

4. **AI-Ready Dataset**:  
   - `ai_ready_data.csv` contains spectrum–structure pairs.  
   - To standardize input dimensions while preserving spectral shape and energy range, all spectra are resampled to 500 points, resulting in `resampled_ai_ready_data.csv`.

5. **Benchmark Updates**: This benchmark will continue to expand, targeting ~4,000 spectrum–structure pairs in the final release.

### Acknowledgments

We sincerely thank Prof. Yang Bo, Prof. Huai Ping, Mentor. Lei Lei, and others for their guidance. This work was supported by the National Key Research and Development Program of China (2022YFA1503804) and the National Natural Science Foundation of China (22322302). We also appreciate the encouragement from the NeurIPS 2025 AI4Science Workshop reviewers.
