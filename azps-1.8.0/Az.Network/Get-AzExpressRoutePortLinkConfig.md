---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: 5288ca32e43635db69598d72948e345f9e4c3256
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709542"
---
# <span data-ttu-id="88b69-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="88b69-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="88b69-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88b69-102">SYNOPSIS</span></span>
<span data-ttu-id="88b69-103">Pobiera konfigurację linku ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="88b69-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="88b69-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88b69-104">SYNTAX</span></span>

### <span data-ttu-id="88b69-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="88b69-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88b69-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88b69-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88b69-107">Opis</span><span class="sxs-lookup"><span data-stu-id="88b69-107">DESCRIPTION</span></span>
<span data-ttu-id="88b69-108">Polecenie cmdlet **Get-AzExpressRoutePortLinkConfig** Pobiera konfigurację linku do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="88b69-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="88b69-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88b69-109">EXAMPLES</span></span>

### <span data-ttu-id="88b69-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="88b69-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="88b69-111">Pobiera konfigurację link1 dla ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="88b69-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="88b69-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="88b69-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="88b69-113">Pobiera konfigurację linku z identyfikatorem ResourceId $id w programie ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="88b69-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="88b69-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88b69-114">PARAMETERS</span></span>

### <span data-ttu-id="88b69-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b69-115">-DefaultProfile</span></span>
<span data-ttu-id="88b69-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="88b69-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88b69-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="88b69-117">-ExpressRoutePort</span></span>
<span data-ttu-id="88b69-118">Odwołanie do zasobu ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="88b69-118">The reference of the ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="88b69-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88b69-119">-Name</span></span>
<span data-ttu-id="88b69-120">Nazwa linku.</span><span class="sxs-lookup"><span data-stu-id="88b69-120">Name of the link.</span></span>

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

### <span data-ttu-id="88b69-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88b69-121">-ResourceId</span></span>
<span data-ttu-id="88b69-122">Identyfikator zasobu linku.</span><span class="sxs-lookup"><span data-stu-id="88b69-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="88b69-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b69-123">CommonParameters</span></span>
<span data-ttu-id="88b69-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88b69-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b69-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88b69-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b69-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88b69-126">INPUTS</span></span>

### <span data-ttu-id="88b69-127">System. String</span><span class="sxs-lookup"><span data-stu-id="88b69-127">System.String</span></span>

### <span data-ttu-id="88b69-128">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="88b69-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="88b69-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88b69-129">OUTPUTS</span></span>

### <span data-ttu-id="88b69-130">Microsoft. Azure. Commands. Network. models. PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="88b69-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="88b69-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88b69-131">NOTES</span></span>

## <span data-ttu-id="88b69-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88b69-132">RELATED LINKS</span></span>
