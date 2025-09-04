# Fundamentos de Boas Práticas de Código

## 1. KISS – Keep It Simple, Stupid

**Princípio:** Mantenha o código simples e direto. Evite complicações desnecessárias.

**Ideia:** Se existe uma maneira simples de fazer algo, não tente reinventar a roda com soluções complexas.

**Exemplo ruim:**

```java
if (x == true) {
    return true;
} else {
    return false;
}
```

**Exemplo bom:**

```java
return x;
```

**Resumo:** Código simples é mais fácil de ler, manter e testar.

---

## 2. DRY – Don’t Repeat Yourself

**Princípio:** Não repita código. Se perceber padrões iguais, crie funções ou abstrações.

**Ideia:** Reduz erros, facilita manutenção e deixa o código mais limpo.

**Exemplo ruim:**

```java
int total1 = valor1 + valor2;
int total2 = valor3 + valor4;
```

**Exemplo bom:**

```java
int somar(int a, int b) {
    return a + b;
}

int total1 = somar(valor1, valor2);
int total2 = somar(valor3, valor4);
```

**Resumo:** Funções e métodos reutilizáveis economizam tempo e evitam bugs.

---

## 3. YAGNI – You Aren’t Gonna Need It

**Princípio:** Não crie funcionalidades que não precisa agora.

**Ideia:** Evita desperdício de tempo e complexidade no código.

**Exemplo ruim:** Criar várias formas de autenticação “por segurança futura”, quando o sistema só precisa de senha.

**Exemplo bom:** Implemente apenas a autenticação por senha agora e expanda quando necessário.

**Resumo:** Só programe o que é realmente necessário.

---

## 4. Nomenclatura significativa

**Princípio:** Variáveis, funções e classes devem ter nomes claros que descrevam seu propósito.

**Exemplo ruim:**

```java
int x;
fun1();
```

**Exemplo bom:**

```java
int totalVendas;
double calcularMediaNotas(int[] notas);
```

**Resumo:** Nomes claros ajudam qualquer pessoa (inclusive você no futuro) a entender o código sem precisar decifrar.

---

## 5. Funções pequenas e coesas

**Princípio:** Cada função deve ter uma única responsabilidade e ser curta.

**Exemplo ruim:**

```java
void processarTudo() {
    lerDados();
    processarDados();
    gerarRelatorio();
    enviarEmail();
}
```

**Exemplo bom:**

```java
void lerDados() { ... }
void processarDados() { ... }
void gerarRelatorio() { ... }
void enviarEmail() { ... }
```

**Resumo:** Funções pequenas são mais legíveis, fáceis de testar e manter.

---

## 6. Evitar duplicação e responsabilidades múltiplas

**Ideia:** Não misture várias tarefas em uma única função ou classe.

**Exemplo ruim:** Uma função que cadastra usuário, envia email e atualiza relatório.
**Exemplo bom:** Dividir em funções separadas:

```java
cadastrarUsuario();
enviarEmailBoasVindas();
atualizarRelatorio();
```

**Resumo:** Uma função = uma responsabilidade. Menos bugs e código mais organizado.

---

## 7. Código que se explica sozinho

**Princípio:** Escreva código autoexplicativo, evitando comentários desnecessários.

**Exemplo ruim:**

```java
// soma a e b
int soma = a + b;
```

**Exemplo bom:**

```java
int totalVendas = vendasJaneiro + vendasFevereiro;
```

**Resumo:** Nomes claros e funções pequenas reduzem a necessidade de comentários.
