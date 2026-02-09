# ${{ values.name }}

Projeto Spring Boot criado com Backstage.

## 🚀 Tecnologias

- Java 17
- Spring Boot 3.2.0
- Spring Web
- Spring Actuator
- Maven

## 📋 Pré-requisitos

- Java 17 ou superior
- Maven 3.6 ou superior

## 🔧 Como rodar

### Desenvolvimento

```bash
# Compilar o projeto
mvn clean install

# Executar a aplicação
mvn spring-boot:run
```

A aplicação estará disponível em `http://localhost:8080`

## 🌐 Endpoints

### Hello Endpoint
```
GET http://localhost:8080/api/hello
```

Resposta:
```json
{
  "message": "Hello from ${{ values.name }}!"
}
```

### Health Check
```
GET http://localhost:8080/actuator/health
```

## 🧪 Testes

```bash
# Executar testes
mvn test
```

## 🐳 Docker

```bash
# Build da imagem
docker build -t ${{ values.name }}:latest .

# Executar container
docker run -p 8080:8080 ${{ values.name }}:latest

