---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/new-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: 554ebe0e6c4ef8a4b0d262071595c0dc6336f482
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055836"
---
# New-AzsNetworkQuota

## STRESZCZENIe
Tworzenie lub aktualizowanie przydziału.

## POLECENIA

### Rozszerzenie (domyślne)
```
New-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Tworzonych
```
New-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CreateViaIdentity
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> -Quota <IQuota> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CreateViaIdentityExpanded
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-MaxLoadBalancersPerSubscription <Int64>]
 [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxSecurityGroupsPerSubscription <Int64>] [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Opis
Tworzenie lub aktualizowanie przydziału.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

Utwórz nowy przydział sieci z wartościami domyślnymi.

### --------------------------PRZYKŁAD 2--------------------------
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```
Utwórz nowy przydział sieci z wartościami niedomyślnymi przydziału.



## PARAMETRÓW

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
Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### — Lokalizacja
Lokalizacja zasobu.

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxLoadBalancersPerSubscription
Maksymalna liczba modułów równoważenia obciążenia, które może inicjować abonament dzierżawy.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxNicsPerSubscription
Maksymalna liczba kart sieciowych, które może inicjować abonament dzierżawy.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxPublicIpsPerSubscription
Maksymalna liczba publicznych adresów IP, które może inicjować abonament dzierżawy.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxSecurityGroupsPerSubscription
Maksymalna liczba grup zabezpieczeń, które może inicjować abonament dzierżawy.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxVirtualNetworkGatewayConnectionsPerSubscription
Maksymalna liczba połączeń bramy sieci wirtualnej, które mogą być obsługiwane przez subskrypcję dzierżawy.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxVirtualNetworkGatewaysPerSubscription
Maksymalna liczba wirtualnych bram sieciowych, które mogą inicjować abonament dzierżawy.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxVnetsPerSubscription
Maksymalna liczba sieci wirtualnych, których może postanowić abonament dzierżawy.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### -Name (nazwa)
Nazwa zasobu.

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Przydział
Zasób przydział sieci.
Aby skonstruować, zobacz sekcję notatki dla właściwości przydziału i Utwórz tablicę skrótów.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -Subskrypcji
Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.
Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### -Tag
Lista par kluczy wartości.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
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

### Microsoft. Azure. PowerShell. polecenia. NetworkAdmin. models. Api20150615. IQuota

### Microsoft. Azure. PowerShell. polecenia. NetworkAdmin. models. INetworkAdminIdentity

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. NetworkAdmin. models. Api20150615. IQuota



## INFORMACYJN

ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości. Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.

INPUTobject <INetworkAdminIdentity> : parametr Identity
  - `[Id <String>]`: Ścieżka tożsamości zasobu
  - `[Location <String>]`: Lokalizacja zasobu.
  - `[ResourceName <String>]`: Nazwa zasobu.
  - `[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.

PRZYDZIAŁ <IQuota> : zasób przydział sieci.
  - `[Tag <IResourceTags>]`: Lista par kluczy wartości.
    - `[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.
  - `[MaxLoadBalancersPerSubscription <Int64?>]`: Maksymalna liczba modułów równoważenia obciążenia, które może inicjować abonament dzierżawy.
  - `[MaxNicsPerSubscription <Int64?>]`: Maksymalna liczba kart sieciowych, które może inicjować abonament dzierżawy.
  - `[MaxPublicIpsPerSubscription <Int64?>]`: Maksymalna liczba publicznych adresów IP, które może inicjować abonament dzierżawy.
  - `[MaxSecurityGroupsPerSubscription <Int64?>]`: Maksymalna liczba grup zabezpieczeń, które może inicjować abonament dzierżawy.
  - `[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maksymalna liczba połączeń bramy sieci wirtualnej, których może postanowić subskrypcja dzierżawy.
  - `[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maksymalna liczba wirtualnych bram sieciowych, które mogą inicjować abonament dzierżawy.
  - `[MaxVnetsPerSubscription <Int64?>]`: Maksymalna liczba sieci wirtualnych, których może postanowić abonament dzierżawy.

## LINKI POKREWNE

