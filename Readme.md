## Bağımlılık Enjeksiyonu (Dependency Injection) ve Servis Koleksiyonları

Bu README dosyası, bağımlılık enjeksiyonu ve servis koleksiyonlarını (dependency injection ve service collection) kısa ve net bir şekilde açıklar ve .NET Core özelinde yaygın olarak kullanılan `AddSingleton`, `AddTransient`, ve `AddScoped` yöntemlerini tanıtır.

## Bağımlılık Enjeksiyonu Nedir?

Bağımlılık enjeksiyonu, bir yazılım bileşeninin diğer bileşenlere gereksinim duyduğu nesneleri (bağımlılıkları) doğrudan yaratmak yerine, bu bağımlılıkların dışarıdan verildiği bir tasarım desenidir. Bu şekilde, bileşenler daha bağımsız, daha test edilebilir ve yeniden kullanılabilir hale gelir.

## Servis Koleksiyonları (Service Collection)

Servis koleksiyonları, bağımlılıkları yönetmek ve uygulama içinde servisleri kaydetmek için kullanılan bir yapıdır. .NET Core ve ASP.NET Core gibi çerçeveler, bu işlemi kolaylaştırmak için servis koleksiyonları sağlar.

## `AddSingleton`

`AddSingleton`, uygulamanızın yaşam süresi boyunca yalnızca bir kez oluşturulan bir servis nesnesi tanımlamanıza olanak tanır. Her talep edildiğinde aynı örneği döndürür. Genellikle, uygulama düzeyinde paylaşılması gereken tekil nesneler için kullanılır.

```csharp
services.AddSingleton<ISampleService, SampleService>();
mlılık Enjeksiyonu (Dependency Injection) ve Servis Koleksiyonları

Bu README dosyası, bağımlılık enjeksiyonu ve servis koleksiyonlarını (dependency injection ve service collection) kısa ve net bir şekilde açıklar ve .NET Core özelinde yaygın olarak kullanılan `AddSingleton`, `AddTransient`, ve `AddScoped` yöntemlerini tanıtır.

## Bağımlılık Enjeksiyonu Nedir?

Bağımlılık enjeksiyonu, bir yazılım bileşeninin diğer bileşenlere gereksinim duyduğu nesneleri (bağımlılıkları) doğrudan yaratmak yerine, bu bağımlılıkların dışarıdan verildiği bir tasarım desenidir. Bu şekilde, bileşenler daha bağımsız, daha test edilebilir ve yeniden kullanılabilir hale gelir.

## Servis Koleksiyonları (Service Collection)

Servis koleksiyonları, bağımlılıkları yönetmek ve uygulama içinde servisleri kaydetmek için kullanılan bir yapıdır. .NET Core ve ASP.NET Core gibi çerçeveler, bu işlemi kolaylaştırmak için servis koleksiyonları sağlar.

## `AddSingleton`

`AddSingleton`, uygulamanızın yaşam süresi boyunca yalnızca bir kez oluşturulan bir servis nesnesi tanımlamanıza olanak tanır. Her talep edildiğinde aynı örneği döndürür. Genellikle, uygulama düzeyinde paylaşılması gereken tekil nesneler için kullanılır.

```csharp
services.AddSingleton<ISampleService, SampleService>();

AddTransient

AddTransient, her talep edildiğinde yeni bir servis örneği oluşturur. Bu, hızlı geçici nesneler için kullanışlıdır ve her kullanım için yeni bir örnek gerektiğinde tercih edilir.

csharp

services.AddTransient<ITransientService, TransientService>();

AddScoped

AddScoped, her HTTP isteği için bir kapsam (scope) boyunca aynı servis örneğini sağlar. Bu, web uygulamalarında isteğin ömrü boyunca aynı nesnenin kullanılmasını gerektiğinde kullanışlıdır.

csharp

services.AddScoped<IScopedService, ScopedService>();


Bu README.md dosyası, bağımlılık enjeksiyonunu ve servis koleksiyonlarını anlamanıza yardımcı olmak için hazırlanmıştır. Daha fazla bilgi için ilgili .NET Core veya ASP.NET Core belgelerine başvurabilirsiniz.

go

Bu örnek README.md dosyası, bağımlılık enjeksiyonu ve `AddSingleton`, `AddTransie
