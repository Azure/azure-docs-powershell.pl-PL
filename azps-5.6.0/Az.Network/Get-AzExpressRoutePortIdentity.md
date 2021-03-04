---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
ms.openlocfilehash: a64bbe0dfad8e9e82138c50e6ff436a445f68392
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957018"
---
# <span data-ttu-id="a6c1b-101">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="a6c1b-101">Get-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="a6c1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c1b-103">Uzyskaj tożsamość przypisaną do portu ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="a6c1b-103">Get identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="a6c1b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a6c1b-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6c1b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a6c1b-105">DESCRIPTION</span></span>
<span data-ttu-id="a6c1b-106">Polecenie **cmdlet Get-AzExpressRoutePortIdentity** otrzymuje tożsamość przypisywaną do lokalnego obiektu usługi Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="a6c1b-106">The **Get-AzExpressRoutePortIdentity** cmdlet gets identity assigned to a local Azure ExpressRoutePort object.</span></span>

## <span data-ttu-id="a6c1b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a6c1b-107">EXAMPLES</span></span>

### <span data-ttu-id="a6c1b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a6c1b-108">Example 1</span></span>
```powershell
PS C:\> $exrPort = Get-AzExpressRoutePort -Name $exrPortName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzExpressRoutePortIdentity -ExpressRoutePort $exrPort
```

## <span data-ttu-id="a6c1b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6c1b-109">PARAMETERS</span></span>

### <span data-ttu-id="a6c1b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6c1b-110">-DefaultProfile</span></span>
<span data-ttu-id="a6c1b-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c1b-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6c1b-112">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a6c1b-112">-ExpressRoutePort</span></span>
<span data-ttu-id="a6c1b-113">Port usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="a6c1b-113">The ExpressRoute Port</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6c1b-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c1b-114">CommonParameters</span></span>
<span data-ttu-id="a6c1b-115">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6c1b-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c1b-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6c1b-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c1b-117">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6c1b-117">INPUTS</span></span>

### <span data-ttu-id="a6c1b-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a6c1b-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="a6c1b-119">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6c1b-119">OUTPUTS</span></span>

### <span data-ttu-id="a6c1b-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="a6c1b-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="a6c1b-121">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a6c1b-121">NOTES</span></span>

## <span data-ttu-id="a6c1b-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6c1b-122">RELATED LINKS</span></span>
[<span data-ttu-id="a6c1b-123">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="a6c1b-123">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="a6c1b-124">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="a6c1b-124">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="a6c1b-125">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="a6c1b-125">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)