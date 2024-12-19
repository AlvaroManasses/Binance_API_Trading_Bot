
# Robô de Trading Automático para Binance

Este projeto implementa um robô de trading automático utilizando a API da Binance. Ele analisa médias móveis para identificar oportunidades de compra e venda de ativos, operando de forma contínua.

---

## **Funcionamento**

O robô executa as seguintes etapas:

1. **Busca de dados**:
   - Utiliza a função `get_klines` da API da Binance para obter histórico de preços (candles) de um ativo especificado.
   - Converte os dados para um DataFrame do pandas, facilitando o cálculo de indicadores.

2. **Estratégia**:
   - Calcula duas médias móveis: uma rápida (7 períodos) e outra lenta (40 períodos).
   - Compara as médias:
     - Se a média rápida ultrapassar a lenta, o robô compra o ativo.
     - Se a média rápida cair abaixo da lenta, o robô vende o ativo.

3. **Execução de Ordens**:
   - Opera através de ordens de mercado, comprando ou vendendo a quantidade especificada.

4. **Loop Contínuo**:
   - Repete as etapas acima a cada intervalo de 1 hora, garantindo operações em tempo real.

---

## **Ambiente de Desenvolvimento**

Para executar este projeto, você precisa do seguinte ambiente:

- **Sistema Operacional**: Windows, macOS ou Linux
- **Python**: Versão 3.8 ou superior
- **Bibliotecas Necessárias**:
  - `pandas`
  - `python-binance`
  - `python-dotenv`

Certifique-se de instalar as dependências com o comando:
```bash
pip install -r requirements.txt
```

---

## **Boa Prática: Proteção das Chaves de API**

**Importante:** Nunca exponha suas chaves privadas de API em repositórios públicos, como o GitHub. Use arquivos `.env` para armazenar suas credenciais de forma segura. Este projeto utiliza a biblioteca `python-dotenv` para carregar as chaves diretamente do arquivo `.env`. Exemplo de configuração:

`.env`:
```plaintext
KEY_BINANCE=SuaAPIKey
SECRET_BINANCE=SuaSecretKey
```

---

## **Isenção de Responsabilidade**

Este robô não é uma recomendação de investimento. Ele foi criado apenas para fins educacionais. O mercado de criptomoedas é volátil e apresenta riscos significativos. Antes de utilizar este código, certifique-se de compreender os riscos envolvidos.

**Sugerimos** que você realize o curso da plataforma [Varos](https://plataforma.varos.com.br/) para melhor entendimento do funcionamento deste robô e das estratégias de trading.


