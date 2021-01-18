---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: 09fd2e23cf8c91c2ffea1c10b5363011b9b189a5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504212"
---
# <span data-ttu-id="8aeaa-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="8aeaa-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="8aeaa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8aeaa-102">SYNOPSIS</span></span>
<span data-ttu-id="8aeaa-103">Pobiera stan dostępności punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="8aeaa-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="8aeaa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8aeaa-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8aeaa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8aeaa-105">DESCRIPTION</span></span>
<span data-ttu-id="8aeaa-106">Polecenie cmdlet **Get-AzCdnEndpointNameAvailability** Pobiera stan dostępności punktu końcowego sieci dostarczania zawartości Azure (CDN, Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="8aeaa-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="8aeaa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8aeaa-107">EXAMPLES</span></span>

## <span data-ttu-id="8aeaa-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8aeaa-108">PARAMETERS</span></span>

### <span data-ttu-id="8aeaa-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aeaa-109">-DefaultProfile</span></span>
<span data-ttu-id="8aeaa-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8aeaa-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8aeaa-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="8aeaa-111">-EndpointName</span></span>
<span data-ttu-id="8aeaa-112">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="8aeaa-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="8aeaa-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aeaa-113">CommonParameters</span></span>
<span data-ttu-id="8aeaa-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aeaa-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aeaa-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8aeaa-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aeaa-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8aeaa-116">INPUTS</span></span>

### <span data-ttu-id="8aeaa-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8aeaa-117">None</span></span>

## <span data-ttu-id="8aeaa-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8aeaa-118">OUTPUTS</span></span>

### <span data-ttu-id="8aeaa-119">Microsoft. Azure. Commands. CDN. models. Endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="8aeaa-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="8aeaa-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8aeaa-120">NOTES</span></span>

## <span data-ttu-id="8aeaa-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8aeaa-121">RELATED LINKS</span></span>
