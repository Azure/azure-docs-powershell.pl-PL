---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
ms.openlocfilehash: 70a6e57b45e1703b06343cb66d5b83b526b55063
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547023"
---
# <span data-ttu-id="953c2-101">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="953c2-101">Set-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="953c2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="953c2-102">SYNOPSIS</span></span>
<span data-ttu-id="953c2-103">Umożliwia zaktualizowanie punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="953c2-103">Updates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="953c2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="953c2-104">SYNTAX</span></span>

```
Set-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="953c2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="953c2-105">DESCRIPTION</span></span>
<span data-ttu-id="953c2-106">Polecenie cmdlet **Set-AzureRmCdnEndpoint** umożliwia zaktualizowanie punktu końcowego sieci dostarczania zawartości Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="953c2-106">The **Set-AzureRmCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="953c2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="953c2-107">EXAMPLES</span></span>

## <span data-ttu-id="953c2-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="953c2-108">PARAMETERS</span></span>

### <span data-ttu-id="953c2-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="953c2-109">-CdnEndpoint</span></span>
<span data-ttu-id="953c2-110">Określa punkt końcowy, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="953c2-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="953c2-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="953c2-111">-Confirm</span></span>
<span data-ttu-id="953c2-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="953c2-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="953c2-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="953c2-113">-WhatIf</span></span>
<span data-ttu-id="953c2-114">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="953c2-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="953c2-115">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="953c2-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="953c2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="953c2-116">-DefaultProfile</span></span>
<span data-ttu-id="953c2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="953c2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="953c2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="953c2-118">CommonParameters</span></span>
<span data-ttu-id="953c2-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="953c2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="953c2-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="953c2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="953c2-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="953c2-121">INPUTS</span></span>

### <span data-ttu-id="953c2-122">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="953c2-122">PSEndpoint</span></span>
<span data-ttu-id="953c2-123">Parametr "CdnEndpoint" akceptuje wartość typu "PSEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="953c2-123">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="953c2-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="953c2-124">OUTPUTS</span></span>

### <span data-ttu-id="953c2-125">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="953c2-125">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="953c2-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="953c2-126">NOTES</span></span>

## <span data-ttu-id="953c2-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="953c2-127">RELATED LINKS</span></span>

[<span data-ttu-id="953c2-128">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="953c2-128">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="953c2-129">Nowe — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="953c2-129">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="953c2-130">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="953c2-130">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="953c2-131">Start — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="953c2-131">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="953c2-132">Zatrzymaj — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="953c2-132">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


