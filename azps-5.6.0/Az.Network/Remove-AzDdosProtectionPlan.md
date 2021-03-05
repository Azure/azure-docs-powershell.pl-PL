---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
ms.openlocfilehash: 8aad20fc16d160ba024dd3d4a9b6f14b65ad951e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976650"
---
# <span data-ttu-id="d7248-101">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="d7248-101">Remove-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="d7248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7248-102">SYNOPSIS</span></span>
<span data-ttu-id="d7248-103">Usuwa plan ochrony przed DDoS.</span><span class="sxs-lookup"><span data-stu-id="d7248-103">Removes a DDoS protection plan.</span></span>

## <span data-ttu-id="d7248-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d7248-104">SYNTAX</span></span>

```
Remove-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7248-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d7248-105">DESCRIPTION</span></span>
<span data-ttu-id="d7248-106">Polecenie Remove-AzDdosProtectionPlan cmdlet usuwa plan ochrony przed DDoS.</span><span class="sxs-lookup"><span data-stu-id="d7248-106">The Remove-AzDdosProtectionPlan cmdlet removes a DDoS protection plan.</span></span>

## <span data-ttu-id="d7248-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d7248-107">EXAMPLES</span></span>

### <span data-ttu-id="d7248-108">Przykład 1. Usuwanie pustego planu ochrony przed DDoS</span><span class="sxs-lookup"><span data-stu-id="d7248-108">Example 1: Remove an empty DDoS protection plan</span></span>
```
D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="d7248-109">W tym przypadku usuwamy plan ochrony przed DDoS zgodnie z określonymi.</span><span class="sxs-lookup"><span data-stu-id="d7248-109">In this case, we remove a DDoS protection plan as specified.</span></span>

### <span data-ttu-id="d7248-110">Przykład 2. Usuwanie planu ochrony przed DDoS skojarzonego z siecią wirtualną</span><span class="sxs-lookup"><span data-stu-id="d7248-110">Example 2: Remove a DDoS protection plan associated with a virtual network</span></span>
```
D:\> $vnet = Get-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = $null
D:\> $vnet.EnableDdosProtection = $false
D:\> $vnet | Set-AzVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"65947351-747e-4686-aa8b-c40da58f6c8b"
ResourceGuid           : fcb7bc1e-ee0d-4005-b3f1-feda76e3756c
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "10.0.0.0/16"
                           ]
                         }
DhcpOptions            : {
                           "DnsServers": [
                             "8.8.8.8"
                           ]
                         }
Subnets                : [
                           {
                             "Name": "SubnetName",
                             "Etag": "W/\"65947351-747e-4686-aa8b-c40da58f6c8b\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
EnableVmProtection     : false


D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="d7248-111">Planów ochrony przed DDoS nie można usunąć, jeśli są skojarzone z siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="d7248-111">DDoS protection plans cannot be deleted if they are associated with a virtual network.</span></span> <span data-ttu-id="d7248-112">Pierwszym krokiem jest więc nieskojarzenie obu obiektów.</span><span class="sxs-lookup"><span data-stu-id="d7248-112">So the first step is to disassociate both objects.</span></span> <span data-ttu-id="d7248-113">Tutaj jest skojarzona najbardziej zaktualizowana wersja sieci wirtualnej skojarzonej z planem i ustawiamy dla właściwości **DdosProtectionPlan** wartość pustą i flagę **EnableDdosProtection** (ta flaga nie może zostać spełniona bez planu).</span><span class="sxs-lookup"><span data-stu-id="d7248-113">Here, we get the most updated version of the virtual network associated with the plan, and we set the property **DdosProtectionPlan** to an empty value and the flag **EnableDdosProtection** (this flag cannot be true without a plan).</span></span>
<span data-ttu-id="d7248-114">Następnie utrzymujemy nowy stan, rurując zmienną lokalną do **Set-AzVirtualNetwork.**</span><span class="sxs-lookup"><span data-stu-id="d7248-114">Then, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span> <span data-ttu-id="d7248-115">W tym momencie plan nie jest już skojarzony z siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="d7248-115">At this point, the plan is no longer associated with the virtual network.</span></span>
<span data-ttu-id="d7248-116">Jeśli jest to ostatni plan skojarzony z planem, możemy usunąć plan ochrony DDoS za pomocą polecenia Remove-AzDdosProtectionPlan.</span><span class="sxs-lookup"><span data-stu-id="d7248-116">If this is the last one associated with the plan, we can remove the DDoS protection plan by using the command Remove-AzDdosProtectionPlan.</span></span>

## <span data-ttu-id="d7248-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7248-117">PARAMETERS</span></span>

### <span data-ttu-id="d7248-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7248-118">-DefaultProfile</span></span>
<span data-ttu-id="d7248-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7248-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7248-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d7248-120">-Name</span></span>
<span data-ttu-id="d7248-121">Określa nazwę planu ochrony przed DDoS do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d7248-121">Specifies the name of the DDoS protection plan to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7248-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7248-122">-PassThru</span></span>
<span data-ttu-id="d7248-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="d7248-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d7248-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d7248-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d7248-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7248-125">-ResourceGroupName</span></span>
<span data-ttu-id="d7248-126">Określa grupę zasobów planu ochrony przed DDoS do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d7248-126">Specifies the resource group of the DDoS protection plan to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7248-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7248-127">-Confirm</span></span>
<span data-ttu-id="d7248-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d7248-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7248-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7248-129">-WhatIf</span></span>
<span data-ttu-id="d7248-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7248-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7248-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d7248-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7248-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7248-132">CommonParameters</span></span>
<span data-ttu-id="d7248-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7248-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7248-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7248-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7248-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7248-135">INPUTS</span></span>

### <span data-ttu-id="d7248-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d7248-136">System.String</span></span>

## <span data-ttu-id="d7248-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7248-137">OUTPUTS</span></span>

### <span data-ttu-id="d7248-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d7248-138">System.Boolean</span></span>

## <span data-ttu-id="d7248-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d7248-139">NOTES</span></span>

## <span data-ttu-id="d7248-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7248-140">RELATED LINKS</span></span>

[<span data-ttu-id="d7248-141">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="d7248-141">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="d7248-142">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="d7248-142">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="d7248-143">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d7248-143">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="d7248-144">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d7248-144">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="d7248-145">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d7248-145">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)