---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySecureScore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
ms.openlocfilehash: 0cce3e4e1aa0f5de93e9c54c00cfa1902a4c24b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995947"
---
# <span data-ttu-id="63b65-101">Get-AzSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="63b65-101">Get-AzSecuritySecureScore</span></span>

## <span data-ttu-id="63b65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63b65-102">SYNOPSIS</span></span>
<span data-ttu-id="63b65-103">Otrzymuje bezpieczne wyniki i wyniki z subskrypcji</span><span class="sxs-lookup"><span data-stu-id="63b65-103">Gets security secure scores and their results on a subscription</span></span>

## <span data-ttu-id="63b65-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="63b65-104">SYNTAX</span></span>

### <span data-ttu-id="63b65-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="63b65-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63b65-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="63b65-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScore -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63b65-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="63b65-107">EXAMPLES</span></span>

### <span data-ttu-id="63b65-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="63b65-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScore
```

<span data-ttu-id="63b65-109">Otrzymuje wszystkie bezpieczne wyniki w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="63b65-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="63b65-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63b65-110">PARAMETERS</span></span>

### <span data-ttu-id="63b65-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63b65-111">-DefaultProfile</span></span>
<span data-ttu-id="63b65-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="63b65-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63b65-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="63b65-113">-Name</span></span>
<span data-ttu-id="63b65-114">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="63b65-114">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63b65-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63b65-115">CommonParameters</span></span>
<span data-ttu-id="63b65-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63b65-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63b65-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63b65-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63b65-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63b65-118">INPUTS</span></span>

### <span data-ttu-id="63b65-119">System.String</span><span class="sxs-lookup"><span data-stu-id="63b65-119">System.String</span></span>

## <span data-ttu-id="63b65-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63b65-120">OUTPUTS</span></span>

### <span data-ttu-id="63b65-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="63b65-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span></span>

## <span data-ttu-id="63b65-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="63b65-122">NOTES</span></span>

## <span data-ttu-id="63b65-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63b65-123">RELATED LINKS</span></span>
