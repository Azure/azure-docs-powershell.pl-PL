---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePort.md
ms.openlocfilehash: 36c15c9a0bfae9bbf3a14f59877d23c1c8778163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719094"
---
# <span data-ttu-id="c3186-101">Get-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c3186-101">Get-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="c3186-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3186-102">SYNOPSIS</span></span>
<span data-ttu-id="c3186-103">Pobiera zasób usługi Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="c3186-103">Gets an Azure ExpressRoutePort resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3186-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3186-104">SYNTAX</span></span>

### <span data-ttu-id="c3186-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c3186-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3186-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3186-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3186-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c3186-107">DESCRIPTION</span></span>
<span data-ttu-id="c3186-108">Polecenie cmdlet **Get-AzureRmExpressRoutePort** służy do pobierania obiektu ExpressRoutePort z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c3186-108">The **Get-AzureRmExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="c3186-109">Zwrócony obiekt expressrouteport może być wykorzystywany jako dane wejściowe dla innych poleceń cmdlet, które działają na ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="c3186-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="c3186-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3186-110">EXAMPLES</span></span>

### <span data-ttu-id="c3186-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c3186-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="c3186-112">Pobiera obiekt ExpressRoutePort o nazwie $PortName w grupie zasobów $rg w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c3186-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="c3186-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c3186-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePort -ResourceId $id
```

<span data-ttu-id="c3186-114">Pobiera obiekt ExpressRoutePort o identyfikatorze ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="c3186-114">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="c3186-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3186-115">PARAMETERS</span></span>

### <span data-ttu-id="c3186-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3186-116">-DefaultProfile</span></span>
<span data-ttu-id="c3186-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3186-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3186-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c3186-118">-Name</span></span>
<span data-ttu-id="c3186-119">Nazwa ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="c3186-119">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3186-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3186-120">-ResourceGroupName</span></span>
<span data-ttu-id="c3186-121">Nazwa grupy zasobów ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="c3186-121">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3186-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3186-122">-ResourceId</span></span>
<span data-ttu-id="c3186-123">Identyfikator zasobu Express Route port.</span><span class="sxs-lookup"><span data-stu-id="c3186-123">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3186-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3186-124">CommonParameters</span></span>
<span data-ttu-id="c3186-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3186-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3186-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3186-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3186-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3186-127">INPUTS</span></span>

### <span data-ttu-id="c3186-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c3186-128">System.String</span></span>

## <span data-ttu-id="c3186-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3186-129">OUTPUTS</span></span>

### <span data-ttu-id="c3186-130">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c3186-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="c3186-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3186-131">NOTES</span></span>

## <span data-ttu-id="c3186-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3186-132">RELATED LINKS</span></span>
