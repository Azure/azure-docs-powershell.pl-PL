---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: dcd45719754cc8bbb3ef45d8aa9927ae30156937
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181883"
---
# <span data-ttu-id="46b07-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="46b07-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="46b07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46b07-102">SYNOPSIS</span></span>
<span data-ttu-id="46b07-103">Sprawdza poprawność adresu URL adresu URL.</span><span class="sxs-lookup"><span data-stu-id="46b07-103">Validates a probe URL.</span></span>

## <span data-ttu-id="46b07-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="46b07-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46b07-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="46b07-105">DESCRIPTION</span></span>
<span data-ttu-id="46b07-106">Polecenie cmdlet **Confirm-AzCdnEndpointProbeURL** potwierdza, czy podany adres URL może być używany do dynamicznego przyspieszenia witryny.</span><span class="sxs-lookup"><span data-stu-id="46b07-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="46b07-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="46b07-107">EXAMPLES</span></span>

### <span data-ttu-id="46b07-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="46b07-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="46b07-109">Sprawdza poprawność adresu URL" http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="46b07-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="46b07-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46b07-110">PARAMETERS</span></span>

### <span data-ttu-id="46b07-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b07-111">-DefaultProfile</span></span>
<span data-ttu-id="46b07-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="46b07-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46b07-113">- Nawiązka</span><span class="sxs-lookup"><span data-stu-id="46b07-113">-ProbeUrl</span></span>
<span data-ttu-id="46b07-114">Proponowana nazwa adresu URL do weryfikacji.</span><span class="sxs-lookup"><span data-stu-id="46b07-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="46b07-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b07-115">CommonParameters</span></span>
<span data-ttu-id="46b07-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46b07-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46b07-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46b07-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b07-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46b07-118">INPUTS</span></span>

### <span data-ttu-id="46b07-119">Brak</span><span class="sxs-lookup"><span data-stu-id="46b07-119">None</span></span>

## <span data-ttu-id="46b07-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46b07-120">OUTPUTS</span></span>

### <span data-ttu-id="46b07-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="46b07-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="46b07-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="46b07-122">NOTES</span></span>

## <span data-ttu-id="46b07-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46b07-123">RELATED LINKS</span></span>
