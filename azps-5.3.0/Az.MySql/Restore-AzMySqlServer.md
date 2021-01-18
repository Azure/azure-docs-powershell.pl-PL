---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restore-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
ms.openlocfilehash: 7a53cefa9aca7e4ea679b31763c19e82d4d1e841
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498897"
---
# Restore-AzMySqlServer

## STRESZCZENIe
Przywracanie serwera z istniejącej kopii zapasowej

## POLECENIA

### Subrestore (domyślne)
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### PointInTimeRestore
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## Opis
Przywracanie serwera z istniejącej kopii zapasowej

## Przykłady

### Przykład 1: Przywracanie serwera MySql przy użyciu funkcji przywracania rerepliki
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test-replica | Restore-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -UseGeoRestore 

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

To polecenie cmdlet przywraca serwer MySql przy użyciu funkcji przywracania replik.

### Przykład 2: Przywracanie serwera MySql przy użyciu funkcji przywracania PointInTime
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-restore eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

Te polecenia cmdlet Przywróć serwer MySql przy użyciu funkcji przywracania PointInTime.

## PARAMETRÓW

### -AsJob
Uruchom polecenie jako zadanie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Inputobject
Źródłowy obiekt serwera do przywrócenia.
Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Lokalizacja
Miejsce, w którym znajduje się zasób.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa serwera.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nowait
Uruchom polecenie asynchronicznie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów zawierającej dany zasób możesz uzyskać tę wartość z interfejsu API Menedżera zasobów platformy Azure lub portalu.

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

### -RestorePointInTime
Miejsce, w którym znajduje się zasób.

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subskrypcji
Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Metadane specyficzne dla aplikacji w postaci par klucz-wartość.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseGeoRestore
Przywracanie za pomocą trybu geograficznego

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsePointInTimeRestore
Przywracanie za pomocą trybu PointInTime

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IServer

## WYSYŁA

### Microsoft. Azure. PowerShell. cmdlet. MySql. MODELES. Api20171201. IServer

## INFORMACYJN

PISUJE

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.


WEJŚCIE <IServer> : obiekt serwera źródłowego do przywrócenia.
  - `Location <String>`: Lokalizacja geograficzna, w której mieszka zasób
  - `SkuName <String>`: Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.
  - `[Tag <ITrackedResourceTags>]`: Znaczniki zasobów.
    - `[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.
  - `[AdministratorLogin <String>]`: Nazwa logowania administratora serwera. Można określić tylko podczas tworzenia serwera (i jest on wymagany do utworzenia).
  - `[EarliestRestoreDate <DateTime?>]`: Najwcześniejszy czas tworzenia punktu przywracania (format ISO8601)
  - `[FullyQualifiedDomainName <String>]`: W pełni kwalifikowana nazwa domeny serwera.
  - `[IdentityType <IdentityType?>]`: Typ tożsamości. Ustaw tę wartość na "SystemAssigned", aby automatycznie utworzyć i przypisać podmiot zabezpieczeń usługi Azure Active Directory dla tego zasobu.
  - `[InfrastructureEncryption <InfrastructureEncryption?>]`: Stan wskazujący, czy na serwerze włączono szyfrowanie infrastruktury.
  - `[MasterServerId <String>]`: Identyfikator głównego serwera repliki.
  - `[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Wymuszanie minimalnej wersji protokołu TLS dla serwera.
  - `[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Określanie, czy dla tego serwera jest dozwolony dostęp do sieci publicznej. Wartość jest opcjonalna, ale jeśli została przekazana, musi być "włączone" lub "wyłączone".
  - `[ReplicaCapacity <Int32?>]`: Maksymalna liczba replik, które może mieć serwer główny.
  - `[ReplicationRole <String>]`: Rola replikacji serwera.
  - `[SkuCapacity <Int32?>]`: Wydajność skalowania w górę/poza, reprezentująca jednostki obliczeniowe serwera.
  - `[SkuFamily <String>]`: Rodzina sprzętu.
  - `[SkuSize <String>]`: Kod rozmiaru, który ma być interpretowany według odpowiednich zasobów.
  - `[SkuTier <SkuTier?>]`: Warstwa konkretnej jednostki SKU, na przykład podstawowa.
  - `[SslEnforcement <SslEnforcementEnum?>]`: Włączanie wymuszania protokołu SSL lub nie podczas nawiązywania połączenia z serwerem.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: Dni przechowywania kopii zapasowej serwera.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Włączanie geograficznie nadmiarowych lub niezwiązanych z kopią zapasową serwera.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Włączanie automatycznego zwiększania przestrzeni dyskowej.
  - `[StorageProfileStorageMb <Int32?>]`: Maksymalna ilość miejsca do magazynowania dozwolona dla serwera.
  - `[UserVisibleState <ServerState?>]`: Stan serwera, który jest widoczny dla użytkownika.
  - `[Version <ServerVersion?>]`: Wersja serwera.

## LINKI POKREWNE

