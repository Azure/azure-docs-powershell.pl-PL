---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 2f46b13570ef1f538658dae6d02000848822c150
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953889"
---
# <span data-ttu-id="2effc-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="2effc-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="2effc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2effc-102">SYNOPSIS</span></span>
<span data-ttu-id="2effc-103">Tworzy znacznik IP.</span><span class="sxs-lookup"><span data-stu-id="2effc-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="2effc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2effc-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2effc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2effc-105">DESCRIPTION</span></span>
<span data-ttu-id="2effc-106">Polecenie **cmdlet New-AzPublicIpTag** tworzy tag IP.</span><span class="sxs-lookup"><span data-stu-id="2effc-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="2effc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2effc-107">EXAMPLES</span></span>

### <span data-ttu-id="2effc-108">Przykład 1. Tworzenie nowego tagu IP</span><span class="sxs-lookup"><span data-stu-id="2effc-108">Example 1: Create a new IP Tag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="2effc-109">To polecenie tworzy nowy tag IP z takim tagiem jak "FirstPartyUsage" i tagiem, takim jak "/Sql".</span><span class="sxs-lookup"><span data-stu-id="2effc-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="2effc-110">Jest to używane w przypadku tworzenia publicIpAddress z tymi określonymi tagami do przydzielenia.</span><span class="sxs-lookup"><span data-stu-id="2effc-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="2effc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2effc-111">PARAMETERS</span></span>

### <span data-ttu-id="2effc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2effc-112">-DefaultProfile</span></span>
<span data-ttu-id="2effc-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2effc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2effc-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="2effc-114">-IpTagType</span></span>
<span data-ttu-id="2effc-115">Typ ipTag, przykład:FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="2effc-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2effc-116">— Tag</span><span class="sxs-lookup"><span data-stu-id="2effc-116">-Tag</span></span>
<span data-ttu-id="2effc-117">Wartość ipTag, przykład:/sql</span><span class="sxs-lookup"><span data-stu-id="2effc-117">IpTag value Example:/Sql</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2effc-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2effc-118">-Confirm</span></span>
<span data-ttu-id="2effc-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2effc-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2effc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2effc-120">-WhatIf</span></span>
<span data-ttu-id="2effc-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2effc-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2effc-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2effc-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2effc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2effc-123">CommonParameters</span></span>
<span data-ttu-id="2effc-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2effc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2effc-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2effc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2effc-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2effc-126">INPUTS</span></span>

### <span data-ttu-id="2effc-127">System.String</span><span class="sxs-lookup"><span data-stu-id="2effc-127">System.String</span></span>

## <span data-ttu-id="2effc-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2effc-128">OUTPUTS</span></span>

### <span data-ttu-id="2effc-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="2effc-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="2effc-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2effc-130">NOTES</span></span>

## <span data-ttu-id="2effc-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2effc-131">RELATED LINKS</span></span>
