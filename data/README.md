## Data
Contains the replication data (input-output pairs) and auxiliary data used in the paper. The files use the epoch timestamp as their identifier. 
- train-test-val: This folder contains the 16776 input-output pairs used to develop NOIRE-Net
  1. ionograms: contains the input ionograms in (.png) format with dimensions 310x310x1
  2. parameters: contains the output parameters in (.par) format with the manual labeling and scaling information
- test-multi-human: This folder contains the 652 ionograms that were labeled and scaled by multiple human experts. The files use the epoch timestamp as their identifier along with the human initials (for the output .par files).
  1. ionograms: contains the input ionograms in (.png) format with dimensions 310x310x1
  2. parameters: contains the output parameters in (.par) format with the manual labeling and scaling information.
  3. NOIRE-Net-analyzed: contains classified and scaled ionograms in (.png) format, automatically processed by NOIRE-Net
  4. NOIRE-Net-analyzed-movie.mp4: is a movie of the .png images in the subfolder "NOIRE-Net-analyzed"
- test-24-hours: This folder contains the 1404 consecutive ionograms that were manually labeled and scaled. This folder also contains the auxiliary images from the all-sky camera in Kiruna, operated by the Swedish Institute of Space Physics.
  1. ionograms: contains the input ionograms in (.png) format with dimensions 310x310x1
  2. parameters: contains the output parameters in (.par) format with the manual labeling and scaling information
  3. NOIRE-Net-analyzed: contains classified and scaled ionograms in (.png) format, automatically processed by NOIRE-Net
  4. IRF-all-sky-images: contains the all-sky images acquired by the camera in Kiruna. See IRF-license.pdf for the license agreement before using this data.
  5. IRF-license.pdf: License agreement for data obtained from Kiruna Atmospheric and Geophysical Observatory at Swedish Institute of Space Physics
  6. NOIRE-Net-analyzed-movie.mp4: is a movie of the .png images in the subfolder "NOIRE-Net-analyzed"
