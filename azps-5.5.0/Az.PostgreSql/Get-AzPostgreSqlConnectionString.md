---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
ms.openlocfilehash: 7f2040455e48130615a52ba06186b189b67ea971
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191426"
---
# Get-AzPostgreSqlConnectionString

## SYNOPSIS
Pobierz parametrów połączenia według dostawcy połączenia klienta.

## SKŁADNIA

### Pobierz (domyślne)
```
Get-AzPostgreSqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzPostgreSqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## OPIS
Pobierz parametrów połączenia według dostawcy połączenia klienta.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie parametrów połączenia serwera PostgreSql według nazwy grupy zasobów i serwera
```powershell
PS C:\> Get-AzPostgreSqlConnectionString -Client ADO.NET -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG

Server=postgresqltestserver.postgres.database.azure.com;Database={your_database};Port=5432;User Id=pwsh@postgresqltestserver;Password={your_password};Ssl Mode=Require;
```

To polecenie cmdlet pobiera ciąg połączenia serwera PostgreSql według nazwy grupy zasobów i serwera.

### Przykład 2. Uzyskiwanie parametrów połączenia serwera PostgreSql według tożsamości
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh@postgresqltestserver password={your_password} sslmode=require
```

To polecenie cmdlet pobiera ciąg połączenia serwera PostgreSql według tożsamości.

## PARAMETERS

### —Klient
Dostawca połączenia klienta.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Serwer parametrów połączenia Do skonstruowania, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótów.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Nazwa
Nazwa serwera.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów zawierającej zasób. Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - SubscriptionId
Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20171201.IServer

## DANE WYJŚCIOWE

### System.String

## NOTATKI

ALIASY

COMPLEX PARAMETER PROPERTIES

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


INPUTOBJECT: <IServer> serwer parametrów połączenia
  - `Location <String>`: lokalizacja geograficzna, w której znajduje się zasób
  - `[Tag <ITrackedResourceTags>]`: tagi zasobów.
    - `[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.
  - `[AdministratorLogin <String>]`: nazwa logowania administratora serwera. Można określić tylko wtedy, gdy serwer jest tworzony (i jest wymagany do utworzenia).
  - `[EarliestRestoreDate <DateTime?>]`: najwcześniejszy czas tworzenia punktów przywracania (format ISO8601)
  - `[FullyQualifiedDomainName <String>]`: w pełni kwalifikowana nazwa domeny serwera.
  - `[IdentityType <IdentityType?>]`: typ tożsamości. Ustaw tę wartość na "SystemAssigned", aby automatycznie utworzyć i przypisać do zasobu podmiot zabezpieczeń usługi Azure Active Directory.
  - `[InfrastructureEncryption <InfrastructureEncryption?>]`: Stan pokazujący, czy szyfrowanie infrastruktury było włączone dla serwera.
  - `[MasterServerId <String>]`: Główny identyfikator serwera repliki.
  - `[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: wymuszanie minimalnej wersji Tls dla serwera.
  - `[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: czy dla tego serwera jest dozwolony dostęp do sieci publicznej. Wartość jest opcjonalna, ale jeśli zostanie przekazana, musi mieć wartość "Włączone" lub "Wyłączone".
  - `[ReplicaCapacity <Int32?>]`: Maksymalna liczba replik, które może mieć serwer główny.
  - `[ReplicationRole <String>]`: rola replikacji serwera.
  - `[SkuCapacity <Int32?>]`: Skalowanie wydajności w górę/wy, czyli jednostek obliczeniowych serwera.
  - `[SkuFamily <String>]`: Rodzina sprzętu.
  - `[SkuName <String>]`: nazwa sKU, zazwyczaj warstwa + rodzina + podstawy, na przykład B_Gen4_1, GP_Gen5_8.
  - `[SkuSize <String>]`: Kod rozmiaru, który ma być interpretowany przez zasób w zależności od potrzeb.
  - `[SkuTier <SkuTier?>]`: warstwa określonej wersji SKU, np. Podstawowa.
  - `[SslEnforcement <SslEnforcementEnum?>]`: Włącz wymuszanie ssl lub nie wymusz w przypadku łączenia się z serwerem.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: Dni przechowywania kopii zapasowej dla serwera.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Włącz funkcję nadmiarowej lokalizacji geograficznej lub nie umożliwia tworzenia kopii zapasowej na serwerze.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Włącz automatyczne powiększanie magazynu.
  - `[StorageProfileStorageMb <Int32?>]`: Maksymalna dozwolona ilość miejsca do magazynowania na serwerze.
  - `[UserVisibleState <ServerState?>]`: stan serwera widoczny dla użytkownika.
  - `[Version <ServerVersion?>]`: Wersja serwera.

## LINKI POKREWNE

