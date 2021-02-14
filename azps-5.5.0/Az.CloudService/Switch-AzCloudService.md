---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/Switch-AzCloudService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
ms.openlocfilehash: f10d11dbbe98c098286a072d5882bf5d3a464d8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195114"
---
# Switch-AzCloudService

## SYNOPSIS
Zamienia punkty VIP między dwoma równoważeniem obciążenia usług w chmurze (wsparcie rozszerzone).

## SKŁADNIA

### CloudServiceName (Domyślna)
```
Switch-AzCloudService -CloudServiceName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Async] [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CloudService
```
Switch-AzCloudService -CloudService <CloudService> [-SubscriptionId <String>] [-Async]
 [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## OPIS
Zamienia punkty VIP między dwoma równoważeniem obciążenia usług w chmurze (wsparcie rozszerzone).

## PRZYKŁADY

### Przykład 1. Przełączanie usługi w chmurze przy użyciu nazwy
```powershell
PS C:\> Switch-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

Powyższe polecenie wywoła operację vipswap w usłudze w chmurze o nazwie "BService" i wykona operację, gdy użytkownik potwierdzi akcję w wierszu potwierdzenia.
Usługa "BService" zostanie zamieniona na usługę w chmurze, która można zamienić.

### Przykład 2. Przełączanie usługi w chmurze przy użyciu obiektu usługi w chmurze
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Switch-AzCloudService -CloudService $cs

```

Powyższe polecenie wywoła operację vipswap w usłudze w chmurze o nazwie "BService" i wykona operację, gdy użytkownik potwierdzi akcję w wierszu potwierdzenia.
Usługa "BService" zostanie zamieniona na usługę w chmurze, która można zamienić.

## PARAMETERS

### — AsJob
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

### — Async


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

### — CloudService
Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach usługi CLOUDSERVICE i utworzyć tabelę skrótu.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudService
Parameter Sets: CloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloudServiceName


```yaml
Type: System.String
Parameter Sets: CloudServiceName
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

### -ResourceGroupName


```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - SubscriptionId
Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.
Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.

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

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

## DANE WYJŚCIOWE

### System.Boolean

## NOTATKI

ALIASY

COMPLEX PARAMETER PROPERTIES

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


<CloudService>CLOUDSERVICE: 
  - `Location <String>`: lokalizacja zasobu.
  - `[Configuration <String>]`: określa konfigurację usługi XML (cscfg) dla usługi w chmurze.
  - `[ConfigurationUrl <String>]`: Określa adres URL, który odwołuje się do lokalizacji konfiguracji usługi w usłudze obiektów blob. Adres URL pakietu usługi może być URI podpisu dostępu udostępnionego (SAS) z dowolnego konta magazynu.         Jest to właściwość tylko do zapisu i nie jest zwracana w wywołaniach GET.
  - `[ExtensionProfile <ICloudServiceExtensionProfile>]`: w tym artykule opisano profil rozszerzenia usługi w chmurze.
    - `[Extension <IExtension[]>]`: Lista rozszerzeń dla usługi w chmurze.
      - `[AutoUpgradeMinorVersion <Boolean?>]`: Jawnie określ, czy platforma może automatycznie uaktualniać typHandlerVersion do wyższych wersji pomocniczych, gdy staną się dostępne.
      - `[ForceUpdateTag <String>]`: Tag wymusza zastosowanie podanych ustawień publicznych i chronionych.         Zmiana wartości tagu umożliwia ponowne uruchomienie rozszerzenia bez zmieniania jakichkolwiek ustawień publicznych i chronionych.         Jeśli forceUpdateTag nie zostanie zmieniony, program obsługi nadal będzie stosować aktualizacje ustawień publicznych lub chronionych.         Jeśli ani forceUpdateTag, ani żadne ustawienia publiczne lub chronione nie ujdą, rozszerzenie przepływa do wystąpienia roli z tym samym numerem sekwencji, a implementacja programu obsługi może być uruchamiana ponownie, czy nie.
      - `[Name <String>]`: nazwa rozszerzenia.
      - `[ProtectedSetting <String>]`: chronione ustawienia rozszerzenia, które są szyfrowane przed wysłaniem do wystąpienia roli.
      - `[ProtectedSettingFromKeyVaultSecretUrl <String>]`: 
      - `[Publisher <String>]`: nazwa wydawcy programu obsługi rozszerzenia.
      - `[RolesAppliedTo <String[]>]`: Opcjonalna lista ról do zastosowania tego rozszerzenia. Jeśli nie określono właściwości lub określono wartość "*", rozszerzenie jest stosowane do wszystkich ról w usłudze w chmurze.
      - `[Setting <String>]`: ustawienia publiczne rozszerzenia. W przypadku rozszerzeń JSON są to ustawienia JSON rozszerzenia. W przypadku rozszerzenia XML (takiego jak RDP) jest to ustawienie XML rozszerzenia.
      - `[SourceVaultId <String>]`: Identyfikator zasobu
      - `[Type <String>]`: określa typ rozszerzenia.
      - `[TypeHandlerVersion <String>]`: określa wersję rozszerzenia. Określa wersję rozszerzenia. Jeśli ten element nie zostanie określony lub jako wartość zostanie użyta gwiazdka (*), zostanie użyta najnowsza wersja rozszerzenia. Jeśli wartość zostanie określona z głównym numerem wersji i gwiazdką jako pomocniczy numer wersji (X),zostanie wybrana najnowsza wersja pomocnicza określonej wersji głównych. Jeśli podano główny numer wersji i numer wersji pomocniczej (X.Y), wybrana jest określona wersja rozszerzenia. Jeśli jest określona wersja, w wystąpieniu roli jest wykonywane automatyczne uaktualnianie.
  - `[NetworkProfile <ICloudServiceNetworkProfile>]`: Profil sieciowy usługi w chmurze.
    - `[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: lista konfiguracji równoważenia obciążenia dla usługi w chmurze.
      - `[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: lista adresów IP
        - `[Name <String>]`: 
        - `[PrivateIPAddress <String>]`: prywatny adres IP, do których odwołuje się usługa w chmurze.
        - `[PublicIPAddressId <String>]`: Identyfikator zasobu
        - `[SubnetId <String>]`: Identyfikator zasobu
      - `[Name <String>]`: Nazwa zasobu
    - `[SwappableCloudService <ISubResource>]`: 
      - `[Id <String>]`: Identyfikator zasobu
  - `[OSProfile <ICloudServiceOSProfile>]`: w tym artykule opisano profil systemu operacyjnego usługi w chmurze.
    - `[Secret <ICloudServiceVaultSecretGroup[]>]`: Określa zestaw certyfikatów, które powinny być instalowane w wystąpieniach ról.
      - `[SourceVaultId <String>]`: Identyfikator zasobu
      - `[VaultCertificate <ICloudServiceVaultCertificate[]>]`: lista odwołań do magazynu kluczy w u źródłach SourceVault, które zawierają certyfikaty.
        - `[CertificateUrl <String>]`: jest to adres URL certyfikatu, który został przekazany do magazynu kluczy jako tajny.
  - `[PackageUrl <String>]`: Określa adres URL, który odwołuje się do lokalizacji pakietu usługi w usłudze obiektów blob. Adres URL pakietu usługi może być URI podpisu dostępu udostępnionego (SAS) z dowolnego konta magazynu.         Jest to właściwość tylko do zapisu i nie jest zwracana w wywołaniach GET.
  - `[RoleProfile <ICloudServiceRoleProfile>]`: opis profilu roli dla usługi w chmurze.
    - `[Role <ICloudServiceRoleProfileProperties[]>]`: lista ról dla usługi w chmurze.
      - `[Name <String>]`: nazwa zasobu.
      - `[SkuCapacity <Int64?>]`: określa liczbę wystąpień ról w usłudze w chmurze.
      - `[SkuName <String>]`: nazwa sKU. UWAGA: Jeśli nowa wersja SKU nie jest obsługiwana na sprzęcie, na który obecnie działa usługa w chmurze, musisz usunąć i ponownie utworzyć usługę w chmurze lub wrócić do starej.
      - `[SkuTier <String>]`: określa warstwę usługi w chmurze. Dopuszczalne wartości to <br /><br /> **Standardowe** <br /><br /> **Podstawowe**
  - `[StartCloudService <Boolean?>]`: (Opcjonalnie) Wskazuje, czy usługa w chmurze ma być uruchamiana natychmiast po jej utworzeniu. Wartość domyślna `true` to.         Jeśli wartość jest fałszywa, model usługi jest nadal wdrażany, ale kod nie jest uruchamiany natychmiast. Zamiast tego usługa będzie się uruchamiać do momentu wywołania startowego, o której usługa zostanie uruchomiona. Wdrożona usługa nadal wiąże się z opłatami, nawet jeśli zostanie wyłączony.
  - `[Tag <ICloudServiceTags>]`: tagi zasobów.
    - `[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.
  - `[UpgradeMode <CloudServiceUpgradeMode?>]`: tryb aktualizacji dla usługi w chmurze. Wystąpienia ról są przydzielane do aktualizowania domen podczas wdrażania usługi. Aktualizacje mogą być inicjowane ręcznie w każdej domenie aktualizacji lub inicjowane automatycznie we wszystkich domenach aktualizacji.         Dopuszczalne wartości to <br /><br />**Automatycznie**<br /><br />**Ręcznie** <br /><br />**Jednoczesne**<br /><br />         Jeśli nie zostanie określona, wartością domyślną jest Auto. Jeśli ta wartość jest ustawiona na Ręcznie, aby zastosować aktualizację, musi zostać wywołana nazwa PUT UpdateDomain. Jeśli ta opcja jest ustawiona na Automatyczne, aktualizacja jest automatycznie stosowana do każdej domeny aktualizacji w sekwencji.

## LINKI POKREWNE

