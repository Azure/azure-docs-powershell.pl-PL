---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
ms.openlocfilehash: 13b5b219ec789ac54332caa366cfb0277f0bfacb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544539"
---
# <span data-ttu-id="eed88-101">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eed88-101">Set-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="eed88-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eed88-102">SYNOPSIS</span></span>
<span data-ttu-id="eed88-103">Umożliwia zaktualizowanie punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="eed88-103">Updates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eed88-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eed88-104">SYNTAX</span></span>

```
Set-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eed88-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eed88-105">DESCRIPTION</span></span>
<span data-ttu-id="eed88-106">Polecenie cmdlet **Set-AzureRmCdnEndpoint** umożliwia zaktualizowanie punktu końcowego sieci dostarczania zawartości Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="eed88-106">The **Set-AzureRmCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="eed88-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eed88-107">EXAMPLES</span></span>

## <span data-ttu-id="eed88-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eed88-108">PARAMETERS</span></span>

### <span data-ttu-id="eed88-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eed88-109">-CdnEndpoint</span></span>
<span data-ttu-id="eed88-110">Określa punkt końcowy, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eed88-110">Specifies the endpoint that this cmdlet updates.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eed88-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed88-111">-DefaultProfile</span></span>
<span data-ttu-id="eed88-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="eed88-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eed88-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eed88-113">-Confirm</span></span>
<span data-ttu-id="eed88-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eed88-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eed88-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eed88-115">-WhatIf</span></span>
<span data-ttu-id="eed88-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eed88-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eed88-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eed88-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eed88-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed88-118">CommonParameters</span></span>
<span data-ttu-id="eed88-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eed88-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed88-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eed88-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed88-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eed88-121">INPUTS</span></span>

### <span data-ttu-id="eed88-122">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="eed88-122">PSEndpoint</span></span>
<span data-ttu-id="eed88-123">Parametr "CdnEndpoint" akceptuje wartość typu "PSEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="eed88-123">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="eed88-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eed88-124">OUTPUTS</span></span>

### <span data-ttu-id="eed88-125">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="eed88-125">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="eed88-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eed88-126">NOTES</span></span>

## <span data-ttu-id="eed88-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eed88-127">RELATED LINKS</span></span>

[<span data-ttu-id="eed88-128">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eed88-128">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="eed88-129">Nowe — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eed88-129">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="eed88-130">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eed88-130">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="eed88-131">Start — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eed88-131">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="eed88-132">Zatrzymaj — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eed88-132">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


