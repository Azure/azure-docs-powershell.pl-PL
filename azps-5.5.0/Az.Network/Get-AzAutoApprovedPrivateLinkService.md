---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: b03aad1f76c5151746d50e69bc48ccf10e60842f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189818"
---
# <span data-ttu-id="b83e4-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b83e4-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="b83e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b83e4-102">SYNOPSIS</span></span>
<span data-ttu-id="b83e4-103">Pobiera tablicę prywatnego identyfikatora usługi linku, który można połączyć z prywatnym punktem końcowy za pomocą automatycznego zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="b83e4-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="b83e4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b83e4-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b83e4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b83e4-105">DESCRIPTION</span></span>
<span data-ttu-id="b83e4-106">**Get-AzAutoApprowedPrivateLinkService** pobiera tablicę prywatnego identyfikatora usługi linku, który można połączyć z prywatnym punktem końcowy za pomocą auto zatwierdzonego.</span><span class="sxs-lookup"><span data-stu-id="b83e4-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="b83e4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b83e4-107">EXAMPLES</span></span>

### <span data-ttu-id="b83e4-108">Przykład</span><span class="sxs-lookup"><span data-stu-id="b83e4-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="b83e4-109">W tym przykładzie zwracana jest tablica prywatnego identyfikatora usługi linku, która może zostać połączona z prywatnym punktem końcowy za pomocą automatycznego zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="b83e4-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="b83e4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b83e4-110">PARAMETERS</span></span>

### <span data-ttu-id="b83e4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b83e4-111">-DefaultProfile</span></span>
<span data-ttu-id="b83e4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b83e4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b83e4-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b83e4-113">-Location</span></span>
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

### <span data-ttu-id="b83e4-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b83e4-114">-ResourceGroupName</span></span>
<span data-ttu-id="b83e4-115">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b83e4-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b83e4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b83e4-116">CommonParameters</span></span>
<span data-ttu-id="b83e4-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b83e4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b83e4-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b83e4-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b83e4-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b83e4-119">INPUTS</span></span>

### <span data-ttu-id="b83e4-120">Brak</span><span class="sxs-lookup"><span data-stu-id="b83e4-120">None</span></span>

## <span data-ttu-id="b83e4-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b83e4-121">OUTPUTS</span></span>

### <span data-ttu-id="b83e4-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprowedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b83e4-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="b83e4-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b83e4-123">NOTES</span></span>

## <span data-ttu-id="b83e4-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b83e4-124">RELATED LINKS</span></span>
