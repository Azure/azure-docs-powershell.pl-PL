---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
ms.openlocfilehash: 9a227c742892d94417d42be7137f903e17b8b928
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242298"
---
# <span data-ttu-id="2eee6-101">Set-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="2eee6-101">Set-AzSecurityAssessment</span></span>

## <span data-ttu-id="2eee6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eee6-102">SYNOPSIS</span></span>
<span data-ttu-id="2eee6-103">Tworzenie lub aktualizowanie wyniku oceny zabezpieczeń dla zasobu</span><span class="sxs-lookup"><span data-stu-id="2eee6-103">Create or update a security assessment result on a resource</span></span>

## <span data-ttu-id="2eee6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2eee6-104">SYNTAX</span></span>

### <span data-ttu-id="2eee6-105">SubscriptionLevelResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="2eee6-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAssessment -Name <String> [-StatusCode <String>] [-StatusCause <String>]
 [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eee6-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="2eee6-106">ResourceIdLevelResource</span></span>
```
Set-AzSecurityAssessment -Name <String> -AssessedResourceId <String> -StatusCode <String>
 [-StatusCause <String>] [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eee6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="2eee6-107">DESCRIPTION</span></span>
<span data-ttu-id="2eee6-108">Utwórz lub zaktualizuj wynik oceny zabezpieczeń dla zasobu. Za jego pomocą można zmienić stan istniejącego wyniku lub dodać dodatkowe dane.</span><span class="sxs-lookup"><span data-stu-id="2eee6-108">Create or update a security assessment result on a resource, can be used to change the status of an existing result or add additional data.</span></span>
<span data-ttu-id="2eee6-109">mogą być używane tylko w przypadku typów ocen "CustomerManaged" i tylko po utworzeniu dopasowanej metadanych oceny.</span><span class="sxs-lookup"><span data-stu-id="2eee6-109">can only be used for "CustomerManaged" assessment types and only after the matched assessment metadata is created.</span></span>

## <span data-ttu-id="2eee6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2eee6-110">EXAMPLES</span></span>

### <span data-ttu-id="2eee6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2eee6-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D -StatusCode "Unhealthy"
```

<span data-ttu-id="2eee6-112">Oznacza wynik subskrypcji jako "Zła kondycja" dla oceny typu "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" — więcej szczegółowych informacji o typie oceny można znaleźć w ramach typu danych oceny</span><span class="sxs-lookup"><span data-stu-id="2eee6-112">Marks the subscription result as "Unhealthy" for assessment of type "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" - more details about the assessment type will be found under the assessmentMetadata type</span></span>

## <span data-ttu-id="2eee6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2eee6-113">PARAMETERS</span></span>

### <span data-ttu-id="2eee6-114">-AdditionalData</span><span class="sxs-lookup"><span data-stu-id="2eee6-114">-AdditionalData</span></span>
<span data-ttu-id="2eee6-115">Dane dołączone do wyniku oceny w celu lepszego badania lub przejrzystości stanu.</span><span class="sxs-lookup"><span data-stu-id="2eee6-115">Data that is attached to the assessment result for better investigations or status clarity.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eee6-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="2eee6-116">-AssessedResourceId</span></span>
<span data-ttu-id="2eee6-117">Pełny identyfikator zasobu, na podstawie których jest obliczana ocena.</span><span class="sxs-lookup"><span data-stu-id="2eee6-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="2eee6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eee6-118">-DefaultProfile</span></span>
<span data-ttu-id="2eee6-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2eee6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eee6-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2eee6-120">-Name</span></span>
<span data-ttu-id="2eee6-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="2eee6-121">Resource name.</span></span>

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

### <span data-ttu-id="2eee6-122">- StatusCause</span><span class="sxs-lookup"><span data-stu-id="2eee6-122">-StatusCause</span></span>
<span data-ttu-id="2eee6-123">Kod progrematyczny przyczyny wyniku oceny.</span><span class="sxs-lookup"><span data-stu-id="2eee6-123">Progremmatic code for the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="2eee6-124">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="2eee6-124">-StatusCode</span></span>
<span data-ttu-id="2eee6-125">Kod progrematyczny wyniku oceny.</span><span class="sxs-lookup"><span data-stu-id="2eee6-125">Progremmatic code for the result of the assessment.</span></span>
<span data-ttu-id="2eee6-126">może być "W dobrej kondycji", "Zła kondycja" lub "Niestosowalna"</span><span class="sxs-lookup"><span data-stu-id="2eee6-126">can be "Healthy", "Unhealthy" or "NotApplicable"</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: False
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

### <span data-ttu-id="2eee6-127">-StatusDescription</span><span class="sxs-lookup"><span data-stu-id="2eee6-127">-StatusDescription</span></span>
<span data-ttu-id="2eee6-128">Czytelny dla człowieka opis przyczyny wyniku oceny.</span><span class="sxs-lookup"><span data-stu-id="2eee6-128">Human readable description of the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="2eee6-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2eee6-129">-Confirm</span></span>
<span data-ttu-id="2eee6-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2eee6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eee6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eee6-131">-WhatIf</span></span>
<span data-ttu-id="2eee6-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eee6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eee6-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2eee6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eee6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eee6-134">CommonParameters</span></span>
<span data-ttu-id="2eee6-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eee6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eee6-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2eee6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eee6-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2eee6-137">INPUTS</span></span>

### <span data-ttu-id="2eee6-138">Brak</span><span class="sxs-lookup"><span data-stu-id="2eee6-138">None</span></span>

## <span data-ttu-id="2eee6-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2eee6-139">OUTPUTS</span></span>

### <span data-ttu-id="2eee6-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="2eee6-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="2eee6-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2eee6-141">NOTES</span></span>

## <span data-ttu-id="2eee6-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2eee6-142">RELATED LINKS</span></span>
