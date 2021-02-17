---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 2ee468c47f22e90ce47b003dcae1becfb905134e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202382"
---
# <span data-ttu-id="51811-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="51811-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="51811-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51811-102">SYNOPSIS</span></span>
<span data-ttu-id="51811-103">Sprawdza, czy nazwa domeny w strefie cloudapp.azure.com jest dostępna do użycia.</span><span class="sxs-lookup"><span data-stu-id="51811-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="51811-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="51811-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="51811-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="51811-105">DESCRIPTION</span></span>
<span data-ttu-id="51811-106">Sprawdza, czy nazwa domeny w strefie cloudapp.azure.com jest dostępna do użycia.</span><span class="sxs-lookup"><span data-stu-id="51811-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="51811-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="51811-107">EXAMPLES</span></span>

### <span data-ttu-id="51811-108">Przykład 1. Sprawdź, czy contoso.westus.cloudapp.azure.com jest dostępna do użycia.</span><span class="sxs-lookup"><span data-stu-id="51811-108">Example 1: Check if contoso.westus.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="51811-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51811-109">PARAMETERS</span></span>

### <span data-ttu-id="51811-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51811-110">-DefaultProfile</span></span>
<span data-ttu-id="51811-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="51811-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51811-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="51811-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="51811-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="51811-113">-Location</span></span>
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

### <span data-ttu-id="51811-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51811-114">CommonParameters</span></span>
<span data-ttu-id="51811-115">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51811-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51811-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51811-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51811-117">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51811-117">INPUTS</span></span>

### <span data-ttu-id="51811-118">Brak</span><span class="sxs-lookup"><span data-stu-id="51811-118">None</span></span>

## <span data-ttu-id="51811-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="51811-119">OUTPUTS</span></span>

### <span data-ttu-id="51811-120">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="51811-120">System.Boolean</span></span>

## <span data-ttu-id="51811-121">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="51811-121">NOTES</span></span>

## <span data-ttu-id="51811-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51811-122">RELATED LINKS</span></span>
