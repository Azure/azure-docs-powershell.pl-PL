---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: c84b91e70d428a7ba05aa3766bf1a63840b6ffa4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706535"
---
# <span data-ttu-id="c06b1-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c06b1-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="c06b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c06b1-102">SYNOPSIS</span></span>
<span data-ttu-id="c06b1-103">Umożliwia zaktualizowanie punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="c06b1-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="c06b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c06b1-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c06b1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c06b1-105">DESCRIPTION</span></span>
<span data-ttu-id="c06b1-106">Polecenie cmdlet **Set-AzCdnEndpoint** umożliwia zaktualizowanie punktu końcowego sieci dostarczania zawartości Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="c06b1-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="c06b1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c06b1-107">EXAMPLES</span></span>

## <span data-ttu-id="c06b1-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c06b1-108">PARAMETERS</span></span>

### <span data-ttu-id="c06b1-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c06b1-109">-CdnEndpoint</span></span>
<span data-ttu-id="c06b1-110">Określa punkt końcowy, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c06b1-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="c06b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c06b1-111">-DefaultProfile</span></span>
<span data-ttu-id="c06b1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c06b1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c06b1-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c06b1-113">-Confirm</span></span>
<span data-ttu-id="c06b1-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c06b1-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c06b1-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c06b1-115">-WhatIf</span></span>
<span data-ttu-id="c06b1-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c06b1-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c06b1-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c06b1-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c06b1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c06b1-118">CommonParameters</span></span>
<span data-ttu-id="c06b1-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c06b1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c06b1-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c06b1-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c06b1-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c06b1-121">INPUTS</span></span>

### <span data-ttu-id="c06b1-122">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="c06b1-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="c06b1-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c06b1-123">OUTPUTS</span></span>

### <span data-ttu-id="c06b1-124">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="c06b1-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="c06b1-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c06b1-125">NOTES</span></span>

## <span data-ttu-id="c06b1-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c06b1-126">RELATED LINKS</span></span>

[<span data-ttu-id="c06b1-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c06b1-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="c06b1-128">Nowe — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c06b1-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="c06b1-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c06b1-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="c06b1-130">Start — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c06b1-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="c06b1-131">Zatrzymaj — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c06b1-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


