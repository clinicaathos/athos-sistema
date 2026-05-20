# Áthos — Sistema de Gestão de Locação de Salas

Sistema web para gestão de locação de salas da Clínica Áthos.

---

## Configuração do Firebase (passo a passo)

### 1. Obter as credenciais do Firebase

1. Acesse https://console.firebase.google.com/project/clinicaathossistema
2. Clique na engrenagem (⚙️) > **Configurações do projeto**
3. Role até **Seus aplicativos** > clique no ícone `</>`
4. Registre o app com o nome "Áthos Sistema"
5. Copie o objeto `firebaseConfig` que aparecer

### 2. Colar as credenciais no sistema

Abra o arquivo `public/index.html` e localize esta seção:

```javascript
const firebaseConfig = {
  apiKey: "COLE_AQUI_SUA_API_KEY",
  authDomain: "clinicaathossistema.firebaseapp.com",
  projectId: "clinicaathossistema",
  storageBucket: "clinicaathossistema.appspot.com",
  messagingSenderId: "COLE_AQUI_MESSAGING_ID",
  appId: "COLE_AQUI_APP_ID"
};
```

Substitua os valores `COLE_AQUI_...` pelos valores reais do seu projeto.

### 3. Ativar Autenticação

1. No Firebase Console > **Authentication** > **Sign-in method**
2. Ative **E-mail/senha**
3. Vá em **Users** > **Add user**
4. Adicione o e-mail e senha da administradora

### 4. Criar o Firestore

1. No Firebase Console > **Firestore Database**
2. Clique em **Criar banco de dados**
3. Escolha **Iniciar no modo de produção**
4. Selecione a região **southamerica-east1 (São Paulo)**
5. Clique em **Ativar**

### 5. Configurar as Regras do Firestore

1. No Firestore > aba **Regras**
2. Cole o conteúdo do arquivo `firestore.rules`
3. Clique em **Publicar**

### 6. Publicar no GitHub

1. Acesse github.com com a conta da clínica
2. Crie um novo repositório: `athos-sistema`
3. Faça upload de todos os arquivos desta pasta

### 7. Conectar Firebase com GitHub (deploy automático)

1. No Firebase Console > **Hosting** > **Começar**
2. Siga as instruções até chegar em "Connect to GitHub"
3. Selecione o repositório `clinicaathos/athos-sistema`
4. Escolha a pasta `public` como pasta de publicação
5. Clique em **Finalizar**

O sistema estará disponível em:
**https://clinicaathossistema.web.app**

---

## Coleções do Firestore

| Coleção | Descrição |
|---|---|
| `config` | Configurações gerais (salas, preços, horários) |
| `profissionais` | Cadastro completo dos profissionais |
| `locacoes` | Agendamentos e reservas de salas |
| `receitas` | Contas a receber |
| `despesas` | Contas a pagar (com histórico de edições) |
| `planos` | Pacotes de horas disponíveis |

---

## Funcionalidades

- ✅ Login seguro com Firebase Auth
- ✅ Dashboard com alertas de vencimento, aniversário e vínculo anual
- ✅ Agenda com visão Dia, Semana e Mês
- ✅ Cadastro completo de profissionais (abordagem, público-alvo, valor de sessão, endereço)
- ✅ Campo automático "Sem vínculo / Com vínculo"
- ✅ Contagem de renovações de contrato
- ✅ Contagem de horas em pacotes com barra de progresso
- ✅ Financeiro com previsão do mês seguinte
- ✅ Relatórios mensal, semestral e anual com gráficos
- ✅ Despesas editáveis com histórico de alterações
- ✅ Status clicável em Contas a Receber e Contas a Pagar
- ✅ Configurações editáveis (salas, preços, alertas)
- ✅ Backup automático via Firebase
- ✅ Responsividade mobile completa

---

## Suporte

Sistema desenvolvido por Jardel Santiago Gadelha.
