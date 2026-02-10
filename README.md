# Kurrikulum-a
## Iraitz Guisado
### Informazio pertsonala

### Gustuko esparruak

- #### Informatika
Nire ikasketak informatika esparruan garatzen hari naiz

- #### Garapena
Aplikazioen garapena gustoko dut

- #### Ikerketa
Garapenaren inguruko ikerketa egitea gustoko dut

### Ikasketak

- #### Batxillergo zientifikoa 
- 2022 Iraila - 2024 Ekaina
- #### Plataforma anitzeko aplikazioen garapena
- 2024 Iraila - 2026 Maiataza

### Lan esperientzia

| Enpresa izena | Lanpostuaren izena | Zereginak | Iraupena |
| :--- | :--- | :--- | :--- |
| The Champions Burger | Zerbitzaria | Janaria eta edariak prestatu eta zerbitzatu |2024 Uztaila |
| Servicios Araba | Umeen zaintza | Umeen zaintzaz arduratu |2024 Urtarrila |
| Goerri eskola | Web garapena | Laravel erabiliz web orrialde bat garatu | 2025 Maiatza |
| Ayesa | In situ teknikaria | Hainbat intzidentzien resoluzioaz arduratu | 2025 Uztaila - 2026 Ekaina |

### Garatutako gaitasunak

#### Hainbat lenguaietan garatzeko gaitasuna dut

- Nire kode zatiak
- - C#
``` c#
  public class NHibernateSessionMiddleware
{
    private readonly RequestDelegate _next;
    private readonly ISessionFactory _sessionFactory;

    public NHibernateSessionMiddleware(RequestDelegate next, ISessionFactory sessionFactory)
    {
        _next = next;
        _sessionFactory = sessionFactory;
    }

    public async Task Invoke(HttpContext context)
    {
        var session = _sessionFactory.OpenSession();
        NHibernate.Context.CurrentSessionContext.Bind(session);

        try
        {
            await _next(context);

            if (session.IsOpen)
                await session.FlushAsync();
        }
        finally
        {
            
            NHibernate.Context.CurrentSessionContext.Unbind(_sessionFactory);

            if (session.IsOpen)
                session.Dispose();
        }
    }
}
```



- - Java
  
``` Java
    public static String pasahitzaHasheatu(String input) {
        try {
            MessageDigest digest = MessageDigest.getInstance("SHA-256");
            byte[] hash = digest.digest(input.getBytes());
            StringBuilder hexString = new StringBuilder();
            for (byte b : hash) {
                String hex = Integer.toHexString(0xff & b);
                if (hex.length() == 1) hexString.append('0');
                hexString.append(hex);
            }

            return hexString.toString();

        } catch (NoSuchAlgorithmException e) {
            throw new RuntimeException(e);
        }
    }
```



