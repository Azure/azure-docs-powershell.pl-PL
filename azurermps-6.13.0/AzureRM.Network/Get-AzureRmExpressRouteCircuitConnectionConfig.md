---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 4d9442ba87ba46704aaa93b31f41f111519c980b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553520"
---
# <span data-ttu-id="42cf9-101">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="42cf9-101">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="42cf9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="42cf9-103">Pobiera konfigurację połączenia obwodu ExpressRoute powiązaną z prywatnym elementem równorzędnym ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="42cf9-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42cf9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42cf9-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42cf9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="42cf9-105">DESCRIPTION</span></span>
<span data-ttu-id="42cf9-106">Polecenie cmdlet **Get-AzureRmExpressRouteCircuitConnectionConfig** Pobiera konfigurację połączenia obwodu powiązanego z prywatnym łączem równorzędnym na obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="42cf9-106">The **Get-AzureRmExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="42cf9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42cf9-107">EXAMPLES</span></span>

### <span data-ttu-id="42cf9-108">Przykład 1: Wyświetlanie konfiguracji połączenia obwodowego obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="42cf9-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="42cf9-109">Przykład 2: Pobieranie zasobu połączenia obwodowego skojarzonego ze obwodem ExpressRoute przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="42cf9-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="42cf9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42cf9-110">PARAMETERS</span></span>

### <span data-ttu-id="42cf9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42cf9-111">-DefaultProfile</span></span>
<span data-ttu-id="42cf9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="42cf9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42cf9-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="42cf9-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="42cf9-114">Obiekt obwodu ExpressRoute zawierający konfigurację połączenia obwodowego.</span><span class="sxs-lookup"><span data-stu-id="42cf9-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42cf9-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="42cf9-115">-Name</span></span>
<span data-ttu-id="42cf9-116">Nazwa konfiguracji połączenia obwodowego, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="42cf9-116">The name of the circuit connection configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42cf9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42cf9-117">CommonParameters</span></span>
<span data-ttu-id="42cf9-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42cf9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42cf9-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42cf9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42cf9-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42cf9-120">INPUTS</span></span>

### <span data-ttu-id="42cf9-121">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="42cf9-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="42cf9-122">Parametry: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="42cf9-122">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="42cf9-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42cf9-123">OUTPUTS</span></span>

### <span data-ttu-id="42cf9-124">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="42cf9-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="42cf9-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42cf9-125">NOTES</span></span>

## <span data-ttu-id="42cf9-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42cf9-126">RELATED LINKS</span></span>

[<span data-ttu-id="42cf9-127">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="42cf9-127">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="42cf9-128">Dodaj-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="42cf9-128">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="42cf9-129">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="42cf9-129">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="42cf9-130">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="42cf9-130">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="42cf9-131">Nowe — AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="42cf9-131">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)
