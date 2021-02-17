---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: 7a369fafec712d23c7ac2aac30d3aa6928877355
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184699"
---
# <span data-ttu-id="f4ba1-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4ba1-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="f4ba1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4ba1-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ba1-103">Otrzymuje publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="f4ba1-103">Gets a public IP address.</span></span>

## <span data-ttu-id="f4ba1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f4ba1-104">SYNTAX</span></span>

### <span data-ttu-id="f4ba1-105">NoExpandStandAloneIp (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f4ba1-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4ba1-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="f4ba1-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4ba1-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="f4ba1-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4ba1-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="f4ba1-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4ba1-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="f4ba1-109">DESCRIPTION</span></span>
<span data-ttu-id="f4ba1-110">Polecenie **cmdlet Get-AzPublicIPAddress** pobiera jeden lub więcej publicznych adresów IP w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f4ba1-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="f4ba1-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f4ba1-111">EXAMPLES</span></span>

### <span data-ttu-id="f4ba1-112">Przykład 1. Uzyskiwanie publicznego zasobu adresów IP</span><span class="sxs-lookup"><span data-stu-id="f4ba1-112">Example 1: Get a public IP resource</span></span>
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

<span data-ttu-id="f4ba1-113">To polecenie pobiera publiczny zasób adresu IP o nazwie myPublicIp w grupie zasobów myRg.</span><span class="sxs-lookup"><span data-stu-id="f4ba1-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="f4ba1-114">Przykład 2. Uzyskiwanie publicznych zasobów IP przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="f4ba1-114">Example 2: Get public IP resources using filtering</span></span>
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

<span data-ttu-id="f4ba1-115">To polecenie pobiera wszystkie zasoby publicznych adresów IP, których nazwa zaczyna się od myPublicIp.</span><span class="sxs-lookup"><span data-stu-id="f4ba1-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="f4ba1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4ba1-116">PARAMETERS</span></span>

### <span data-ttu-id="f4ba1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ba1-117">-DefaultProfile</span></span>
<span data-ttu-id="f4ba1-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ba1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4ba1-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f4ba1-119">-ExpandResource</span></span>
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

### <span data-ttu-id="f4ba1-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f4ba1-120">-IpConfigurationName</span></span>
<span data-ttu-id="f4ba1-121">Nazwa konfiguracji protokołu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="f4ba1-121">Network Interface IP Configuration Name.</span></span>

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

### <span data-ttu-id="f4ba1-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f4ba1-122">-Name</span></span>
<span data-ttu-id="f4ba1-123">Określa nazwę publicznego adresu IP, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4ba1-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f4ba1-124">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="f4ba1-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="f4ba1-125">Nazwa interfejsu sieciowego maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="f4ba1-125">Virtual Machine Network Interface Name.</span></span>

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

### <span data-ttu-id="f4ba1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ba1-126">-ResourceGroupName</span></span>
<span data-ttu-id="f4ba1-127">Określa nazwę grupy zasobów zawierającej publiczny adres IP, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4ba1-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f4ba1-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="f4ba1-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="f4ba1-129">Indeks maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="f4ba1-129">Virtual Machine Index.</span></span>

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

### <span data-ttu-id="f4ba1-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f4ba1-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="f4ba1-131">Nazwa zestawu skal maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="f4ba1-131">Virtual Machine Scale Set Name.</span></span>

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

### <span data-ttu-id="f4ba1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ba1-132">CommonParameters</span></span>
<span data-ttu-id="f4ba1-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4ba1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ba1-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4ba1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ba1-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4ba1-135">INPUTS</span></span>

### <span data-ttu-id="f4ba1-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f4ba1-136">System.String</span></span>

## <span data-ttu-id="f4ba1-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f4ba1-137">OUTPUTS</span></span>

### <span data-ttu-id="f4ba1-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4ba1-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="f4ba1-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f4ba1-139">NOTES</span></span>

## <span data-ttu-id="f4ba1-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4ba1-140">RELATED LINKS</span></span>

[<span data-ttu-id="f4ba1-141">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4ba1-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="f4ba1-142">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4ba1-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="f4ba1-143">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4ba1-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


