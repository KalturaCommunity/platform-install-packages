**[Track milestones progress](https://github.com/kaltura/platform-install-packages/issues/milestones)**.

#### 2014-03-02:

**Install Packages Updates**

+ Stable version is now 9.12.0, Testing version is 9.13.0
+ Migration path between 9.11.0, 9.12.0 was tested by several users and found stable. 
+ 9.13.0 passed all CI tests.
+ Added [script to configure NFS client side](https://github.com/kaltura/platform-install-packages/blob/master/RPM/scripts/postinst/kaltura-nfs-client-config.sh)
+ Added new [FAQ section for commonly asked questions help](https://github.com/kaltura/platform-install-packages/blob/master/doc/kaltura-packages-faq.md)
+ All CI tests were wrapped as local post-install sanity tests kit for users to run after installation verifying their install. [See sanity-test kit screenshot](https://raw.githubusercontent.com/kaltura/platform-install-packages/master/doc/post-inst-sanity-tests-output.png).
+ Install scripts output is now presented in colors to make messages easier to read and understand [See install output screenshot](https://raw.githubusercontent.com/kaltura/platform-install-packages/master/doc/rpm_install_console_colors.png)
+ Missing KMC documentation and bulk upload samples were added.
+ Widgets upgrade and cleanup completed - updated to use new github links rather than old SVN. And added CI test to check for existence of all widget swfs that are referenced by uiConfs.
+ Discovered missing old uiConf files - list is being checked against core to verify cleanup.
+ [@blackyboy](https://github.com/blackyboy) contributed [Configuring Drop Folder, Amazon S3 Remote Storage, Amazon CloudFront CDN, and CloudFront RTMP](https://github.com/kaltura/platform-install-packages/issues/61#issuecomment-38462301), will be added document shortly, and inspired the idea for [Create Post-Inst Scripts for CDN Configurations](https://github.com/kaltura/platform-install-packages/issues/80).
+ [@DBezemer](https://github.com/DBezemer) tested and updated [Deploying Kaltura Clusters guide](https://github.com/kaltura/platform-install-packages/blob/master/doc/rpm-cluster-deployment-instructions.md) to be even more "fool-proof".
+ [Deploy Local Repository for Offline Install](https://github.com/kaltura/platform-install-packages/blob/master/doc/deploy-local-rpm-repo-offline-install.md) guide was added to support environments that are not connected to the internet. 

**Continuous Integration Updates**

+ Nightly sanity occurs each night on EC2, logs entries to SQLite and sends a CSV report by email. See [example CSV Report](https://github.com/kaltura/platform-install-packages/blob/master/doc/ci_example_csv_report.csv)
+ Erected a cluster to test on ESXi for testing, integration in progress
+ Currently working on integration using [The Foremen](http://www.theforeman.org/) to support wider range of deployment options.

#### 2014-03-02:

+ Alpha tests have all passes sucessfully. 
+ Further Cluster and Chef deployment guides were tested on AWS.
+ Red5 package fully tested (both webcam and FMLE).
+ QA Analytics reporting events deployed, users can now opt-in to send repoting events for system stability reports and deployment issue assistance.
+ IX-9.11.0 was released and tested.
+ Specifications and definition for the [Kaltura Platform Packages CI Project](https://github.com/kaltura/platform-continuous-integration) were created.
+ Entered [Phase D - Public Beta, and Continuous Integration System](http://kaltura.github.io/platform-install-packages/#phase-d).
   
#### 2014-02-17:
Cluster install passed successfully, Chef scripts created, many tests passed and bugs crushed.

+ Red5 package was added to kaltura-server and KCW webcam tested.
+ monit package was fully tested.
+ [Chef scripts were created](https://github.com/kaltura/platform-install-packages/tree/master/RPM/chef-repo) - now you can deploy a complete Kaltura cluster with the click of a button!
+ 18 packaging bugs crushed (thanks to [@DBezemer](https://github.com/DBezemer), [@mobcdi](https://github.com/mobcdi) and [@doubleshot](https://github.com/doubleshot))!
+ [7 fix patches submitted to core](https://github.com/kaltura/server/pull/871) by [@jessp01](https://github.com/jessp01).
+ [1 Admin Console view](https://github.com/kaltura/server/pull/872 ) contributed by  [@DBezemer](https://github.com/DBezemer).
+ New documents published: 1) [cluster deployment document](http://bit.ly/kipp-cluster-yum), 2) [configuring platform monitors](http://bit.ly/kipp-monitoring).
+ Local Drop folders passed tests.
+ Upgrade to 9.10 will be skipped. As 9.11 planned for release next week, nightly will progress straight to 9.11.
+ [Project announced on a blog post!](http://blog.kaltura.org/introducing-kipp-kaltura-install-made-simple)

#### 2014-02-03:
Single server installed passes successfully, including sanity of the following features:   

+ Partner creation
+ Content upload of various kinds
+ Convert
+ Thumbnail creation
+ Entry investigation
+ Entry embed
+ Partner config options via Admin Console
+ API v3 tests for the PHP5 and Java client libs
+ Cluster install is in final stages of testing and expected to finish sanity today
+ Monitoring suite is under way and is also expected to be released for testing today
+ Entered [Phase C.2 - Alpha Repositories & Testing](http://kaltura.github.io/platform-install-packages/#phase-c2)
      
#### 2014-01-27:
We are thrilled to share that we've reached public alpha testing phase of the RPM packages.
If you're running a RedHat based distro and would like to test, please review the RPM installation steps.
