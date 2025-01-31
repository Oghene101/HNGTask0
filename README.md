# ASP.NET Core Web API - Details Endpoint

This project is a simple ASP.NET Core Web API that provides details such as email, current UTC timestamp, and GitHub repository URL via a GET endpoint.

## Prerequisites

- .NET 6.0 SDK or later ([Download .NET](https://dotnet.microsoft.com/download))
- Any IDE supporting .NET development (e.g., JetBrains Rider, Visual Studio, or VS Code)

## Setup Instructions

### 1. Clone the Repository

```sh
git clone https://github.com/Oghene101/HNGTask0.git
cd HNGTask0
```

### 2. Restore Dependencies

```sh
dotnet restore
```

### 3. Run the Project

```sh
dotnet run
```

The API will start and be accessible at `http://localhost:5260` (or another port if configured).

---

## API Documentation

### **Endpoint: Get Details**

**URL:**

```http
GET /details
```

**Response Format:**

```json
{
    "email": "ogheneruemu.engineer@gmail.com",
    "date": "2024-01-31T12:34:56.789Z",
    "gitHubUrl": "https://github.com/Oghene101/HNGTask0"
}
```

### **Example Usage**

#### Using cURL

```sh
curl -X GET http://localhost:5260/details
```

#### Using Postman

1. Open Postman.
2. Create a new GET request.
3. Enter the URL: `http://localhost:5260/details`.
4. Click **Send**.

#### Using C# HttpClient

```csharp
using System;
using System.Net.Http;
using System.Threading.Tasks;

class Program
{
    static async Task Main()
    {
        HttpClient client = new HttpClient();
        var response = await client.GetStringAsync("http://localhost:5260/details");
        Console.WriteLine(response);
    }
}
```

---

## License

This project is open-source and available under the MIT License.

