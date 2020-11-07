---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 6d6626164000957ffaa987a71131987f35a977c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872075"
---
# <span data-ttu-id="c5709-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="c5709-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="c5709-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c5709-102">SYNOPSIS</span></span>
<span data-ttu-id="c5709-103">Sprawdza, czy nazwa domeny w strefie cloudapp.azure.com jest dostępna do użycia.</span><span class="sxs-lookup"><span data-stu-id="c5709-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="c5709-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c5709-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5709-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c5709-105">DESCRIPTION</span></span>
<span data-ttu-id="c5709-106">Sprawdza, czy nazwa domeny w strefie cloudapp.azure.com jest dostępna do użycia.</span><span class="sxs-lookup"><span data-stu-id="c5709-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="c5709-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c5709-107">EXAMPLES</span></span>

### <span data-ttu-id="c5709-108">Przykład 1: Sprawdź, czy contoso.cloudapp.azure.com jest dostępny do użycia.</span><span class="sxs-lookup"><span data-stu-id="c5709-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="c5709-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5709-109">PARAMETERS</span></span>

### <span data-ttu-id="c5709-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5709-110">-DefaultProfile</span></span>
<span data-ttu-id="c5709-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c5709-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5709-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="c5709-112">-DomainNameLabel</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainQualifiedName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5709-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c5709-113">-Location</span></span>
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

### <span data-ttu-id="c5709-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5709-114">CommonParameters</span></span>
<span data-ttu-id="c5709-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5709-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5709-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5709-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5709-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5709-117">INPUTS</span></span>

### <span data-ttu-id="c5709-118">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c5709-118">None</span></span>

## <span data-ttu-id="c5709-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c5709-119">OUTPUTS</span></span>

### <span data-ttu-id="c5709-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c5709-120">System.Boolean</span></span>

## <span data-ttu-id="c5709-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c5709-121">NOTES</span></span>

## <span data-ttu-id="c5709-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5709-122">RELATED LINKS</span></span>
