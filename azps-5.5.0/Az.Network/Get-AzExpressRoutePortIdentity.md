---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 246675a2473bb20e5040f3898b6931f1b3ee6933
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187155"
---
# <span data-ttu-id="e7a3d-101">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e7a3d-101">Get-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="e7a3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7a3d-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a3d-103">Uzyskaj tożsamość przypisaną do portu ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="e7a3d-103">Get identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="e7a3d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e7a3d-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7a3d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e7a3d-105">DESCRIPTION</span></span>
<span data-ttu-id="e7a3d-106">Polecenie **cmdlet Get-AzExpressRoutePortIdentity** pobiera tożsamość przypisywaną do lokalnego obiektu usługi Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="e7a3d-106">The **Get-AzExpressRoutePortIdentity** cmdlet gets identity assigned to a local Azure ExpressRoutePort object.</span></span>

## <span data-ttu-id="e7a3d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e7a3d-107">EXAMPLES</span></span>

### <span data-ttu-id="e7a3d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7a3d-108">Example 1</span></span>
```powershell
PS C:\> $exrPort = Get-AzExpressRoutePort -Name $exrPortName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzExpressRoutePortIdentity -ExpressRoutePort $exrPort
```

## <span data-ttu-id="e7a3d-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7a3d-109">PARAMETERS</span></span>

### <span data-ttu-id="e7a3d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a3d-110">-DefaultProfile</span></span>
<span data-ttu-id="e7a3d-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7a3d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7a3d-112">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e7a3d-112">-ExpressRoutePort</span></span>
<span data-ttu-id="e7a3d-113">Port usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="e7a3d-113">The ExpressRoute Port</span></span>

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

### <span data-ttu-id="e7a3d-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a3d-114">CommonParameters</span></span>
<span data-ttu-id="e7a3d-115">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7a3d-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a3d-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7a3d-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a3d-117">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7a3d-117">INPUTS</span></span>

### <span data-ttu-id="e7a3d-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e7a3d-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="e7a3d-119">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7a3d-119">OUTPUTS</span></span>

### <span data-ttu-id="e7a3d-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="e7a3d-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="e7a3d-121">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e7a3d-121">NOTES</span></span>

## <span data-ttu-id="e7a3d-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7a3d-122">RELATED LINKS</span></span>
[<span data-ttu-id="e7a3d-123">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e7a3d-123">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="e7a3d-124">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e7a3d-124">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="e7a3d-125">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e7a3d-125">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)