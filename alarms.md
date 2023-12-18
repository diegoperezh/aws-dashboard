Details

Name
    Outposts EBS Volume Capacity lower than 50%

Type
    Metric alarm

Description
    Outposts coportativo con capacidad de volumenes de EBS menor al 50%

State

    OK

Threshold
    EBSVolumeTypeCapacityAvailability <= 50 for 1 datapoints within 5 minutes

Last change
    2023-12-14 16:18:14

Actions

    Actions enabled

Namespace
    AWS/Outposts

Metric name
    EBSVolumeTypeCapacityAvailability

OutpostId
    op-05d2acf0919c259c2

VolumeType
    gp2

Statistic
    Maximum

Period
    5 minutes

Datapoints to alarm
    1 out of 1

Missing data treatment
    Treat missing data as missing

Percentiles with low samples
    evaluate

ARN
    arn:aws:cloudwatch:ca-central-1:646994745391:alarm:Outposts EBS Volume Capacity lower than 50%



Notification	When in alarm, send message to topic "Default_CloudWatch_Alarms_Topic"	



Type: AWS::CloudWatch::Alarm
Properties:
    AlarmName: Outposts EBS Volume Capacity lower than 50%
    AlarmDescription: "# Outposts coportativo con capacidad de volumenes de EBS menor al 50%"
    ActionsEnabled: true
    OKActions: []
    AlarmActions:
        - arn:aws:sns:ca-central-1:646994745391:Default_CloudWatch_Alarms_Topic
    InsufficientDataActions: []
    MetricName: EBSVolumeTypeCapacityAvailability
    Namespace: AWS/Outposts
    Statistic: Maximum
    Dimensions:
        - Name: OutpostId
          Value: op-05d2acf0919c259c2
        - Name: VolumeType
          Value: gp2
    Period: 300
    EvaluationPeriods: 1
    DatapointsToAlarm: 1
    Threshold: 50
    ComparisonOperator: LessThanOrEqualToThreshold
    TreatMissingData: missing
