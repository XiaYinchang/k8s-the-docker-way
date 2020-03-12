A detailed description of the command-line flag of kube-proxy



### Deprecated

- bind-address 0.0.0.0

    The IP address for the proxy server to serve on (set to 0.0.0.0 for all IPv4 interfaces and `::` for all IPv6 interfaces) (default 0.0.0.0)

- cluster-cidr string

    The CIDR range of pods in the cluster. When configured, traffic sent to a Service cluster IP from outside this range will be masqueraded and traffic sent from pods to an external LoadBalancer IP will be directed to the respective cluster IP instead

- config-sync-period duration

    How often configuration from the apiserver is refreshed.  Must be greater than 0. (default 15m0s)

- conntrack-max-per-core int32

    Maximum number of NAT connections to track per CPU core (0 to leave the limit as-is and ignore conntrack-min). (default 32768)

- conntrack-min int32

    Minimum number of conntrack entries to allocate, regardless of conntrack-max-per-core (set conntrack-max-per-core=0 to leave the limit as-is). (default 131072)

- conntrack-tcp-timeout-close-wait duration

    NAT timeout for TCP connections in the CLOSE_WAIT state (default 1h0m0s)

- conntrack-tcp-timeout-established duration

    Idle timeout for established TCP connections (0 to leave as-is) (default 24h0m0s)

- feature-gates mapStringBool

    A set of key=value pairs that describe feature gates for alpha/experimental features. Options are:
```
APIListChunking=true|false (BETA - default=true)
APIPriorityAndFairness=true|false (ALPHA - default=false)
APIResponseCompression=true|false (BETA - default=true)
AllAlpha=true|false (ALPHA - default=false)
AllBeta=true|false (BETA - default=false)
AllowInsecureBackendProxy=true|false (BETA - default=true)
AppArmor=true|false (BETA - default=true)
BalanceAttachedNodeVolumes=true|false (ALPHA - default=false)
BlockVolume=true|false (BETA - default=true)
BoundServiceAccountTokenVolume=true|false (ALPHA - default=false)
CPUManager=true|false (BETA - default=true)
CRIContainerLogRotation=true|false (BETA - default=true)
CSIBlockVolume=true|false (BETA - default=true)
CSIDriverRegistry=true|false (BETA - default=true)
CSIInlineVolume=true|false (BETA - default=true)
CSIMigration=true|false (BETA - default=true)
CSIMigrationAWS=true|false (BETA - default=false)
CSIMigrationAWSComplete=true|false (ALPHA - default=false)
CSIMigrationAzureDisk=true|false (ALPHA - default=false)
CSIMigrationAzureDiskComplete=true|false (ALPHA - default=false)
CSIMigrationAzureFile=true|false (ALPHA - default=false)
CSIMigrationAzureFileComplete=true|false (ALPHA - default=false)
CSIMigrationGCE=true|false (BETA - default=false)
CSIMigrationGCEComplete=true|false (ALPHA - default=false)
CSIMigrationOpenStack=true|false (ALPHA - default=false)
CSIMigrationOpenStackComplete=true|false (ALPHA - default=false)
CustomCPUCFSQuotaPeriod=true|false (ALPHA - default=false)
DevicePlugins=true|false (BETA - default=true)
DryRun=true|false (BETA - default=true)
DynamicAuditing=true|false (ALPHA - default=false)
DynamicKubeletConfig=true|false (BETA - default=true)
EndpointSlice=true|false (BETA - default=false)
EphemeralContainers=true|false (ALPHA - default=false)
EvenPodsSpread=true|false (ALPHA - default=false)
ExpandCSIVolumes=true|false (BETA - default=true)
ExpandInUsePersistentVolumes=true|false (BETA - default=true)
ExpandPersistentVolumes=true|false (BETA - default=true)
ExperimentalHostUserNamespaceDefaulting=true|false (BETA - default=false)
HPAScaleToZero=true|false (ALPHA - default=false)
HyperVContainer=true|false (ALPHA - default=false)
IPv6DualStack=true|false (ALPHA - default=false)
KubeletPodResources=true|false (BETA - default=true)
LegacyNodeRoleBehavior=true|false (ALPHA - default=true)
LocalStorageCapacityIsolation=true|false (BETA - default=true)
LocalStorageCapacityIsolationFSQuotaMonitoring=true|false (ALPHA - default=false)
NodeDisruptionExclusion=true|false (ALPHA - default=false)
NonPreemptingPriority=true|false (ALPHA - default=false)
PodDisruptionBudget=true|false (BETA - default=true)
PodOverhead=true|false (ALPHA - default=false)
ProcMountType=true|false (ALPHA - default=false)
QOSReserved=true|false (ALPHA - default=false)
RemainingItemCount=true|false (BETA - default=true)
RemoveSelfLink=true|false (ALPHA - default=false)
ResourceLimitsPriorityFunction=true|false (ALPHA - default=false)
RotateKubeletClientCertificate=true|false (BETA - default=true)
RotateKubeletServerCertificate=true|false (BETA - default=true)
RunAsGroup=true|false (BETA - default=true)
RuntimeClass=true|false (BETA - default=true)
SCTPSupport=true|false (ALPHA - default=false)
ServerSideApply=true|false (BETA - default=true)
ServiceNodeExclusion=true|false (ALPHA - default=false)
ServiceTopology=true|false (ALPHA - default=false)
StartupProbe=true|false (ALPHA - default=false)
StorageVersionHash=true|false (BETA - default=true)
StreamingProxyRedirects=true|false (BETA - default=true)
SupportNodePidsLimit=true|false (BETA - default=true)
SupportPodPidsLimit=true|false (BETA - default=true)
Sysctls=true|false (BETA - default=true)
TTLAfterFinished=true|false (ALPHA - default=false)
TaintBasedEvictions=true|false (BETA - default=true)
TokenRequest=true|false (BETA - default=true)
TokenRequestProjection=true|false (BETA - default=true)
TopologyManager=true|false (ALPHA - default=false)
ValidateProxyRedirects=true|false (BETA - default=true)
VolumePVCDataSource=true|false (BETA - default=true)
VolumeSnapshotDataSource=true|false (BETA - default=true)
WinDSR=true|false (ALPHA - default=false)
WinOverlay=true|false (ALPHA - default=false)
WindowsGMSA=true|false (BETA - default=true)
WindowsRunAsUserName=true|false (BETA - default=true)
```

- healthz-bind-address 0.0.0.0

    The IP address for the health check server to serve on (set to 0.0.0.0 for all IPv4 interfaces and `::` for all IPv6 interfaces) (default 0.0.0.0:10256)

- healthz-port int32

    The port to bind the health check server. Use 0 to disable. (default 10256)

- hostname-override string

    If non-empty, will use this string as identification instead of the actual hostname.

- iptables-masquerade-bit int32

    If using the pure iptables proxy, the bit of the fwmark space to mark packets requiring SNAT with.  Must be within the range [0, 31]. (default 14)

- iptables-min-sync-period duration

    The minimum interval of how often the iptables rules can be refreshed as endpoints and services change (e.g. '5s', '1m', '2h22m').

- iptables-sync-period duration

    The maximum interval of how often iptables rules are refreshed (e.g. '5s', '1m', '2h22m').  Must be greater than 0. (default 30s)

- ipvs-exclude-cidrs strings

    A comma-separated list of CIDR's which the ipvs proxier should not touch when cleaning up IPVS rules.

- ipvs-min-sync-period duration

    The minimum interval of how often the ipvs rules can be refreshed as endpoints and services change (e.g. '5s', '1m', '2h22m').

- ipvs-scheduler string

    The ipvs scheduler type when proxy mode is ipvs

- ipvs-strict-arp

    Enable strict ARP by setting arp_ignore to 1 and arp_announce to 2

- ipvs-sync-period duration

    The maximum interval of how often ipvs rules are refreshed (e.g. '5s', '1m', '2h22m').  Must be greater than 0. (default 30s)

- kube-api-burst int32

    Burst to use while talking with kubernetes apiserver (default 10)

- kube-api-content-type string

    Content type of requests sent to apiserver. (default "application/vnd.kubernetes.protobuf")

- kube-api-qps float32

    QPS to use while talking with kubernetes apiserver (default 5)

- kubeconfig string

    Path to kubeconfig file with authorization information (the master location is set by the master flag).

- masquerade-all

    If using the pure iptables proxy, SNAT all traffic sent via Service cluster IPs (this not commonly needed)

- master string

    The address of the Kubernetes API server (overrides any value in kubeconfig)

- metrics-bind-address 0.0.0.0

    The IP address for the metrics server to serve on (set to 0.0.0.0 for all IPv4 interfaces and `::` for all IPv6 interfaces) (default 127.0.0.1:10249)

- metrics-port int32

    The port to bind the metrics server. Use 0 to disable. (default 10249)

- nodeport-addresses strings

    A string slice of values which specify the addresses to use for NodePorts. Values may be valid IP blocks (e.g. 1.2.3.0/24, 1.2.3.4/32). The default empty string slice ([]) means to use all local addresses.

- oom-score-adj int32

    The oom-score-adj value for kube-proxy process. Values must be within the range [-1000, 1000] (default -999)

- profiling

    If true enables profiling via web interface on /debug/pprof handler.

- proxy-mode ProxyMode

    Which proxy mode to use: 'userspace' (older) or 'iptables' (faster) or 'ipvs'. If blank, use the best-available proxy (currently iptables).  If the iptables proxy is selected, regardless of how, but the system's kernel or iptables versions are insufficient, this always falls back to the userspace proxy.

- proxy-port-range port-range

    Range of host ports (beginPort-endPort, single port or beginPort+offset, inclusive) that may be consumed in order to proxy service traffic. If (unspecified, 0, or 0-0) then ports will be randomly chosen.

- udp-timeout duration

    How long an idle UDP connection will be kept open (e.g. '250ms', '2s').  Must be greater than 0. Only applicable for proxy-mode=userspace (default 250ms)



### Main

- cleanup

    If true cleanup iptables and ipvs rules and exit.

- config string

    The path to the configuration file.

- write-config-to string

    If set, write the default configuration values to this file and exit.



### misc

- help

    help for kube-proxy

- log-flush-frequency duration

    Maximum number of seconds between log flushes (default 5s)

- version version[=true]

    Print version information and quit



### uncategorized

- add-dir-header

    If true, adds the file directory to the header

- log-file-max-size uint

    Defines the maximum size a log file can grow to. Unit is megabytes. If the value is 0, the maximum file size is unlimited. (default 1800)

- skip-log-headers

    If true, avoid headers when opening log files



### vendor.klog

- alsologtostderr

    log to standard error as well as files

- log-backtrace-at traceLocation

    when logging hits line file:N, emit a stack trace (default :0)

- log-dir string

    If non-empty, write log files in this directory

- log-file string

    If non-empty, use this log file

- logtostderr

    log to standard error instead of files (default true)

- skip-headers

    If true, avoid header prefixes in the log messages

- stderrthreshold severity

    logs at or above this threshold go to stderr (default 2)

- v Level

    number for the log level verbosity

- vmodule moduleSpec

    comma-separated list of pattern=N settings for file-filtered logging

