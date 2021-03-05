---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: c85ece43045144d0befd6a6ed1e7ac1d7431796f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010449"
---
# Get-AzMySqlConnectionString

## SYNOPSIS
Pobierz parametrów połączenia według dostawcy połączenia klienta.

## SKŁADNIA

### Pobierz (domyślne)
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## OPIS
Pobierz parametrów połączenia według dostawcy połączenia klienta.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie parametrów połączenia serwera MySql według nazwy grupy zasobów i serwera
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

To polecenie cmdlet pobiera ciąg połączenia serwera MySql według nazwy grupy zasobów i serwera.

### Przykład 2. Uzyskiwanie parametrów połączenia serwera MySql według tożsamości
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

To polecenie cmdlet pobiera ciąg połączenia serwera MySql według tożsamości.

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
Serwer parametrów połączenia.
Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótu.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
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

### Microsoft.Azure.PowerShell.cmdlet.mySql.models.api20171201.iServer

## DANE WYJŚCIOWE

### System.String

## NOTATKI

ALIASY

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


INPUTOBJECT: <IServer> Serwer parametrów połączenia.
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
  - `[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: czy na tym serwerze jest dozwolony dostęp do sieci publicznej. Wartość jest opcjonalna, ale jeśli zostanie przekazana, musi mieć wartość "Włączona" lub "Wyłączona".
  - `[ReplicaCapacity <Int32?>]`: Maksymalna liczba replik, które może mieć serwer główny.
  - `[ReplicationRole <String>]`: rola replikacji serwera.
  - `[SkuCapacity <Int32?>]`: Skalowanie wydajności w górę/wy, czyli jednostek obliczeniowych serwera.
  - `[SkuFamily <String>]`: Rodzina sprzętu.
  - `[SkuName <String>]`: nazwa sKU, zazwyczaj warstwa + rodzina + core, na przykład B_Gen4_1, GP_Gen5_8.
  - `[SkuSize <String>]`: Kod rozmiaru, który ma być interpretowany przez zasób w zależności od potrzeb.
  - `[SkuTier <SkuTier?>]`: warstwa określonej wersji SKU, np. Podstawowa.
  - `[SslEnforcement <SslEnforcementEnum?>]`: Włącz wymuszanie ssl lub nie wymusz w przypadku łączenia się z serwerem.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: Dni przechowywania kopii zapasowej dla serwera.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Włącz funkcję nadmiarowej lokalizacji geograficznej lub nie umożliwia tworzenia kopii zapasowej na serwerze.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Włącz automatyczne powiększanie magazynu.
  - `[StorageProfileStorageMb <Int32?>]`: Maksymalna dozwolona przestrzeń dyskowa na serwerze.
  - `[UserVisibleState <ServerState?>]`: stan serwera, który jest widoczny dla użytkownika.
  - `[Version <ServerVersion?>]`: Wersja serwera.

## LINKI POKREWNE

