---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: f9ce00bb5efbe5182143a08f9f205101b9f85611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979585"
---
# <span data-ttu-id="3df16-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3df16-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="3df16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3df16-102">SYNOPSIS</span></span>
<span data-ttu-id="3df16-103">Pobiera zasób Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="3df16-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="3df16-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3df16-104">SYNTAX</span></span>

### <span data-ttu-id="3df16-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="3df16-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3df16-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3df16-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3df16-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3df16-107">DESCRIPTION</span></span>
<span data-ttu-id="3df16-108">Polecenie **cmdlet Get-AzExpressRoutePort** służy do pobierania obiektu ExpressRoutePort z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3df16-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="3df16-109">Zwrócony obiekt expressrouteport może być używany jako dane wejściowe do innych cmdlet, które operują na expressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="3df16-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="3df16-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3df16-110">EXAMPLES</span></span>

### <span data-ttu-id="3df16-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3df16-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="3df16-112">Pobiera obiekt ExpressRoutePort o nazwie $PortName w grupie zasobów $rg w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3df16-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="3df16-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3df16-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="3df16-114">Pobiera wszystkie obiekty expressRoutePort, których nazwa zaczyna się od "test".</span><span class="sxs-lookup"><span data-stu-id="3df16-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="3df16-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="3df16-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="3df16-116">Pobiera obiekt ExpressRoutePort z właściwością ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="3df16-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="3df16-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3df16-117">PARAMETERS</span></span>

### <span data-ttu-id="3df16-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df16-118">-DefaultProfile</span></span>
<span data-ttu-id="3df16-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3df16-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3df16-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3df16-120">-Name</span></span>
<span data-ttu-id="3df16-121">Nazwa portu expressroutePort.</span><span class="sxs-lookup"><span data-stu-id="3df16-121">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="3df16-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3df16-122">-ResourceGroupName</span></span>
<span data-ttu-id="3df16-123">Nazwa grupy zasobów dlaportu ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="3df16-123">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="3df16-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3df16-124">-ResourceId</span></span>
<span data-ttu-id="3df16-125">ResourceId portu trasy ekspresowej.</span><span class="sxs-lookup"><span data-stu-id="3df16-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="3df16-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df16-126">CommonParameters</span></span>
<span data-ttu-id="3df16-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3df16-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df16-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3df16-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df16-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3df16-129">INPUTS</span></span>

### <span data-ttu-id="3df16-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3df16-130">System.String</span></span>

## <span data-ttu-id="3df16-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3df16-131">OUTPUTS</span></span>

### <span data-ttu-id="3df16-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3df16-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="3df16-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3df16-133">NOTES</span></span>

## <span data-ttu-id="3df16-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3df16-134">RELATED LINKS</span></span>

[<span data-ttu-id="3df16-135">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3df16-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="3df16-136">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3df16-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="3df16-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3df16-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
