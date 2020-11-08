---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 7985a979f9bbb89d6594416575e3fa00640784b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062598"
---
# <span data-ttu-id="b08cf-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b08cf-101">Get-AzVmss</span></span>

## <span data-ttu-id="b08cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b08cf-102">SYNOPSIS</span></span>
<span data-ttu-id="b08cf-103">Pobiera właściwości VMSS.</span><span class="sxs-lookup"><span data-stu-id="b08cf-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="b08cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b08cf-104">SYNTAX</span></span>

### <span data-ttu-id="b08cf-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b08cf-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b08cf-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b08cf-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b08cf-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="b08cf-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b08cf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b08cf-108">DESCRIPTION</span></span>
<span data-ttu-id="b08cf-109">Polecenie cmdlet **Get-AzVmss** umożliwia wyświetlenie modelu i widoku wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b08cf-109">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="b08cf-110">Widok modelu to określone przez użytkownika właściwości zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b08cf-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="b08cf-111">Widok wystąpienia jest stanem poziomu wystąpienia zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b08cf-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="b08cf-112">Określ parametr *InstanceView* , aby uzyskać tylko widok wystąpienia skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b08cf-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="b08cf-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b08cf-113">EXAMPLES</span></span>

### <span data-ttu-id="b08cf-114">Przykład 1: uzyskiwanie właściwości VMSS</span><span class="sxs-lookup"><span data-stu-id="b08cf-114">Example 1: Get the properties of a VMSS</span></span>
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

<span data-ttu-id="b08cf-115">To polecenie pobiera właściwości VMSS o nazwie VMSS001 należące do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="b08cf-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="b08cf-116">Ponieważ polecenie nie określa parametru przełącznika *InstanceView* , funkcja cmdlet pobiera widok modelu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b08cf-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

### <span data-ttu-id="b08cf-117">Przykład 2: pobieranie wszystkich VMSS w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="b08cf-117">Example 2: Get all Vmss in a resource group</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001"

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
```

<span data-ttu-id="b08cf-118">Pobierz wszystkie VMSS w grupie zasobów "Group001"</span><span class="sxs-lookup"><span data-stu-id="b08cf-118">Get all Vmss in resource group "Group001"</span></span>

### <span data-ttu-id="b08cf-119">Przykład 3: uzyskiwanie wszystkich VMSS w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b08cf-119">Example 3: Get all Vmss in a subscription</span></span>
```
PS C:\> Get-AzVmss

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="b08cf-120">Pobierz wszystkie VMSS w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="b08cf-120">Get all Vmss in subscription.</span></span>

### <span data-ttu-id="b08cf-121">Przykład 4: pobieranie wszystkich VMSS przy użyciu funkcji filtrowania</span><span class="sxs-lookup"><span data-stu-id="b08cf-121">Example 4: Get all Vmss using filtering</span></span>
```
PS C:\> Get-AzVmss -Name VMSS00*

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="b08cf-122">Pobierz wszystkie VMSS w subskrypcji rozpoczynające się od "VMSS00".</span><span class="sxs-lookup"><span data-stu-id="b08cf-122">Get all Vmss in subscription that start with "VMSS00".</span></span>

## <span data-ttu-id="b08cf-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b08cf-123">PARAMETERS</span></span>

### <span data-ttu-id="b08cf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b08cf-124">-DefaultProfile</span></span>
<span data-ttu-id="b08cf-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b08cf-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b08cf-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="b08cf-126">-InstanceView</span></span>
<span data-ttu-id="b08cf-127">Wskazuje, że ten aplet polecenia pobiera tylko widok skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b08cf-127">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="b08cf-128">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="b08cf-128">-OSUpgradeHistory</span></span>
<span data-ttu-id="b08cf-129">Wskazuje, że to polecenie cmdlet wyświetla historię uaktualnienia systemu operacyjnego zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b08cf-129">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="b08cf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b08cf-130">-ResourceGroupName</span></span>
<span data-ttu-id="b08cf-131">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="b08cf-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="b08cf-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b08cf-132">-VMScaleSetName</span></span>
<span data-ttu-id="b08cf-133">Gatunek nazwy VMSS.</span><span class="sxs-lookup"><span data-stu-id="b08cf-133">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="b08cf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b08cf-134">CommonParameters</span></span>
<span data-ttu-id="b08cf-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b08cf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b08cf-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b08cf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b08cf-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b08cf-137">INPUTS</span></span>

### <span data-ttu-id="b08cf-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b08cf-138">System.String</span></span>

## <span data-ttu-id="b08cf-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b08cf-139">OUTPUTS</span></span>

### <span data-ttu-id="b08cf-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b08cf-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b08cf-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b08cf-141">NOTES</span></span>

## <span data-ttu-id="b08cf-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b08cf-142">RELATED LINKS</span></span>

[<span data-ttu-id="b08cf-143">Nowe — AzVmss</span><span class="sxs-lookup"><span data-stu-id="b08cf-143">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="b08cf-144">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b08cf-144">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="b08cf-145">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b08cf-145">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="b08cf-146">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b08cf-146">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="b08cf-147">Start — AzVmss</span><span class="sxs-lookup"><span data-stu-id="b08cf-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="b08cf-148">Zatrzymaj — AzVmss</span><span class="sxs-lookup"><span data-stu-id="b08cf-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="b08cf-149">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b08cf-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


