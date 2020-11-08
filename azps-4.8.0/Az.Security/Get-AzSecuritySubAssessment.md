---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: 10808d7e4f6e270801ef56e48b605f4c23cd6246
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220362"
---
# <span data-ttu-id="8a645-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="8a645-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="8a645-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a645-102">SYNOPSIS</span></span>
<span data-ttu-id="8a645-103">Pobiera wyniki podrzędne w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8a645-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="8a645-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a645-104">SYNTAX</span></span>

### <span data-ttu-id="8a645-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8a645-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a645-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="8a645-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a645-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="8a645-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a645-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="8a645-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a645-109">Zasobów</span><span class="sxs-lookup"><span data-stu-id="8a645-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a645-110">Opis</span><span class="sxs-lookup"><span data-stu-id="8a645-110">DESCRIPTION</span></span>
<span data-ttu-id="8a645-111">Pobiera wyniki podrzędne w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8a645-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="8a645-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a645-112">EXAMPLES</span></span>

### <span data-ttu-id="8a645-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8a645-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="8a645-114">Pobiera wszystkie wyniki podkluczeń w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8a645-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="8a645-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a645-115">PARAMETERS</span></span>

### <span data-ttu-id="8a645-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="8a645-116">-AssessedResourceId</span></span>
<span data-ttu-id="8a645-117">Pełny identyfikator zasobu, dla którego jest obliczana Ocena.</span><span class="sxs-lookup"><span data-stu-id="8a645-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="8a645-118">-Assessmentname</span><span class="sxs-lookup"><span data-stu-id="8a645-118">-AssessmentName</span></span>
<span data-ttu-id="8a645-119">Nazwa zasobu oceny.</span><span class="sxs-lookup"><span data-stu-id="8a645-119">Name of the assessment resource.</span></span>

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

### <span data-ttu-id="8a645-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a645-120">-DefaultProfile</span></span>
<span data-ttu-id="8a645-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a645-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a645-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8a645-122">-Name</span></span>
<span data-ttu-id="8a645-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="8a645-123">Resource name.</span></span>

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

### <span data-ttu-id="8a645-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a645-124">-ResourceId</span></span>
<span data-ttu-id="8a645-125">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="8a645-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="8a645-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a645-126">CommonParameters</span></span>
<span data-ttu-id="8a645-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a645-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a645-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a645-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a645-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a645-129">INPUTS</span></span>

### <span data-ttu-id="8a645-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8a645-130">System.String</span></span>

## <span data-ttu-id="8a645-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a645-131">OUTPUTS</span></span>

### <span data-ttu-id="8a645-132">Microsoft. Azure. Commands. Security. MODELES. suboceny. PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="8a645-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="8a645-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a645-133">NOTES</span></span>

## <span data-ttu-id="8a645-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a645-134">RELATED LINKS</span></span>
