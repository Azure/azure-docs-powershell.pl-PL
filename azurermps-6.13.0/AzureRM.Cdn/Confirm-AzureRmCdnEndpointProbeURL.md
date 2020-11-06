---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/confirm-azurermcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Confirm-AzureRmCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Confirm-AzureRmCdnEndpointProbeURL.md
ms.openlocfilehash: d6cf25c352c89592112aaa0a60cf7ba14ff7acf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547548"
---
# <span data-ttu-id="7212d-101">Confirm-AzureRmCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="7212d-101">Confirm-AzureRmCdnEndpointProbeURL</span></span>

## <span data-ttu-id="7212d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7212d-102">SYNOPSIS</span></span>
<span data-ttu-id="7212d-103">Sprawdza poprawność adresu URL badania.</span><span class="sxs-lookup"><span data-stu-id="7212d-103">Validates a probe URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7212d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7212d-104">SYNTAX</span></span>

```
Confirm-AzureRmCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7212d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7212d-105">DESCRIPTION</span></span>
<span data-ttu-id="7212d-106">Polecenie cmdlet **Confirm-AzureRmCdnEndpointProbeURL** potwierdza, że podany adres URL próbnika może być używany do przyspieszania witryn dynamicznych.</span><span class="sxs-lookup"><span data-stu-id="7212d-106">The **Confirm-AzureRmCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="7212d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7212d-107">EXAMPLES</span></span>

### <span data-ttu-id="7212d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7212d-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzureRmCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="7212d-109">Sprawdza poprawność adresu URL badania " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="7212d-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="7212d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7212d-110">PARAMETERS</span></span>

### <span data-ttu-id="7212d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7212d-111">-DefaultProfile</span></span>
<span data-ttu-id="7212d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7212d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7212d-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="7212d-113">-ProbeUrl</span></span>
<span data-ttu-id="7212d-114">Proponowana nazwa adresu URL sondy do sprawdzenia poprawności.</span><span class="sxs-lookup"><span data-stu-id="7212d-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="7212d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7212d-115">CommonParameters</span></span>
<span data-ttu-id="7212d-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7212d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7212d-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7212d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7212d-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7212d-118">INPUTS</span></span>

### <span data-ttu-id="7212d-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7212d-119">None</span></span>

## <span data-ttu-id="7212d-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7212d-120">OUTPUTS</span></span>

### <span data-ttu-id="7212d-121">Microsoft. Azure. Commands. CDN. models. Endpoint. PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="7212d-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="7212d-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7212d-122">NOTES</span></span>

## <span data-ttu-id="7212d-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7212d-123">RELATED LINKS</span></span>
