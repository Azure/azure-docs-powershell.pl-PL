---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: 4270f7c9781ef960cdbb20a8a067a3dc22255723
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996864"
---
# <span data-ttu-id="1f2cb-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f2cb-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="1f2cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f2cb-102">SYNOPSIS</span></span>
<span data-ttu-id="1f2cb-103">Aktualizuje punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="1f2cb-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="1f2cb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1f2cb-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f2cb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1f2cb-105">DESCRIPTION</span></span>
<span data-ttu-id="1f2cb-106">Polecenie **cmdlet Set-AzCdnEndpoint** aktualizuje punkt końcowy usługi Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="1f2cb-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="1f2cb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1f2cb-107">EXAMPLES</span></span>

## <span data-ttu-id="1f2cb-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f2cb-108">PARAMETERS</span></span>

### <span data-ttu-id="1f2cb-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f2cb-109">-CdnEndpoint</span></span>
<span data-ttu-id="1f2cb-110">Określa punkt końcowy, który będzie aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f2cb-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="1f2cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f2cb-111">-DefaultProfile</span></span>
<span data-ttu-id="1f2cb-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1f2cb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f2cb-113">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f2cb-113">-Confirm</span></span>
<span data-ttu-id="1f2cb-114">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1f2cb-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f2cb-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f2cb-115">-WhatIf</span></span>
<span data-ttu-id="1f2cb-116">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f2cb-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f2cb-117">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1f2cb-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f2cb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f2cb-118">CommonParameters</span></span>
<span data-ttu-id="1f2cb-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f2cb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f2cb-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f2cb-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f2cb-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f2cb-121">INPUTS</span></span>

### <span data-ttu-id="1f2cb-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f2cb-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="1f2cb-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f2cb-123">OUTPUTS</span></span>

### <span data-ttu-id="1f2cb-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f2cb-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="1f2cb-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1f2cb-125">NOTES</span></span>

## <span data-ttu-id="1f2cb-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f2cb-126">RELATED LINKS</span></span>

[<span data-ttu-id="1f2cb-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f2cb-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="1f2cb-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f2cb-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="1f2cb-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f2cb-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="1f2cb-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f2cb-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="1f2cb-131">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f2cb-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


