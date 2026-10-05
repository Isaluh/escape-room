<h1 align="center">Projeto Entregas</h1>

Sistema Java de console desenvolvido para o controle de mercadorias e seus respectivos endereços de entrega. O sistema permite cadastrar e gerenciar mercadorias, associando cada uma delas a um endereço de destino.

## Requisitos
- Java 17 ou superior
- Maven 3.8 ou superior

## Compilar e executar
```bash
mvn clean package
java -cp target/classes br.edu.entregas.Main
```

## Acesso de demonstração
- Usuário: `admin`
- Senha: `12345678`

## Passo a passo para desenvolvimento
1. Clone o projeto usando `git clone https://github.com/Isaluh/escape-room.git`;
2. Configure os parâmetros descritos abaixo;
3. Crie sua branch de desenvolvimento `git checkout -b <nome>`;
4. Desenvolva as novas funcionalidades ou correções necessárias;
5. Mantenha o código organizado e siga o padrão já utilizado no projeto;
6. Testar as alterações e executar o sistema após cada alteração relevante;
7. Verifique as funcionalidades afetadas e confirme se o comportamento esperado foi mantido;
8. Registre as alterações e descreva de forma clara as modificações realizadas com `git commit -m <mensagem>`;
10. Atualize a documentação caso novas configurações ou procedimentos tenham sido adicionados;
11. Abra um pull request para análise de merge na main.

## Parâmetros
- app.name: nome da aplicação.
- db.user: usuário utilizado para acesso ao banco de dados.
- db.password: senha utilizada para acesso ao banco de dados.
- api.token: token utilizado para autenticação em APIs.

## Dados para cadastro
Para inserir uma nova mercadoria no sistema, informe os dados da mercadoria e seu respectivo endereço de entrega no seguinte formato: (exemplo)

```json
{
  "id": 1,
  "nome": "Notebook",
  "descricao": "Notebook para escritório",
  "peso": 2.5,
  "valor": 3500.00,
  "status": "EM_TRANSITO",
  "endereco": {
    "logradouro": "Rua das Flores",
    "complemento": "Apto 202",
    "numero": "150",
    "cep": "74000-000",
    "cidade": "Goiânia",
    "estado": "GO"
  }
}
```

### Campos da mercadoria
`id:` identificador único da mercadoria. <br>
`nome:` nome da mercadoria. <br>
`descricao:` descrição da mercadoria. <br>
`peso:` peso da mercadoria. <br>
`valor:` valor da mercadoria. <br>
`status:` situação atual da entrega. <br>
`endereco:` endereço de destino da mercadoria.

### Campos do endereço
`logradouro:` rua, avenida ou outra via. <br>
`complemento:` informações adicionais, como apartamento ou bloco. <br>
`numero:` número do imóvel. <br>
`cep:` CEP do endereço. <br>
`cidade:` cidade de destino. <br>
`estado:` estado de destino (UF). <br><br>

> Cada mercadoria deve possuir exatamente um endereço de entrega.
