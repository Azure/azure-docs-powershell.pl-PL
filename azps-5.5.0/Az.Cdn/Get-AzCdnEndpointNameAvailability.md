---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: 09fd2e23cf8c91c2ffea1c10b5363011b9b189a5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181867"
---
# <span data-ttu-id="398fc-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="398fc-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="398fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="398fc-102">SYNOPSIS</span></span>
<span data-ttu-id="398fc-103">Pobiera stan dostępności punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="398fc-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="398fc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="398fc-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="398fc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="398fc-105">DESCRIPTION</span></span>
<span data-ttu-id="398fc-106">Polecenie **cmdlet Get-AzCdnEndpointNameAvailability** uzyskuje stan dostępności punktu końcowego azure dostarczania zawartości (CDN, Content Delivery Network) platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="398fc-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="398fc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="398fc-107">EXAMPLES</span></span>

## <span data-ttu-id="398fc-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="398fc-108">PARAMETERS</span></span>

### <span data-ttu-id="398fc-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="398fc-109">-DefaultProfile</span></span>
<span data-ttu-id="398fc-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="398fc-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="398fc-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="398fc-111">-EndpointName</span></span>
<span data-ttu-id="398fc-112">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="398fc-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="398fc-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="398fc-113">CommonParameters</span></span>
<span data-ttu-id="398fc-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="398fc-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="398fc-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="398fc-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="398fc-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="398fc-116">INPUTS</span></span>

### <span data-ttu-id="398fc-117">Brak</span><span class="sxs-lookup"><span data-stu-id="398fc-117">None</span></span>

## <span data-ttu-id="398fc-118">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="398fc-118">OUTPUTS</span></span>

### <span data-ttu-id="398fc-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="398fc-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="398fc-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="398fc-120">NOTES</span></span>

## <span data-ttu-id="398fc-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="398fc-121">RELATED LINKS</span></span>
