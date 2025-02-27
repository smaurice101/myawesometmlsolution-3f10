[myawesometmlsolution-3f10] Details
============================

Generated On: 2025-02-27 15:25:59 UTC

TML Solution DAG Parameters' Details: User Chosen Parametets
----------------------------

STEP 1: Get TML Core Params: `tml_system_step_1_getparams_dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/myawesometmlsolution-3f10/tml_system_step_1_getparams_dag-myawesometmlsolution-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - solutionname
     - myawesometmlsolution-3f10
   * - solutiontitle
     - IoT Real-Time Monitoring Solution
   * - solutiondescription
     - This is an awesome real-time solution built by TSS
   * - brokerhost
     - 127.0.0.1
   * - brokerport
     - 9092
   * - cloudusername
     - None
   * - ingestdatamethod
     - LOCALFILE
 
STEP 2: Create Kafka Topics: `tml_system_step_2_kafka_createtopic_dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/myawesometmlsolution-3f10/tml_system_step_2_kafka_createtopic_dag-myawesometmlsolution-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - companyname
     - Otics
   * - myname
     - Sebastian
   * - myemail
     - Sebastian.Maurice
   * - mylocation
     - Toronto
   * - replication
     - 1
   * - numpartitions
     - 1
   * - enabletls
     - 1
   * - microserviceid
     - 
   * - raw_data_topic
     - iot-raw-data
   * - preprocess_data_topic
     - iot-preprocess,iot-preprocess2
   * - ml_data_topic
     - ml-data
   * - prediction_data_topic
     - prediction-data

STEP 3: `Produce to Kafka Topics <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/myawesometmlsolution-3f10/tml_read_LOCALFILE_step_3_kafka_producetotopic_dag-myawesometmlsolution-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - PRODUCETYPE
     - LOCALFILE
   * - TOPIC
     - iot-raw-data
   * - PORT
     - _39399
   * - IDENTIFIER
     - TML solution,/rawdatademo/IoTData.txt
   * - HTTPADDR
     - https://
   * - FROMHOST
     - ('seb', '127.0.1.1')
   * - TOHOST
     - 0.0.0.0
   * - CLIENTPORT
     - Not Applicable
   * - TSS_CLIENTPORT
     - Not Applicable
   * - TML_CLIENTPORT
     - Not Applicable
   * - docfolder
     - 
   * - doctopic
     - 
   * - chunks
     - 0
   * - docingestinterval
     - 0

STEP 4: Preprocesing Data: `tml-system-step-4-kafka-preprocess-dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/myawesometmlsolution-3f10/tml_system_step_4_kafka_preprocess_dag-myawesometmlsolution-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - raw_data_topic
     - iot-raw-data
   * - preprocess_data_topic
     - iot-preprocess,iot-preprocess2
   * - preprocessconditions
     - 
   * - delay
     - 70
   * - maxrows
     - 800
   * - array
     - 0
   * - saveasarray
     - 1
   * - topicid
     - -999
   * - rawdataoutput
     - 1
   * - asynctimeout
     - 120
   * - timedelay
     - 0
   * - preprocesstypes
     - anomprob,trend,avg
   * - pathtotmlattrs
     - --pathtotmlattrs--
   * - identifier
     - IoT device performance and failures
   * - jsoncriteria
     - uid=metadata.dsn,filter:allrecords~subtopics=metadata.property_name~values=datapoint.value~identifiers=metadata.display_name~datetime=datapoint.updated_at~msgid=datapoint.id~latlong=lat:long

STEP 4b: Preprocesing Data: `tml-system-step-4b-kafka-preprocess-dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/myawesometmlsolution-3f10/tml_system_step_4b_kafka_preprocess_dag-myawesometmlsolution-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - raw_data_topic
     - --raw_data_topic2--
   * - preprocess_data_topic
     - --preprocess_data_topic2--
   * - preprocessconditions
     - --preprocessconditions2--
   * - delay
     - --delay2--
   * - maxrows
     - --maxrows2--
   * - array
     - --array2--
   * - saveasarray
     - --saveasarray2--
   * - topicid
     - --topicid2--
   * - rawdataoutput
     - --rawdataoutput2--
   * - asynctimeout
     - --asynctimeout2--
   * - timedelay
     - --timedelay2--
   * - preprocesstypes
     - --preprocesstypes2--
   * - pathtotmlattrs
     - --pathtotmlattrs2--
   * - identifier
     - --identifier2--
   * - jsoncriteria
     - --jsoncriteria2--

STEP 4c: Preprocesing Data: `tml-system-step-4c-kafka-preprocess-dag  <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/myawesometmlsolution-3f10/tml_system_step_4c_kafka_preprocess_dag-myawesometmlsolution-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - raw_data_topic
     - --raw_data_topic3--
   * - preprocess_data_topic
     - --preprocess_data_topic3--
   * - delay
     - --delay3--
   * - maxrows
     - --maxrows3--
   * - array
     - --array3--
   * - saveasarray
     - --saveasarray3--
   * - topicid
     - --topicid3--
   * - rawdataoutput
     - --rawdataoutput3--
   * - asynctimeout
     - --asynctimeout3--
   * - timedelay
     - --timedelay3--
   * - searchterms
     - --rtmssearchterms--
   * - rtmsstream
     - --rtmsstream--
   * - identifier
     - --identifier3--
   * - rememberpastwindows
     - --rememberpastwindows--
   * - patternscorethreshold
     - --patternscorethreshold--

STEP 5: Entity Based Machine Learning : `tml-system-step-5-kafka-machine-learning-dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/myawesometmlsolution-3f10/tml_system_step_5_kafka_machine_learning_dag-myawesometmlsolution-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - preprocess_data_topic
     - iot-preprocess,iot-preprocess2
   * - ml_data_topic
     - ml-data
   * - modelruns
     - --modelruns--
   * - offset
     - -1
   * - islogistic
     - --islogistic--
   * - networktimeout
     - --networktimeout--
   * - modelsearchtuner
     - --modelsearchtuner--
   * - processlogic
     - --processlogic--
   * - dependentvariable
     - --dependentvariable--
   * - independentvariables
     - --independentvariables--
   * - rollbackoffsets
     - --rollbackoffsets--
   * - topicid
     - -999
   * - consumefrom
     - --consumefrom--
   * - fullpathtotrainingdata
     - --fullpathtotrainingdata--
   * - transformtype
     - --transformtype--
   * - sendcoefto
     - --sendcoefto--
   * - coeftoprocess
     - --coeftoprocess--
   * - coefsubtopicnames
     - --coefsubtopicnames--

STEP 6: Entity Based Predictions: `tml-system-step-6-kafka-predictions-dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/myawesometmlsolution-3f10/tml_system_step_6_kafka_predictions_dag-myawesometmlsolution-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - preprocess_data_topic
     - iot-preprocess,iot-preprocess2
   * - ml_prediction_topic
     - --ml_prediction_topic--
   * - streamstojoin
     - --streamstojoin--
   * - inputdata
     - --inputdata--
   * - consumefrom
     - --consumefrom2--
   * - offset
     - -1
   * - delay
     - 70
   * - usedeploy
     - --usedeploy--
   * - networktimeout
     - --networktimeout--
   * - maxrows
     - 800
   * - topicid
     - -999
   * - pathtoalgos
     - --pathtoalgos--

STEP 7: Real-Time Visualization: `tml-system-step-7-kafka-visualization-dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/myawesometmlsolution-3f10/tml_system_step_7_kafka_visualization_dag-myawesometmlsolution-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - vipervizport
     - 49689
   * - topic
     - iot-preprocess
   * - dashboardhtml
     - dashboard.html
   * - secure
     - 1
   * - offset
     - -1
   * - append
     - 0
   * - chip
     - amd64
   * - rollbackoffset
     - 400

STEP 8: `tml_system_step_8_deploy_solution_to_docker_dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/myawesometmlsolution-3f10/tml_system_step_8_deploy_solution_to_docker_dag-myawesometmlsolution-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^
.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - Docker Container
     - maadsdocker/myawesometmlsolution-3f10-amd64 (https://hub.docker.com/r/maadsdocker/myawesometmlsolution-3f10-amd64)
   * - Docker Run Command
     - docker run -d -p 45797:45797 -p 49513:49513 -p 57655:57655 \
          --env TSS=0 \
          --env SOLUTIONNAME=myawesometmlsolution-3f10 \
          --env SOLUTIONDAG=solution_preprocessing_dag-myawesometmlsolution-3f10 \
          --env GITUSERNAME=smaurice101  \
          --env GITREPOURL=https://github.com/smaurice101/raspberrypitss.git \
          --env SOLUTIONEXTERNALPORT=45797 \
          -v /var/run/docker.sock:/var/run/docker.sock:z \
          -v /your_localmachine/foldername:/rawdata:z \
          --env CHIP=amd64 \
          --env SOLUTIONAIRFLOWPORT=49513 \
          --env SOLUTIONVIPERVIZPORT=57655 \
          --env DOCKERUSERNAME='maadsdocker' \
          --env EXTERNALPORT=39399 \
          --env KAFKACLOUDUSERNAME='MUHRHBPKJYPROKBX' \
          --env VIPERVIZPORT=49689 \
          --env MQTTUSERNAME='smaurice' \
          --env AIRFLOWPORT=9000 \
          --env MQTTPASSWORD='<Enter mqtt password>' \
          --env KAFKACLOUDPASSWORD='<Enter API secret>' \
          --env GITPASSWORD='<Enter Github Password>' \
          --env READTHEDOCS='<Enter Readthedocs token>' \
          maadsdocker/myawesometmlsolution-3f10-amd64

STEP 9: `tml_system_step_9_privategpt_qdrant_dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/myawesometmlsolution-3f10/tml_system_step_9_privategpt_qdrant_dag-myawesometmlsolution-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^
.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - PrivateGPT Container
     - --pgptcontainername--
   * - PrivateGPT Run Command
     - --privategptrun--
   * - Qdrant Container
     - --qdrantcontainer--
   * - Qdrant Run Command
     - --qdrantrun--
   * - Consumefrom
     - --consumefrom--
   * - pgpt_data_topic
     - --pgpt_data_topic--
   * - offset
     - -1
   * - rollbackoffset
     - 400
   * - topicid
     - -999
   * - enabletls
     - 1
   * - partition
     - --partition--
   * - prompt
     - --prompt--
   * - context
     - --context--
   * - jsonkeytogather
     - --jsonkeytogather--
   * - keyattribute
     - --keyattribute--
   * - keyprocesstype
     - --keyprocesstype--
   * - vectordbcollectionname
     - --vectordbcollectionname--
   * - concurrency
     - --concurrency--
   * - CUDA_VISIBLE_DEVICES
     - --cuda--
   * - pgpthost
     - --pgpthost--
   * - pgptport
     - --pgptport--
   * - hyperbatch
     - --hyperbatch--
   * - docfolder
     - --docfolder--
   * - docfolderingestinterval
     - --docfolderingestinterval--
   * - useidentifierinprompt
     - --useidentifierinprompt--
   * - searchterms
     - --searchterms--
   * - streamall
     - --streamall--
   * - temperature
     - --temperature--
   * - vectorsearchtype
     - --vectorsearchtype--
   * - llm
     - --llmmodel--
   * - embedding
     - --embedding--
   * - vectorsize
     - --vectorsize--

STEP 10: `tml_system_step_10_documentation_dag <https://github.com/smaurice101/raspberrypitss/tree/main/tml-airflow/dags/tml-solutions/myawesometmlsolution-3f10/tml_system_step_10_documentation_dag-myawesometmlsolution-3f10.py>`_
^^^^^^^^^^^^^^^^^^^^^
.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - Solution Documentation URL
     - https://myawesometmlsolution-3f10.readthedocs.io
