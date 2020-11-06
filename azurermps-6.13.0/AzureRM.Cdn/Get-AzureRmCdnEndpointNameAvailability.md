---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
ms.openlocfilehash: c5db5d27edb537602638ff5654a6da3ac35813ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549411"
---
# <span data-ttu-id="41bdf-101">Get-AzureRmCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="41bdf-101">Get-AzureRmCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="41bdf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="41bdf-103">Pobiera stan dostępności punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="41bdf-103">Gets availability status of the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41bdf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41bdf-104">SYNTAX</span></span>

```
Get-AzureRmCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41bdf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="41bdf-105">DESCRIPTION</span></span>
<span data-ttu-id="41bdf-106">Polecenie cmdlet **Get-AzureRmCdnEndpointNameAvailability** Pobiera stan dostępności punktu końcowego sieci dostarczania zawartości Azure (CDN, Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="41bdf-106">The **Get-AzureRmCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="41bdf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41bdf-107">EXAMPLES</span></span>

## <span data-ttu-id="41bdf-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41bdf-108">PARAMETERS</span></span>

### <span data-ttu-id="41bdf-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41bdf-109">-DefaultProfile</span></span>
<span data-ttu-id="41bdf-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="41bdf-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41bdf-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="41bdf-111">-EndpointName</span></span>
<span data-ttu-id="41bdf-112">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="41bdf-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="41bdf-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41bdf-113">CommonParameters</span></span>
<span data-ttu-id="41bdf-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41bdf-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41bdf-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41bdf-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41bdf-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41bdf-116">INPUTS</span></span>

### <span data-ttu-id="41bdf-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="41bdf-117">None</span></span>

## <span data-ttu-id="41bdf-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41bdf-118">OUTPUTS</span></span>

### <span data-ttu-id="41bdf-119">Microsoft. Azure. Commands. CDN. models. Endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="41bdf-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="41bdf-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41bdf-120">NOTES</span></span>

## <span data-ttu-id="41bdf-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41bdf-121">RELATED LINKS</span></span>
