---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e2588e1516b8b0ee41e260b27ea40ed72a199613
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872399"
---
# <span data-ttu-id="7094b-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="7094b-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="7094b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7094b-102">SYNOPSIS</span></span>
<span data-ttu-id="7094b-103">Pobiera obiekt PeerAsn z RAMIENIa.</span><span class="sxs-lookup"><span data-stu-id="7094b-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="7094b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7094b-104">SYNTAX</span></span>

```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7094b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7094b-105">DESCRIPTION</span></span>
<span data-ttu-id="7094b-106">Pobiera PeerAsn dla abonamentu.</span><span class="sxs-lookup"><span data-stu-id="7094b-106">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="7094b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7094b-107">EXAMPLES</span></span>

### <span data-ttu-id="7094b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7094b-108">Example 1</span></span>
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

<span data-ttu-id="7094b-109">Pobiera PeerAsn</span><span class="sxs-lookup"><span data-stu-id="7094b-109">Gets the PeerAsn</span></span>

## <span data-ttu-id="7094b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7094b-110">PARAMETERS</span></span>

### <span data-ttu-id="7094b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7094b-111">-DefaultProfile</span></span>
<span data-ttu-id="7094b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7094b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7094b-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7094b-113">-Name</span></span>
<span data-ttu-id="7094b-114">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="7094b-114">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="7094b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7094b-115">CommonParameters</span></span>
<span data-ttu-id="7094b-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7094b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7094b-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7094b-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7094b-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7094b-118">INPUTS</span></span>

### <span data-ttu-id="7094b-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7094b-119">None</span></span>

## <span data-ttu-id="7094b-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7094b-120">OUTPUTS</span></span>

### <span data-ttu-id="7094b-121">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="7094b-121">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="7094b-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7094b-122">NOTES</span></span>

## <span data-ttu-id="7094b-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7094b-123">RELATED LINKS</span></span>
