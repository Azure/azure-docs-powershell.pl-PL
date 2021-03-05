---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: 9498183e66a0991f7a724065bb5a88e954cd6594
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989605"
---
# <span data-ttu-id="3fd18-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="3fd18-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="3fd18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fd18-102">SYNOPSIS</span></span>
<span data-ttu-id="3fd18-103">Pobiera obiekt PeerAsn z ARM.</span><span class="sxs-lookup"><span data-stu-id="3fd18-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="3fd18-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3fd18-104">SYNTAX</span></span>

### <span data-ttu-id="3fd18-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="3fd18-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fd18-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3fd18-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fd18-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3fd18-107">DESCRIPTION</span></span>
<span data-ttu-id="3fd18-108">Pobiera usługę PeerAsn dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3fd18-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="3fd18-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3fd18-109">EXAMPLES</span></span>

### <span data-ttu-id="3fd18-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3fd18-110">Example 1</span></span>
```powershell
PS C:> Get-AzPeerAsn -Name Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="3fd18-111">Pobiera do komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="3fd18-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="3fd18-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fd18-112">PARAMETERS</span></span>

### <span data-ttu-id="3fd18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fd18-113">-DefaultProfile</span></span>
<span data-ttu-id="3fd18-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd18-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fd18-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3fd18-115">-Name</span></span>
<span data-ttu-id="3fd18-116">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="3fd18-116">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd18-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fd18-117">-ResourceId</span></span>
<span data-ttu-id="3fd18-118">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="3fd18-118">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fd18-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fd18-119">CommonParameters</span></span>
<span data-ttu-id="3fd18-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fd18-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fd18-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3fd18-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fd18-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fd18-122">INPUTS</span></span>

### <span data-ttu-id="3fd18-123">System.String</span><span class="sxs-lookup"><span data-stu-id="3fd18-123">System.String</span></span>

## <span data-ttu-id="3fd18-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fd18-124">OUTPUTS</span></span>

### <span data-ttu-id="3fd18-125">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="3fd18-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="3fd18-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3fd18-126">NOTES</span></span>

## <span data-ttu-id="3fd18-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3fd18-127">RELATED LINKS</span></span>
