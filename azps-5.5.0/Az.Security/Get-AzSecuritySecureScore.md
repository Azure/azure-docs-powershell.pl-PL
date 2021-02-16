---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
ms.openlocfilehash: 5b14298f48c5723b4d84b0f22d799ac0a21699e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189171"
---
# <span data-ttu-id="23cd3-101">Get-AzSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="23cd3-101">Get-AzSecuritySecureScore</span></span>

## <span data-ttu-id="23cd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="23cd3-103">Otrzymuje bezpieczne wyniki i wyniki z subskrypcji</span><span class="sxs-lookup"><span data-stu-id="23cd3-103">Gets security secure scores and their results on a subscription</span></span>

## <span data-ttu-id="23cd3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="23cd3-104">SYNTAX</span></span>

### <span data-ttu-id="23cd3-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="23cd3-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23cd3-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="23cd3-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScore -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23cd3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="23cd3-107">EXAMPLES</span></span>

### <span data-ttu-id="23cd3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23cd3-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScore
```

<span data-ttu-id="23cd3-109">Otrzymuje wszystkie bezpieczne wyniki w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="23cd3-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="23cd3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23cd3-110">PARAMETERS</span></span>

### <span data-ttu-id="23cd3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23cd3-111">-DefaultProfile</span></span>
<span data-ttu-id="23cd3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="23cd3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23cd3-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="23cd3-113">-Name</span></span>
<span data-ttu-id="23cd3-114">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="23cd3-114">Resource name.</span></span>

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

### <span data-ttu-id="23cd3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23cd3-115">CommonParameters</span></span>
<span data-ttu-id="23cd3-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23cd3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23cd3-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23cd3-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23cd3-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23cd3-118">INPUTS</span></span>

### <span data-ttu-id="23cd3-119">System.String</span><span class="sxs-lookup"><span data-stu-id="23cd3-119">System.String</span></span>

## <span data-ttu-id="23cd3-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23cd3-120">OUTPUTS</span></span>

### <span data-ttu-id="23cd3-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="23cd3-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span></span>

## <span data-ttu-id="23cd3-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="23cd3-122">NOTES</span></span>

## <span data-ttu-id="23cd3-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23cd3-123">RELATED LINKS</span></span>
