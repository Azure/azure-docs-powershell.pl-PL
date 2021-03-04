---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: efe587cf01fa2adf16e4b6beaaa319312f3c9fa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969569"
---
# Add-AzVMNetworkInterface

## SYNOPSIS
Dodaje interfejs sieciowy do maszyny wirtualnej.

## SKŁADNIA

### GetNicFromNicId (domyślne)
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetNicFromNicObject
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Add-AzVMNetworkInterface** dodaje interfejs sieciowy do maszyny wirtualnej.
Interfejs można dodać podczas tworzenia maszyny wirtualnej lub do istniejącej maszyny wirtualnej.

## PRZYKŁADY

### Przykład 1. Dodawanie interfejsu sieciowego do nowej maszyny wirtualnej
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

Pierwsze polecenie tworzy obiekt maszyny wirtualnej, a następnie przechowuje go w $VirtualMachine zmienną.
To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.
Drugie polecenie dodaje interfejs sieciowy do maszyny wirtualnej przechowywanej w $VirtualMachine.

### Przykład 2. Dodawanie interfejsu sieciowego do istniejącej maszyny wirtualnej
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Pierwsze polecenie pobiera maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet **Get-AzVM.**
Polecenie przechowuje maszynę wirtualną w $VirtualMachine zmienną.
Drugie polecenie dodaje interfejs sieciowy do maszyny wirtualnej przechowywanej w $VirtualMachine.
Ostatnie polecenie aktualizuje stan maszyny wirtualnej przechowywanej w u $VirtualMachine ResourceGroup11.

## PARAMETERS

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

### — Identyfikator
Określa identyfikator interfejsu sieciowego do dodania do maszyny wirtualnej.
Aby uzyskać interfejs sieciowy, możesz użyć polecenia cmdlet [Get-AzNetworkInterface.](/powershell/module/az.network/get-aznetworkinterface)

```yaml
Type: System.String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - NetworkInterface
Określa interfejs sieciowy.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]
Parameter Sets: GetNicFromNicObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — podstawowy
Wskazuje, że to polecenie cmdlet dodaje interfejs sieciowy jako interfejs podstawowy.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — MASZYNY WIRTUALNEJ
Określa lokalny obiekt maszyny wirtualnej, do którego ma być dodać interfejs sieciowy.
Aby utworzyć maszynę wirtualną, użyj polecenia cmdlet **New-AzVMConfig.**
Aby uzyskać istniejącą maszynę wirtualną, użyj polecenia cmdlet **Get-AzVM.**

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

### System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

### System.Management.Automation.SwitchParameters

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTATKI

## LINKI POKREWNE

[New-AzVMConfig](./New-AzVMConfig.md)

[Get-AzVM](./Get-AzVM.md)

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)
