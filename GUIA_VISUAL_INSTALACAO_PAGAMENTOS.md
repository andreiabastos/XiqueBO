# 🎨 Guia Visual - Sistema de Pagamentos XiquêGo

## 📸 Passo a Passo com Imagens

---

## 🔧 PASSO 1: Criar Arquivo .env

### Windows

```
1. Abra o Explorador de Arquivos
   📁 C:\Users\Pichau\OneDrive\Documentos\APP XIQUE GO - MOVE XIQUE XIQUE\XIQUEGO

2. Clique com botão direito → Novo → Documento de Texto

3. Nomeie o arquivo como: .env
   (com ponto no início, sem extensão)

4. Se Windows não permitir, use:
   - Abra o Bloco de Notas
   - Cole o conteúdo abaixo
   - Arquivo → Salvar Como
   - Nome: .env
   - Tipo: Todos os Arquivos (*.*)
   - Salvar
```

### Conteúdo do arquivo .env:

```env
MERCADO_PAGO_PUBLIC_KEY=TEST-5f05202a-1837-4533-8bfb-ce3ff225c0aa
MERCADO_PAGO_ACCESS_TOKEN=TEST-3592412332909878-102106-411c527d855ad54c5e4db290a1126a7d-553797548
APP_COMMISSION_PERCENTAGE=2
APP_MIN_WITHDRAWAL_AMOUNT=127
```

### ✅ Verificar

Estrutura final deve ser:
```
XIQUEGO/
├── .env                  ← Arquivo criado
├── .gitignore
├── package.json
├── app/
├── config/
└── services/
```

---

## 📱 PASSO 2: Estrutura de Telas

### Tela 1: Seleção de Método

```
┌─────────────────────────────────────┐
│  ← Pagamento da Corrida             │
├─────────────────────────────────────┤
│                                     │
│   ┌───────────────────────────┐    │
│   │  Valor total              │    │
│   │  R$ 50,00                 │    │
│   │                           │    │
│   │  Motorista: R$ 49,00      │    │
│   │  Taxa (2%): R$ 1,00       │    │
│   └───────────────────────────┘    │
│                                     │
│   Escolha a forma de pagamento      │
│                                     │
│   ┌─────────────────────────────┐  │
│   │ 📱  PIX                     │  │
│   │     Aprovação instantânea   │  │
│   └─────────────────────────────┘  │
│                                     │
│   ┌─────────────────────────────┐  │
│   │ 💳  Cartão Crédito/Débito   │  │
│   │     Todas as bandeiras      │  │
│   └─────────────────────────────┘  │
│                                     │
│   ┌─────────────────────────────┐  │
│   │ 💵  Dinheiro                │  │
│   │     Pague ao motorista      │  │
│   └─────────────────────────────┘  │
│                                     │
│   🔒 Pagamento Seguro               │
│   Criptografia ponta a ponta        │
│                                     │
└─────────────────────────────────────┘
```

---

### Tela 2: Pagamento PIX

```
┌─────────────────────────────────────┐
│  ← Pagamento via PIX                │
├─────────────────────────────────────┤
│                                     │
│   ┌───────────────────────────┐    │
│   │  Valor a pagar            │    │
│   │  R$ 50,00                 │    │
│   └───────────────────────────┘    │
│                                     │
│   ⏱️  Tempo restante: 9:45          │
│                                     │
│   Instruções:                       │
│   1️⃣ Abra o app do seu banco        │
│   2️⃣ Escolha pagar com PIX          │
│   3️⃣ Escaneie o QR Code             │
│   4️⃣ Confirme o pagamento           │
│                                     │
│   QR Code PIX                       │
│   ┌─────────────────────────┐      │
│   │                         │      │
│   │    ███████  ███  ███    │      │
│   │    █     █  █ █  █ █    │      │
│   │    █ ███ █  ███  ███    │      │
│   │    █ ███ █  █ █  █ █    │      │
│   │    ███████  ███  ███    │      │
│   │                         │      │
│   └─────────────────────────┘      │
│                                     │
│   Chave PIX Copia e Cola            │
│   ┌─────────────────────────────┐  │
│   │ 00020126360014BR.GOV.BCB... │  │
│   └─────────────────────────────┘  │
│                                     │
│   [ 📋 Copiar Chave PIX ]           │
│                                     │
│   [ 🔍 Verificar Pagamento ]        │
│                                     │
└─────────────────────────────────────┘
```

---

### Tela 3: Pagamento com Cartão

```
┌─────────────────────────────────────┐
│  ← Pagamento com Cartão             │
├─────────────────────────────────────┤
│                                     │
│   ┌───────────────────────────┐    │
│   │  Valor a pagar            │    │
│   │  R$ 50,00                 │    │
│   └───────────────────────────┘    │
│                                     │
│   Dados do Cartão                   │
│                                     │
│   Número do Cartão                  │
│   ┌─────────────────────────────┐  │
│   │ 0000 0000 0000 0000         │  │
│   └─────────────────────────────┘  │
│                                     │
│   Nome no Cartão                    │
│   ┌─────────────────────────────┐  │
│   │ NOME COMPLETO               │  │
│   └─────────────────────────────┘  │
│                                     │
│   Validade        CVV               │
│   ┌─────────┐   ┌─────────┐        │
│   │ MM/AA   │   │ 123     │        │
│   └─────────┘   └─────────┘        │
│                                     │
│   CPF do Titular                    │
│   ┌─────────────────────────────┐  │
│   │ 000.000.000-00              │  │
│   └─────────────────────────────┘  │
│                                     │
│   Parcelamento                      │
│   [1x] [2x] [3x] [4x] [5x] [6x]    │
│                                     │
│   [ Pagar R$ 50,00 ]                │
│                                     │
│   🔒 Transação Segura               │
│                                     │
└─────────────────────────────────────┘
```

---

### Tela 4: Pagamento em Dinheiro

```
┌─────────────────────────────────────┐
│  ← Pagamento em Dinheiro            │
├─────────────────────────────────────┤
│                                     │
│   ┌───────────────────────────┐    │
│   │  Valor a pagar            │    │
│   │  R$ 50,00                 │    │
│   └───────────────────────────┘    │
│                                     │
│           💵                        │
│                                     │
│   Como funciona                     │
│                                     │
│   1️⃣ Cliente paga ao motorista      │
│   2️⃣ Motorista confirma no app      │
│   3️⃣ Taxa 2% descontada no saque    │
│                                     │
│   Detalhamento                      │
│   ┌─────────────────────────────┐  │
│   │ Valor total:     R$ 50,00   │  │
│   │ ─────────────────────────── │  │
│   │ Motorista:       R$ 49,00   │  │
│   │ Taxa (2%):       R$ 1,00    │  │
│   └─────────────────────────────┘  │
│                                     │
│   ⚠️ Atenção Motorista               │
│   Confirme SOMENTE após             │
│   receber o dinheiro                │
│                                     │
│   [ ✓ Confirmar Recebimento ]       │
│                                     │
└─────────────────────────────────────┘
```

---

## 🎯 Fluxo Visual Completo

```
┌─────────────┐
│   Cliente   │
│  finaliza   │
│   corrida   │
└──────┬──────┘
       │
       ↓
┌─────────────────────────────────┐
│  Tela: payment-selection        │
│                                 │
│  Valor: R$ 50,00                │
│  Motorista: R$ 49,00            │
│  Taxa: R$ 1,00                  │
│                                 │
│  [ PIX ]                        │
│  [ Cartão ]                     │
│  [ Dinheiro ]                   │
└─────────────────────────────────┘
       │
       ├──────────┬──────────┐
       │          │          │
       ↓          ↓          ↓
   ┌─────┐    ┌──────┐  ┌─────────┐
   │ PIX │    │Cartão│  │Dinheiro │
   └──┬──┘    └───┬──┘  └────┬────┘
      │           │          │
      ↓           ↓          ↓
   ┌─────┐    ┌──────┐  ┌─────────┐
   │QR   │    │Form  │  │Confirma │
   │Code │    │Card  │  │Motorista│
   └──┬──┘    └───┬──┘  └────┬────┘
      │           │          │
      └───────────┴──────────┘
                  │
                  ↓
          ┌───────────────┐
          │  ✅ Aprovado  │
          │               │
          │  Corrida      │
          │  finalizada   │
          └───────────────┘
```

---

## 🧪 Testes Visuais

### Teste 1: Botão de Teste (DEBUG)

Adicione na Página Inicial:

```typescript
{__DEV__ && (
  <View style={{
    position: 'absolute',
    bottom: 100,
    right: 20,
    backgroundColor: 'red',
    padding: 15,
    borderRadius: 10,
  }}>
    <TouchableOpacity 
      onPress={() => router.push('/payment-selection?amount=99.90')}
    >
      <Text style={{ color: 'white', fontWeight: 'bold' }}>
        💳 TESTE
      </Text>
    </TouchableOpacity>
  </View>
)}
```

**Resultado Visual:**

```
┌─────────────────────────────────────┐
│  Página Inicial                     │
│                                     │
│  [Mapa]                             │
│                                     │
│  [Origem]                           │
│  [Destino]                          │
│                                     │
│                                     │
│                      ┌──────────┐   │
│                      │ 💳 TESTE │   │ ← BOTÃO
│                      └──────────┘   │
│                                     │
│  [Início] [Atividades] [Perfil]    │
└─────────────────────────────────────┘
```

---

### Teste 2: Integração com Corrida

```
Antes da Corrida:
┌─────────────────────────────────────┐
│  📍 Origem: Centro                  │
│  🎯 Destino: Perto Velha            │
│                                     │
│  Valor estimado: R$ 35,00           │
│                                     │
│  [ Solicitar Corrida ]              │
└─────────────────────────────────────┘

Durante a Corrida:
┌─────────────────────────────────────┐
│  🚗 Corrida em Andamento            │
│                                     │
│  Motorista: João                    │
│  Placa: ABC-1234                    │
│                                     │
│  [Mapa em tempo real]               │
│                                     │
│  Valor: R$ 35,00                    │
└─────────────────────────────────────┘

Ao Finalizar:
┌─────────────────────────────────────┐
│  ✅ Corrida Finalizada              │
│                                     │
│  Origem: Centro                     │
│  Destino: Perto Velha               │
│  Distância: 5 km                    │
│                                     │
│  Valor: R$ 35,00                    │
│                                     │
│  [ Ir para Pagamento ]  ← NOVO     │
└─────────────────────────────────────┘
       │
       ↓
┌─────────────────────────────────────┐
│  Pagamento da Corrida               │
│  [PIX] [Cartão] [Dinheiro]          │
└─────────────────────────────────────┘
```

---

## 📊 Dashboard de Pagamentos (Futuro)

```
┌─────────────────────────────────────┐
│  Pagamentos - Hoje                  │
├─────────────────────────────────────┤
│                                     │
│  Total Recebido: R$ 450,00          │
│  ├─ PIX:      R$ 200,00 (40%)      │
│  ├─ Cartão:   R$ 150,00 (35%)      │
│  └─ Dinheiro: R$ 100,00 (25%)      │
│                                     │
│  Comissão XiquêGo: R$ 9,00 (2%)     │
│  Motoristas: R$ 441,00 (98%)        │
│                                     │
│  Transações                         │
│  ┌─────────────────────────────┐   │
│  │ 10:30 - PIX    - R$ 25,00   │   │
│  │ 11:15 - Cartão - R$ 35,00   │   │
│  │ 12:00 - Dinhe. - R$ 20,00   │   │
│  │ 13:45 - PIX    - R$ 40,00   │   │
│  └─────────────────────────────┘   │
│                                     │
└─────────────────────────────────────┘
```

---

## 🎨 Paleta de Cores Usada

```
PIX (Verde):
  Background: #4CAF50
  Hover: #45a049
  Text: #FFFFFF

Cartão (Azul):
  Background: #2196F3
  Hover: #1976D2
  Text: #FFFFFF

Dinheiro (Laranja):
  Background: #FF9800
  Hover: #F57C00
  Text: #FFFFFF

Sucesso (Verde Claro):
  Background: #e8f5e9
  Border: #4CAF50
  Text: #2e7d32

Erro (Vermelho):
  Background: #ffebee
  Border: #f44336
  Text: #c62828

Alerta (Amarelo):
  Background: #fff3e0
  Border: #ffc107
  Text: #e65100
```

---

## 📱 Responsividade

### Mobile (375px)
```
┌──────────────┐
│              │
│   [Botões]   │
│   ocupam     │
│   100% da    │
│   largura    │
│              │
└──────────────┘
```

### Tablet (768px)
```
┌─────────────────────┐
│                     │
│   [Botões com]      │
│   [padding maior]   │
│                     │
└─────────────────────┘
```

---

## ✅ Checklist Visual

- [ ] Arquivo `.env` criado
- [ ] App reiniciado após criar `.env`
- [ ] Botão de teste adicionado
- [ ] Tela de seleção carrega
- [ ] Tela PIX mostra QR Code
- [ ] Tela Cartão aceita input
- [ ] Tela Dinheiro mostra cálculo
- [ ] Navegação entre telas funciona
- [ ] Cores estão corretas
- [ ] Textos legíveis
- [ ] Botões responsivos ao toque

---

## 🎉 Resultado Final Visual

```
          ANTES                      DEPOIS
┌──────────────────┐      ┌──────────────────┐
│                  │      │                  │
│  Finalizar       │      │  Finalizar e     │
│  Corrida         │  →   │  [💳 Pagar]      │
│                  │      │                  │
│  (sem pagamento) │      │  PIX/Cartão/$$   │
│                  │      │                  │
└──────────────────┘      └──────────────────┘

Agora com 3 métodos integrados! ✨
```

---

**XiquêGo - Visual e Funcional! 🚗💳🎨**




