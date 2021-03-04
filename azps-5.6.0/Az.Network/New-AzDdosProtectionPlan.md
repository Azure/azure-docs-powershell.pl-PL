---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
ms.openlocfilehash: 0a8386a4ed91fa6e35adafbdc8ec532bb781f75e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958570"
---
# <span data-ttu-id="f9f21-101">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="f9f21-101">New-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="f9f21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9f21-102">SYNOPSIS</span></span>
<span data-ttu-id="f9f21-103">Tworzy plan ochrony przed DDoS.</span><span class="sxs-lookup"><span data-stu-id="f9f21-103">Creates a DDoS protection plan.</span></span>

## <span data-ttu-id="f9f21-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f9f21-104">SYNTAX</span></span>

```
New-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9f21-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f9f21-105">DESCRIPTION</span></span>
<span data-ttu-id="f9f21-106">Polecenie New-AzDdosProtectionPlan cmdlet tworzy plan ochrony przed DDoS.</span><span class="sxs-lookup"><span data-stu-id="f9f21-106">The New-AzDdosProtectionPlan cmdlet creates a DDoS protection plan.</span></span>

## <span data-ttu-id="f9f21-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f9f21-107">EXAMPLES</span></span>

### <span data-ttu-id="f9f21-108">Przykład 1. Tworzenie i kojarzenie planu ochrony przed DDoS z nową siecią wirtualną</span><span class="sxs-lookup"><span data-stu-id="f9f21-108">Example 1: Create and associate a DDoS protection plan with a new virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name SubnetName -AddressPrefix 10.0.1.0/24
D:\> $vnet = New-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName -Location "West US" -AddressPrefix 10.0.0.0/16 -DnsServer 8.8.8.8 -Subnet $subnet -EnableDdoSProtection -DdosProtectionPlanId $ddosProtectionPlan.Id
```

<span data-ttu-id="f9f21-109">Najpierw tworzymy nowy plan ochrony DDoS za pomocą **polecenia New-AzDdosProtectionPlan.**</span><span class="sxs-lookup"><span data-stu-id="f9f21-109">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="f9f21-110">Następnie tworzymy nową sieć wirtualną za pomocą **funkcji New-AzVirtualNetwork** i określamy identyfikator nowo utworzonego planu w parametrze **DdosProtectionPlanId.**</span><span class="sxs-lookup"><span data-stu-id="f9f21-110">Then, we create a new virtual network with **New-AzVirtualNetwork** and we specify the ID of the newly created plan in the parameter **DdosProtectionPlanId**.</span></span> <span data-ttu-id="f9f21-111">W tym przypadku, ponieważ kojarzymy sieć wirtualną z planem, możemy również określić parametr **EnableDdoSProtection.**</span><span class="sxs-lookup"><span data-stu-id="f9f21-111">In this case, since we are associating the virtual network with a plan, we can also specify the parameter **EnableDdoSProtection**.</span></span>

### <span data-ttu-id="f9f21-112">Przykład 2. Tworzenie i kojarzenie planu ochrony przed DDoS z istniejącą siecią wirtualną</span><span class="sxs-lookup"><span data-stu-id="f9f21-112">Example 2: Create and associate a DDoS protection plan with an existing virtual network</span></span>
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

<span data-ttu-id="f9f21-113">Najpierw tworzymy nowy plan ochrony DDoS za pomocą **polecenia New-AzDdosProtectionPlan.**</span><span class="sxs-lookup"><span data-stu-id="f9f21-113">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="f9f21-114">Po drugie, otrzymuję najbardziej zaktualizowaną wersję sieci wirtualnej, którą chcemy skojarzyć z planem.</span><span class="sxs-lookup"><span data-stu-id="f9f21-114">Second, we get the most updated version of the virtual network we want to associate with the plan.</span></span> <span data-ttu-id="f9f21-115">Aktualizujemy właściwość **DdosProtectionPlan** za pomocą obiektu **PSResourceId zawierającego** odwołanie do identyfikatora nowo utworzonego planu.</span><span class="sxs-lookup"><span data-stu-id="f9f21-115">We update the property **DdosProtectionPlan** with a **PSResourceId** object containing a reference to the ID of the newly created plan.</span></span> <span data-ttu-id="f9f21-116">W takim przypadku, jeśli skojarzymy sieć wirtualną z planem ochrony przed DDoS, możemy również ustawić dla flagi **EnableDdosProtection** wartość true.</span><span class="sxs-lookup"><span data-stu-id="f9f21-116">In this case, if we associate the virtual network with a DDoS protection plan, we can also set the flag **EnableDdosProtection** to true.</span></span>
<span data-ttu-id="f9f21-117">Na koniec utrzymujemy nowy stan, ustawiając zmienną lokalną do **Set-AzVirtualNetwork.**</span><span class="sxs-lookup"><span data-stu-id="f9f21-117">Finally, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span>

## <span data-ttu-id="f9f21-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9f21-118">PARAMETERS</span></span>

### <span data-ttu-id="f9f21-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f9f21-119">-AsJob</span></span>
<span data-ttu-id="f9f21-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f9f21-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9f21-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9f21-121">-DefaultProfile</span></span>
<span data-ttu-id="f9f21-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9f21-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9f21-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f9f21-123">-Location</span></span>
<span data-ttu-id="f9f21-124">Określa lokalizację planu ochrony przed DDoS, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="f9f21-124">Specifies the location of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="f9f21-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f9f21-125">-Name</span></span>
<span data-ttu-id="f9f21-126">Określa nazwę planu ochrony przed DDoS, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="f9f21-126">Specifies the name of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="f9f21-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9f21-127">-ResourceGroupName</span></span>
<span data-ttu-id="f9f21-128">Określa grupę zasobów planu ochrony przed DDoS, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="f9f21-128">Specifies the resource group of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="f9f21-129">— Tag</span><span class="sxs-lookup"><span data-stu-id="f9f21-129">-Tag</span></span>
<span data-ttu-id="f9f21-130">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="f9f21-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f9f21-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f9f21-131">-Confirm</span></span>
<span data-ttu-id="f9f21-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f9f21-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9f21-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9f21-133">-WhatIf</span></span>
<span data-ttu-id="f9f21-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9f21-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9f21-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f9f21-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9f21-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9f21-136">CommonParameters</span></span>
<span data-ttu-id="f9f21-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9f21-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9f21-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9f21-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9f21-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9f21-139">INPUTS</span></span>

### <span data-ttu-id="f9f21-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f9f21-140">System.String</span></span>

### <span data-ttu-id="f9f21-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f9f21-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f9f21-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9f21-142">OUTPUTS</span></span>

### <span data-ttu-id="f9f21-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="f9f21-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="f9f21-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f9f21-144">NOTES</span></span>

## <span data-ttu-id="f9f21-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9f21-145">RELATED LINKS</span></span>

[<span data-ttu-id="f9f21-146">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="f9f21-146">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="f9f21-147">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="f9f21-147">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="f9f21-148">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f9f21-148">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="f9f21-149">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f9f21-149">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="f9f21-150">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f9f21-150">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)