---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: cf27cf7f82e44ec52978b3d04af973ba47cd1632
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336094"
---
# <span data-ttu-id="39e6b-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="39e6b-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="39e6b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="39e6b-103">Tworzy nowy element ASN</span><span class="sxs-lookup"><span data-stu-id="39e6b-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="39e6b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39e6b-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -ContactDetail <PSContactDetail[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39e6b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="39e6b-105">DESCRIPTION</span></span>
<span data-ttu-id="39e6b-106">Tworzy nowy obiekt PeerAsn dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="39e6b-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="39e6b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39e6b-107">EXAMPLES</span></span>

### <span data-ttu-id="39e6b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="39e6b-108">Example 1</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="39e6b-109">Tworzy nowy PeerAsn</span><span class="sxs-lookup"><span data-stu-id="39e6b-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="39e6b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39e6b-110">PARAMETERS</span></span>

### <span data-ttu-id="39e6b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39e6b-111">-AsJob</span></span>
<span data-ttu-id="39e6b-112">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="39e6b-112">Run in the background.</span></span>

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

### <span data-ttu-id="39e6b-113">-ContactDetail</span><span class="sxs-lookup"><span data-stu-id="39e6b-113">-ContactDetail</span></span>
<span data-ttu-id="39e6b-114">Adresy e-mail używane do kontaktowania się, jeśli problemy Arrise zwykle Network Operation Center</span><span class="sxs-lookup"><span data-stu-id="39e6b-114">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39e6b-115">-DefaultProfile</span></span>
<span data-ttu-id="39e6b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="39e6b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39e6b-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="39e6b-117">-Name</span></span>
<span data-ttu-id="39e6b-118">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="39e6b-118">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="39e6b-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="39e6b-119">-PeerAsn</span></span>
<span data-ttu-id="39e6b-120">Identyfikator zasobu elementu równorzędnego ASN. Użyj Get-AzPeerAsn, aby pobrać identyfikator.</span><span class="sxs-lookup"><span data-stu-id="39e6b-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="39e6b-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="39e6b-121">-PeerName</span></span>
<span data-ttu-id="39e6b-122">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="39e6b-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="39e6b-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="39e6b-123">-Confirm</span></span>
<span data-ttu-id="39e6b-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39e6b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39e6b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39e6b-125">-WhatIf</span></span>
<span data-ttu-id="39e6b-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39e6b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39e6b-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="39e6b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39e6b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39e6b-128">CommonParameters</span></span>
<span data-ttu-id="39e6b-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39e6b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39e6b-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39e6b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39e6b-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39e6b-131">INPUTS</span></span>

### <span data-ttu-id="39e6b-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="39e6b-132">None</span></span>

## <span data-ttu-id="39e6b-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39e6b-133">OUTPUTS</span></span>

### <span data-ttu-id="39e6b-134">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="39e6b-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="39e6b-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39e6b-135">NOTES</span></span>

## <span data-ttu-id="39e6b-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39e6b-136">RELATED LINKS</span></span>
