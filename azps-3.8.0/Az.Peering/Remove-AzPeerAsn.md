---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: d1ff0baeff3bf4b5747ff1d024b0de6e5184688a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051726"
---
# <span data-ttu-id="ba9a0-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="ba9a0-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="ba9a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba9a0-102">SYNOPSIS</span></span>
<span data-ttu-id="ba9a0-103">Usuń element ASN</span><span class="sxs-lookup"><span data-stu-id="ba9a0-103">Remove Peer Asn</span></span>

## <span data-ttu-id="ba9a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba9a0-104">SYNTAX</span></span>

### <span data-ttu-id="ba9a0-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ba9a0-105">Default (Default)</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba9a0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ba9a0-106">ByName</span></span>
```
Remove-AzPeerAsn [-Name] <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba9a0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ba9a0-107">DESCRIPTION</span></span>
<span data-ttu-id="ba9a0-108">Usuń PeerAsn z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ba9a0-108">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="ba9a0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba9a0-109">EXAMPLES</span></span>

### <span data-ttu-id="ba9a0-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ba9a0-110">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="ba9a0-111">Usuwa element ASN</span><span class="sxs-lookup"><span data-stu-id="ba9a0-111">Removes the Peer Asn</span></span>

## <span data-ttu-id="ba9a0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba9a0-112">PARAMETERS</span></span>

### <span data-ttu-id="ba9a0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba9a0-113">-AsJob</span></span>
<span data-ttu-id="ba9a0-114">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="ba9a0-114">Run in the background.</span></span>

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

### <span data-ttu-id="ba9a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba9a0-115">-DefaultProfile</span></span>
<span data-ttu-id="ba9a0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba9a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba9a0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ba9a0-117">-Force</span></span>
<span data-ttu-id="ba9a0-118">{{Opis siły wypełniania}}</span><span class="sxs-lookup"><span data-stu-id="ba9a0-118">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="ba9a0-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ba9a0-119">-InputObject</span></span>
<span data-ttu-id="ba9a0-120">Obiekt PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="ba9a0-120">The PeerAsn object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba9a0-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ba9a0-121">-Name</span></span>
<span data-ttu-id="ba9a0-122">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="ba9a0-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba9a0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba9a0-123">-PassThru</span></span>
<span data-ttu-id="ba9a0-124">Zwraca wartość PRAWDA, jeśli została ukończona</span><span class="sxs-lookup"><span data-stu-id="ba9a0-124">Return true if complete</span></span>

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

### <span data-ttu-id="ba9a0-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ba9a0-125">-Confirm</span></span>
<span data-ttu-id="ba9a0-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba9a0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba9a0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba9a0-127">-WhatIf</span></span>
<span data-ttu-id="ba9a0-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba9a0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba9a0-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ba9a0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba9a0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba9a0-130">CommonParameters</span></span>
<span data-ttu-id="ba9a0-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba9a0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba9a0-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba9a0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba9a0-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba9a0-133">INPUTS</span></span>

### <span data-ttu-id="ba9a0-134">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="ba9a0-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="ba9a0-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba9a0-135">OUTPUTS</span></span>

### <span data-ttu-id="ba9a0-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba9a0-136">System.Boolean</span></span>

## <span data-ttu-id="ba9a0-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba9a0-137">NOTES</span></span>

## <span data-ttu-id="ba9a0-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba9a0-138">RELATED LINKS</span></span>
