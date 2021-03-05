---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 71aa555528ff1cdb5748c1a4ac62481ddd17c17c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991495"
---
# New-AzVMConfig

## SYNOPSIS
Tworzy konfigurowalny obiekt maszyny wirtualnej.

## SKŁADNIA

### DefaultParameterSet (Domyślne)
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzVMConfig** tworzy konfigurowalny obiekt maszyny wirtualnej dla platformy Azure.
Inne polecenia cmdlet mogą być używane do konfigurowania obiektu maszyny wirtualnej, takiego jak Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface i Set-AzVMOSSystem.

## PRZYKŁADY

### Przykład 1. Tworzenie obiektu maszyny wirtualnej
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailabilitySet03 w grupie zasobów o nazwie Grupa Zasobów11, a następnie przechowuje ten obiekt w zmiennej $AvailabilitySet zasobów.
Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie przechowuje go w $VirtualMachine zmienną.
To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.
Maszynę wirtualną należy do zestawu dostępności przechowywanego w $AvailabilitySet.

## PARAMETERS

### -AvailabilitySetId
Określa identyfikator zestawu dostępności.
Aby uzyskać obiekt zestawu dostępności, użyj Get-AzAvailabilitySet cmdlet.
Obiekt zestawu dostępności zawiera właściwość Identyfikator. <br>
Maszyny wirtualne określone w tym samym zestawie dostępności są przydzielane do różnych węzłów w celu zmaksymalizowania dostępności. <br>
Aby uzyskać więcej informacji na temat zestawów dostępności, zobacz [Zarządzanie dostępnością maszyn wirtualnych.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json) <br>
Aby uzyskać więcej informacji na temat planowanej konserwacji platformy Azure, zobacz [Planowane konserwacje maszyn wirtualnych na platformie Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json) <br>
Obecnie maszyny wirtualnej można dodać tylko do zestawu dostępności podczas tworzenia. Zestaw dostępności, do którego jest dodawana maszyny wirtualnej, powinien być w tej samej grupie zasobów, do której jest dodawany zasób zestawu dostępności. Istniejącej maszyny wirtualnej nie można dodać do zestawu dostępności. <br>
Ta właściwość nie może istnieć wraz z odwołaniem do właściwości innych niż null.virtualMachineScaleSet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### -EnableUltrasSD
Umożliwia możliwość, że jedna lub więcej zarządzanych dysków danych UltraSSD_LRS typ konta magazynu w maszyny wirtualnej.
Dysk zarządzany z kontem magazynu typu UltraSSD_LRS można dodawać do maszyny wirtualnej tylko wtedy, gdy ta właściwość jest włączona.


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
Zasady eksmisji dla maszyny wirtualnej usługi Azure Spot.  Obsługiwane wartości to "Deallocate" i "Delete".

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

### -HostId
Identyfikator hosta

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

### - IdentityId
Określa listę tożsamości użytkowników skojarzonych z zestawem skal maszyn wirtualnych.
Odwołania do tożsamości użytkownika ARM identyfikatory zasobów w postaci: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"

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
Tożsamość maszyny wirtualnej, jeśli została skonfigurowana.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseType
Określa typ licencji, który wskazuje, że obraz lub dysk maszyny wirtualnej został licencjonowany lokalnie.
Możliwe wartości dla systemu Windows Server to:
- Windows_Client
- Windows_Server możliwe wartości dla systemu operacyjnego Linux Server to: 
- RHEL_BYOS (dla RBLOCK) 
- SLES_BYOS (dla SUSE) 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - MaxCena
Określa maksymalną cenę za niską płatność za maszyny wirtualne/maszyny wirtualne o niskim priorytecie. Ta cena jest w dolarach amerykańskich. Ta cena będzie porównywana z bieżącą ceną o niskim priorytecie dla rozmiaru maszyny wirtualnej. Ponadto ceny są porównywane w czasie tworzenia/aktualizacji maszyny wirtualnej/maszyny wirtualnej o niskim priorytecie, a operacja zakończy się powodzeniem tylko wtedy, gdy wartość maxCena jest większa niż obecna cena o niskim priorytecie. Cena maksymalna będzie również używana do evicowania maszyny wirtualnej/maszyny wirtualnej o niskim priorytecie, jeśli bieżąca cena o niskim priorytecie przekracza wartość maxCena po utworzeniu maszyny wirtualnej/maszyny wirtualnej. Dopuszczalne wartości to: dowolna wartość dziesiętna większa niż zero. Przykład: 0,01538.  -1 oznacza, że maszyny wirtualnej/maszyny wirtualnej o niskim priorytecie nie należy ich ujednać ze względu na cenę. Ponadto domyślna maksymalna cena to -1, jeśli nie jest ona przez Ciebie dostarczana.

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

### -EncryptionAtHost
Właściwość EncryptionAtHost może być używana przez użytkownika w żądaniu włączenia lub wyłączenia szyfrowania hosta dla zestawu skali maszyny wirtualnej lub maszyny wirtualnej. Spowoduje to włączenie szyfrowania dla wszystkich dysków, w tym dysku zasobu/tempa na samym hoście. Domyślne: Szyfrowanie na hoście zostanie wyłączone, chyba że dla zasobu ta właściwość jest ustawiona na prawda.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### — Priority (Priorytet)
Priorytet maszyny wirtualnej.  Obsługiwane są tylko wartości "Zwykła", "Spot" i "Niska".
"Zwykła" jest dla zwykłej maszyny wirtualnej.
"Spot" jest dla maszyny wirtualnej spot.
"Low" jest również dla spot virtual machine, ale jest zastępowany przez "Spot". Użyj pozycji Spot (Spot) zamiast "Low" (Najniszej).

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
Identyfikator zasobu grupy Położenie odległości, która ma być używania z tą maszyną wirtualną.

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

### — Tagi
Tagi dołączone do zasobu.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NAZWA.MASZYNY.WIRTUALNEJ
Określa nazwę maszyny wirtualnej.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSize
Określa rozmiar maszyny wirtualnej.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - Maszyny wirtualne
Identyfikator zestawu skali maszyny wirtualnej

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

### — Strefa
Określa listę stref dostępności dla maszyny wirtualnej. Dozwolone wartości zależą od możliwości regionu. Dozwolone wartości zwykle to 1;2;3.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### System.String[]

### System.Collections.Hashtable

### System.Management.Automation.SwitchParameters

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTATKI

## LINKI POKREWNE

[Update-AzVM](./Update-AzVM.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)

[Set-AzVMSourceImage](./Set-AzVMSourceImage.md)

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)


