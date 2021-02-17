---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e6d47a040c9eb34361e0073421f618c27b4b762a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191459"
---
# <span data-ttu-id="9adcb-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="9adcb-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="9adcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9adcb-102">SYNOPSIS</span></span>
<span data-ttu-id="9adcb-103">Pobiera obiekt PeerAsn z ARM.</span><span class="sxs-lookup"><span data-stu-id="9adcb-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="9adcb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9adcb-104">SYNTAX</span></span>

### <span data-ttu-id="9adcb-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="9adcb-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9adcb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9adcb-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9adcb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9adcb-107">DESCRIPTION</span></span>
<span data-ttu-id="9adcb-108">Pobiera usługę PeerAsn dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9adcb-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="9adcb-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9adcb-109">EXAMPLES</span></span>

### <span data-ttu-id="9adcb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9adcb-110">Example 1</span></span>
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

<span data-ttu-id="9adcb-111">Pobiera do komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="9adcb-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="9adcb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9adcb-112">PARAMETERS</span></span>

### <span data-ttu-id="9adcb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9adcb-113">-DefaultProfile</span></span>
<span data-ttu-id="9adcb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9adcb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9adcb-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9adcb-115">-Name</span></span>
<span data-ttu-id="9adcb-116">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="9adcb-116">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="9adcb-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9adcb-117">-ResourceId</span></span>
<span data-ttu-id="9adcb-118">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="9adcb-118">The resource id string name.</span></span>

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

### <span data-ttu-id="9adcb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9adcb-119">CommonParameters</span></span>
<span data-ttu-id="9adcb-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9adcb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9adcb-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9adcb-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9adcb-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9adcb-122">INPUTS</span></span>

### <span data-ttu-id="9adcb-123">System.String</span><span class="sxs-lookup"><span data-stu-id="9adcb-123">System.String</span></span>

## <span data-ttu-id="9adcb-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9adcb-124">OUTPUTS</span></span>

### <span data-ttu-id="9adcb-125">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="9adcb-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="9adcb-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9adcb-126">NOTES</span></span>

## <span data-ttu-id="9adcb-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9adcb-127">RELATED LINKS</span></span>
