---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: 42e7b805e772e42ed395f8893b1140faaab715ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993917"
---
# <span data-ttu-id="ad7d3-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ad7d3-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="ad7d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad7d3-102">SYNOPSIS</span></span>
<span data-ttu-id="ad7d3-103">Pobiera tablicę prywatnego identyfikatora usługi linku, który można połączyć z prywatnym punktem końcowy za pomocą automatycznego zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="ad7d3-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="ad7d3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ad7d3-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad7d3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ad7d3-105">DESCRIPTION</span></span>
<span data-ttu-id="ad7d3-106">Usługa **Get-AzAutoApprowedPrivateLinkService** pobiera tablicę prywatnego identyfikatora usługi linku, który można połączyć z prywatnym punktem końcowy za pomocą auto zatwierdzonego.</span><span class="sxs-lookup"><span data-stu-id="ad7d3-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="ad7d3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ad7d3-107">EXAMPLES</span></span>

### <span data-ttu-id="ad7d3-108">Przykład</span><span class="sxs-lookup"><span data-stu-id="ad7d3-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="ad7d3-109">W tym przykładzie zwracana jest tablica prywatnego identyfikatora usługi linku, która może zostać połączona z prywatnym punktem końcowy za pomocą automatycznego zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="ad7d3-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="ad7d3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad7d3-110">PARAMETERS</span></span>

### <span data-ttu-id="ad7d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad7d3-111">-DefaultProfile</span></span>
<span data-ttu-id="ad7d3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad7d3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad7d3-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ad7d3-113">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad7d3-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad7d3-114">-ResourceGroupName</span></span>
<span data-ttu-id="ad7d3-115">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad7d3-115">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad7d3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad7d3-116">CommonParameters</span></span>
<span data-ttu-id="ad7d3-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad7d3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad7d3-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad7d3-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad7d3-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad7d3-119">INPUTS</span></span>

### <span data-ttu-id="ad7d3-120">Brak</span><span class="sxs-lookup"><span data-stu-id="ad7d3-120">None</span></span>

## <span data-ttu-id="ad7d3-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad7d3-121">OUTPUTS</span></span>

### <span data-ttu-id="ad7d3-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprowedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ad7d3-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="ad7d3-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ad7d3-123">NOTES</span></span>

## <span data-ttu-id="ad7d3-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad7d3-124">RELATED LINKS</span></span>
