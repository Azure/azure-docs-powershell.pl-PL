---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e9ec68d7c3991d7a3eded2566d8e299ddcc36c85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177394"
---
# Update-AzVM

## SYNOPSIS
Aktualizuje stan maszyny wirtualnej platformy Azure.

## SKŁADNIA

### ResourceGroupNameParameterSetName (Domyślna)
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### IdParameterSetName
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Update-AzVM** aktualizuje stan maszyny wirtualnej platformy Azure do stanu obiektu maszyny wirtualnej.

## PRZYKŁADY

### Przykład 1. Aktualizowanie maszyny wirtualnej
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

To polecenie aktualizuje maszynę wirtualną w $VirtualMachine ResourceGroup11.
Polecenie aktualizuje je przy użyciu obiektu maszyny wirtualnej przechowywanego w $VirtualMachine zmienną.
Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet **Get-AzVM.**

## PARAMETERS

### — AsJob
Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - HostId
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

### -EncryptionAtHost
Właściwość EncryptionAtHost może być używana przez użytkownika w żądaniu włączenia lub wyłączenia szyfrowania hosta dla zestawu skali maszyny wirtualnej lub maszyny wirtualnej. Spowoduje to włączenie szyfrowania dla wszystkich dysków, w tym dysku zasobu/tempa na samym hoście. 

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

### — Id
Określa identyfikator zasobu maszyny wirtualnej.

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - IdentityId
Określa listę tożsamości użytkowników skojarzonych z maszyną wirtualną.
Odwołania do tożsamości użytkownika będą mieć ARM w postaci: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityType
Typ tożsamości używany dla maszyny wirtualnej. Prawidłowe wartości to SystemAssigned, UserAssigned, SystemAssignedUserAssigned i None.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - MaxCena
Określa maksymalną cenę za niską płatność za maszyny wirtualne/maszyny wirtualne o niskim priorytecie. Ta cena jest w dolarach amerykańskich. Ta cena będzie porównywana z bieżącą ceną o niskim priorytecie dla rozmiaru maszyny wirtualnej. Ponadto ceny są porównywane w czasie tworzenia/aktualizacji maszyny wirtualnej/maszyny wirtualnej o niskim priorytecie, a operacja zakończy się powodzeniem tylko wtedy, gdy wartość maxCena jest większa niż obecna cena o niskim priorytecie. Cena maksymalna będzie również używana do evicowania maszyny wirtualnej/maszyny wirtualnej o niskim priorytecie, jeśli bieżąca cena o niskim priorytecie przekracza wartość maxPrice po utworzeniu maszyny wirtualnej/maszyny wirtualnej. Dopuszczalne wartości to: dowolna wartość dziesiętna większa niż zero. Przykład: 0,01538.  -1 oznacza, że maszyny wirtualnej/maszyny wirtualnej o niskim priorytecie nie należy ich ujednać ze względu na cenę. Ponadto domyślna maksymalna cena to -1, jeśli nie jest ona przez Ciebie dostarczana.

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

### -NoWait
Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem. Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.

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

### -Os JednakowyAccelerator
Określa, czy funkcja WriteAccelerator ma być włączona, czy wyłączona na dysku systemu operacyjnego.

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

### -ProximityPlacementGroupId
Identyfikator zasobu grupy Położenie odległości do użycia z tą maszyną wirtualną.

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

### -ResourceGroupName
Określa nazwę grupy zasobów maszyny wirtualnej.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Tag
Określa zasoby i grupy zasobów, które można otagowyć za pomocą zestawu par nazwa-wartość.
Dodawanie tagów do zasobów umożliwia grupowanie zasobów w różnych grupach zasobów i tworzenie własnych widoków.
Każda grupa zasobów lub zasobu może mieć maksymalnie 15 tagów.

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

### -UltraSSDEnabled
Flaga, która włącza lub wyłącza możliwość, że jedna lub więcej zarządzanych dysków danych UltraSSD_LRS typ konta magazynu na maszyny wirtualnej.
Dysk zarządzany z kontem typu magazynu UltraSSD_LRS można dodawać do maszyny wirtualnej tylko wtedy, gdy ta właściwość jest włączona.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - MASZYNY WIRTUALNEJ
Określa lokalny obiekt maszyny wirtualnej.
Aby uzyskać obiekt maszyny wirtualnej, użyj Get-AzVM cmdlet.
Ten obiekt maszyny wirtualnej zawiera zaktualizowany stan maszyny wirtualnej.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```


### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.Boolean

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## NOTATKI

## LINKI POKREWNE

[Get-AzVM](./Get-AzVM.md)

[New-AzVM](./New-AzVM.md)

[Remove-AzVM](./Remove-AzVM.md)

[Restart-AzVM](./Restart-AzVM.md)

[Start-AzVM](./Start-AzVM.md)

[Stop-AzVM](./Stop-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)


