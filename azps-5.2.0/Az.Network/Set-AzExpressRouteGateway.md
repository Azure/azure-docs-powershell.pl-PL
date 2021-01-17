---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: bd800f362a1a5fb66968e0f75b1211b2f0bbdf72
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339949"
---
# <span data-ttu-id="ea144-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="ea144-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="ea144-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea144-102">SYNOPSIS</span></span>
<span data-ttu-id="ea144-103">Aktualizacja skalowalnej bramy ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ea144-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="ea144-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea144-104">SYNTAX</span></span>

### <span data-ttu-id="ea144-105">ByExpressRouteGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ea144-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-MinScaleUnits <UInt32>]
 [-MaxScaleUnits <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea144-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ea144-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea144-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="ea144-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea144-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ea144-108">DESCRIPTION</span></span>

<span data-ttu-id="ea144-109">Polecenie cmdlet **Set-AzExpressRouteGateway** umożliwia zaktualizowanie jednostek skali dla istniejącej ExpressRouteGateway lub aktualizowanie znaczników zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea144-109">The **Set-AzExpressRouteGateway** cmdlet enables you to update the scale units for an existing ExpressRouteGateway or update the resource tags.</span></span>

## <span data-ttu-id="ea144-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea144-110">EXAMPLES</span></span>

### <span data-ttu-id="ea144-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ea144-111">Example 1</span></span>

```powershell
PS C:\>Set-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan =Set-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub =Set-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\>New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\>Set-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -MinScaleUnits 3

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 3
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="ea144-112">Powyższa grupa spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum danych w Stanach Zjednoczonych na zachodnim obszarze na platformie Azure w grupie zasobów "testRG".</span><span class="sxs-lookup"><span data-stu-id="ea144-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="ea144-113">Brama ExpressRoute zostanie utworzona następnie w koncentratorze wirtualnym z dwoma jednostkami skali, które zostaną zmodyfikowane na 3 jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="ea144-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="ea144-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea144-114">PARAMETERS</span></span>

### <span data-ttu-id="ea144-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea144-115">-AsJob</span></span>
<span data-ttu-id="ea144-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ea144-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea144-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea144-117">-DefaultProfile</span></span>
<span data-ttu-id="ea144-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea144-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea144-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ea144-119">-InputObject</span></span>
<span data-ttu-id="ea144-120">ExpressRouteGateway, który należy zaktualizować.</span><span class="sxs-lookup"><span data-stu-id="ea144-120">The ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea144-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="ea144-121">-MaxScaleUnits</span></span>
<span data-ttu-id="ea144-122">Maksymalna liczba jednostek skali dla tego ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="ea144-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="ea144-123">Prawidłowy zakres > 2</span><span class="sxs-lookup"><span data-stu-id="ea144-123">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea144-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="ea144-124">-MinScaleUnits</span></span>
<span data-ttu-id="ea144-125">Minimalna liczba jednostek skali dla tego ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="ea144-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="ea144-126">Prawidłowy zakres > 2</span><span class="sxs-lookup"><span data-stu-id="ea144-126">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea144-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ea144-127">-Name</span></span>
<span data-ttu-id="ea144-128">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="ea144-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea144-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea144-129">-ResourceGroupName</span></span>
<span data-ttu-id="ea144-130">Nazwa grupy zasobów ExpressRouteGateway, która ma zostać zaktualizowana.</span><span class="sxs-lookup"><span data-stu-id="ea144-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea144-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea144-131">-ResourceId</span></span>
<span data-ttu-id="ea144-132">Identyfikator ExpressRouteGateway, który należy zaktualizować.</span><span class="sxs-lookup"><span data-stu-id="ea144-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea144-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="ea144-133">-Tag</span></span>
<span data-ttu-id="ea144-134">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea144-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea144-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea144-135">-Confirm</span></span>
<span data-ttu-id="ea144-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea144-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea144-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea144-137">-WhatIf</span></span>
<span data-ttu-id="ea144-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea144-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea144-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ea144-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea144-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea144-140">CommonParameters</span></span>
<span data-ttu-id="ea144-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea144-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea144-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea144-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea144-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea144-143">INPUTS</span></span>

### <span data-ttu-id="ea144-144">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ea144-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="ea144-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ea144-145">System.String</span></span>

## <span data-ttu-id="ea144-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea144-146">OUTPUTS</span></span>

### <span data-ttu-id="ea144-147">Microsoft. Azure. Commands. Network. models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="ea144-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="ea144-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea144-148">NOTES</span></span>

## <span data-ttu-id="ea144-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea144-149">RELATED LINKS</span></span>
