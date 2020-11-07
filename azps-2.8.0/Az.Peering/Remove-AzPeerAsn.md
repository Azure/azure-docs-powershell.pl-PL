---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: 82a112363a561e7566b0d748d00acc75dc026ebb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872359"
---
# <span data-ttu-id="196bd-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="196bd-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="196bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="196bd-102">SYNOPSIS</span></span>
<span data-ttu-id="196bd-103">Usuń element ASN</span><span class="sxs-lookup"><span data-stu-id="196bd-103">Remove Peer Asn</span></span>

## <span data-ttu-id="196bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="196bd-104">SYNTAX</span></span>

### <span data-ttu-id="196bd-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="196bd-105">Default (Default)</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="196bd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="196bd-106">ByName</span></span>
```
Remove-AzPeerAsn [-Name] <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="196bd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="196bd-107">DESCRIPTION</span></span>
<span data-ttu-id="196bd-108">Usuń PeerAsn z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="196bd-108">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="196bd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="196bd-109">EXAMPLES</span></span>

### <span data-ttu-id="196bd-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="196bd-110">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="196bd-111">Usuwa element ASN</span><span class="sxs-lookup"><span data-stu-id="196bd-111">Removes the Peer Asn</span></span>

## <span data-ttu-id="196bd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="196bd-112">PARAMETERS</span></span>

### <span data-ttu-id="196bd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="196bd-113">-AsJob</span></span>
<span data-ttu-id="196bd-114">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="196bd-114">Run in the background.</span></span>

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

### <span data-ttu-id="196bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="196bd-115">-DefaultProfile</span></span>
<span data-ttu-id="196bd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="196bd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="196bd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="196bd-117">-Force</span></span>
<span data-ttu-id="196bd-118">{{Opis siły wypełniania}}</span><span class="sxs-lookup"><span data-stu-id="196bd-118">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="196bd-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="196bd-119">-InputObject</span></span>
<span data-ttu-id="196bd-120">Obiekt PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="196bd-120">The PeerAsn object.</span></span>

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

### <span data-ttu-id="196bd-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="196bd-121">-Name</span></span>
<span data-ttu-id="196bd-122">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="196bd-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="196bd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="196bd-123">-PassThru</span></span>
<span data-ttu-id="196bd-124">Zwraca wartość PRAWDA, jeśli została ukończona</span><span class="sxs-lookup"><span data-stu-id="196bd-124">Return true if complete</span></span>

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

### <span data-ttu-id="196bd-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="196bd-125">-Confirm</span></span>
<span data-ttu-id="196bd-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="196bd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="196bd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="196bd-127">-WhatIf</span></span>
<span data-ttu-id="196bd-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="196bd-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="196bd-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="196bd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="196bd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="196bd-130">CommonParameters</span></span>
<span data-ttu-id="196bd-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="196bd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="196bd-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="196bd-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="196bd-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="196bd-133">INPUTS</span></span>

### <span data-ttu-id="196bd-134">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="196bd-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="196bd-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="196bd-135">OUTPUTS</span></span>

### <span data-ttu-id="196bd-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="196bd-136">System.Boolean</span></span>

## <span data-ttu-id="196bd-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="196bd-137">NOTES</span></span>

## <span data-ttu-id="196bd-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="196bd-138">RELATED LINKS</span></span>
