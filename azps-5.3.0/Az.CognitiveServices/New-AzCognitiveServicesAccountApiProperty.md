---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 97cf393d0d95dbc9ecfec06f53795713f59aecbd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501979"
---
# <span data-ttu-id="22b53-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="22b53-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="22b53-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22b53-102">SYNOPSIS</span></span>
<span data-ttu-id="22b53-103">Generowanie nowej instancji ApiProperties konta usług poznawczych</span><span class="sxs-lookup"><span data-stu-id="22b53-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="22b53-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22b53-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22b53-105">Opis</span><span class="sxs-lookup"><span data-stu-id="22b53-105">DESCRIPTION</span></span>
<span data-ttu-id="22b53-106">Generowanie nowego wystąpienia ApiProperties konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="22b53-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="22b53-107">ApiProperties można użyć podczas tworzenia nowego konta lub aktualizowania istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="22b53-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="22b53-108">ApiProperties jest wymagany przez niektóre typy kont.</span><span class="sxs-lookup"><span data-stu-id="22b53-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="22b53-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22b53-109">EXAMPLES</span></span>

### <span data-ttu-id="22b53-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="22b53-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="22b53-111">Powyższy przykład utworzy konto QnAMaker z właściwością interfejsu API "QnaRuntimeEndpoint".</span><span class="sxs-lookup"><span data-stu-id="22b53-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="22b53-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22b53-112">PARAMETERS</span></span>

### <span data-ttu-id="22b53-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b53-113">-DefaultProfile</span></span>
<span data-ttu-id="22b53-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="22b53-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22b53-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="22b53-115">-Confirm</span></span>
<span data-ttu-id="22b53-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22b53-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22b53-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22b53-117">-WhatIf</span></span>
<span data-ttu-id="22b53-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22b53-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22b53-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="22b53-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22b53-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b53-120">CommonParameters</span></span>
<span data-ttu-id="22b53-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22b53-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b53-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22b53-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b53-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22b53-123">INPUTS</span></span>

### <span data-ttu-id="22b53-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="22b53-124">None</span></span>

## <span data-ttu-id="22b53-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22b53-125">OUTPUTS</span></span>

### <span data-ttu-id="22b53-126">Microsoft. Azure. Management. CognitiveServices. MODELES. CognitiveServicesAccountApiProperties</span><span class="sxs-lookup"><span data-stu-id="22b53-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="22b53-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22b53-127">NOTES</span></span>

## <span data-ttu-id="22b53-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22b53-128">RELATED LINKS</span></span>
