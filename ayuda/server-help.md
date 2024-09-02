`rcssserver server::help`.

```markdown
# Guía de Opciones y Configuraciones de `rcssserver`

## Introducción

`rcssserver` es el servidor para el simulador de fútbol RoboCup. La siguiente guía detalla las opciones de configuración disponibles para el módulo "server" en `rcssserver-19.0.0`.

## Uso General

Para obtener ayuda sobre las opciones generales de `rcssserver`, puedes usar el siguiente comando:

```bash
rcssserver [[-[-]]namespace::option=value]
           [[-[-]][namespace::]help]
           [[-[-]]include=file]
```

### Opciones Generales:

- **`help`**: Muestra ayuda general.
- **`include=file`**: Lee el archivo de configuración especificado. Los archivos de configuración tienen el mismo formato que las opciones de línea de comandos y se procesan antes de las opciones posteriores.
- **`server::help`**: Muestra ayuda detallada para el módulo "server".
- **`player::help`**: Muestra ayuda detallada para el módulo "player".
- **`CSVSaver::help`**: Muestra ayuda detallada para el módulo "CSVSaver".

## Opciones del Servidor

A continuación, se detallan las opciones específicas del módulo "server":

### Configuración General del Servidor:

- **`server::catch_ban_cycle=<INTEGER>`**: Valor actual: `5`
- **`server::clang_advice_win=<INTEGER>`**: Valor actual: `1`
- **`server::clang_define_win=<INTEGER>`**: Valor actual: `1`
- **`server::clang_del_win=<INTEGER>`**: Valor actual: `1`
- **`server::clang_info_win=<INTEGER>`**: Valor actual: `1`
- **`server::clang_mess_delay=<INTEGER>`**: Valor actual: `50`
- **`server::clang_mess_per_cycle=<INTEGER>`**: Valor actual: `1`
- **`server::clang_meta_win=<INTEGER>`**: Valor actual: `1`
- **`server::clang_rule_win=<INTEGER>`**: Valor actual: `1`
- **`server::clang_win_size=<INTEGER>`**: Valor actual: `300`
- **`server::coach_port=<INTEGER>`**: Valor actual: `6001`
- **`server::connect_wait=<INTEGER>`**: Valor actual: `300`
- **`server::drop_ball_time=<INTEGER>`**: Valor actual: `100`
- **`server::extra_half_time=<INTEGER>`**: Valor actual: `100`
- **`server::foul_cycles=<INTEGER>`**: Valor actual: `5`
- **`server::freeform_send_period=<INTEGER>`**: Valor actual: `20`
- **`server::freeform_wait_period=<INTEGER>`**: Valor actual: `600`
- **`server::game_log_compression=<INTEGER>`**: Valor actual: `0`
- **`server::game_log_version=<INTEGER>`**: Valor actual: `6`
- **`server::game_over_wait=<INTEGER>`**: Valor actual: `100`
- **`server::goalie_max_moves=<INTEGER>`**: Valor actual: `2`
- **`server::half_time=<INTEGER>`**: Valor actual: `300`
- **`server::hear_decay=<INTEGER>`**: Valor actual: `1`
- **`server::hear_inc=<INTEGER>`**: Valor actual: `1`
- **`server::hear_max=<INTEGER>`**: Valor actual: `1`
- **`server::illegal_defense_duration=<INTEGER>`**: Valor actual: `20`
- **`server::illegal_defense_number=<INTEGER>`**: Valor actual: `0` (si es 0, la regla de defensa ilegal estará deshabilitada)
- **`server::keepaway_start=<INTEGER>`**: Valor actual: `-1`
- **`server::kick_off_wait=<INTEGER>`**: Valor actual: `100`
- **`server::max_goal_kicks=<INTEGER>`**: Valor actual: `3`
- **`server::max_monitors=<INTEGER>`**: Valor actual: `-1`
- **`server::nr_extra_halfs=<INTEGER>`**: Número de períodos extra en un juego si termina empatado. Valor actual: `2`
- **`server::nr_normal_halfs=<INTEGER>`**: Número de mitades normales en un juego. Valor actual: `2`
- **`server::olcoach_port=<INTEGER>`**: Valor actual: `6002`
- **`server::pen_before_setup_wait=<INTEGER>`**: Valor actual: `10`
- **`server::pen_max_extra_kicks=<INTEGER>`**: Valor actual: `5`
- **`server::pen_nr_kicks=<INTEGER>`**: Valor actual: `5`
- **`server::pen_ready_wait=<INTEGER>`**: Valor actual: `10`
- **`server::pen_setup_wait=<INTEGER>`**: Valor actual: `70`
- **`server::pen_taken_wait=<INTEGER>`**: Valor actual: `150`
- **`server::point_to_ban=<INTEGER>`**: Valor actual: `5`
- **`server::point_to_duration=<INTEGER>`**: Valor actual: `20`
- **`server::port=<INTEGER>`**: Valor actual: `6000`
- **`server::recv_step=<INTEGER>`**: Valor actual: `10`
- **`server::say_coach_cnt_max=<INTEGER>`**: Valor actual: `128`
- **`server::say_coach_msg_size=<INTEGER>`**: Valor actual: `128`
- **`server::say_msg_size=<INTEGER>`**: Valor actual: `10`
- **`server::send_step=<INTEGER>`**: Valor actual: `150`
- **`server::send_vi_step=<INTEGER>`**: Valor actual: `100`
- **`server::sense_body_step=<INTEGER>`**: Valor actual: `100`
- **`server::simulator_step=<INTEGER>`**: Valor actual: `100`
- **`server::slow_down_factor=<INTEGER>`**: Valor actual: `1`
- **`server::start_goal_l=<INTEGER>`**: Valor actual: `0`
- **`server::start_goal_r=<INTEGER>`**: Valor actual: `0`
- **`server::synch_micro_sleep=<INTEGER>`**: Valor actual: `1`
- **`server::synch_offset=<INTEGER>`**: Valor actual: `60`
- **`server::synch_see_offset=<INTEGER>`**: Valor actual: `0`
- **`server::tackle_cycles=<INTEGER>`**: Valor actual: `10`
- **`server::text_log_compression=<INTEGER>`**: Valor actual: `0`

### Configuración de Comportamiento:

- **`server::auto_mode=<on|off|true|false|1|0|>`**: Valor actual: `false`
- **`server::back_passes=<on|off|true|false|1|0|>`**: Valor actual: `true`
- **`server::coach=<on|off|true|false|1|0|>`**: Valor actual: `false`
- **`server::coach_w_referee=<on|off|true|false|1|0|>`**: Valor actual: `false`
- **`server::forbid_kick_off_offside=<on|off|true|false|1|0|>`**: Valor actual: `true`
- **`server::free_kick_faults=<on|off|true|false|1|0|>`**: Valor actual: `true`
- **`server::fullstate_l=<on|off|true|false|1|0|>`**: Valor actual: `false`
- **`server::fullstate_r=<on|off|true|false|1|0|>`**: Valor actual: `false`
- **`server::game_log_dated=<on|off|true|false|1|0|>`**: Valor actual: `true`
- **`server::game_log_fixed=<on|off|true|false|1|0|>`**: Valor actual: `false`
- **`server::game_logging=<on|off|true|false|1|0|>`**: Valor actual: `true`
- **`server::golden_goal=<on|off|true|false|1|0|>`**: Valor actual: `false`
- **`server::keepaway=<on|off|true|false|1|0|>`**: Valor actual: `false`
- **`server::keepaway_log_dated=<on|off|true|false|1|0|>`**: Valor actual: `true`
- **`server::keepaway_log_fixed=<on|off|true|false|1|0|>`**: Valor actual: `false`
- **`server::keepaway_logging=<on|off|true|false|1|0|>`**: Valor actual: `true`
- **`server::log_times=<on|off|true|false|1|0|>`**: Valor actual: `false`
- **`server::old_coach_hear=<on|off|true|false|1|0|>`**: Valor actual: `false