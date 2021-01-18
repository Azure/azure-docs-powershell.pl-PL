---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 0ce25af607d2460abf2ec4585dacc124a1f2e65c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500801"
---
# New-AzMariaDbReplica

## STRESZCZENIe
Tworzenie repliki serwera MariaDB.

## POLECENIA

### Nazwa_serwera (domyślnie)
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Serverobject
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## Opis
Tworzenie repliki serwera MariaDB.

## Przykłady

### Przykład 1. Tworzenie bazy danych repliki dla MariaDB
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

To polecenie tworzy bazę danych repliki dla MariaDB.

### Przykład 2: Tworzenie bazy danych repliki dla MariaDB
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

To polecenie tworzy bazę danych repliki dla MariaDB.

### Przykład 3: Tworzenie bazy danych repliki dla MariaDB
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

To polecenie z parametrem inputobject powoduje utworzenie bazy danych repliki z parametrem inputobject dla MariaDB.

## PARAMETRÓW

### -AsJob
Uruchamianie polecenia jako zadania

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
Region DefaultParameters poświadczenia, konto, dzierżawca i abonament używane do komunikacji z usługą Azure.

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

### -Master
Źródłowy obiekt serwera do przywrócenia.
Aby skonstruować, zobacz sekcję notatki dla właściwości wzorca i Utwórz tablicę skrótów.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MASTERNAME
Nazwa serwera MariaDB.

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nowait
Wykonywanie polecenia asynchronicznie

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

### -Replicaname
Nazwa repliki.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicaServerName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.

```yaml
Type: System.String
Parameter Sets: ServerName
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
Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.

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

### Microsoft. Azure. PowerShell. polecenia. MariaDb. models. Api20180601Preview. IServer

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. MariaDb. models. Api20180601Preview. IServer

## INFORMACYJN

PISUJE

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.


WZORZEC <IServer> : źródłowy obiekt serwera do przywrócenia.
  - `Location <String>`: Lokalizacja, w której znajduje się zasób.
  - `[Tag <ITrackedResourceTags>]`: Metadane specyficzne dla aplikacji w postaci par klucz-wartość.
    - `[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.
  - `[AdministratorLogin <String>]`: Nazwa logowania administratora serwera. Można określić tylko podczas tworzenia serwera (i jest on wymagany do utworzenia).
  - `[EarliestRestoreDate <DateTime?>]`: Najwcześniejszy czas tworzenia punktu przywracania (format ISO8601)
  - `[FullyQualifiedDomainName <String>]`: W pełni kwalifikowana nazwa domeny serwera.
  - `[IdentityType <IdentityType?>]`: Typ tożsamości. Ustaw tę wartość na "SystemAssigned", aby automatycznie utworzyć i przypisać podmiot zabezpieczeń usługi Azure Active Directory dla tego zasobu.
  - `[MasterServerId <String>]`: Identyfikator głównego serwera repliki.
  - `[ReplicaCapacity <Int32?>]`: Maksymalna liczba replik, które może mieć serwer główny.
  - `[ReplicationRole <String>]`: Rola replikacji serwera.
  - `[SkuCapacity <Int32?>]`: Wydajność skalowania w górę/poza, reprezentująca jednostki obliczeniowe serwera.
  - `[SkuFamily <String>]`: Rodzina sprzętu.
  - `[SkuName <String>]`: Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.
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

