```sh
# ${pod_name}_${namespace}_${container_name}-${container_id}.log
/var/log/containers/{fedlearner-filebeat-sdjb2}_{fedlearner-uat}_{fedlearner-filebeat}-{b2c108c745e2778dfa7de461a9000f33a5708c2716f9e9af64c52c779052bf2c}.log 
```

```sh
# ${namespace}_${pod_name}_${pod_id}/${container_name}/0.log
/var/log/pods/{fedlearner-uat}_{fedlearner-filebeat-sdjb2}_{be6dd46d-f172-4c59-a650-eb96cfa14019}/{fedlearner-filebeat}/0.log
```

```sh
root@fedlearner-filebeat-sdjb2:/var/log/containers# pwd
/var/log/containers
root@fedlearner-filebeat-sdjb2:/var/log/containers# ll
total 112
drwxr-xr-x  2 root root 12288 Mar  6 11:17 ./
drwxrwxr-x 16 root  111  4096 Mar 12 00:00 ../
lrwxrwxrwx  1 root root    92 Feb 27 16:19 ama-logs-twfpv_kube-system_ama-logs-6b46729b56b67cf92f49a61d35b81ef51bac2b1e2cfdb23449e8bb1e13f0ee7e.log -> /var/log/pods/kube-system_ama-logs-twfpv_334eb02c-10aa-4daf-8a15-a1833688d46c/ama-logs/0.log
lrwxrwxrwx  1 root root   103 Feb 27 16:19 ama-logs-twfpv_kube-system_ama-logs-prometheus-b9a18f5e4b8b7bb677b9dd8c776978fa413af65e183c29aba7b3564d084dd177.log -> /var/log/pods/kube-system_ama-logs-twfpv_334eb02c-10aa-4daf-8a15-a1833688d46c/ama-logs-prometheus/0.log
lrwxrwxrwx  1 root root   114 Feb 27 16:20 azure-ip-masq-agent-pkpn5_kube-system_azure-ip-masq-agent-247abaa0252969f171ecddee8eeea0639b7245cbdef4a5497fac12d5a908b5a8.log -> /var/log/pods/kube-system_azure-ip-masq-agent-pkpn5_c0202112-dc3c-4801-a271-a7974d58b4ee/azure-ip-masq-agent/0.log
lrwxrwxrwx  1 root root   112 Feb 20 09:05 cloud-node-manager-r6gmz_kube-system_cloud-node-manager-7ad973c79265656b8f2750934e1a35ff7a8130841c56db08351b193f5e3bc9a4.log -> /var/log/pods/kube-system_cloud-node-manager-r6gmz_2187fbdf-4bde-4526-9e76-f2c081524aa6/cloud-node-manager/0.log
lrwxrwxrwx  1 root root   114 Feb 20 09:06 controller-manager-76df5fc76-2sbkc_fedlearner-uat_manager-29b7c87d0bf32ee3120e39af8f92fd04f6c41956c034115ae5501c39cc230751.log -> /var/log/pods/fedlearner-uat_controller-manager-76df5fc76-2sbkc_86e7fc8a-27d9-4c31-9b2f-61595704f74b/manager/0.log
lrwxrwxrwx  1 root root   103 Feb 20 09:05 csi-azuredisk-node-h78mh_kube-system_azuredisk-19d087eaf60377c29901898483322e281d8cbe170fe8f908e1f360aef0288195.log -> /var/log/pods/kube-system_csi-azuredisk-node-h78mh_ba27f536-c129-4156-bd51-79eacff1e5af/azuredisk/0.log
lrwxrwxrwx  1 root root   108 Feb 20 09:05 csi-azuredisk-node-h78mh_kube-system_liveness-probe-cd1588ebf92c8b03515247af915a92afbf112800cfffcc3dae8bba57a422da3e.log-> /var/log/pods/kube-system_csi-azuredisk-node-h78mh_ba27f536-c129-4156-bd51-79eacff1e5af/liveness-probe/0.log
lrwxrwxrwx  1 root root   115 Feb 20 09:05 csi-azuredisk-node-h78mh_kube-system_node-driver-registrar-a8f002574cea220d98430920e768199e9bd62257cac7b99ac65cf9eefa5fed91.log -> /var/log/pods/kube-system_csi-azuredisk-node-h78mh_ba27f536-c129-4156-bd51-79eacff1e5af/node-driver-registrar/0.log
lrwxrwxrwx  1 root root   103 Feb 20 09:05 csi-azurefile-node-fxv8k_kube-system_azurefile-e566e84a956a6b5df50793176f873d56641849edce7f24110e938eb47aefb18d.log -> /var/log/pods/kube-system_csi-azurefile-node-fxv8k_389e6d21-d319-4f1f-b0ef-740a044c98c4/azurefile/0.log
lrwxrwxrwx  1 root root   108 Feb 20 09:05 csi-azurefile-node-fxv8k_kube-system_liveness-probe-940ba30c300324a739d8ea4d0587c363904b98c1b5e9b10c4f203403a09f86ba.log-> /var/log/pods/kube-system_csi-azurefile-node-fxv8k_389e6d21-d319-4f1f-b0ef-740a044c98c4/liveness-probe/0.log
lrwxrwxrwx  1 root root   115 Feb 20 09:05 csi-azurefile-node-fxv8k_kube-system_node-driver-registrar-be5b5feb5cccac0d0314a46cbe69f6d3c2ac674070c72a2f29f017a66d1ba8db.log -> /var/log/pods/kube-system_csi-azurefile-node-fxv8k_389e6d21-d319-4f1f-b0ef-740a044c98c4/node-driver-registrar/0.log
lrwxrwxrwx  1 root root   117 Mar  6 11:17 fedlearner-filebeat-sdjb2_fedlearner-uat_fedlearner-filebeat-b2c108c745e2778dfa7de461a9000f33a5708c2716f9e9af64c52c779052bf2c.log -> /var/log/pods/fedlearner-uat_fedlearner-filebeat-sdjb2_be6dd46d-f172-4c59-a650-eb96cfa14019/fedlearner-filebeat/0.log
lrwxrwxrwx  1 root root   141 Mar  6 11:17 fedlearner-filebeat-sdjb2_fedlearner-uat_fedlearner-filebeat-uat-prometheus-exporter-77938b3315ee3a12528af3afe6454b982efd19393f4af25268320039ef1f734a.log -> /var/log/pods/fedlearner-uat_fedlearner-filebeat-sdjb2_be6dd46d-f172-4c59-a650-eb96cfa14019/fedlearner-filebeat-uat-prometheus-exporter/0.log
lrwxrwxrwx  1 root root   128 Mar  2 20:23 fedlearner-operator-78b5b65d55-twdnm_fedlearner-dev_fedlearner-operator-05b6d2a7f982c51651d82f0a8ad7f08be9bd5486f32cc31d19631d5fdedac6d4.log -> /var/log/pods/fedlearner-dev_fedlearner-operator-78b5b65d55-twdnm_4d7d2eac-2e59-467b-9549-475794d94888/fedlearner-operator/1.log
lrwxrwxrwx  1 root root   128 Feb 20 09:07 fedlearner-operator-78b5b65d55-twdnm_fedlearner-dev_fedlearner-operator-972231239b7beefd1b7d6a082b7df01276c55fa1ae0ac296c21e760fa02e3931.log -> /var/log/pods/fedlearner-dev_fedlearner-operator-78b5b65d55-twdnm_4d7d2eac-2e59-467b-9549-475794d94888/fedlearner-operator/0.log
lrwxrwxrwx  1 root root   139 Feb 20 09:13 fedlearner-web-console-v2-64566dddfc-rn6kk_fedlearner-qa_fedlearner-web-console-v2-400b1eebae49f67dadc3dee789a8c204b3187d551e736e53718289ebc6235ecb.log -> /var/log/pods/fedlearner-qa_fedlearner-web-console-v2-64566dddfc-rn6kk_5cd8fd9c-f9e7-4ada-8eef-ba14836f7503/fedlearner-web-console-v2/0.log
lrwxrwxrwx  1 root root   140 Feb 20 09:08 fedlearner-web-console-v2-6c5cb7ffdd-9m6fc_fedlearner-dev_fedlearner-web-console-v2-515f249eb7142b182e2196e2b65112c126e1129827e5bc3a84aedfcab16d59b8.log -> /var/log/pods/fedlearner-dev_fedlearner-web-console-v2-6c5cb7ffdd-9m6fc_c97a6f4e-75de-4519-b81a-99d026102ae6/fedlearner-web-console-v2/0.log
lrwxrwxrwx  1 root root   135 Feb 20 09:05 gatekeeper-audit-7d444c5495-jr9gt_gatekeeper-system_gatekeeper-audit-container-769f7ec3787eb07b2cf3913b685d07b9669c5962b0c00cc11953dd6076d7a99f.log -> /var/log/pods/gatekeeper-system_gatekeeper-audit-7d444c5495-jr9gt_6d47f9d5-7d61-46a6-914f-b7fec6357f61/gatekeeper-audit-container/0.log
lrwxrwxrwx  1 root root    96 Feb 20 09:05 kube-proxy-pm66x_kube-system_kube-proxy-58f30423831cca8188828684644d2135ca2b6a36043dc4cd93ded28cc96bdeb1.log -> /var/log/pods/kube-system_kube-proxy-pm66x_9de2b6ee-7f8e-48dc-9bbd-19240bd5cc83/kube-proxy/0.log
lrwxrwxrwx  1 root root   106 Feb 20 09:05 kube-proxy-pm66x_kube-system_kube-proxy-bootstrap-7894683b15af8f3dd8505988201ec0cbe445cab0fc5bfcd53f179c3c30028605.log -> /var/log/pods/kube-system_kube-proxy-pm66x_9de2b6ee-7f8e-48dc-9bbd-19240bd5cc83/kube-proxy-bootstrap/0.log
lrwxrwxrwx  1 root root   103 Feb 20 09:05 node-exporter-qqxfj_lens-metrics_node-exporter-6ecb60ab3eea5a80238f21293efb29ff9bf0002f311b1f9e7c090648861b06c7.log -> /var/log/pods/lens-metrics_node-exporter-qqxfj_1db3610a-ee26-41b0-a962-f0b41d95890e/node-exporter/0.log
lrwxrwxrwx  1 root root    90 Feb 20 09:05 tke-log-agent-nb9g2_lcs_log-agent-670512cebba19ac6ad16c50c31fe0b837726d5e5ea5d045ad1066cdc9581da8f.log -> /var/log/pods/lcs_tke-log-agent-nb9g2_8b0e4c92-b6c8-4227-9b71-b51dfe0ece3d/log-agent/0.log
lrwxrwxrwx  1 root root    92 Feb 20 09:06 tke-log-agent-nb9g2_lcs_loglistener-ce930d974bd97df52a03e1d63ffa01b49bd6317c0ece1e4ac73153baecc82587.log -> /var/log/pods/lcs_tke-log-agent-nb9g2_8b0e4c92-b6c8-4227-9b71-b51dfe0ece3d/loglistener/0.log
lrwxrwxrwx  1 root root    95 Feb 20 09:05 yunjing-agent-b6rw5_tcss_yunjing-agent-ea4d7bd6c4ce4e8b03a78d68d739728511f0f4f2fe0cd79db42d60b25d0a338e.log -> /var/log/pods/tcss_yunjing-agent-b6rw5_fb8bd46d-c47f-43e5-b06c-544b26fe595d/yunjing-agent/0.log
root@fedlearner-filebeat-sdjb2:/var/log/containers#
```