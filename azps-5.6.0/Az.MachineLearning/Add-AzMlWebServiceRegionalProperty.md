---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: 8b645154e9aaa011fccf1fa01624481e44b4eebb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952353"
---
# <span data-ttu-id="0cc8f-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="0cc8f-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="0cc8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cc8f-102">SYNOPSIS</span></span>
<span data-ttu-id="0cc8f-103">Tworzy właściwości regionalnych usług sieci Web.</span><span class="sxs-lookup"><span data-stu-id="0cc8f-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="0cc8f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0cc8f-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cc8f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0cc8f-105">DESCRIPTION</span></span>
<span data-ttu-id="0cc8f-106">Tworzy właściwości regionalne usługi Azure Machine Learning dla istniejącej usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="0cc8f-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="0cc8f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0cc8f-107">EXAMPLES</span></span>

### <span data-ttu-id="0cc8f-108">Przykład 1. Dodawanie nowych właściwości regionalnych dla Stanów Zjednoczonych Środkowych Zachód</span><span class="sxs-lookup"><span data-stu-id="0cc8f-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="0cc8f-109">To przykładowe polecenie tworzy właściwość regionalną usługi sieci Web w regionie "Zachód Środkowe Stany Zjednoczone".</span><span class="sxs-lookup"><span data-stu-id="0cc8f-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="0cc8f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0cc8f-110">PARAMETERS</span></span>

### <span data-ttu-id="0cc8f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cc8f-111">-DefaultProfile</span></span>
<span data-ttu-id="0cc8f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="0cc8f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cc8f-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="0cc8f-113">-Force</span></span>
<span data-ttu-id="0cc8f-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0cc8f-114">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc8f-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0cc8f-115">-Name</span></span>
<span data-ttu-id="0cc8f-116">Nazwa usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="0cc8f-116">The name for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cc8f-117">— Region</span><span class="sxs-lookup"><span data-stu-id="0cc8f-117">-Region</span></span>
<span data-ttu-id="0cc8f-118">Region, w którym mają być tworzyć właściwości usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="0cc8f-118">The region in which to create the web service properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc8f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cc8f-119">-ResourceGroupName</span></span>
<span data-ttu-id="0cc8f-120">Grupa zasobów, do której należy usługa sieci Web.</span><span class="sxs-lookup"><span data-stu-id="0cc8f-120">The resource group in which the web service belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cc8f-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0cc8f-121">-Confirm</span></span>
<span data-ttu-id="0cc8f-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0cc8f-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc8f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cc8f-123">-WhatIf</span></span>
<span data-ttu-id="0cc8f-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cc8f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cc8f-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0cc8f-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc8f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cc8f-126">CommonParameters</span></span>
<span data-ttu-id="0cc8f-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cc8f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cc8f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cc8f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cc8f-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0cc8f-129">INPUTS</span></span>

### <span data-ttu-id="0cc8f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0cc8f-130">System.String</span></span>

## <span data-ttu-id="0cc8f-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0cc8f-131">OUTPUTS</span></span>

### <span data-ttu-id="0cc8f-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="0cc8f-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="0cc8f-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0cc8f-133">NOTES</span></span>
<span data-ttu-id="0cc8f-134">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="0cc8f-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="0cc8f-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0cc8f-135">RELATED LINKS</span></span>
