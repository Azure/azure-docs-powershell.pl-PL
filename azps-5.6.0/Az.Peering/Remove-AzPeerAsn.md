---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: a5b50fd4d57fc7036196decdb7b967e2867b21f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989325"
---
# <span data-ttu-id="cccb5-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="cccb5-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="cccb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cccb5-102">SYNOPSIS</span></span>
<span data-ttu-id="cccb5-103">Usuń współpracowników</span><span class="sxs-lookup"><span data-stu-id="cccb5-103">Remove Peer Asn</span></span>

## <span data-ttu-id="cccb5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cccb5-104">SYNTAX</span></span>

### <span data-ttu-id="cccb5-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="cccb5-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cccb5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cccb5-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cccb5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cccb5-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cccb5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cccb5-108">DESCRIPTION</span></span>
<span data-ttu-id="cccb5-109">Usuń subskrypcję z usługi PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="cccb5-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="cccb5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cccb5-110">EXAMPLES</span></span>

### <span data-ttu-id="cccb5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cccb5-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="cccb5-112">Usuwa współpracownika</span><span class="sxs-lookup"><span data-stu-id="cccb5-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="cccb5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cccb5-113">PARAMETERS</span></span>

### <span data-ttu-id="cccb5-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="cccb5-114">-AsJob</span></span>
<span data-ttu-id="cccb5-115">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="cccb5-115">Run in the background.</span></span>

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

### <span data-ttu-id="cccb5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cccb5-116">-DefaultProfile</span></span>
<span data-ttu-id="cccb5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cccb5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cccb5-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="cccb5-118">-Force</span></span>
<span data-ttu-id="cccb5-119">{{ Fill Force Description }}</span><span class="sxs-lookup"><span data-stu-id="cccb5-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="cccb5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cccb5-120">-InputObject</span></span>
<span data-ttu-id="cccb5-121">Obiekt PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="cccb5-121">The PeerAsn object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cccb5-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cccb5-122">-Name</span></span>
<span data-ttu-id="cccb5-123">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="cccb5-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cccb5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cccb5-124">-PassThru</span></span>
<span data-ttu-id="cccb5-125">Zwracanie wartości prawda, jeśli są ukończone</span><span class="sxs-lookup"><span data-stu-id="cccb5-125">Return true if complete</span></span>

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

### <span data-ttu-id="cccb5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cccb5-126">-ResourceId</span></span>
<span data-ttu-id="cccb5-127">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="cccb5-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cccb5-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cccb5-128">-Confirm</span></span>
<span data-ttu-id="cccb5-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cccb5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cccb5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cccb5-130">-WhatIf</span></span>
<span data-ttu-id="cccb5-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cccb5-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cccb5-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cccb5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cccb5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cccb5-133">CommonParameters</span></span>
<span data-ttu-id="cccb5-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cccb5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cccb5-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cccb5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cccb5-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cccb5-136">INPUTS</span></span>

### <span data-ttu-id="cccb5-137">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="cccb5-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="cccb5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cccb5-138">System.String</span></span>

## <span data-ttu-id="cccb5-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cccb5-139">OUTPUTS</span></span>

### <span data-ttu-id="cccb5-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cccb5-140">System.Boolean</span></span>

## <span data-ttu-id="cccb5-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cccb5-141">NOTES</span></span>

## <span data-ttu-id="cccb5-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cccb5-142">RELATED LINKS</span></span>
