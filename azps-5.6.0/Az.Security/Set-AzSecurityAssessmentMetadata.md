---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: e72766e754394bb43775f73072941dc0d3989c3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986546"
---
# <span data-ttu-id="bdeb4-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="bdeb4-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="bdeb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdeb4-102">SYNOPSIS</span></span>
<span data-ttu-id="bdeb4-103">Tworzy lub aktualizuje typ oceny zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="bdeb4-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="bdeb4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bdeb4-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdeb4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bdeb4-105">DESCRIPTION</span></span>
<span data-ttu-id="bdeb4-106">Tworzy lub aktualizuje metadane oceny zabezpieczeń, za pomocą których można tworzyć różne właściwości oceny i zarządzać nimi.</span><span class="sxs-lookup"><span data-stu-id="bdeb4-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="bdeb4-107">Po tej akcji będzie można raportować wyniki testów dla dowolnego zasobu w tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bdeb4-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="bdeb4-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bdeb4-108">EXAMPLES</span></span>

### <span data-ttu-id="bdeb4-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bdeb4-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="bdeb4-110">Utwórz nowy typ oceny w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bdeb4-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="bdeb4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdeb4-111">PARAMETERS</span></span>

### <span data-ttu-id="bdeb4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdeb4-112">-DefaultProfile</span></span>
<span data-ttu-id="bdeb4-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bdeb4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdeb4-114">— Opis</span><span class="sxs-lookup"><span data-stu-id="bdeb4-114">-Description</span></span>
<span data-ttu-id="bdeb4-115">Szczegółowy ciąg, który pomoże użytkownikom zrozumieć znaczenie tej oceny i sposób jej obliczenia.</span><span class="sxs-lookup"><span data-stu-id="bdeb4-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdeb4-116">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="bdeb4-116">-DisplayName</span></span>
<span data-ttu-id="bdeb4-117">Czytelny dla człowieka tytuł tego obiektu.</span><span class="sxs-lookup"><span data-stu-id="bdeb4-117">Human readable title for this object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdeb4-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bdeb4-118">-Name</span></span>
<span data-ttu-id="bdeb4-119">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="bdeb4-119">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdeb4-120">- RemediationDescription</span><span class="sxs-lookup"><span data-stu-id="bdeb4-120">-RemediationDescription</span></span>
<span data-ttu-id="bdeb4-121">Szczegółowy ciąg, który pomoże użytkownikom zrozumieć różne sposoby ograniczenia lub rozwiązania problemu z zabezpieczeniami.</span><span class="sxs-lookup"><span data-stu-id="bdeb4-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdeb4-122">— Ważność</span><span class="sxs-lookup"><span data-stu-id="bdeb4-122">-Severity</span></span>
<span data-ttu-id="bdeb4-123">Wskazuje ważność ryzyka związanego z zabezpieczeniami, jeśli ocena jest zła.</span><span class="sxs-lookup"><span data-stu-id="bdeb4-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdeb4-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bdeb4-124">-Confirm</span></span>
<span data-ttu-id="bdeb4-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bdeb4-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdeb4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdeb4-126">-WhatIf</span></span>
<span data-ttu-id="bdeb4-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdeb4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdeb4-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bdeb4-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdeb4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdeb4-129">CommonParameters</span></span>
<span data-ttu-id="bdeb4-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdeb4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdeb4-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bdeb4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdeb4-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdeb4-132">INPUTS</span></span>

### <span data-ttu-id="bdeb4-133">Brak</span><span class="sxs-lookup"><span data-stu-id="bdeb4-133">None</span></span>

## <span data-ttu-id="bdeb4-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdeb4-134">OUTPUTS</span></span>

### <span data-ttu-id="bdeb4-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="bdeb4-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="bdeb4-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bdeb4-136">NOTES</span></span>

## <span data-ttu-id="bdeb4-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdeb4-137">RELATED LINKS</span></span>
