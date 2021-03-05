---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 4290c178ad1f84400f542c16a2f90c51c654985c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013706"
---
# Get-AzVmss

## SYNOPSIS
Pobiera właściwości maszyny wirtualnej.

## SKŁADNIA

### DefaultParameters (domyślny)
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### OSUpgradeHistoryMethodParameters
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzVmss** pobiera widok modelu i wystąpienia zestawu skal maszyn wirtualnych (VMSS).
Widok modelu to właściwości określone przez użytkownika zestawu skal maszyn wirtualnych.
Widok wystąpienia jest stanem poziomu wystąpienia zestawu skali maszyny wirtualnej.
Określ parametr *InstanceView,* aby uzyskać tylko widok wystąpienia zestawu skali maszyny wirtualnej.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie właściwości maszyn wirtualnych
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"

ResourceGroupName                           : Group001
Sku                                         :
  Name                                      : Standard_DS1_v2
  Tier                                      : Standard
  Capacity                                  : 2
UpgradePolicy                               :
  Mode                                      : Manual
VirtualMachineProfile                       :
  OsProfile                                 :
    ComputerNamePrefix                      : test
    AdminUsername                           : contoso
    WindowsConfiguration                    :
      ProvisionVMAgent                      : True
      EnableAutomaticUpdates                : True
  StorageProfile                            :
    ImageReference                          :
      Publisher                             : MicrosoftWindowsServer
      Offer                                 : WindowsServer
      Sku                                   : 2016-Datacenter
      Version                               : latest
    OsDisk                                  :
      Caching                               : None
      CreateOption                          : FromImage
      ManagedDisk                           :
        StorageAccountType                  : Premium_LRS
  NetworkProfile                            :
    NetworkInterfaceConfigurations[0]       :
      Name                                  : Group001
      Primary                               : True
      EnableAcceleratedNetworking           : False
      NetworkSecurityGroup                  :
        Id                                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001
/providers/Microsoft.Network/networkSecurityGroups/Group001
      DnsSettings                           :
      IpConfigurations[0]                   :
        Name                                : Group001
        Subnet                              :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/virtualNetworks/Group001/subnets/Group001
        PrivateIPAddressVersion             : IPv4
        LoadBalancerBackendAddressPools[0]  :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/backendAddressPools/Group001
        LoadBalancerInboundNatPools[0]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
        LoadBalancerInboundNatPools[1]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
      EnableIPForwarding                    : False
ProvisioningState                           : Succeeded
Overprovision                               : True
UniqueId                                    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SinglePlacementGroup                        : False
Id                                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001/
providers/Microsoft.Compute/virtualMachineScaleSets/VMSS001
Name                                        : VMSS001
Type                                        : Microsoft.Compute/virtualMachineScaleSets
Location                                    : eastus
Tags                                        : {}
```

To polecenie pobiera właściwości maszyny wirtualnej o nazwie VMSS001, która należy do grupy zasobów o nazwie Group001.
Ponieważ to polecenie nie określa *parametru przełącznika InstanceView,* polecenie cmdlet pobiera widok modelu zestawu skali maszyny wirtualnej.

### Przykład 2. Uzyskiwanie wszystkich maszyn wirtualnych w grupie zasobów
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001"

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
```

Pobierz wszystkie maszyny wirtualne w grupie zasobów "Group001"

### Przykład 3. Pobierz wszystkie maszyny wirtualne w subskrypcji
```
PS C:\> Get-AzVmss

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

Pobierz wszystkie maszyny wirtualne w subskrypcji.

### Przykład 4. Pobierz wszystkie maszyny wirtualne przy użyciu filtrowania
```
PS C:\> Get-AzVmss -Name VMSS00*

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

Pobierz wszystkie maszyny wirtualne w subskrypcji, które zaczynają się od "VMSS00".

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

### -InstanceView
Wskazuje, że to polecenie cmdlet pobiera tylko widok wystąpienia zestawu skali maszyny wirtualnej.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSUpgradeHistory
Wskazuje, że to polecenie cmdlet zawiera historię uaktualniania systemu operacyjnego zestawu skal maszyn wirtualnych.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów maszyn wirtualnych.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -VMScaleSetName
Nazwa maszyny wirtualnej to "gatunek".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## NOTATKI

## LINKI POKREWNE

[New-AzVmss](./New-AzVmss.md)

[Remove-AzVmss](./Remove-AzVmss.md)

[Restart-AzVmss](./Restart-AzVmss.md)

[Set-AzVmss](./Set-AzVmss.md)

[Start-AzVmss](./Start-AzVmss.md)

[Stop-AzVmss](./Stop-AzVmss.md)

[Update-AzVmss](./Update-AzVmss.md)


