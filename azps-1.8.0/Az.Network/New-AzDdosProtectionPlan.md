---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
ms.openlocfilehash: e301873b191a47be32298505b98eecd88cab9ac6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709331"
---
# <span data-ttu-id="9fe9a-101">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="9fe9a-101">New-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="9fe9a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9fe9a-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe9a-103">Tworzy plan ochrony DDoS.</span><span class="sxs-lookup"><span data-stu-id="9fe9a-103">Creates a DDoS protection plan.</span></span>

## <span data-ttu-id="9fe9a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9fe9a-104">SYNTAX</span></span>

```
New-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fe9a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9fe9a-105">DESCRIPTION</span></span>
<span data-ttu-id="9fe9a-106">Polecenie cmdlet New-AzDdosProtectionPlan tworzy plan ochrony DDoS.</span><span class="sxs-lookup"><span data-stu-id="9fe9a-106">The New-AzDdosProtectionPlan cmdlet creates a DDoS protection plan.</span></span>

## <span data-ttu-id="9fe9a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9fe9a-107">EXAMPLES</span></span>

### <span data-ttu-id="9fe9a-108">Przykład 1: Tworzenie i kojarzenie planu ochrony DDoS z nową siecią wirtualną</span><span class="sxs-lookup"><span data-stu-id="9fe9a-108">Example 1: Create and associate a DDoS protection plan with a new virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name SubnetName -AddressPrefix 10.0.1.0/24
D:\> $vnet = New-AzvirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName -Location "West US" -AddressPrefix 10.0.0.0/16 -DnsServer 8.8.8.8 -Subnet $subnet -EnableDdoSProtection -DdosProtectionPlanId $ddosProtectionPlan.Id
```

<span data-ttu-id="9fe9a-109">Najpierw tworzymy nowy plan ochrony DDoS za pomocą polecenia **New-AzDdosProtectionPlan** .</span><span class="sxs-lookup"><span data-stu-id="9fe9a-109">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="9fe9a-110">Następnie tworzymy nową sieć wirtualną z **nowymi — AzvirtualNetwork** i określimy identyfikator nowo utworzonego planu w parametrze **DdosProtectionPlanId**.</span><span class="sxs-lookup"><span data-stu-id="9fe9a-110">Then, we create a new virtual network with **New-AzvirtualNetwork** and we specify the ID of the newly created plan in the parameter **DdosProtectionPlanId**.</span></span> <span data-ttu-id="9fe9a-111">W tym przypadku ze względu na to, że kojarzy sieć wirtualną z planem, możemy także określić parametr **EnableDdoSProtection**.</span><span class="sxs-lookup"><span data-stu-id="9fe9a-111">In this case, since we are associating the virtual network with a plan, we can also specify the parameter **EnableDdoSProtection**.</span></span>

### <span data-ttu-id="9fe9a-112">Przykład 2: Tworzenie i kojarzenie planu ochrony DDoS z istniejącą siecią wirtualną</span><span class="sxs-lookup"><span data-stu-id="9fe9a-112">Example 2: Create and associate a DDoS protection plan with an existing virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $vnet = Get-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = New-Object Microsoft.Azure.Commands.Network.Models.PSResourceId
D:\> $vnet.DdosProtectionPlan.Id = $ddosProtectionPlan.Id
D:\> $vnet.EnableDdosProtection = $true
D:\> $vnet | Set-AzVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb"
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
                             "Etag": "W/\"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : true
DdosProtectionPlan     : {
                           "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName"
                         }
EnableVmProtection     : false
```

<span data-ttu-id="9fe9a-113">Najpierw tworzymy nowy plan ochrony DDoS za pomocą polecenia **New-AzDdosProtectionPlan** .</span><span class="sxs-lookup"><span data-stu-id="9fe9a-113">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="9fe9a-114">Następnie uzyskujemy najnowszą wersję sieci wirtualnej, którą chcemy skojarzyć z planem.</span><span class="sxs-lookup"><span data-stu-id="9fe9a-114">Second, we get the most updated version of the virtual network we want to associate with the plan.</span></span> <span data-ttu-id="9fe9a-115">Aktualizacja właściwości **DdosProtectionPlan** z obiektem **PSResourceId** zawierającym odwołanie do identyfikatora nowo utworzonego planu.</span><span class="sxs-lookup"><span data-stu-id="9fe9a-115">We update the property **DdosProtectionPlan** with a **PSResourceId** object containing a reference to the ID of the newly created plan.</span></span> <span data-ttu-id="9fe9a-116">W tym przypadku, jeśli skojarzię sieć wirtualną z planem ochrony DDoS, możemy również ustawić flagę **EnableDdosProtection** na true (prawda).</span><span class="sxs-lookup"><span data-stu-id="9fe9a-116">In this case, if we associate the virtual network with a DDoS protection plan, we can also set the flag **EnableDdosProtection** to true.</span></span>
<span data-ttu-id="9fe9a-117">Na koniec nowy stan utrzymuje się, gdy zmienna lokalna jest ustawiona na **Set-AzVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="9fe9a-117">Finally, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span>

## <span data-ttu-id="9fe9a-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9fe9a-118">PARAMETERS</span></span>

### <span data-ttu-id="9fe9a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9fe9a-119">-AsJob</span></span>
<span data-ttu-id="9fe9a-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9fe9a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9fe9a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe9a-121">-DefaultProfile</span></span>
<span data-ttu-id="9fe9a-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9fe9a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fe9a-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9fe9a-123">-Location</span></span>
<span data-ttu-id="9fe9a-124">Określa lokalizację planu ochrony DDoS, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="9fe9a-124">Specifies the location of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="9fe9a-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9fe9a-125">-Name</span></span>
<span data-ttu-id="9fe9a-126">Określa nazwę planu ochrony DDoS, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="9fe9a-126">Specifies the name of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="9fe9a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fe9a-127">-ResourceGroupName</span></span>
<span data-ttu-id="9fe9a-128">Określa grupę zasobów dla planu ochrony DDoS, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="9fe9a-128">Specifies the resource group of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="9fe9a-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="9fe9a-129">-Tag</span></span>
<span data-ttu-id="9fe9a-130">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="9fe9a-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe9a-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9fe9a-131">-Confirm</span></span>
<span data-ttu-id="9fe9a-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fe9a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fe9a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fe9a-133">-WhatIf</span></span>
<span data-ttu-id="9fe9a-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fe9a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fe9a-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9fe9a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fe9a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe9a-136">CommonParameters</span></span>
<span data-ttu-id="9fe9a-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fe9a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe9a-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fe9a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe9a-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fe9a-139">INPUTS</span></span>

### <span data-ttu-id="9fe9a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9fe9a-140">System.String</span></span>

### <span data-ttu-id="9fe9a-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9fe9a-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9fe9a-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9fe9a-142">OUTPUTS</span></span>

### <span data-ttu-id="9fe9a-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="9fe9a-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="9fe9a-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9fe9a-144">NOTES</span></span>

## <span data-ttu-id="9fe9a-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9fe9a-145">RELATED LINKS</span></span>

[<span data-ttu-id="9fe9a-146">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="9fe9a-146">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="9fe9a-147">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="9fe9a-147">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="9fe9a-148">Nowe — AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9fe9a-148">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="9fe9a-149">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9fe9a-149">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="9fe9a-150">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9fe9a-150">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)