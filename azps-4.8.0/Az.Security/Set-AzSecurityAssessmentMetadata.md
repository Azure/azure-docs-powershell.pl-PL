---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: d65cd0a5f29f15d2d82227aad6520df34fd4357f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219850"
---
# <span data-ttu-id="a361c-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="a361c-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="a361c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a361c-102">SYNOPSIS</span></span>
<span data-ttu-id="a361c-103">Umożliwia utworzenie lub zaktualizowanie typu oceny zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="a361c-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="a361c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a361c-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a361c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a361c-105">DESCRIPTION</span></span>
<span data-ttu-id="a361c-106">Służy do tworzenia lub aktualizowania metadanych oceny zabezpieczeń, których można użyć w celu utworzenia różnych właściwości oceny i zarządzania nimi.</span><span class="sxs-lookup"><span data-stu-id="a361c-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="a361c-107">Po wykonaniu tej akcji możesz raportować wyniki oceny dowolnego zasobu w tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a361c-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="a361c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a361c-108">EXAMPLES</span></span>

### <span data-ttu-id="a361c-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a361c-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="a361c-110">Utwórz nowy typ oceny w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a361c-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="a361c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a361c-111">PARAMETERS</span></span>

### <span data-ttu-id="a361c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a361c-112">-DefaultProfile</span></span>
<span data-ttu-id="a361c-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a361c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a361c-114">— Opis</span><span class="sxs-lookup"><span data-stu-id="a361c-114">-Description</span></span>
<span data-ttu-id="a361c-115">Szczegółowy ciąg, który pomoże użytkownikom zrozumieć znaczenie tej oceny i sposobu jej obliczania.</span><span class="sxs-lookup"><span data-stu-id="a361c-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

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

### <span data-ttu-id="a361c-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a361c-116">-DisplayName</span></span>
<span data-ttu-id="a361c-117">Odczytany przez człowieka tytuł tego obiektu.</span><span class="sxs-lookup"><span data-stu-id="a361c-117">Human readable title for this object.</span></span>

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

### <span data-ttu-id="a361c-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a361c-118">-Name</span></span>
<span data-ttu-id="a361c-119">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a361c-119">Resource name.</span></span>

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

### <span data-ttu-id="a361c-120">-RemediationDescription</span><span class="sxs-lookup"><span data-stu-id="a361c-120">-RemediationDescription</span></span>
<span data-ttu-id="a361c-121">Szczegółowy ciąg, który pomoże użytkownikom zrozumieć różne sposoby łagodzenia i rozwiązywania problemu z zabezpieczeniami.</span><span class="sxs-lookup"><span data-stu-id="a361c-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

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

### <span data-ttu-id="a361c-122">— Ważność</span><span class="sxs-lookup"><span data-stu-id="a361c-122">-Severity</span></span>
<span data-ttu-id="a361c-123">Wskazuje ważność ryzyka związanego z zabezpieczeniami, jeśli Szacowanie jest niezdrowe.</span><span class="sxs-lookup"><span data-stu-id="a361c-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

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

### <span data-ttu-id="a361c-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a361c-124">-Confirm</span></span>
<span data-ttu-id="a361c-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a361c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a361c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a361c-126">-WhatIf</span></span>
<span data-ttu-id="a361c-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a361c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a361c-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a361c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a361c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a361c-129">CommonParameters</span></span>
<span data-ttu-id="a361c-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a361c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a361c-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a361c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a361c-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a361c-132">INPUTS</span></span>

### <span data-ttu-id="a361c-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a361c-133">None</span></span>

## <span data-ttu-id="a361c-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a361c-134">OUTPUTS</span></span>

### <span data-ttu-id="a361c-135">Microsoft. Azure. Commands. Security. models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="a361c-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="a361c-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a361c-136">NOTES</span></span>

## <span data-ttu-id="a361c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a361c-137">RELATED LINKS</span></span>
