---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: c371749643952e8209b3cbec0721331a4d380d94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011706"
---
# <span data-ttu-id="8e1e7-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="8e1e7-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="8e1e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e1e7-102">SYNOPSIS</span></span>
<span data-ttu-id="8e1e7-103">Pobiera wyniki podo testów w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8e1e7-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="8e1e7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8e1e7-104">SYNTAX</span></span>

### <span data-ttu-id="8e1e7-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8e1e7-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e1e7-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="8e1e7-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e1e7-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="8e1e7-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e1e7-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="8e1e7-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e1e7-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e1e7-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e1e7-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="8e1e7-110">DESCRIPTION</span></span>
<span data-ttu-id="8e1e7-111">Pobiera wyniki podo testów w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8e1e7-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="8e1e7-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8e1e7-112">EXAMPLES</span></span>

### <span data-ttu-id="8e1e7-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8e1e7-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="8e1e7-114">Pobiera wszystkie wyniki podo testów w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8e1e7-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="8e1e7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e1e7-115">PARAMETERS</span></span>

### <span data-ttu-id="8e1e7-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="8e1e7-116">-AssessedResourceId</span></span>
<span data-ttu-id="8e1e7-117">Pełny identyfikator zasobu, na podstawie których jest obliczana ocena.</span><span class="sxs-lookup"><span data-stu-id="8e1e7-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionScope, SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e1e7-118">-AssessmentName</span><span class="sxs-lookup"><span data-stu-id="8e1e7-118">-AssessmentName</span></span>
<span data-ttu-id="8e1e7-119">Nazwa zasobu oceniania.</span><span class="sxs-lookup"><span data-stu-id="8e1e7-119">Name of the assessment resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e1e7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e1e7-120">-DefaultProfile</span></span>
<span data-ttu-id="8e1e7-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e1e7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e1e7-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8e1e7-122">-Name</span></span>
<span data-ttu-id="8e1e7-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="8e1e7-123">Resource name.</span></span>

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
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e1e7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e1e7-124">-ResourceId</span></span>
<span data-ttu-id="8e1e7-125">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="8e1e7-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="8e1e7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e1e7-126">CommonParameters</span></span>
<span data-ttu-id="8e1e7-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e1e7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e1e7-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e1e7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e1e7-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e1e7-129">INPUTS</span></span>

### <span data-ttu-id="8e1e7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8e1e7-130">System.String</span></span>

## <span data-ttu-id="8e1e7-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e1e7-131">OUTPUTS</span></span>

### <span data-ttu-id="8e1e7-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="8e1e7-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="8e1e7-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8e1e7-133">NOTES</span></span>

## <span data-ttu-id="8e1e7-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e1e7-134">RELATED LINKS</span></span>
