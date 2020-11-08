---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: 670880a9fa82e4845f37cdb5f0d108533a2b72c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223119"
---
# <span data-ttu-id="51b99-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="51b99-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="51b99-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51b99-102">SYNOPSIS</span></span>
<span data-ttu-id="51b99-103">Pobiera zasób usługi Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="51b99-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="51b99-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51b99-104">SYNTAX</span></span>

### <span data-ttu-id="51b99-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="51b99-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51b99-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51b99-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51b99-107">Opis</span><span class="sxs-lookup"><span data-stu-id="51b99-107">DESCRIPTION</span></span>
<span data-ttu-id="51b99-108">Polecenie cmdlet **Get-AzExpressRoutePort** służy do pobierania obiektu ExpressRoutePort z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="51b99-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="51b99-109">Zwrócony obiekt expressrouteport może być wykorzystywany jako dane wejściowe dla innych poleceń cmdlet, które działają na ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="51b99-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="51b99-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51b99-110">EXAMPLES</span></span>

### <span data-ttu-id="51b99-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="51b99-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="51b99-112">Pobiera obiekt ExpressRoutePort o nazwie $PortName w grupie zasobów $rg w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="51b99-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="51b99-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="51b99-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="51b99-114">Pobiera wszystkie obiekty ExpressRoutePort, których nazwa zaczyna się od tekstu "test".</span><span class="sxs-lookup"><span data-stu-id="51b99-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="51b99-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="51b99-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="51b99-116">Pobiera obiekt ExpressRoutePort o identyfikatorze ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="51b99-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="51b99-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51b99-117">PARAMETERS</span></span>

### <span data-ttu-id="51b99-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b99-118">-DefaultProfile</span></span>
<span data-ttu-id="51b99-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="51b99-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51b99-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="51b99-120">-Name</span></span>
<span data-ttu-id="51b99-121">Nazwa ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="51b99-121">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="51b99-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51b99-122">-ResourceGroupName</span></span>
<span data-ttu-id="51b99-123">Nazwa grupy zasobów ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="51b99-123">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="51b99-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51b99-124">-ResourceId</span></span>
<span data-ttu-id="51b99-125">Identyfikator zasobu Express Route port.</span><span class="sxs-lookup"><span data-stu-id="51b99-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="51b99-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b99-126">CommonParameters</span></span>
<span data-ttu-id="51b99-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51b99-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b99-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51b99-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b99-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51b99-129">INPUTS</span></span>

### <span data-ttu-id="51b99-130">System. String</span><span class="sxs-lookup"><span data-stu-id="51b99-130">System.String</span></span>

## <span data-ttu-id="51b99-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51b99-131">OUTPUTS</span></span>

### <span data-ttu-id="51b99-132">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="51b99-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="51b99-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51b99-133">NOTES</span></span>

## <span data-ttu-id="51b99-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51b99-134">RELATED LINKS</span></span>

[<span data-ttu-id="51b99-135">Nowe — AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="51b99-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="51b99-136">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="51b99-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="51b99-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="51b99-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
