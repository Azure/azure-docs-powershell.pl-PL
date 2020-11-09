---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: 7cc9dbe5c4727c283ead66e88b6c52c9c2fcd00e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309162"
---
# <span data-ttu-id="dfba9-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="dfba9-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="dfba9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dfba9-102">SYNOPSIS</span></span>
<span data-ttu-id="dfba9-103">Aktualizacja skalowalnej bramy ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dfba9-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="dfba9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dfba9-104">SYNTAX</span></span>

### <span data-ttu-id="dfba9-105">ByExpressRouteGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dfba9-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 -MaxScaleUnits <UInt32> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfba9-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="dfba9-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dfba9-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="dfba9-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dfba9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dfba9-108">DESCRIPTION</span></span>

<span data-ttu-id="dfba9-109">Set-AzExpressRouteGateway aktualizuje jednostki skali dla ExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="dfba9-109">Set-AzExpressRouteGateway updates the scale units for the ExpressRouteGateway</span></span>

## <span data-ttu-id="dfba9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dfba9-110">EXAMPLES</span></span>

### <span data-ttu-id="dfba9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dfba9-111">Example 1</span></span>

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

<span data-ttu-id="dfba9-112">Powyższa grupa spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum danych w Stanach Zjednoczonych na zachodnim obszarze na platformie Azure w grupie zasobów "testRG".</span><span class="sxs-lookup"><span data-stu-id="dfba9-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="dfba9-113">Brama ExpressRoute zostanie utworzona następnie w koncentratorze wirtualnym z dwoma jednostkami skali, które zostaną zmodyfikowane na 3 jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="dfba9-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="dfba9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dfba9-114">PARAMETERS</span></span>

### <span data-ttu-id="dfba9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfba9-115">-AsJob</span></span>
<span data-ttu-id="dfba9-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="dfba9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dfba9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfba9-117">-DefaultProfile</span></span>
<span data-ttu-id="dfba9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dfba9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfba9-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dfba9-119">-InputObject</span></span>
<span data-ttu-id="dfba9-120">ExpressRouteGateway, który należy zaktualizować.</span><span class="sxs-lookup"><span data-stu-id="dfba9-120">The ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="dfba9-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="dfba9-121">-MaxScaleUnits</span></span>
<span data-ttu-id="dfba9-122">Maksymalna liczba jednostek skali dla tego ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="dfba9-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="dfba9-123">Prawidłowy zakres > 2</span><span class="sxs-lookup"><span data-stu-id="dfba9-123">Valid range > 2</span></span>

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

### <span data-ttu-id="dfba9-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="dfba9-124">-MinScaleUnits</span></span>
<span data-ttu-id="dfba9-125">Minimalna liczba jednostek skali dla tego ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="dfba9-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="dfba9-126">Prawidłowy zakres > 2</span><span class="sxs-lookup"><span data-stu-id="dfba9-126">Valid range > 2</span></span>

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

### <span data-ttu-id="dfba9-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dfba9-127">-Name</span></span>
<span data-ttu-id="dfba9-128">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="dfba9-128">The resource name.</span></span>

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

### <span data-ttu-id="dfba9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfba9-129">-ResourceGroupName</span></span>
<span data-ttu-id="dfba9-130">Nazwa grupy zasobów ExpressRouteGateway, która ma zostać zaktualizowana.</span><span class="sxs-lookup"><span data-stu-id="dfba9-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

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

### <span data-ttu-id="dfba9-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfba9-131">-ResourceId</span></span>
<span data-ttu-id="dfba9-132">Identyfikator ExpressRouteGateway, który należy zaktualizować.</span><span class="sxs-lookup"><span data-stu-id="dfba9-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

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

### <span data-ttu-id="dfba9-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="dfba9-133">-Tag</span></span>
<span data-ttu-id="dfba9-134">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="dfba9-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="dfba9-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dfba9-135">-Confirm</span></span>
<span data-ttu-id="dfba9-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfba9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfba9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfba9-137">-WhatIf</span></span>
<span data-ttu-id="dfba9-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfba9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfba9-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dfba9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfba9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfba9-140">CommonParameters</span></span>
<span data-ttu-id="dfba9-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfba9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfba9-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfba9-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfba9-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dfba9-143">INPUTS</span></span>

### <span data-ttu-id="dfba9-144">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="dfba9-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="dfba9-145">System. String</span><span class="sxs-lookup"><span data-stu-id="dfba9-145">System.String</span></span>

## <span data-ttu-id="dfba9-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dfba9-146">OUTPUTS</span></span>

### <span data-ttu-id="dfba9-147">Microsoft. Azure. Commands. Network. models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="dfba9-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="dfba9-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dfba9-148">NOTES</span></span>

## <span data-ttu-id="dfba9-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dfba9-149">RELATED LINKS</span></span>
