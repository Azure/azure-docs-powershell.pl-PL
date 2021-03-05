---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/update-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
ms.openlocfilehash: bb67420e3fbb4479a79c7a837aad3b9a65635d88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007178"
---
# Update-AzCloudService

## SYNOPSIS
Tworzenie lub aktualizowanie usługi w chmurze.
Niektóre właściwości można ustawić tylko podczas tworzenia usługi w chmurze.

## SKŁADNIA

```
Update-AzCloudService -InputObject <ICloudServiceIdentity> -Parameter <ICloudService>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## OPIS
Tworzenie lub aktualizowanie usługi w chmurze.
Niektóre właściwości można ustawić tylko podczas tworzenia usługi w chmurze.

## PRZYKŁADY

### Przykład 1. Dodawanie rozszerzenia RDP do istniejącej usługi w chmurze
```powershell
# Create RDP extension object
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name "RDPExtension" -Credential $credential -Expiration $expiration -TypeHandlerVersion "1.2.1"
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Add RDP extension to existing cloud service extension object
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension + $rdpExtension
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

Powyższy zestaw poleceń dodaje rozszerzenie RDP do istniejącej już usługi w chmurze o nazwie ContosoCS, która należy do grupy zasobów o nazwie ContosOrg.

### Przykład 2. Usuwanie wszystkich rozszerzeń z usługi w chmurze
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Set extension to empty list
PS C:\> $cloudService.ExtensionProfile.Extension = @()
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

Powyższy zestaw poleceń usuwa wszystkie rozszerzenia istniejącej usługi w chmurze o nazwie ContosoCS, które należą do grupy zasobów o nazwie ContosOrg.

### Przykład 3. Usuwanie rozszerzenia RDP z usługi w chmurze
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Remove extension by name RDPExtension
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension | Where-Object { $_.Name -ne "RDPExtension" }
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

Powyższy zestaw poleceń usuwa rozszerzenie RDP istniejącej usługi w chmurze o nazwie ContosoCS, które należy do grupy zasobów o nazwie ContosOrg.

### Przykład 4. Scale-Out / Scale-In wystąpień ról
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"

# Scale-out all role instance count by 1
PS C:\> $cloudService.RoleProfile.Role | ForEach-Object {$_.SkuCapacity += 1}

# Scale-in ContosoFrontend role instance count by 1
PS C:\> $role = $cloudService.RoleProfile.Role | Where-Object {$_.Name -eq "ContosoFrontend"}
PS C:\> $role.SkuCapacity -= 1

# Update cloud service configuration as per the new role instance count
PS C:\> $cloudService.Configuration = $configuration

# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

Powyżej zestawu poleceń pokazano, jak przeskalować i skalować wystąpienia ról dla usługi w chmurze o nazwie ContosoCS, która należy do grupy zasobów o nazwie ContosOrg.

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
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoWait
Uruchamianie polecenia asynchronicznie

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

### - Parametr
W tym artykule opisano usługę w chmurze.
Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach PARAMETRu i utworzyć tabelę skrótu.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.Api20201001Preview.iCloudService

### Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.ICloudServiceIdentity

## DANE WYJŚCIOWE

### Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.Api20201001Preview.iCloudService

## NOTATKI

ALIASY

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


INPUTOBJECT: <ICloudServiceIdentity> Parametr tożsamości
  - `[CloudServiceName <String>]`: 
  - `[Id <String>]`: ścieżka tożsamości zasobu
  - `[ResourceGroupName <String>]`: 
  - `[RoleInstanceName <String>]`: nazwa wystąpienia roli.
  - `[RoleName <String>]`: nazwa roli.
  - `[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.
  - `[UpdateDomain <Int32?>]`: określa wartość całkowitą identyfikującą domenę aktualizacji. Domeny aktualizacji są identyfikowane za pomocą indeksu opartego na zeru: pierwsza domena aktualizacji ma identyfikator 0, druga ma identyfikator 1 i tak dalej.

PARAMETR: <ICloudService> w tym artykule opisano usługę w chmurze.
  - `Location <String>`: lokalizacja zasobu.
  - `[Configuration <String>]`: określa konfigurację usługi XML (cscfg) dla usługi w chmurze.
  - `[ConfigurationUrl <String>]`: Określa adres URL, który odwołuje się do lokalizacji konfiguracji usługi w usłudze obiektów blob. Adres URL pakietu usługi może być URI podpisu dostępu udostępnionego (SAS) z dowolnego konta magazynu.         Jest to właściwość tylko do zapisu i nie jest zwracana w wywołaniach GET.
  - `[ExtensionProfile <ICloudServiceExtensionProfile>]`: w tym artykule opisano profil rozszerzenia usługi w chmurze.
    - `[Extension <IExtension[]>]`: Lista rozszerzeń dla usługi w chmurze.
      - `[AutoUpgradeMinorVersion <Boolean?>]`: Jawnie określ, czy platforma może automatycznie uaktualniać typHandlerVersion do wyższych wersji pomocniczych, gdy staną się dostępne.
      - `[ForceUpdateTag <String>]`: Tag wymusza zastosowanie podanych ustawień publicznych i chronionych.         Zmiana wartości tagu umożliwia ponowne uruchomienie rozszerzenia bez zmieniania jakichkolwiek ustawień publicznych i chronionych.         Jeśli tag forceUpdate nie zostanie zmieniony, program obsługi nadal będzie stosować aktualizacje ustawień publicznych lub chronionych.         Jeśli ani forceUpdateTag, ani żadne ustawienia publiczne lub chronione nie ujdą, rozszerzenie przepływa do wystąpienia roli z tym samym numerem sekwencji, a implementacja programu obsługi może być uruchamiana ponownie, czy nie.
      - `[Name <String>]`: nazwa rozszerzenia.
      - `[ProtectedSetting <String>]`: ustawienia chronione rozszerzenia, które są szyfrowane przed wysłaniem do wystąpienia roli.
      - `[ProtectedSettingFromKeyVaultSecretUrl <String>]`: 
      - `[Publisher <String>]`: nazwa wydawcy programu obsługi rozszerzenia.
      - `[RolesAppliedTo <String[]>]`: Opcjonalna lista ról do zastosowania tego rozszerzenia. Jeśli nie określono właściwości lub określono wartość "*", rozszerzenie jest stosowane do wszystkich ról w usłudze w chmurze.
      - `[Setting <String>]`: ustawienia publiczne rozszerzenia. W przypadku rozszerzeń JSON są to ustawienia JSON rozszerzenia. W przypadku rozszerzenia XML (takiego jak RDP) jest to ustawienie XML rozszerzenia.
      - `[SourceVaultId <String>]`: Identyfikator zasobu
      - `[Type <String>]`: określa typ rozszerzenia.
      - `[TypeHandlerVersion <String>]`: określa wersję rozszerzenia. Określa wersję rozszerzenia. Jeśli ten element nie jest określony lub jako wartość zostanie użyta gwiazdka (*), zostanie użyta najnowsza wersja rozszerzenia. Jeśli wartość zostanie określona z głównym numerem wersji i gwiazdką jako pomocniczy numer wersji (X),zostanie wybrana najnowsza wersja pomocnicza określonej wersji głównych. Jeśli określono główny numer wersji i numer wersji pomocniczej (X.Y), wybrana jest określona wersja rozszerzenia. Jeśli jest określona wersja, automatyczne uaktualnianie jest wykonywane w wystąpieniu roli.
  - `[NetworkProfile <ICloudServiceNetworkProfile>]`: Profil sieciowy dla usługi w chmurze.
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

