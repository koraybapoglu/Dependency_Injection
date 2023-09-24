# Bağımlılık Enjeksiyonu ve Servis Koleksiyonları

Bu README dosyası, bağımlılık enjeksiyonu (dependency injection) kavramını ve .NET Core'da kullanılan `AddSingleton`, `AddTransient`, ve `AddScoped` yöntemlerini basit ve net bir şekilde açıklar.

## Bağımlılık Enjeksiyonu Nedir?

Bağımlılık enjeksiyonu, bir yazılım bileşeninin ihtiyaç duyduğu nesneleri doğrudan oluşturmak yerine, bu nesnelerin dışarıdan sağlandığı bir tasarım desenidir. Bu yaklaşım, kodun daha bağımsız, test edilebilir ve yeniden kullanılabilir olmasını sağlar.

## Servis Koleksiyonları (Service Collection)

Servis koleksiyonları, bağımlılıkları yönetmek ve servisleri kaydetmek için kullanılan yapılar olarak düşünülebilir. .NET Core gibi çerçeveler, bu işlemi kolaylaştırmak için servis koleksiyonları sunar.

## `AddSingleton`, `AddTransient`, ve `AddScoped`

- `AddSingleton`: Uygulama yaşam döngüsü boyunca sadece bir örneği paylaşır. Uygulama düzeyinde tekil nesneler için kullanışlıdır.

services.AddSingleton<ISampleService, SampleService>();

-`AddTransient`: Her talep edildiğinde yeni bir örnek oluşturur. Hızlı geçici nesneler için kullanılır.

services.AddTransient<ITransientService, TransientService>();

`AddScoped`: Her HTTP isteği için aynı örneği paylaşır. Web uygulamalarında isteğin ömrü boyunca aynı nesnenin kullanılması gerektiğinde kullanılır.

services.AddScoped<IScopedService, ScopedService>();
