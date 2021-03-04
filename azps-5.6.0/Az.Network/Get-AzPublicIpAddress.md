---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: d9a0d35b58a69bca8a48cdb42342a720c8bc6da1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954113"
---
# <span data-ttu-id="7078a-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7078a-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="7078a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7078a-102">SYNOPSIS</span></span>
<span data-ttu-id="7078a-103">Otrzymuje publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="7078a-103">Gets a public IP address.</span></span>

## <span data-ttu-id="7078a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7078a-104">SYNTAX</span></span>

### <span data-ttu-id="7078a-105">NoExpandStandAloneIp (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7078a-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7078a-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="7078a-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7078a-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="7078a-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7078a-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="7078a-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7078a-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="7078a-109">DESCRIPTION</span></span>
<span data-ttu-id="7078a-110">Polecenie **cmdlet Get-AzPublicIPAddress** pobiera jeden lub więcej publicznych adresów IP w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7078a-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="7078a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7078a-111">EXAMPLES</span></span>

### <span data-ttu-id="7078a-112">Przykład 1. Uzyskiwanie publicznego zasobu adresów IP</span><span class="sxs-lookup"><span data-stu-id="7078a-112">Example 1: Get a public IP resource</span></span>
```powershell
Get-AzPublicIpAddress -Name myPublicIp1 -ResourceGroupName myRg

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic", 
                             "Tier": "Regional"
                           }
IpTags                   : []
```

<span data-ttu-id="7078a-113">To polecenie pobiera publiczny zasób adresu IP o nazwie myPublicIp w grupie zasobów myRg.</span><span class="sxs-lookup"><span data-stu-id="7078a-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="7078a-114">Przykład 2. Uzyskiwanie publicznych zasobów IP przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="7078a-114">Example 2: Get public IP resources using filtering</span></span>
```powershell
Get-AzPublicIpAddress -Name myPublicIp*

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
IpTags                   : []
```

<span data-ttu-id="7078a-115">To polecenie pobiera wszystkie zasoby publicznych adresów IP, których nazwa zaczyna się od myPublicIp.</span><span class="sxs-lookup"><span data-stu-id="7078a-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="7078a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7078a-116">PARAMETERS</span></span>

### <span data-ttu-id="7078a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7078a-117">-DefaultProfile</span></span>
<span data-ttu-id="7078a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7078a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7078a-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="7078a-119">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7078a-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7078a-120">-IpConfigurationName</span></span>
<span data-ttu-id="7078a-121">Nazwa konfiguracji protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="7078a-121">Network Interface IP Configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7078a-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7078a-122">-Name</span></span>
<span data-ttu-id="7078a-123">Określa nazwę publicznego adresu IP, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7078a-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7078a-124">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="7078a-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="7078a-125">Nazwa interfejsu sieciowego maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="7078a-125">Virtual Machine Network Interface Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7078a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7078a-126">-ResourceGroupName</span></span>
<span data-ttu-id="7078a-127">Określa nazwę grupy zasobów zawierającej publiczny adres IP, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7078a-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7078a-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="7078a-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="7078a-129">Indeks maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="7078a-129">Virtual Machine Index.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7078a-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7078a-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="7078a-131">Nazwa zestawu skal maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="7078a-131">Virtual Machine Scale Set Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7078a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7078a-132">CommonParameters</span></span>
<span data-ttu-id="7078a-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7078a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7078a-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7078a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7078a-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7078a-135">INPUTS</span></span>

### <span data-ttu-id="7078a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7078a-136">System.String</span></span>

## <span data-ttu-id="7078a-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7078a-137">OUTPUTS</span></span>

### <span data-ttu-id="7078a-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7078a-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="7078a-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7078a-139">NOTES</span></span>

## <span data-ttu-id="7078a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7078a-140">RELATED LINKS</span></span>

[<span data-ttu-id="7078a-141">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7078a-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="7078a-142">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7078a-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="7078a-143">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7078a-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


