---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: 197d18f5d7585f6ae7e865b1c2b0449d032b4238
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203085"
---
# <span data-ttu-id="7773b-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="7773b-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="7773b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7773b-102">SYNOPSIS</span></span>
<span data-ttu-id="7773b-103">Pobiera konfigurację linku do usługi ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7773b-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="7773b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7773b-104">SYNTAX</span></span>

### <span data-ttu-id="7773b-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="7773b-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7773b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7773b-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7773b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7773b-107">DESCRIPTION</span></span>
<span data-ttu-id="7773b-108">Polecenie **cmdlet Get-AzExpressRoutePortLinkConfig** pobiera konfigurację linku do usługi ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7773b-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="7773b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7773b-109">EXAMPLES</span></span>

### <span data-ttu-id="7773b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7773b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="7773b-111">Pobiera konfigurację Link1 usługi ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="7773b-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="7773b-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7773b-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="7773b-113">Pobiera konfigurację linku za pomocą usługi ResourceId $id w uchcie ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="7773b-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="7773b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7773b-114">PARAMETERS</span></span>

### <span data-ttu-id="7773b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7773b-115">-DefaultProfile</span></span>
<span data-ttu-id="7773b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7773b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7773b-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7773b-117">-ExpressRoutePort</span></span>
<span data-ttu-id="7773b-118">Odwołanie do zasobu ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7773b-118">The reference of the ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7773b-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7773b-119">-Name</span></span>
<span data-ttu-id="7773b-120">Nazwa linku.</span><span class="sxs-lookup"><span data-stu-id="7773b-120">Name of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7773b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7773b-121">-ResourceId</span></span>
<span data-ttu-id="7773b-122">ResourceId linku.</span><span class="sxs-lookup"><span data-stu-id="7773b-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="7773b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7773b-123">CommonParameters</span></span>
<span data-ttu-id="7773b-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7773b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7773b-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7773b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7773b-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7773b-126">INPUTS</span></span>

### <span data-ttu-id="7773b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="7773b-127">System.String</span></span>

### <span data-ttu-id="7773b-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7773b-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="7773b-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7773b-129">OUTPUTS</span></span>

### <span data-ttu-id="7773b-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="7773b-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="7773b-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7773b-131">NOTES</span></span>

## <span data-ttu-id="7773b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7773b-132">RELATED LINKS</span></span>
