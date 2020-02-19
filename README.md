# reproducibility-tutorial    1  cd /scratch
    2  git clone git@github.com:kcarini/reproducibility-tutorial.git
    3  git clone https://github.com/kcarini/reproducibility-tutorial.git
    4  wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
    5  bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda
    6  ln -s /opt/conda/pkgs/*/bin/* /bin
    7  ln -s /opt/conda/pkgs/*/lib/* /usr/lib
    8  /opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3
    9  /opt/conda/bin/conda install -c conda-forge -y nodejs=10.13.0
   10  /opt/conda/bin/pip install bash_kernel
   11  /opt/conda/bin/pip install ipykernel
   12  /opt/conda/bin/python3 -m bash_kernel.install
   13  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
   14  /opt/conda/bin/conda search -c bioconda snakemake
   15  /opt/conda/bin/conda install -c bioconda -c conda-forge -y snakemake=5.8.1
   16  ln -s /opt/conda/bin/* /bin
   17  ln -s /opt/conda/lib/* /usr/lib
   18  snakemake --version
   19  sudo apt-get update
   20  sudo apt-get install -y apt-transport-https ca-certificates curl gnupg-agent software-properties-common
   21  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
   22  sudo add-apt-repository  "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
 $(lsb_release -cs) \
 stable"
   23  sudo apt-get update
   24  sudo apt-get install -y docker-ce docker-ce-cli containerd.io
   25  docker run hello-world
   26  cd /scratch/reproducibility-tutorial/
   27  history >>README.md
