---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: cf27cf7f82e44ec52978b3d04af973ba47cd1632
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184043"
---
# <span data-ttu-id="e1f5f-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="e1f5f-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="e1f5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f5f-103">Tworzy nową równorzędną asn</span><span class="sxs-lookup"><span data-stu-id="e1f5f-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="e1f5f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e1f5f-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -ContactDetail <PSContactDetail[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1f5f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e1f5f-105">DESCRIPTION</span></span>
<span data-ttu-id="e1f5f-106">Tworzy nowy obiekt komunikacji równorzędnej dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e1f5f-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="e1f5f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e1f5f-107">EXAMPLES</span></span>

### <span data-ttu-id="e1f5f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e1f5f-108">Example 1</span></span>
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

<span data-ttu-id="e1f5f-109">Tworzy nową peerasn</span><span class="sxs-lookup"><span data-stu-id="e1f5f-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="e1f5f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1f5f-110">PARAMETERS</span></span>

### <span data-ttu-id="e1f5f-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e1f5f-111">-AsJob</span></span>
<span data-ttu-id="e1f5f-112">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="e1f5f-112">Run in the background.</span></span>

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

### <span data-ttu-id="e1f5f-113">-ContactDetail</span><span class="sxs-lookup"><span data-stu-id="e1f5f-113">-ContactDetail</span></span>
<span data-ttu-id="e1f5f-114">Adresy e-mail używane do kontaktowania się w przypadku, gdy problemy są zwykle związane z Centrum operacji sieciowych</span><span class="sxs-lookup"><span data-stu-id="e1f5f-114">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="e1f5f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f5f-115">-DefaultProfile</span></span>
<span data-ttu-id="e1f5f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1f5f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1f5f-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e1f5f-117">-Name</span></span>
<span data-ttu-id="e1f5f-118">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="e1f5f-118">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e1f5f-119">- PeerAsn</span><span class="sxs-lookup"><span data-stu-id="e1f5f-119">-PeerAsn</span></span>
<span data-ttu-id="e1f5f-120">Identyfikator zasobu równorzędnego asn. Użyj Get-AzPeerAsn, aby pobrać identyfikator.</span><span class="sxs-lookup"><span data-stu-id="e1f5f-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="e1f5f-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="e1f5f-121">-PeerName</span></span>
<span data-ttu-id="e1f5f-122">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="e1f5f-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e1f5f-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e1f5f-123">-Confirm</span></span>
<span data-ttu-id="e1f5f-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e1f5f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1f5f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1f5f-125">-WhatIf</span></span>
<span data-ttu-id="e1f5f-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1f5f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1f5f-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e1f5f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1f5f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f5f-128">CommonParameters</span></span>
<span data-ttu-id="e1f5f-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1f5f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f5f-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1f5f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f5f-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1f5f-131">INPUTS</span></span>

### <span data-ttu-id="e1f5f-132">Brak</span><span class="sxs-lookup"><span data-stu-id="e1f5f-132">None</span></span>

## <span data-ttu-id="e1f5f-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e1f5f-133">OUTPUTS</span></span>

### <span data-ttu-id="e1f5f-134">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="e1f5f-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="e1f5f-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e1f5f-135">NOTES</span></span>

## <span data-ttu-id="e1f5f-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1f5f-136">RELATED LINKS</span></span>
