---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 524a10f910b6e0d1b247f74a0b99063cbecba65c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242402"
---
# <span data-ttu-id="dffde-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="dffde-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="dffde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dffde-102">SYNOPSIS</span></span>
<span data-ttu-id="dffde-103">Pobiera oceny zabezpieczeń i ich wyniki w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="dffde-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="dffde-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dffde-104">SYNTAX</span></span>

### <span data-ttu-id="dffde-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="dffde-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dffde-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="dffde-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dffde-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="dffde-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dffde-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="dffde-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dffde-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="dffde-109">DESCRIPTION</span></span>
<span data-ttu-id="dffde-110">Pobiera ocenę zabezpieczeń i ich wyniki w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dffde-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="dffde-111">Ocena zabezpieczeń pozwoli Ci dowiedzieć się, które najlepsze rozwiązania są rekompresowane przez Centrum zabezpieczeń Azure w celu ograniczenia subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dffde-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="dffde-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dffde-112">EXAMPLES</span></span>

### <span data-ttu-id="dffde-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dffde-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="dffde-114">Pobiera całą ocenę zabezpieczeń w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="dffde-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="dffde-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dffde-115">PARAMETERS</span></span>

### <span data-ttu-id="dffde-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="dffde-116">-AssessedResourceId</span></span>
<span data-ttu-id="dffde-117">Pełny identyfikator zasobu, na podstawie których jest obliczana ocena.</span><span class="sxs-lookup"><span data-stu-id="dffde-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dffde-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dffde-118">-DefaultProfile</span></span>
<span data-ttu-id="dffde-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dffde-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dffde-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dffde-120">-Name</span></span>
<span data-ttu-id="dffde-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="dffde-121">Resource name.</span></span>

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

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dffde-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dffde-122">-ResourceId</span></span>
<span data-ttu-id="dffde-123">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="dffde-123">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dffde-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dffde-124">CommonParameters</span></span>
<span data-ttu-id="dffde-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dffde-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dffde-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dffde-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dffde-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dffde-127">INPUTS</span></span>

### <span data-ttu-id="dffde-128">System.String</span><span class="sxs-lookup"><span data-stu-id="dffde-128">System.String</span></span>

## <span data-ttu-id="dffde-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dffde-129">OUTPUTS</span></span>

### <span data-ttu-id="dffde-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="dffde-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="dffde-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dffde-131">NOTES</span></span>

## <span data-ttu-id="dffde-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dffde-132">RELATED LINKS</span></span>
