---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: daea57cb0e8c910fca4fedabad0e4583354c4072
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971450"
---
# <span data-ttu-id="41005-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="41005-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="41005-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41005-102">SYNOPSIS</span></span>
<span data-ttu-id="41005-103">Pobiera stan dostępności punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="41005-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="41005-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="41005-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41005-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="41005-105">DESCRIPTION</span></span>
<span data-ttu-id="41005-106">Polecenie **cmdlet Get-AzCdnEndpointNameAvailability** pobiera stan dostępności punktu końcowego usługi Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="41005-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="41005-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="41005-107">EXAMPLES</span></span>

## <span data-ttu-id="41005-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41005-108">PARAMETERS</span></span>

### <span data-ttu-id="41005-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41005-109">-DefaultProfile</span></span>
<span data-ttu-id="41005-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="41005-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41005-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="41005-111">-EndpointName</span></span>
<span data-ttu-id="41005-112">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="41005-112">Specifies the name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41005-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41005-113">CommonParameters</span></span>
<span data-ttu-id="41005-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41005-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41005-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41005-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41005-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41005-116">INPUTS</span></span>

### <span data-ttu-id="41005-117">Brak</span><span class="sxs-lookup"><span data-stu-id="41005-117">None</span></span>

## <span data-ttu-id="41005-118">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41005-118">OUTPUTS</span></span>

### <span data-ttu-id="41005-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="41005-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="41005-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="41005-120">NOTES</span></span>

## <span data-ttu-id="41005-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41005-121">RELATED LINKS</span></span>
