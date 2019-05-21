## Pegasus Install and setup


## Hardware and Software
iMac with Intel i7 Kaby Lake with 32 GB RAM, 1TB fusion HD, running 10.13 High Sierra

## Steps taken
* Installed homebrew, then attempted *brew install pegasus htcondor* [as described](https://pegasus.isi.edu/downloads/)
  * This step was ~unsuccessful after multiple attempts~ ultimately successful
  * The install will appear to hang at several steps, and will take a long time.
  
          ==> Caveats
          In order to run workflows you will also need to install HTCondor. You
          can either do this manually, or you can install the htcondor formula.
          ==> Summary
          🍺  /usr/local/Cellar/pegasus/4.9.1: 2,884 files, 83.8MB, built in 18 minutes 58 seconds
  
  * You should install HTCondor **first** to prevent numerous errors in the install process.
* Downloaded and installed [compiled binaries for Mac OSX](https://pegasus.isi.edu/downloads/)
  * This step was successful
  
        jrcaskey$ cd pegasus-4.9.1/
        jrcaskey$ ls
        LICENSE		README.md	RELEASE_NOTES	bin		etc		lib		share		stamp
        jrcaskey$ cd bin/
        jrcaskey$ ls
        pegasus-analyzer		pegasus-exitcode		pegasus-metadata		pegasus-service
        pegasus-aws-batch		pegasus-globus-online		pegasus-monitord		pegasus-statistics
        pegasus-cluster			pegasus-globus-online-init	pegasus-plan			pegasus-status
        pegasus-config			pegasus-graphviz		pegasus-plots			pegasus-submit-dag
        pegasus-configure-glite		pegasus-halt			pegasus-rc-client		pegasus-submitdir
        pegasus-dagman			pegasus-init			pegasus-remove			pegasus-tc-client
        pegasus-dax-validator		pegasus-integrity		pegasus-run			pegasus-tc-converter
        pegasus-db-admin		pegasus-keg			pegasus-s3			pegasus-transfer
        pegasus-em			pegasus-kickstart		pegasus-sc-converter		pegasus-version
        jrcaskey$ export "PATH=$PATH:${PWD}"
        jrcaskey$ pegasus-version 
        4.9.1
        jrcaskey$ pegasus-status 
        (no matching jobs found in Condor Q)

* Successfully repeated the steps to download the binary for Centos7 on the CHTC submit node
