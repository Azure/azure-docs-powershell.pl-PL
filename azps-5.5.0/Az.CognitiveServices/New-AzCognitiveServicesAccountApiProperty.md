---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 97cf393d0d95dbc9ecfec06f53795713f59aecbd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239040"
---
# <span data-ttu-id="a4f25-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="a4f25-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="a4f25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4f25-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f25-103">Generowanie nowego wystąpienia właściwości ApiProperties konta usług Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="a4f25-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="a4f25-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a4f25-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4f25-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a4f25-105">DESCRIPTION</span></span>
<span data-ttu-id="a4f25-106">Wygeneruj nowe wystąpienie właściwości ApiProperties konta usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="a4f25-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="a4f25-107">Właściwości ApiProperties mogą być używane podczas tworzenia nowego konta lub aktualizowania istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="a4f25-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="a4f25-108">Niektóre typy kont są wymagane przez właściwości ApiProperties.</span><span class="sxs-lookup"><span data-stu-id="a4f25-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="a4f25-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a4f25-109">EXAMPLES</span></span>

### <span data-ttu-id="a4f25-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4f25-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="a4f25-111">Powyższy przykład spowoduje utworzenie konta programu QnAMaker z właściwością interfejsu API "QnaRuntimeEndpoint".</span><span class="sxs-lookup"><span data-stu-id="a4f25-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="a4f25-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4f25-112">PARAMETERS</span></span>

### <span data-ttu-id="a4f25-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f25-113">-DefaultProfile</span></span>
<span data-ttu-id="a4f25-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4f25-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4f25-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4f25-115">-Confirm</span></span>
<span data-ttu-id="a4f25-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a4f25-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4f25-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4f25-117">-WhatIf</span></span>
<span data-ttu-id="a4f25-118">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4f25-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4f25-119">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a4f25-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4f25-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f25-120">CommonParameters</span></span>
<span data-ttu-id="a4f25-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4f25-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f25-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4f25-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f25-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4f25-123">INPUTS</span></span>

### <span data-ttu-id="a4f25-124">Brak</span><span class="sxs-lookup"><span data-stu-id="a4f25-124">None</span></span>

## <span data-ttu-id="a4f25-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a4f25-125">OUTPUTS</span></span>

### <span data-ttu-id="a4f25-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span><span class="sxs-lookup"><span data-stu-id="a4f25-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="a4f25-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a4f25-127">NOTES</span></span>

## <span data-ttu-id="a4f25-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4f25-128">RELATED LINKS</span></span>
