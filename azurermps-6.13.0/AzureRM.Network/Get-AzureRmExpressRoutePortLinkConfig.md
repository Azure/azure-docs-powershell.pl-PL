---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
ms.openlocfilehash: c758131685787ec8627f6e0cd3760e2ee42107c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553512"
---
# <span data-ttu-id="3b7c6-101">Get-AzureRmExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="3b7c6-101">Get-AzureRmExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="3b7c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b7c6-102">SYNOPSIS</span></span>
<span data-ttu-id="3b7c6-103">Pobiera konfigurację linku ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-103">Gets an ExpressRoutePort link configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b7c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b7c6-104">SYNTAX</span></span>

### <span data-ttu-id="3b7c6-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3b7c6-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b7c6-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b7c6-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> -ResourceId <String> 
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b7c6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3b7c6-107">DESCRIPTION</span></span>
<span data-ttu-id="3b7c6-108">Polecenie cmdlet **Get-AzureRmExpressRoutePortLinkConfig** Pobiera konfigurację linku do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-108">The **Get-AzureRmExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="3b7c6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b7c6-109">EXAMPLES</span></span>

### <span data-ttu-id="3b7c6-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3b7c6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="3b7c6-111">Pobiera konfigurację link1 dla ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="3b7c6-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="3b7c6-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3b7c6-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="3b7c6-113">Pobiera konfigurację linku z identyfikatorem ResourceId $id w programie ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="3b7c6-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="3b7c6-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b7c6-114">PARAMETERS</span></span>

### <span data-ttu-id="3b7c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b7c6-115">-DefaultProfile</span></span>
<span data-ttu-id="3b7c6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b7c6-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3b7c6-117">-ExpressRoutePort</span></span>
<span data-ttu-id="3b7c6-118">Odwołanie do zasobu ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-118">The reference of the ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="3b7c6-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3b7c6-119">-Name</span></span>
<span data-ttu-id="3b7c6-120">Nazwa linku.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-120">Name of the link.</span></span>

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

### <span data-ttu-id="3b7c6-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b7c6-121">-ResourceId</span></span>
<span data-ttu-id="3b7c6-122">Identyfikator zasobu linku.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="3b7c6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b7c6-123">CommonParameters</span></span>
<span data-ttu-id="3b7c6-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b7c6-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b7c6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b7c6-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b7c6-126">INPUTS</span></span>

### <span data-ttu-id="3b7c6-127">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3b7c6-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="3b7c6-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b7c6-128">OUTPUTS</span></span>

### <span data-ttu-id="3b7c6-129">Microsoft. Azure. Commands. Network. models. PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="3b7c6-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="3b7c6-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b7c6-130">NOTES</span></span>

## <span data-ttu-id="3b7c6-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b7c6-131">RELATED LINKS</span></span>
