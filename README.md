# VentasReportApi
API .NET 6 que expone reportes de ventas por cliente.

## Requisitos
- .NET 6 SDK
- SQL Server (LocalDB, Express o contenedor Docker)

## Ejecutar
1. Configurar `appsettings.json` -> ConnectionStrings:DefaultConnection
2. Aplicar migraciones:
   - `dotnet ef database update`
   - (o ejecutar `dotnet run` si en Program.cs se llama a Migrate())
3. Ejecutar:
   - `dotnet run`
4. Abrir Swagger:
   - `https://localhost:5001/swagger/index.html`

## Endpoint principal
- `GET /api/reportes/ventas-por-cliente` -> devuelve `{ clienteId, cliente, totalVentas }`
