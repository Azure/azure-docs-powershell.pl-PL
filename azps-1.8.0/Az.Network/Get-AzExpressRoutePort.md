---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: 69a03bc9772e9d74fdc1863221c99b46620ae700
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709543"
---
# <span data-ttu-id="11b6b-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="11b6b-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="11b6b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="11b6b-103">Pobiera zasób usługi Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="11b6b-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="11b6b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11b6b-104">SYNTAX</span></span>

### <span data-ttu-id="11b6b-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="11b6b-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11b6b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11b6b-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11b6b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="11b6b-107">DESCRIPTION</span></span>
<span data-ttu-id="11b6b-108">Polecenie cmdlet **Get-AzExpressRoutePort** służy do pobierania obiektu ExpressRoutePort z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="11b6b-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="11b6b-109">Zwrócony obiekt expressrouteport może być wykorzystywany jako dane wejściowe dla innych poleceń cmdlet, które działają na ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="11b6b-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="11b6b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11b6b-110">EXAMPLES</span></span>

### <span data-ttu-id="11b6b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="11b6b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="11b6b-112">Pobiera obiekt ExpressRoutePort o nazwie $PortName w grupie zasobów $rg w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="11b6b-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="11b6b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="11b6b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="11b6b-114">Pobiera wszystkie obiekty ExpressRoutePort, których nazwa zaczyna się od tekstu "test".</span><span class="sxs-lookup"><span data-stu-id="11b6b-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="11b6b-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="11b6b-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="11b6b-116">Pobiera obiekt ExpressRoutePort o identyfikatorze ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="11b6b-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="11b6b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11b6b-117">PARAMETERS</span></span>

### <span data-ttu-id="11b6b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b6b-118">-DefaultProfile</span></span>
<span data-ttu-id="11b6b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="11b6b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11b6b-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="11b6b-120">-Name</span></span>
<span data-ttu-id="11b6b-121">Nazwa ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="11b6b-121">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="11b6b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11b6b-122">-ResourceGroupName</span></span>
<span data-ttu-id="11b6b-123">Nazwa grupy zasobów ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="11b6b-123">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="11b6b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11b6b-124">-ResourceId</span></span>
<span data-ttu-id="11b6b-125">Identyfikator zasobu Express Route port.</span><span class="sxs-lookup"><span data-stu-id="11b6b-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="11b6b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b6b-126">CommonParameters</span></span>
<span data-ttu-id="11b6b-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11b6b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b6b-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11b6b-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b6b-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11b6b-129">INPUTS</span></span>

### <span data-ttu-id="11b6b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="11b6b-130">System.String</span></span>

## <span data-ttu-id="11b6b-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11b6b-131">OUTPUTS</span></span>

### <span data-ttu-id="11b6b-132">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="11b6b-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="11b6b-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11b6b-133">NOTES</span></span>

## <span data-ttu-id="11b6b-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11b6b-134">RELATED LINKS</span></span>

[<span data-ttu-id="11b6b-135">Nowe — AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="11b6b-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="11b6b-136">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="11b6b-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="11b6b-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="11b6b-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
