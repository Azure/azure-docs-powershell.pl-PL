---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e6d47a040c9eb34361e0073421f618c27b4b762a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318432"
---
# <span data-ttu-id="ed15b-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="ed15b-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="ed15b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed15b-102">SYNOPSIS</span></span>
<span data-ttu-id="ed15b-103">Pobiera obiekt PeerAsn z RAMIENIa.</span><span class="sxs-lookup"><span data-stu-id="ed15b-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="ed15b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed15b-104">SYNTAX</span></span>

### <span data-ttu-id="ed15b-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ed15b-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed15b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ed15b-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed15b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ed15b-107">DESCRIPTION</span></span>
<span data-ttu-id="ed15b-108">Pobiera PeerAsn dla abonamentu.</span><span class="sxs-lookup"><span data-stu-id="ed15b-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="ed15b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed15b-109">EXAMPLES</span></span>

### <span data-ttu-id="ed15b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ed15b-110">Example 1</span></span>
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

<span data-ttu-id="ed15b-111">Pobiera PeerAsn</span><span class="sxs-lookup"><span data-stu-id="ed15b-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="ed15b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed15b-112">PARAMETERS</span></span>

### <span data-ttu-id="ed15b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed15b-113">-DefaultProfile</span></span>
<span data-ttu-id="ed15b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed15b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed15b-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ed15b-115">-Name</span></span>
<span data-ttu-id="ed15b-116">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="ed15b-116">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="ed15b-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed15b-117">-ResourceId</span></span>
<span data-ttu-id="ed15b-118">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="ed15b-118">The resource id string name.</span></span>

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

### <span data-ttu-id="ed15b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed15b-119">CommonParameters</span></span>
<span data-ttu-id="ed15b-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed15b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed15b-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed15b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed15b-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed15b-122">INPUTS</span></span>

### <span data-ttu-id="ed15b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ed15b-123">System.String</span></span>

## <span data-ttu-id="ed15b-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed15b-124">OUTPUTS</span></span>

### <span data-ttu-id="ed15b-125">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="ed15b-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="ed15b-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed15b-126">NOTES</span></span>

## <span data-ttu-id="ed15b-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed15b-127">RELATED LINKS</span></span>
