---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: 559d2d8c069d7e36630600d0fcdc16ea475da9f9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053457"
---
# <span data-ttu-id="081d4-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="081d4-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="081d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="081d4-102">SYNOPSIS</span></span>
<span data-ttu-id="081d4-103">Pobiera obiekt PeerAsn z RAMIENIa.</span><span class="sxs-lookup"><span data-stu-id="081d4-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="081d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="081d4-104">SYNTAX</span></span>

```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="081d4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="081d4-105">DESCRIPTION</span></span>
<span data-ttu-id="081d4-106">Pobiera PeerAsn dla abonamentu.</span><span class="sxs-lookup"><span data-stu-id="081d4-106">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="081d4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="081d4-107">EXAMPLES</span></span>

### <span data-ttu-id="081d4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="081d4-108">Example 1</span></span>
```powershell
PS C:> Get-AzPeerAsn -PeerName Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="081d4-109">Pobiera PeerAsn</span><span class="sxs-lookup"><span data-stu-id="081d4-109">Gets the PeerAsn</span></span>

## <span data-ttu-id="081d4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="081d4-110">PARAMETERS</span></span>

### <span data-ttu-id="081d4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="081d4-111">-DefaultProfile</span></span>
<span data-ttu-id="081d4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="081d4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="081d4-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="081d4-113">-Name</span></span>
<span data-ttu-id="081d4-114">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="081d4-114">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="081d4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="081d4-115">CommonParameters</span></span>
<span data-ttu-id="081d4-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="081d4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="081d4-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="081d4-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="081d4-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="081d4-118">INPUTS</span></span>

### <span data-ttu-id="081d4-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="081d4-119">None</span></span>

## <span data-ttu-id="081d4-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="081d4-120">OUTPUTS</span></span>

### <span data-ttu-id="081d4-121">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="081d4-121">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="081d4-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="081d4-122">NOTES</span></span>

## <span data-ttu-id="081d4-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="081d4-123">RELATED LINKS</span></span>
