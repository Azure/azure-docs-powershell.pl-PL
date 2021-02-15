---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: 7222b33470dc1fff22039c5e88bf3c6560b80c31
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239119"
---
# <span data-ttu-id="ceda8-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ceda8-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="ceda8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceda8-102">SYNOPSIS</span></span>
<span data-ttu-id="ceda8-103">Aktualizuje punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="ceda8-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="ceda8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ceda8-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ceda8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ceda8-105">DESCRIPTION</span></span>
<span data-ttu-id="ceda8-106">Polecenie **cmdlet Set-AzCdnEndpoint** aktualizuje punkt końcowy usługi Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="ceda8-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="ceda8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ceda8-107">EXAMPLES</span></span>

## <span data-ttu-id="ceda8-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ceda8-108">PARAMETERS</span></span>

### <span data-ttu-id="ceda8-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ceda8-109">-CdnEndpoint</span></span>
<span data-ttu-id="ceda8-110">Określa punkt końcowy, który będzie aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceda8-110">Specifies the endpoint that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ceda8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceda8-111">-DefaultProfile</span></span>
<span data-ttu-id="ceda8-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ceda8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ceda8-113">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ceda8-113">-Confirm</span></span>
<span data-ttu-id="ceda8-114">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ceda8-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceda8-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceda8-115">-WhatIf</span></span>
<span data-ttu-id="ceda8-116">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceda8-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ceda8-117">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ceda8-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceda8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceda8-118">CommonParameters</span></span>
<span data-ttu-id="ceda8-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceda8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceda8-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ceda8-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceda8-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ceda8-121">INPUTS</span></span>

### <span data-ttu-id="ceda8-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="ceda8-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="ceda8-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ceda8-123">OUTPUTS</span></span>

### <span data-ttu-id="ceda8-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="ceda8-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="ceda8-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ceda8-125">NOTES</span></span>

## <span data-ttu-id="ceda8-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ceda8-126">RELATED LINKS</span></span>

[<span data-ttu-id="ceda8-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ceda8-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="ceda8-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ceda8-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="ceda8-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ceda8-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="ceda8-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ceda8-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="ceda8-131">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ceda8-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


