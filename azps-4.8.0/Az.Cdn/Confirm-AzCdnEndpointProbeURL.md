---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: dcd45719754cc8bbb3ef45d8aa9927ae30156937
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062939"
---
# <span data-ttu-id="5c249-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="5c249-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="5c249-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c249-102">SYNOPSIS</span></span>
<span data-ttu-id="5c249-103">Sprawdza poprawność adresu URL badania.</span><span class="sxs-lookup"><span data-stu-id="5c249-103">Validates a probe URL.</span></span>

## <span data-ttu-id="5c249-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c249-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c249-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5c249-105">DESCRIPTION</span></span>
<span data-ttu-id="5c249-106">Polecenie cmdlet **Confirm-AzCdnEndpointProbeURL** potwierdza, że podany adres URL próbnika może być używany do przyspieszania witryn dynamicznych.</span><span class="sxs-lookup"><span data-stu-id="5c249-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="5c249-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c249-107">EXAMPLES</span></span>

### <span data-ttu-id="5c249-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5c249-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="5c249-109">Sprawdza poprawność adresu URL badania " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="5c249-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="5c249-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c249-110">PARAMETERS</span></span>

### <span data-ttu-id="5c249-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c249-111">-DefaultProfile</span></span>
<span data-ttu-id="5c249-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5c249-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c249-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="5c249-113">-ProbeUrl</span></span>
<span data-ttu-id="5c249-114">Proponowana nazwa adresu URL sondy do sprawdzenia poprawności.</span><span class="sxs-lookup"><span data-stu-id="5c249-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="5c249-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c249-115">CommonParameters</span></span>
<span data-ttu-id="5c249-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c249-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c249-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c249-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c249-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c249-118">INPUTS</span></span>

### <span data-ttu-id="5c249-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5c249-119">None</span></span>

## <span data-ttu-id="5c249-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c249-120">OUTPUTS</span></span>

### <span data-ttu-id="5c249-121">Microsoft. Azure. Commands. CDN. models. Endpoint. PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="5c249-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="5c249-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c249-122">NOTES</span></span>

## <span data-ttu-id="5c249-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c249-123">RELATED LINKS</span></span>
