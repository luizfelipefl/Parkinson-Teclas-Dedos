
# Dicionário de Dados — Versão 0.1

## Projeto Parkinson — Teclas e Dedos

Este documento descreve a estrutura inicial dos dados coletados pelo sistema de aquisição multimodal.

## 1. participant — Participantes

- participant_id: identificador anônimo do participante.

## 2. session — Sessões

- session_id: identificador único da sessão.
- participant_id: participante associado à sessão.
- layout: configuração do teclado, por exemplo ABNT2.
- hardware_version: versão do hardware utilizado.

## 3. keystroke_event — Eventos de teclado

- event_id: identificador único do evento.
- session_id: sessão associada ao evento.
- key_code: identificação da tecla.
- keydown_ts: instante em que a tecla foi pressionada.
- keyup_ts: instante em que a tecla foi liberada.
- hold_time: duração do pressionamento.

## 4. imu_stream — Dados dos sensores

- session_id: sessão associada.
- sensor_id: identificador do sensor.
- timestamp: instante da medição.
- ax, ay, az: aceleração nos três eixos.
- gx, gy, gz: velocidade angular nos três eixos.

## 5. Convenções iniciais

- IDs não devem conter nomes ou informações pessoais.
- Timestamps de eventos serão registrados usando relógio monotônico.
- Timestamps de eventos serão expressos em segundos relativos ao início da sessão.
- O tempo hold_time será expresso em segundos.
- Dados ausentes serão representados por null quando o formato permitir.
- Os dados brutos dos sensores serão preservados.

## 6. Status

Versão: 0.1 — Proposta inicial.

A estrutura será revisada conforme as decisões da equipe e a integração com o hardware.
