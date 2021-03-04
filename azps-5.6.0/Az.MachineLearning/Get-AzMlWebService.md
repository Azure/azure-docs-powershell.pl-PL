---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: 1dcf881fbe0a3a616a7522236099f7698b50a1a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007777"
---
# <span data-ttu-id="e6b1c-101">Get-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="e6b1c-101">Get-AzMlWebService</span></span>

## <span data-ttu-id="e6b1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6b1c-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b1c-103">Pobiera informacje podsumowujące dla jednej lub większej liczby usług sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-103">Retrieves the summary information for one or more web services.</span></span>

## <span data-ttu-id="e6b1c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e6b1c-104">SYNTAX</span></span>

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6b1c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e6b1c-105">DESCRIPTION</span></span>
<span data-ttu-id="e6b1c-106">Pobiera informacje o definicji usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-106">Retrieves web service definition information.</span></span>
<span data-ttu-id="e6b1c-107">W zależności od przekazanych parametrów polecenie cmdlet zwraca definicję określonej usługi sieci Web, kolekcję definicji usług sieci Web dla określonej grupy zasobów w ramach bieżącej subskrypcji lub kolekcję definicji usług sieci Web w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-107">Depending on the parameters passed, the cmdlet returns the definition for a specific web service, a collection of definitions for the web services for a specified resource group within the current subscription, or a collection of definitions for the web services within the current subscription.</span></span>

## <span data-ttu-id="e6b1c-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e6b1c-108">EXAMPLES</span></span>

### <span data-ttu-id="e6b1c-109">Przykład 1. Uzyskiwanie szczegółowych informacji o konkretnej usłudze sieci Web</span><span class="sxs-lookup"><span data-stu-id="e6b1c-109">Example 1: Get details of specific web service</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="e6b1c-110">Przykład 2. Uzyskiwanie wszystkich zasobów usługi sieci Web w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e6b1c-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzMlWebService
```

### <span data-ttu-id="e6b1c-111">Przykład 3. Uzyskiwanie wszystkich usług sieci Web w bieżącej subskrypcji i danej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e6b1c-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="e6b1c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6b1c-112">PARAMETERS</span></span>

### <span data-ttu-id="e6b1c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b1c-113">-DefaultProfile</span></span>
<span data-ttu-id="e6b1c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e6b1c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b1c-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e6b1c-115">-Name</span></span>
<span data-ttu-id="e6b1c-116">Nazwa usługi sieci Web, dla której są pobierane szczegóły.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-116">The name of the web service for which the details are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b1c-117">— Region</span><span class="sxs-lookup"><span data-stu-id="e6b1c-117">-Region</span></span>
<span data-ttu-id="e6b1c-118">Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="e6b1c-118">The name of region</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b1c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6b1c-119">-ResourceGroupName</span></span>
<span data-ttu-id="e6b1c-120">Grupa zasobów, z której są pobierane szczegóły usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-120">The resource group from which the details for the web service are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b1c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b1c-121">CommonParameters</span></span>
<span data-ttu-id="e6b1c-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6b1c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b1c-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6b1c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b1c-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6b1c-124">INPUTS</span></span>

### <span data-ttu-id="e6b1c-125">Brak</span><span class="sxs-lookup"><span data-stu-id="e6b1c-125">None</span></span>

## <span data-ttu-id="e6b1c-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6b1c-126">OUTPUTS</span></span>

### <span data-ttu-id="e6b1c-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="e6b1c-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="e6b1c-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e6b1c-128">NOTES</span></span>
<span data-ttu-id="e6b1c-129">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="e6b1c-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e6b1c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6b1c-130">RELATED LINKS</span></span>
