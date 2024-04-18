# requires the following python packages
kafka-python
aiokafka

# usage

```yaml
- name: Use kafkaprod_module to take data and create producer message
  producer_kafkapy:
    host: "{{ messages_kafka_hostname }}"
    port: "{{ messages_kafka_port | default('9092') }}"
    verify_mode: "{{ messages_kafka_verify | default(false) }}"
    topic: "{{ messages_kafka_topic }}"
    data: "{{ messages_kafka_data }}"
```
