---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
ms.openlocfilehash: b8ce7dac361124129b3261d8ba368852726812ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869748"
---
# <span data-ttu-id="060b8-101">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="060b8-101">Remove-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="060b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="060b8-102">SYNOPSIS</span></span>
<span data-ttu-id="060b8-103">Usuwa plan ochrony DDoS.</span><span class="sxs-lookup"><span data-stu-id="060b8-103">Removes a DDoS protection plan.</span></span>

## <span data-ttu-id="060b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="060b8-104">SYNTAX</span></span>

```
Remove-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="060b8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="060b8-105">DESCRIPTION</span></span>
<span data-ttu-id="060b8-106">Polecenie cmdlet Remove-AzDdosProtectionPlan usuwa plan ochrony DDoS.</span><span class="sxs-lookup"><span data-stu-id="060b8-106">The Remove-AzDdosProtectionPlan cmdlet removes a DDoS protection plan.</span></span>

## <span data-ttu-id="060b8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="060b8-107">EXAMPLES</span></span>

### <span data-ttu-id="060b8-108">Przykład 1: Usuwanie pustego planu ochrony DDoS</span><span class="sxs-lookup"><span data-stu-id="060b8-108">Example 1: Remove an empty DDoS protection plan</span></span>
```
D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="060b8-109">W tym przypadku firma Microsoft usunie plan ochrony DDoS, jak określono.</span><span class="sxs-lookup"><span data-stu-id="060b8-109">In this case, we remove a DDoS protection plan as specified.</span></span>

### <span data-ttu-id="060b8-110">Przykład 2: usuwanie planu ochrony DDoS skojarzonego z siecią wirtualną</span><span class="sxs-lookup"><span data-stu-id="060b8-110">Example 2: Remove a DDoS protection plan associated with a virtual network</span></span>
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

<span data-ttu-id="060b8-111">Nie można usunąć planów ochrony DDoS, jeśli są one skojarzone z siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="060b8-111">DDoS protection plans cannot be deleted if they are associated with a virtual network.</span></span> <span data-ttu-id="060b8-112">Dlatego pierwszy krok polega na skojarzeniu obu obiektów.</span><span class="sxs-lookup"><span data-stu-id="060b8-112">So the first step is to disassociate both objects.</span></span> <span data-ttu-id="060b8-113">W tym przypadku dostępna jest Najnowsza wersja sieci wirtualnej skojarzona z planem, a właściwość **DdosProtectionPlan** jest ustawiona na wartość pustą, a flaga **EnableDdosProtection** (Ta flaga nie może być prawdziwa bez planu).</span><span class="sxs-lookup"><span data-stu-id="060b8-113">Here, we get the most updated version of the virtual network associated with the plan, and we set the property **DdosProtectionPlan** to an empty value and the flag **EnableDdosProtection** (this flag cannot be true without a plan).</span></span>
<span data-ttu-id="060b8-114">Następnie utrzymujemy nowy stan, przełączając zmienną lokalną do **Set-AzVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="060b8-114">Then, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span> <span data-ttu-id="060b8-115">W tym momencie plan nie jest już skojarzony z siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="060b8-115">At this point, the plan is no longer associated with the virtual network.</span></span>
<span data-ttu-id="060b8-116">Jeśli jest to Ostatnia skojarzona z planem, możemy usunąć plan ochrony DDoS przy użyciu polecenia Remove-AzDdosProtectionPlan.</span><span class="sxs-lookup"><span data-stu-id="060b8-116">If this is the last one associated with the plan, we can remove the DDoS protection plan by using the command Remove-AzDdosProtectionPlan.</span></span>

## <span data-ttu-id="060b8-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="060b8-117">PARAMETERS</span></span>

### <span data-ttu-id="060b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="060b8-118">-DefaultProfile</span></span>
<span data-ttu-id="060b8-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="060b8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="060b8-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="060b8-120">-Name</span></span>
<span data-ttu-id="060b8-121">Określa nazwę planu ochrony DDoS, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="060b8-121">Specifies the name of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="060b8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="060b8-122">-PassThru</span></span>
<span data-ttu-id="060b8-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="060b8-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="060b8-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="060b8-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="060b8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="060b8-125">-ResourceGroupName</span></span>
<span data-ttu-id="060b8-126">Określa grupę zasobów planu ochrony DDoS, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="060b8-126">Specifies the resource group of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="060b8-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="060b8-127">-Confirm</span></span>
<span data-ttu-id="060b8-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="060b8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="060b8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="060b8-129">-WhatIf</span></span>
<span data-ttu-id="060b8-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="060b8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="060b8-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="060b8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="060b8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="060b8-132">CommonParameters</span></span>
<span data-ttu-id="060b8-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="060b8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="060b8-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="060b8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="060b8-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="060b8-135">INPUTS</span></span>

### <span data-ttu-id="060b8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="060b8-136">System.String</span></span>

## <span data-ttu-id="060b8-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="060b8-137">OUTPUTS</span></span>

### <span data-ttu-id="060b8-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="060b8-138">System.Boolean</span></span>

## <span data-ttu-id="060b8-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="060b8-139">NOTES</span></span>

## <span data-ttu-id="060b8-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="060b8-140">RELATED LINKS</span></span>

[<span data-ttu-id="060b8-141">Nowe — AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="060b8-141">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="060b8-142">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="060b8-142">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="060b8-143">Nowe — AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="060b8-143">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="060b8-144">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="060b8-144">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="060b8-145">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="060b8-145">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)