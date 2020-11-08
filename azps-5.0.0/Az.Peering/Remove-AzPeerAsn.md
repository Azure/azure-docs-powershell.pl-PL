---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: b47db38e49bdc066fed9637e65d87693738a4776
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225333"
---
# <span data-ttu-id="df127-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="df127-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="df127-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df127-102">SYNOPSIS</span></span>
<span data-ttu-id="df127-103">Usuń element ASN</span><span class="sxs-lookup"><span data-stu-id="df127-103">Remove Peer Asn</span></span>

## <span data-ttu-id="df127-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df127-104">SYNTAX</span></span>

### <span data-ttu-id="df127-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="df127-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df127-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="df127-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df127-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="df127-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df127-108">Opis</span><span class="sxs-lookup"><span data-stu-id="df127-108">DESCRIPTION</span></span>
<span data-ttu-id="df127-109">Usuń PeerAsn z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="df127-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="df127-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df127-110">EXAMPLES</span></span>

### <span data-ttu-id="df127-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="df127-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="df127-112">Usuwa element ASN</span><span class="sxs-lookup"><span data-stu-id="df127-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="df127-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df127-113">PARAMETERS</span></span>

### <span data-ttu-id="df127-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df127-114">-AsJob</span></span>
<span data-ttu-id="df127-115">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="df127-115">Run in the background.</span></span>

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

### <span data-ttu-id="df127-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df127-116">-DefaultProfile</span></span>
<span data-ttu-id="df127-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df127-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df127-118">-Force</span><span class="sxs-lookup"><span data-stu-id="df127-118">-Force</span></span>
<span data-ttu-id="df127-119">{{Opis siły wypełniania}}</span><span class="sxs-lookup"><span data-stu-id="df127-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="df127-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="df127-120">-InputObject</span></span>
<span data-ttu-id="df127-121">Obiekt PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="df127-121">The PeerAsn object.</span></span>

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

### <span data-ttu-id="df127-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="df127-122">-Name</span></span>
<span data-ttu-id="df127-123">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="df127-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="df127-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df127-124">-PassThru</span></span>
<span data-ttu-id="df127-125">Zwraca wartość PRAWDA, jeśli została ukończona</span><span class="sxs-lookup"><span data-stu-id="df127-125">Return true if complete</span></span>

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

### <span data-ttu-id="df127-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df127-126">-ResourceId</span></span>
<span data-ttu-id="df127-127">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="df127-127">The resource id string name.</span></span>

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

### <span data-ttu-id="df127-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="df127-128">-Confirm</span></span>
<span data-ttu-id="df127-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df127-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df127-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df127-130">-WhatIf</span></span>
<span data-ttu-id="df127-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df127-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df127-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="df127-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df127-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df127-133">CommonParameters</span></span>
<span data-ttu-id="df127-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df127-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df127-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df127-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df127-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df127-136">INPUTS</span></span>

### <span data-ttu-id="df127-137">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="df127-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="df127-138">System. String</span><span class="sxs-lookup"><span data-stu-id="df127-138">System.String</span></span>

## <span data-ttu-id="df127-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df127-139">OUTPUTS</span></span>

### <span data-ttu-id="df127-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="df127-140">System.Boolean</span></span>

## <span data-ttu-id="df127-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df127-141">NOTES</span></span>

## <span data-ttu-id="df127-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df127-142">RELATED LINKS</span></span>
