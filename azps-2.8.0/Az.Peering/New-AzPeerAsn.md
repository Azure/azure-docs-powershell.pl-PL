---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: 5ce29456e79755758989f208802e2850642fdcd7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872367"
---
# <span data-ttu-id="c9999-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="c9999-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="c9999-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9999-102">SYNOPSIS</span></span>
<span data-ttu-id="c9999-103">Tworzy nowy element ASN</span><span class="sxs-lookup"><span data-stu-id="c9999-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="c9999-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9999-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -Email <String[]> -Phone <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9999-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c9999-105">DESCRIPTION</span></span>
<span data-ttu-id="c9999-106">Tworzy nowy obiekt PeerAsn dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c9999-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="c9999-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9999-107">EXAMPLES</span></span>

### <span data-ttu-id="c9999-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c9999-108">Example 1</span></span>
```powershell
PS C:> New-AzPeerAsn -Name Contoso65050 -PeerName Contoso -PeerAsn 65050 -Emails noc@contoso.com -Phone "888-888-8889"

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="c9999-109">Tworzy nowy PeerAsn</span><span class="sxs-lookup"><span data-stu-id="c9999-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="c9999-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9999-110">PARAMETERS</span></span>

### <span data-ttu-id="c9999-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9999-111">-AsJob</span></span>
<span data-ttu-id="c9999-112">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="c9999-112">Run in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9999-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9999-113">-DefaultProfile</span></span>
<span data-ttu-id="c9999-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9999-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9999-115">-Mail</span><span class="sxs-lookup"><span data-stu-id="c9999-115">-Email</span></span>
<span data-ttu-id="c9999-116">Adres e-mail</span><span class="sxs-lookup"><span data-stu-id="c9999-116">Email</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9999-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c9999-117">-Name</span></span>
<span data-ttu-id="c9999-118">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="c9999-118">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9999-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="c9999-119">-PeerAsn</span></span>
<span data-ttu-id="c9999-120">Identyfikator zasobu elementu równorzędnego ASN. Użyj Get-AzPeerAsn, aby pobrać identyfikator.</span><span class="sxs-lookup"><span data-stu-id="c9999-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9999-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="c9999-121">-PeerName</span></span>
<span data-ttu-id="c9999-122">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="c9999-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9999-123">-Phone</span><span class="sxs-lookup"><span data-stu-id="c9999-123">-Phone</span></span>
<span data-ttu-id="c9999-124">Służb</span><span class="sxs-lookup"><span data-stu-id="c9999-124">Phone</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9999-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9999-125">-Confirm</span></span>
<span data-ttu-id="c9999-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9999-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9999-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9999-127">-WhatIf</span></span>
<span data-ttu-id="c9999-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9999-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9999-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c9999-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9999-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9999-130">CommonParameters</span></span>
<span data-ttu-id="c9999-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9999-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9999-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9999-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9999-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9999-133">INPUTS</span></span>

### <span data-ttu-id="c9999-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c9999-134">None</span></span>

## <span data-ttu-id="c9999-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9999-135">OUTPUTS</span></span>

### <span data-ttu-id="c9999-136">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="c9999-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="c9999-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9999-137">NOTES</span></span>

## <span data-ttu-id="c9999-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9999-138">RELATED LINKS</span></span>
