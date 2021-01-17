---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 4fdfd5c5da9cc803cacdd2aca90b7f66771988fd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372626"
---
# New-AzVmssConfig

## STRESZCZENIe
Tworzy obiekt konfiguracji VMSS.

## POLECENIA

### DefaultParameterSet (domyślny)
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] [-EncryptionAtHost]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzVmssConfig** umożliwia utworzenie konfigurowalnego obiektu zestawu lokalnych menedżerów wirtualnych (VMSS). Do skonfigurowania obiektu VMSS są potrzebne inne polecenia cmdlet. Te polecenia cmdlet są następujące:
- Set-AzVmssOsProfile
- Set-AzVmssStorageProfile
- Add-AzVmssNetworkInterfaceConfiguration
- Add-AzVmssExtension

## Przykłady

### Przykład 1. Tworzenie obiektu konfiguracji VMSS
```powershell
PS C:\> $VMSS = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

W tym przykładzie przedstawiono tworzenie obiektu konfiguracji VMSS. W pierwszym poleceniu użyto polecenia cmdlet **New-AzVmssConfig** w celu utworzenia VMSS obiektu konfiguracji i zapisu wyniku w zmiennej o nazwie $VMSS. W drugim poleceniu użyto polecenia cmdlet **New-AzVmss** w celu utworzenia VMSS używającej obiektu konfiguracji VMSS utworzonego w pierwszym poleceniu.

### Przykład 2

Tworzy obiekt konfiguracji VMSS. (autogenerowana)

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## PARAMETRÓW

### -AutomaticRepairGracePeriod
Ilość czasu, w której automatyczne naprawy są zawieszane ze względu na zmianę stanu maszyny wirtualnej. Czas prolongaty rozpoczyna się po zakończeniu zmiany stanu. Pomaga to uniknąć przedwczesnych lub przypadkowych napraw. Czas trwania należy określić w formacie ISO 8601. Minimalny dozwolony okres prolongaty to 30 minut (PT30M), który jest również wartością domyślną. Maksymalny dozwolony okres prolongaty to 90 minut (PT90M).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoOSUpgrade
Określa, czy uaktualnienia systemu operacyjnego mają być automatycznie stosowane do skalowania zestawów w sposób stały, gdy będzie dostępna nowsza wersja obrazu.

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

### -BootDiagnostic
Określa skalę maszyny wirtualnej określającą profil diagnostyczny rozruchu.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.BootDiagnostics
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableAutoRollback
Wyłączanie automatycznego wycofywania dla zasad automatycznej aktualizacji systemu operacyjnego

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutomaticRepair
Włączenie automatycznej naprawy w zestawie skali maszyny wirtualnej.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableUltraSSD
Umożliwia posiadanie jednego lub większej liczby zarządzanych dysków z danymi przy użyciu UltraSSD_LRS typu konta magazynu w zestawie skali maszyny wirtualnej.
Dyski zarządzane z typem konta magazynu UltraSSD_LRS można dodawać do VMSS tylko wtedy, gdy ta właściwość jest włączona.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EncryptionAtHost
Ten parametr umożliwia szyfrowanie wszystkich dysków, w tym dysku Resource/temp, na hoście. Wartość domyślna: szyfrowanie na hoście zostanie wyłączone, chyba że dla tego zasobu zostanie ustawiona wartość true dla tej właściwości.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EvictionPolicy
Określa zasady wykluczania dla maszyn wirtualnych w zestawie skali.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Rozszerzenie
Określa obiekt informacji o rozszerzeniu dla VMSS. Aby dodać ten obiekt, możesz użyć polecenia cmdlet **Add-AzVmssExtension** .

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HealthProbeId
Określa identyfikator sondy modułu równoważenia obciążenia służącego do określania kondycji wystąpienia w zestawie skali maszyny wirtualnej.
HealthProbeId jest w formie "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdentityId
Określa listę tożsamości użytkowników skojarzonych z zestawem skali maszyny wirtualnej.
Odwołania tożsamości użytkownika będą miały identyfikatory zasobów ARM w formularzu: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdentityType
Określa typ tożsamości używanej dla zestawu skali maszyny wirtualnej.
Typ "SystemAssignedUserAssigned" obejmuje zarówno niejawnie utworzoną tożsamość, jak i zestaw tożsamości przypisanych do użytkownika.
Typ "Brak" spowoduje usunięcie wszystkich tożsamości z zestawu skali maszyny wirtualnej.
Dopuszczalne wartości tego parametru to:
- SystemAssigned
- UserAssigned
- SystemAssignedUserAssigned
- Znaleziono

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LicenseType
Określ typ licencji, który umożliwia prowadzenie własnego scenariusza licencji.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Lokalizacja
Określa lokalizację platformy Azure, w której jest tworzony VMSS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxPrice
Określa cenę maksymalną, jaką należy zapłacić za dodatkowe maszyny wirtualne lub VMSS. Ta cena jest w dolarach amerykańskich. Ta cena będzie porównywana z bieżącą ceną na miejscu w danym rozmiarze maszyny wirtualnej. Ceny są również porównywane w czasie tworzenia/aktualizowania dodatkowych maszyn wirtualnych/VMSS, a operacja będzie działać tylko wtedy, gdy maxPrice jest większa niż bieżąca cena. MaxPrice będzie również stosowany do wykluczania dodatkowych maszyn wirtualnych/VMSS, jeśli bieżąca cena na miejscu przekracza maxPrice po utworzeniu maszyny wirtualnej/VMSS. Możliwe wartości: Każda wartość dziesiętna większa niż zero. Przykład: 0,01538.  -1 wskazuje, że docelowa maszyna wirtualna/VMSS nie powinna być wykluczona ze względu na cenę. Ponadto domyślna cena maksymalna wynosi-1, jeśli nie jest podana przez Ciebie.

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkInterfaceConfiguration
Określa obiekt profilu sieciowego, który zawiera właściwości sieci dla konfiguracji VMSS.
Aby dodać ten obiekt, możesz użyć polecenia cmdlet **Add-AzVmssNetworkInterfaceConfiguration** .

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsProfile
Określa obiekt profilu systemu operacyjnego, który zawiera właściwości systemu operacyjnego dla konfiguracji VMSS.
Aby ustawić ten obiekt, możesz użyć polecenia cmdlet **Set-AzVmssOsProfile** .

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Przekazanie
Wskazuje, czy polecenie cmdlet powoduje zarezerwowanie VMSS.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PlanName
Określa nazwę planu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PlanProduct
Określa plan produktu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PlanPromotionCode
Umożliwia określenie kodu promocyjnego planu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PlanPublisher
Umożliwia określenie wydawcy planu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PlatformFaultDomainCount
Liczba domen błędów dla każdej grupy położenia.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Priority (priorytet)
Priorytet machien wirtualnej w zestawie skali.  Obsługiwane są tylko wartości "Regular", "spot" i "Low".
"Zwykła" dotyczy zwykłej maszyny wirtualnej.
"Miejsce na maszynie wirtualnej" jest na miejscu.
"Niski" jest również na odniesieniu do maszyny wirtualnej, ale został zastąpiony przez "punkt". Użyj "spot" zamiast "niski".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProximityPlacementGroupId
Identyfikator zasobu grupy położenia zbliżeniowe, który ma być używany z tym zestawem skali.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RollingUpgradePolicy
Określa zasady uaktualnienia stopniowego.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScaleInPolicy
Reguły, których należy przestrzegać podczas skalowania — w zestawie skali maszyny wirtualnej.  Możliwe wartości: "default", "OldestVM" i "NewestVM".  "Domyślny" gdy zestaw skali maszyny wirtualnej jest skalowany, zestaw skali będzie najpierw równoważony między strefami, jeśli jest ustawionym skalą zona.  Następnie będzie on w miarę możliwości równoważony między domenami błędów.  W każdej domenie błędów maszyny wirtualne wybrane do usunięcia będą to najnowsze, które nie są chronione przed skalą.  OldestVM ' po przeskalowaniu zestawu skali maszyny wirtualnej do usunięcia zostanie wybrana najstarsza maszyna wirtualna, która nie jest chroniona przed przeskalowaniem.  W przypadku zestawów skali maszyny wirtualnej zona zestaw skali będzie najpierw równoważony między strefami.  W obrębie każdej strefy do usunięcia zostaną wybrane najstarsze maszyny wirtualne, które nie są chronione.  NewestVM ' po przeskalowaniu zestawu skali maszyny wirtualnej w celu usunięcia zostanie wybrana Najnowsza maszyna wirtualna, która nie jest chroniona przed przeskalowaniem.  W przypadku zestawów skali maszyny wirtualnej zona zestaw skali będzie najpierw równoważony między strefami.  W ramach każdej strefy do usunięcia zostaną wybrane najnowsze maszyny wirtualne, które nie są chronione.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SinglePlacementGroup
Umożliwia określenie pojedynczej grupy położenia.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipExtensionsOnOverprovisionedVMs
Określa, że rozszerzenia nie są uruchamiane na dodatkowych zarezerwowych maszynach wirtualnych.

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

### -SkuCapacity
Określa liczbę wystąpień w VMSS.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuName
Określa rozmiar wszystkich wystąpień VMSS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuTier
Określa poziom VMSS. Dopuszczalne wartości tego parametru to:
- Standard
- Podstawowym

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageProfile
Określa obiekt profilu magazynu, który zawiera właściwości dysku dla konfiguracji VMSS.
Aby ustawić ten obiekt, możesz użyć polecenia cmdlet **Set-AzVmssStorageProfile** .

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Pary klucz-wartość w formie tabeli skrótów. Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TerminateScheduledEventNotBeforeTimeoutInMinutes
Możliwy do skonfigurowania czas (w minutach), w przypadku której usuwana maszyna wirtualna będzie mogła zatwierdzić zakończenie zdarzenia zaplanowany przed jego automatycznym zatwierdzeniem (przekroczenie limitu czasu).

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TerminateScheduledEvents
Włączanie kończenia zaplanowanych zdarzeń

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UpgradePolicyMode
W zestawie skali wybrano tryb uaktualniania maszyn wirtualnych.
Dopuszczalne wartości tego parametru to:
- Automatyczne
- Ręcznie

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.UpgradeMode]
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Określa listę stref dla zestawu skali maszyny wirtualnej.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ZoneBalance
Czy należy wymusić ścisłe, nawet strefy krzyżowe funkcji dystrybucji maszyn wirtualnych na wypadek awarii strefy.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

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

### System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### System. String

### System. Collections. Hashtable

### System. Int32

### System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. MODELES. Upgrademode; Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

### Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetOSProfile

### Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetStorageProfile

### Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetNetworkConfiguration []

### Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetExtension []

### System. String []

### Microsoft. Azure. Management. COMPUTE. MODELES. RollingUpgradePolicy

### System. Management. Automation. SwitchParameter

### Microsoft. Azure. Management. COMPUTE. MODELES. BootDiagnostics

### System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. ResourceIdentityType, Microsoft. Azure. Management. Framework

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet

## INFORMACYJN

## LINKI POKREWNE

[Set-AzVmssOsProfile](./Set-AzVmssOsProfile.md)

[Set-AzVmssStorageProfile](./Set-AzVmssStorageProfile.md)

[Dodaj-AzVmssNetworkInterfaceConfiguration](./Add-AzVmssNetworkInterfaceConfiguration.md)

[Dodaj-AzVmssExtension](./Add-AzVmssExtension.md)

[Nowe — AzVmss](./New-AzVmss.md)
