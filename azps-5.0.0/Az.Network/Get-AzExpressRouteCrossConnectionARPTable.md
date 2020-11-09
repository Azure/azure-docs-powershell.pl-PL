---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
ms.openlocfilehash: 30addde4594c7b67fd5ba9c1358d64ac206a4531
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309246"
---
# <span data-ttu-id="78b44-101">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="78b44-101">Get-AzExpressRouteCrossConnectionArpTable</span></span>

## <span data-ttu-id="78b44-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78b44-102">SYNOPSIS</span></span>
<span data-ttu-id="78b44-103">Pobiera tabelę ARP z połączenia z ExpressRoute krzyżowego.</span><span class="sxs-lookup"><span data-stu-id="78b44-103">Gets the ARP table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="78b44-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78b44-104">SYNTAX</span></span>

### <span data-ttu-id="78b44-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="78b44-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78b44-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="78b44-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78b44-107">Opis</span><span class="sxs-lookup"><span data-stu-id="78b44-107">DESCRIPTION</span></span>
<span data-ttu-id="78b44-108">Polecenie cmdlet **Get-AzExpressRouteCrossConnectionARPTable** pobiera tabelę ARP z obu interfejsów połączenia krzyżowego ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="78b44-108">The **Get-AzExpressRouteCrossConnectionARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute cross connection.</span></span> <span data-ttu-id="78b44-109">Tabela ARP zawiera mapowanie adresu IPv4 na adres MAC konkretnej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="78b44-109">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="78b44-110">Za pomocą tabeli ARP można sprawdzić konfigurację i łączność warstwy 2.</span><span class="sxs-lookup"><span data-stu-id="78b44-110">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="78b44-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78b44-111">EXAMPLES</span></span>

### <span data-ttu-id="78b44-112">Przykład 1. Wyświetlanie tabeli ARP dla elementu równorzędnego ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="78b44-112">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCrossConnectionARPTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="78b44-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78b44-113">PARAMETERS</span></span>

### <span data-ttu-id="78b44-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="78b44-114">-CrossConnectionName</span></span>
<span data-ttu-id="78b44-115">Nazwa połączenia krzyżowego Express Route</span><span class="sxs-lookup"><span data-stu-id="78b44-115">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78b44-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78b44-116">-DefaultProfile</span></span>
<span data-ttu-id="78b44-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="78b44-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78b44-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="78b44-118">-DevicePath</span></span>
<span data-ttu-id="78b44-119">Dopuszczalne wartości tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="78b44-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b44-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="78b44-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="78b44-121">Połączenie krzyżowe w ramach routingu Express</span><span class="sxs-lookup"><span data-stu-id="78b44-121">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78b44-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="78b44-122">-PeeringType</span></span>
<span data-ttu-id="78b44-123">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="78b44-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b44-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78b44-124">-ResourceGroupName</span></span>
<span data-ttu-id="78b44-125">Nazwa grupy zasobów zawierającej połączenie krzyżowe ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="78b44-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78b44-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78b44-126">CommonParameters</span></span>
<span data-ttu-id="78b44-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78b44-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78b44-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78b44-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78b44-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78b44-129">INPUTS</span></span>

### <span data-ttu-id="78b44-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="78b44-130">None</span></span>
<span data-ttu-id="78b44-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="78b44-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="78b44-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78b44-132">OUTPUTS</span></span>

### <span data-ttu-id="78b44-133">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="78b44-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="78b44-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78b44-134">NOTES</span></span>

## <span data-ttu-id="78b44-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78b44-135">RELATED LINKS</span></span>

[<span data-ttu-id="78b44-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="78b44-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)

[<span data-ttu-id="78b44-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="78b44-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
