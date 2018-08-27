swagger: "2.0"
x-collection-name: Kaltura
x-complete: 1
info:
  title: Kaltura VPaaS
  description: building-video-experiences-consists-of-ingesting-media-files-playing-back-videos-and-reviewing-usage-and-engagement-analytics--in-between-there-is-a-world-of-nuances-required-for-your-unique-usecase-and-application--kaltura-vpaas-is-built-on-the-principles-of-atomic-services-sdks-and-tools-that-allow-you-full-control-and-flexibility-over-every-element-and-process-in-your-medias-life-cycle-
  version: 3.3.0
host: www.kaltura.com
basePath: /api_v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /service/batchcontrol/action/configLoaded:
    get:
      summary: Get Service Batchcontrol Action Configloaded
      description: batch configLoaded action saves the configuration as loaded by
        a remote scheduler
      operationId: batchcontrol.configLoaded
      x-api-path-slug: servicebatchcontrolactionconfigloaded-get
      parameters:
      - in: query
        name: configParam
        description: The parameter that was loaded
      - in: query
        name: configParamPart
        description: The parameter part that was loaded
      - in: query
        name: configValue
        description: The value that was loaded
      - in: query
        name: No Name
      - in: query
        name: scheduler[configs]
      - in: query
        name: scheduler[configuredId]
        description: The id as configured in the batch config
      - in: query
        name: scheduler[host]
        description: The host name
      - in: query
        name: scheduler[name]
        description: The scheduler name
      - in: query
        name: scheduler[statuses]
      - in: query
        name: scheduler[workers]
      - in: query
        name: workerConfigId
        description: The id of the job that the configuration refers to, not mandatory
          if the configuration refers to the scheduler
      - in: query
        name: workerName
        description: The name of the job that the configuration refers to, not mandatory
          if the configuration refers to the scheduler
      responses:
        200:
          description: OK
      tags:
      - Service
      - Batchcontrol
      - Action
      - ConfigLoaded
  /service/batchcontrol/action/getCommand:
    get:
      summary: Get Service Batchcontrol Action Getcommand
      description: batch getCommand action returns the command with its current status
      operationId: batchcontrol.getCommand
      x-api-path-slug: servicebatchcontrolactiongetcommand-get
      parameters:
      - in: query
        name: commandId
        description: The id of the command
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Service
      - Batchcontrol
      - Action
      - GetCommand
  /service/batchcontrol/action/getFullStatus:
    get:
      summary: Get Service Batchcontrol Action Getfullstatus
      description: batch getFullStatus action returns the status of all schedulers
        and queues
      operationId: batchcontrol.getFullStatus
      x-api-path-slug: servicebatchcontrolactiongetfullstatus-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Service
      - Batchcontrol
      - Action
      - GetFullStatus
  /service/batchcontrol/action/kill:
    get:
      summary: Get Service Batchcontrol Action Kill
      description: batch kill action forces stop og a batch on a remote scheduler
      operationId: batchcontrol.kill
      x-api-path-slug: servicebatchcontrolactionkill-get
      parameters:
      - in: query
        name: adminId
        description: The id of the admin that called the stop
      - in: query
        name: batchIndex
        description: The index of the batch job process to be stopped
      - in: query
        name: cause
        description: The reason it was stopped
      - in: query
        name: No Name
      - in: query
        name: workerId
        description: The id of the job to be stopped
      responses:
        200:
          description: OK
      tags:
      - Service
      - Batchcontrol
      - Action
      - Kill
  /service/batchcontrol/action/listCommands:
    get:
      summary: Get Service Batchcontrol Action Listcommands
      description: list batch control commands
      operationId: batchcontrol.listCommands
      x-api-path-slug: servicebatchcontrolactionlistcommands-get
      parameters:
      - in: query
        name: filter[advancedSearch][attribute]
        description: 'Enum Type: `KalturaBaseEntryCompareAttribute`'
      - in: query
        name: filter[advancedSearch][categoriesMatchOr]
      - in: query
        name: filter[advancedSearch][categoryEntryStatusIn]
      - in: query
        name: filter[advancedSearch][categoryIdEqual]
      - in: query
        name: filter[advancedSearch][comparison]
        description: 'Enum Type: `KalturaSearchConditionComparison`'
      - in: query
        name: filter[advancedSearch][contentLike]
      - in: query
        name: filter[advancedSearch][contentMultiLikeAnd]
      - in: query
        name: filter[advancedSearch][contentMultiLikeOr]
      - in: query
        name: filter[advancedSearch][cuePointsFreeText]
      - in: query
        name: filter[advancedSearch][cuePointSubTypeEqual]
      - in: query
        name: filter[advancedSearch][cuePointTypeIn]
      - in: query
        name: filter[advancedSearch][depthGreaterThanEqual]
      - in: query
        name: filter[advancedSearch][distributionProfileId]
      - in: query
        name: filter[advancedSearch][distributionSunStatus]
        description: 'Enum Type: `KalturaEntryDistributionSunStatus`'
      - in: query
        name: filter[advancedSearch][entryDistributionFlag]
        description: 'Enum Type: `KalturaEntryDistributionFlag`'
      - in: query
        name: filter[advancedSearch][entryDistributionStatus]
        description: 'Enum Type: `KalturaEntryDistributionStatus`'
      - in: query
        name: filter[advancedSearch][entryDistributionValidationErrors]
        description: Comma seperated validation error types
      - in: query
        name: filter[advancedSearch][extendedStatusEqual]
        description: 'Enum Type: `KalturaUserEntryExtendedStatus`'
      - in: query
        name: filter[advancedSearch][extendedStatusIn]
      - in: query
        name: filter[advancedSearch][field]
      - in: query
        name: filter[advancedSearch][hasEntryDistributionValidationErrors]
      - in: query
        name: filter[advancedSearch][idEqual]
      - in: query
        name: filter[advancedSearch][idIn]
      - in: query
        name: filter[advancedSearch][indexIdGreaterThan]
      - in: query
        name: filter[advancedSearch][isQuiz]
        description: 'Enum Type: `KalturaNullableBoolean`'
      - in: query
        name: filter[advancedSearch][items]
      - in: query
        name: filter[advancedSearch][memberIdEq]
      - in: query
        name: filter[advancedSearch][memberIdIn]
      - in: query
        name: filter[advancedSearch][memberPermissionsMatchAnd]
      - in: query
        name: filter[advancedSearch][memberPermissionsMatchOr]
      - in: query
        name: filter[advancedSearch][metadataProfileId]
      - in: query
        name: filter[advancedSearch][noDistributionProfiles]
      - in: query
        name: filter[advancedSearch][not]
      - in: query
        name: filter[advancedSearch][objectType]
      - in: query
        name: filter[advancedSearch][orderBy]
        description: 'Enum Type: `KalturaCategoryEntryAdvancedOrderBy`'
      - in: query
        name: filter[advancedSearch][type]
        description: 'Enum Type: `KalturaSearchOperatorType`'
      - in: query
        name: filter[advancedSearch][updatedAtGreaterThanOrEqual]
      - in: query
        name: filter[advancedSearch][updatedAtLessThanOrEqual]
      - in: query
        name: filter[advancedSearch][userIdEqual]
      - in: query
        name: filter[advancedSearch][userIdIn]
      - in: query
        name: filter[advancedSearch][value]
      - in: query
        name: filter[advancedSearch][watermarkId]
      - in: query
        name: filter[createdAtGreaterThanOrEqual]
      - in: query
        name: filter[createdAtLessThanOrEqual]
      - in: query
        name: filter[createdByIdEqual]
      - in: query
        name: filter[idEqual]
      - in: query
        name: filter[idIn]
      - in: query
        name: filter[orderBy]
      - in: query
        name: filter[statusEqual]
        description: 'Enum Type: `KalturaControlPanelCommandStatus`'
      - in: query
        name: filter[statusIn]
      - in: query
        name: filter[targetTypeEqual]
        description: 'Enum Type: `KalturaControlPanelCommandTargetType`'
      - in: query
        name: filter[targetTypeIn]
      - in: query
        name: filter[typeEqual]
        description: 'Enum Type: `KalturaControlPanelCommandType`'
      - in: query
        name: filter[typeIn]
      - in: query
        name: No Name
      - in: query
        name: pager[pageIndex]
        description: The page number for which {pageSize} of objects should be retrieved
          (Default is 1)
      - in: query
        name: pager[pageSize]
        description: The number of objects to retrieve
      responses:
        200:
          description: OK
      tags:
      - Service
      - Batchcontrol
      - Action
      - ListCommands
  /service/batchcontrol/action/listSchedulers:
    get:
      summary: Get Service Batchcontrol Action Listschedulers
      description: list all Schedulers
      operationId: batchcontrol.listSchedulers
      x-api-path-slug: servicebatchcontrolactionlistschedulers-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Service
      - Batchcontrol
      - Action
      - ListSchedulers
  /service/batchcontrol/action/listWorkers:
    get:
      summary: Get Service Batchcontrol Action Listworkers
      description: list all Workers
      operationId: batchcontrol.listWorkers
      x-api-path-slug: servicebatchcontrolactionlistworkers-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Service
      - Batchcontrol
      - Action
      - ListWorkers
  /service/batchcontrol/action/reportStatus:
    get:
      summary: Get Service Batchcontrol Action Reportstatus
      description: batch reportStatus action saves the a status attribute from a remote
        scheduler and returns pending commands for the scheduler
      operationId: batchcontrol.reportStatus
      x-api-path-slug: servicebatchcontrolactionreportstatus-get
      parameters:
      - in: query
        name: No Name
      - in: query
        name: scheduler[configs]
      - in: query
        name: scheduler[configuredId]
        description: The id as configured in the batch config
      - in: query
        name: scheduler[host]
        description: The host name
      - in: query
        name: scheduler[name]
        description: The scheduler name
      - in: query
        name: scheduler[statuses]
      - in: query
        name: scheduler[workers]
      responses:
        200:
          description: OK
      tags:
      - Service
      - Batchcontrol
      - Action
      - ReportStatus
  /service/batchcontrol/action/setCommandResult:
    get:
      summary: Get Service Batchcontrol Action Setcommandresult
      description: batch setCommandResult action saves the results of a command as
        recieved from a remote scheduler
      operationId: batchcontrol.setCommandResult
      x-api-path-slug: servicebatchcontrolactionsetcommandresult-get
      parameters:
      - in: query
        name: commandId
        description: The id of the command
      - in: query
        name: errorDescription
        description: The description, important for failed commands
      - in: query
        name: No Name
      - in: query
        name: status
        description: 'Enum Type: `KalturaControlPanelCommandStatus`The status of the
          command'
      responses:
        200:
          description: OK
      tags:
      - Service
      - Batchcontrol
      - Action
      - SetCommandResult
  /service/batchcontrol/action/setSchedulerConfig:
    get:
      summary: Get Service Batchcontrol Action Setschedulerconfig
      description: batch sets a configuration parameter to be loaded by a scheduler
      operationId: batchcontrol.setSchedulerConfig
      x-api-path-slug: servicebatchcontrolactionsetschedulerconfig-get
      parameters:
      - in: query
        name: adminId
        description: The id of the admin that called the setConfig
      - in: query
        name: cause
        description: The reason it was changed
      - in: query
        name: configParam
        description: The parameter to be set
      - in: query
        name: configParamPart
        description: The parameter part to be set - for additional params
      - in: query
        name: configValue
        description: The value to be set
      - in: query
        name: No Name
      - in: query
        name: schedulerId
        description: The id of the remote scheduler location
      responses:
        200:
          description: OK
      tags:
      - Service
      - Batchcontrol
      - Action
      - SetSchedulerConfig
  /service/batchcontrol/action/setWorkerConfig:
    get:
      summary: Get Service Batchcontrol Action Setworkerconfig
      description: batch sets a configuration parameter to be loaded by a worker
      operationId: batchcontrol.setWorkerConfig
      x-api-path-slug: servicebatchcontrolactionsetworkerconfig-get
      parameters:
      - in: query
        name: adminId
        description: The id of the admin that called the setConfig
      - in: query
        name: cause
        description: The reason it was changed
      - in: query
        name: configParam
        description: The parameter to be set
      - in: query
        name: configParamPart
        description: The parameter part to be set - for additional params
      - in: query
        name: configValue
        description: The value to be set
      - in: query
        name: No Name
      - in: query
        name: workerId
        description: The id of the job to be configured
      responses:
        200:
          description: OK
      tags:
      - Service
      - Batchcontrol
      - Action
      - SetWorkerConfig
  /service/batchcontrol/action/startWorker:
    get:
      summary: Get Service Batchcontrol Action Startworker
      description: batch start action starts a job
      operationId: batchcontrol.startWorker
      x-api-path-slug: servicebatchcontrolactionstartworker-get
      parameters:
      - in: query
        name: adminId
        description: The id of the admin that called the start
      - in: query
        name: cause
        description: The reason it was started
      - in: query
        name: No Name
      - in: query
        name: workerId
        description: The id of the job to be started
      responses:
        200:
          description: OK
      tags:
      - Service
      - Batchcontrol
      - Action
      - StartWorker
  /service/batchcontrol/action/stopScheduler:
    get:
      summary: Get Service Batchcontrol Action Stopscheduler
      description: batch stop action stops a scheduler
      operationId: batchcontrol.stopScheduler
      x-api-path-slug: servicebatchcontrolactionstopscheduler-get
      parameters:
      - in: query
        name: adminId
        description: The id of the admin that called the stop
      - in: query
        name: cause
        description: The reason it was stopped
      - in: query
        name: No Name
      - in: query
        name: schedulerId
        description: The id of the remote scheduler location
      responses:
        200:
          description: OK
      tags:
      - Service
      - Batchcontrol
      - Action
      - StopScheduler
  /service/batchcontrol/action/stopWorker:
    get:
      summary: Get Service Batchcontrol Action Stopworker
      description: batch stop action stops a worker
      operationId: batchcontrol.stopWorker
      x-api-path-slug: servicebatchcontrolactionstopworker-get
      parameters:
      - in: query
        name: adminId
        description: The id of the admin that called the stop
      - in: query
        name: cause
        description: The reason it was stopped
      - in: query
        name: No Name
      - in: query
        name: workerId
        description: The id of the job to be stopped
      responses:
        200:
          description: OK
      tags:
      - Service
      - Batchcontrol
      - Action
      - StopWorker