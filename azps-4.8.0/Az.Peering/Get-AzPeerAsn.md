---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e6d47a040c9eb34361e0073421f618c27b4b762a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063269"
---
# <span data-ttu-id="a66cc-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="a66cc-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="a66cc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a66cc-102">SYNOPSIS</span></span>
<span data-ttu-id="a66cc-103">Pobiera obiekt PeerAsn z RAMIENIa.</span><span class="sxs-lookup"><span data-stu-id="a66cc-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="a66cc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a66cc-104">SYNTAX</span></span>

### <span data-ttu-id="a66cc-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a66cc-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a66cc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a66cc-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a66cc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a66cc-107">DESCRIPTION</span></span>
<span data-ttu-id="a66cc-108">Pobiera PeerAsn dla abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a66cc-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="a66cc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a66cc-109">EXAMPLES</span></span>

### <span data-ttu-id="a66cc-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a66cc-110">Example 1</span></span>
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

<span data-ttu-id="a66cc-111">Pobiera PeerAsn</span><span class="sxs-lookup"><span data-stu-id="a66cc-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="a66cc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a66cc-112">PARAMETERS</span></span>

### <span data-ttu-id="a66cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a66cc-113">-DefaultProfile</span></span>
<span data-ttu-id="a66cc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a66cc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a66cc-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a66cc-115">-Name</span></span>
<span data-ttu-id="a66cc-116">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="a66cc-116">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="a66cc-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a66cc-117">-ResourceId</span></span>
<span data-ttu-id="a66cc-118">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="a66cc-118">The resource id string name.</span></span>

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

### <span data-ttu-id="a66cc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a66cc-119">CommonParameters</span></span>
<span data-ttu-id="a66cc-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a66cc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a66cc-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a66cc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a66cc-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a66cc-122">INPUTS</span></span>

### <span data-ttu-id="a66cc-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a66cc-123">System.String</span></span>

## <span data-ttu-id="a66cc-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a66cc-124">OUTPUTS</span></span>

### <span data-ttu-id="a66cc-125">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="a66cc-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="a66cc-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a66cc-126">NOTES</span></span>

## <span data-ttu-id="a66cc-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a66cc-127">RELATED LINKS</span></span>
