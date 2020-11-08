---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
ms.openlocfilehash: 9a227c742892d94417d42be7137f903e17b8b928
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232473"
---
# <span data-ttu-id="df8dc-101">Set-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="df8dc-101">Set-AzSecurityAssessment</span></span>

## <span data-ttu-id="df8dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df8dc-102">SYNOPSIS</span></span>
<span data-ttu-id="df8dc-103">Tworzenie lub aktualizowanie wyniku oceny zabezpieczeń dla zasobu</span><span class="sxs-lookup"><span data-stu-id="df8dc-103">Create or update a security assessment result on a resource</span></span>

## <span data-ttu-id="df8dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df8dc-104">SYNTAX</span></span>

### <span data-ttu-id="df8dc-105">SubscriptionLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="df8dc-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAssessment -Name <String> [-StatusCode <String>] [-StatusCause <String>]
 [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df8dc-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="df8dc-106">ResourceIdLevelResource</span></span>
```
Set-AzSecurityAssessment -Name <String> -AssessedResourceId <String> -StatusCode <String>
 [-StatusCause <String>] [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df8dc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="df8dc-107">DESCRIPTION</span></span>
<span data-ttu-id="df8dc-108">Tworzenie lub aktualizowanie wyniku oceny zabezpieczeń dla zasobu można użyć w celu zmiany stanu istniejącego wyniku lub dodania dodatkowych danych.</span><span class="sxs-lookup"><span data-stu-id="df8dc-108">Create or update a security assessment result on a resource, can be used to change the status of an existing result or add additional data.</span></span>
<span data-ttu-id="df8dc-109">można użyć tylko w przypadku typów oceny "CustomerManaged" i tylko po utworzeniu dopasowanych metadanych oceny.</span><span class="sxs-lookup"><span data-stu-id="df8dc-109">can only be used for "CustomerManaged" assessment types and only after the matched assessment metadata is created.</span></span>

## <span data-ttu-id="df8dc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df8dc-110">EXAMPLES</span></span>

### <span data-ttu-id="df8dc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="df8dc-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D -StatusCode "Unhealthy"
```

<span data-ttu-id="df8dc-112">Oznacza wynik subskrypcji jako "niezdrowy" dla oceny typu "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" — więcej szczegółów dotyczących typu oceny można znaleźć pod typem assessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="df8dc-112">Marks the subscription result as "Unhealthy" for assessment of type "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" - more details about the assessment type will be found under the assessmentMetadata type</span></span>

## <span data-ttu-id="df8dc-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df8dc-113">PARAMETERS</span></span>

### <span data-ttu-id="df8dc-114">-AdditionalData</span><span class="sxs-lookup"><span data-stu-id="df8dc-114">-AdditionalData</span></span>
<span data-ttu-id="df8dc-115">Dane, które są dołączane do wyniku oceny, w celu uzyskania lepszych wyników badań lub przejrzystości statusu.</span><span class="sxs-lookup"><span data-stu-id="df8dc-115">Data that is attached to the assessment result for better investigations or status clarity.</span></span>

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

### <span data-ttu-id="df8dc-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="df8dc-116">-AssessedResourceId</span></span>
<span data-ttu-id="df8dc-117">Pełny identyfikator zasobu, dla którego jest obliczana Ocena.</span><span class="sxs-lookup"><span data-stu-id="df8dc-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="df8dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df8dc-118">-DefaultProfile</span></span>
<span data-ttu-id="df8dc-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df8dc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df8dc-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="df8dc-120">-Name</span></span>
<span data-ttu-id="df8dc-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="df8dc-121">Resource name.</span></span>

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

### <span data-ttu-id="df8dc-122">-StatusCause</span><span class="sxs-lookup"><span data-stu-id="df8dc-122">-StatusCause</span></span>
<span data-ttu-id="df8dc-123">Progremmatic kod przyczyny wyniku oceny.</span><span class="sxs-lookup"><span data-stu-id="df8dc-123">Progremmatic code for the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="df8dc-124">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="df8dc-124">-StatusCode</span></span>
<span data-ttu-id="df8dc-125">Kod Progremmatic dla wyniku oceny.</span><span class="sxs-lookup"><span data-stu-id="df8dc-125">Progremmatic code for the result of the assessment.</span></span>
<span data-ttu-id="df8dc-126">może mieć wartość "zdrowy", "niezdrowe" lub "NotApplicable"</span><span class="sxs-lookup"><span data-stu-id="df8dc-126">can be "Healthy", "Unhealthy" or "NotApplicable"</span></span>

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

### <span data-ttu-id="df8dc-127">-StatusDescription</span><span class="sxs-lookup"><span data-stu-id="df8dc-127">-StatusDescription</span></span>
<span data-ttu-id="df8dc-128">Zrozumiały dla człowieka opis przyczyny wyniku oceny.</span><span class="sxs-lookup"><span data-stu-id="df8dc-128">Human readable description of the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="df8dc-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="df8dc-129">-Confirm</span></span>
<span data-ttu-id="df8dc-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df8dc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df8dc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df8dc-131">-WhatIf</span></span>
<span data-ttu-id="df8dc-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df8dc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df8dc-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="df8dc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df8dc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df8dc-134">CommonParameters</span></span>
<span data-ttu-id="df8dc-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df8dc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df8dc-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df8dc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df8dc-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df8dc-137">INPUTS</span></span>

### <span data-ttu-id="df8dc-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="df8dc-138">None</span></span>

## <span data-ttu-id="df8dc-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df8dc-139">OUTPUTS</span></span>

### <span data-ttu-id="df8dc-140">Microsoft. Azure. Commands. Security. MODELES. oceny. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="df8dc-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="df8dc-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df8dc-141">NOTES</span></span>

## <span data-ttu-id="df8dc-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df8dc-142">RELATED LINKS</span></span>
