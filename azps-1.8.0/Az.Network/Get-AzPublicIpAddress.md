---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: 38eff375baa948098ac66c8e2b3c3fe1849f3bc0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709471"
---
# <span data-ttu-id="27415-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="27415-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="27415-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="27415-102">SYNOPSIS</span></span>
<span data-ttu-id="27415-103">Pobiera publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="27415-103">Gets a public IP address.</span></span>

## <span data-ttu-id="27415-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="27415-104">SYNTAX</span></span>

### <span data-ttu-id="27415-105">NoExpandStandAloneIp (domyślny)</span><span class="sxs-lookup"><span data-stu-id="27415-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27415-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="27415-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27415-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="27415-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27415-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="27415-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27415-109">Opis</span><span class="sxs-lookup"><span data-stu-id="27415-109">DESCRIPTION</span></span>
<span data-ttu-id="27415-110">Polecenie cmdlet **Get-AzPublicIPAddress** pobiera co najmniej jeden publiczny adres IP w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="27415-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="27415-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="27415-111">EXAMPLES</span></span>

### <span data-ttu-id="27415-112">1: uzyskiwanie publicznego zasobu IP</span><span class="sxs-lookup"><span data-stu-id="27415-112">1: Get a public IP resource</span></span>
```
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
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="27415-113">To polecenie pobiera publiczny zasób adres IP z nazwą myPublicIp w myRg grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="27415-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="27415-114">2: uzyskiwanie publicznych zasobów IP przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="27415-114">2: Get public IP resources using filtering</span></span>
```
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
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="27415-115">To polecenie uzyskuje wszystkie zasoby publicznych adresów IP, których nazwa zaczyna się od myPublicIp.</span><span class="sxs-lookup"><span data-stu-id="27415-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="27415-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="27415-116">PARAMETERS</span></span>

### <span data-ttu-id="27415-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27415-117">-DefaultProfile</span></span>
<span data-ttu-id="27415-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="27415-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27415-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="27415-119">-ExpandResource</span></span>
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

### <span data-ttu-id="27415-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="27415-120">-IpConfigurationName</span></span>
<span data-ttu-id="27415-121">Nazwa konfiguracji adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="27415-121">Network Interface IP Configuration Name.</span></span>

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

### <span data-ttu-id="27415-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="27415-122">-Name</span></span>
<span data-ttu-id="27415-123">Określa nazwę publicznego adresu IP, który ma być pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27415-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="27415-124">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="27415-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="27415-125">Nazwa interfejsu sieci maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="27415-125">Virtual Machine Network Interface Name.</span></span>

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

### <span data-ttu-id="27415-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27415-126">-ResourceGroupName</span></span>
<span data-ttu-id="27415-127">Określa nazwę grupy zasobów zawierającej publiczny adres IP, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27415-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="27415-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="27415-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="27415-129">Indeks maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="27415-129">Virtual Machine Index.</span></span>

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

### <span data-ttu-id="27415-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="27415-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="27415-131">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="27415-131">Virtual Machine Scale Set Name.</span></span>

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

### <span data-ttu-id="27415-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27415-132">CommonParameters</span></span>
<span data-ttu-id="27415-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27415-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27415-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27415-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27415-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27415-135">INPUTS</span></span>

### <span data-ttu-id="27415-136">System. String</span><span class="sxs-lookup"><span data-stu-id="27415-136">System.String</span></span>

## <span data-ttu-id="27415-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="27415-137">OUTPUTS</span></span>

### <span data-ttu-id="27415-138">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="27415-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="27415-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="27415-139">NOTES</span></span>

## <span data-ttu-id="27415-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27415-140">RELATED LINKS</span></span>

[<span data-ttu-id="27415-141">Nowe — AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="27415-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="27415-142">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="27415-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="27415-143">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="27415-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)

