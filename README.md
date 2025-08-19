# EvilCrowV2Schematica

Este projeto utiliza **ESP32 + CC1101** para montar o **Evil Crow RF** (ECRF + Jammer).  
Abaixo estão os materiais necessários e o esquema de ligações.
<img width="568" height="978" alt="image" src="https://github.com/user-attachments/assets/e9eccd09-062d-40bd-92de-7c9a4a28f0d7" />
[Demo Video](https://www.youtube.com/watch?v=oAPZG4rk3v0)


---

## 🛠️ Materiais

- 2 × **ESP32**  
- 2 × **CC1101**  
- 1 × **SD Card Module**  
- 1 × **MicroSD Card**  
- **Cabos jumper / fiação**  
- **PCB**  
- 2 × **Push Button**  

---

## 📡 Ligações CC1101 ↔ ESP32

### ECRF e Jammer
| Pino CC1101 | ESP32 (ECRF) | ESP32 (Jammer) |
|-------------|--------------|----------------|
| **SCK**     | 14           | 14             |
| **MISO**    | 12           | 12             |
| **MOSI**    | 13           | 13             |
| **CSN**     | 5            | 27             |
| **GDO0**    | 2            | 25             |
| **GDO2**    | 4            | 26             |

---
## 🔘 Ligações Push Button

- **Botão 1 → GPIO 34**  
  - Conectar **Resistor 10K** ao **5V ESP32**  
  - Saída vai para **D34 ESP32**  
  - Também conecta em **D4 ESP32** para chavear com **GND ESP32**

- **Botão 2 → GPIO 35**  
  - Mesmo esquema do Botão 1
  - <img width="391" height="490" alt="image" src="https://github.com/user-attachments/assets/978298b7-7374-4651-a262-398d0520af47" />
  ---
  ## 💾 Ligações MicroSD ↔ ESP32

| Pino SD | ESP32 |
|---------|-------|
| **SCK** | 18    |
| **MISO**| 19    |
| **MOSI**| 23    |
| **CSN** | 22    |

---
## ⚙️ Configuração

- Para **ECRF**, usar **apenas 1× CC1101 (Módulo 2)**  
- Configure no menu CC1101:  
  - **SSID:** `ECRF`  
  - **Senha:** `123456789`  
- Acesse a interface web em:  
  - **http://192.168.4.1**  
  - Configure para **Módulo 2** como **Transmitter & Receiver**  

---

📌 **Nota:** O Jammer precisa dos dois módulos, já o ECRF usa apenas **Módulo 2**.

