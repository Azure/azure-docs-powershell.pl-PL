---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 4a59508cc816f3301d76b1d982f52108247b50a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187507"
---
# <span data-ttu-id="36889-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="36889-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="36889-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36889-102">SYNOPSIS</span></span>
<span data-ttu-id="36889-103">Usuwa usługę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="36889-103">Deletes a web service.</span></span>

## <span data-ttu-id="36889-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="36889-104">SYNTAX</span></span>

### <span data-ttu-id="36889-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="36889-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36889-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="36889-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36889-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="36889-107">DESCRIPTION</span></span>
<span data-ttu-id="36889-108">Usuwa usługę internetową Azure Machine Learning, do których odwołuje się grupa zasobów i nazwa.</span><span class="sxs-lookup"><span data-stu-id="36889-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="36889-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="36889-109">EXAMPLES</span></span>

### <span data-ttu-id="36889-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="36889-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="36889-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36889-111">PARAMETERS</span></span>

### <span data-ttu-id="36889-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36889-112">-DefaultProfile</span></span>
<span data-ttu-id="36889-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="36889-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36889-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="36889-114">-Force</span></span>
<span data-ttu-id="36889-115">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="36889-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="36889-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="36889-116">-MlWebService</span></span>
<span data-ttu-id="36889-117">Usługa sieci Web do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="36889-117">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36889-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="36889-118">-Name</span></span>
<span data-ttu-id="36889-119">Nazwa usługi sieci Web do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="36889-119">The name of the web service to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36889-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36889-120">-ResourceGroupName</span></span>
<span data-ttu-id="36889-121">Grupa zasobów usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="36889-121">The resource group of the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36889-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36889-122">-Confirm</span></span>
<span data-ttu-id="36889-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="36889-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36889-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36889-124">-WhatIf</span></span>
<span data-ttu-id="36889-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36889-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36889-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="36889-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36889-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36889-127">CommonParameters</span></span>
<span data-ttu-id="36889-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36889-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36889-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36889-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36889-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36889-130">INPUTS</span></span>

### <span data-ttu-id="36889-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="36889-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="36889-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="36889-132">OUTPUTS</span></span>

### <span data-ttu-id="36889-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="36889-133">System.Void</span></span>

## <span data-ttu-id="36889-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="36889-134">NOTES</span></span>
<span data-ttu-id="36889-135">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="36889-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="36889-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36889-136">RELATED LINKS</span></span>
