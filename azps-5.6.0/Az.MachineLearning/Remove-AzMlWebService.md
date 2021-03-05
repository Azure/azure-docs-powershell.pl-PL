---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 46e9ae8f4b6b4bb954bca158adb82c0d821d67eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006698"
---
# <span data-ttu-id="04ca8-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="04ca8-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="04ca8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="04ca8-103">Usuwa usługę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="04ca8-103">Deletes a web service.</span></span>

## <span data-ttu-id="04ca8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="04ca8-104">SYNTAX</span></span>

### <span data-ttu-id="04ca8-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="04ca8-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04ca8-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="04ca8-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04ca8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="04ca8-107">DESCRIPTION</span></span>
<span data-ttu-id="04ca8-108">Usuwa usługę internetową Azure Machine Learning, do których odwołuje się grupa zasobów i nazwa.</span><span class="sxs-lookup"><span data-stu-id="04ca8-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="04ca8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="04ca8-109">EXAMPLES</span></span>

### <span data-ttu-id="04ca8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="04ca8-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="04ca8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04ca8-111">PARAMETERS</span></span>

### <span data-ttu-id="04ca8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04ca8-112">-DefaultProfile</span></span>
<span data-ttu-id="04ca8-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="04ca8-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04ca8-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="04ca8-114">-Force</span></span>
<span data-ttu-id="04ca8-115">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="04ca8-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="04ca8-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="04ca8-116">-MlWebService</span></span>
<span data-ttu-id="04ca8-117">Usługa sieci Web do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="04ca8-117">The web service to be removed.</span></span>

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

### <span data-ttu-id="04ca8-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="04ca8-118">-Name</span></span>
<span data-ttu-id="04ca8-119">Nazwa usługi sieci Web do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="04ca8-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="04ca8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04ca8-120">-ResourceGroupName</span></span>
<span data-ttu-id="04ca8-121">Grupa zasobów usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="04ca8-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="04ca8-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04ca8-122">-Confirm</span></span>
<span data-ttu-id="04ca8-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="04ca8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04ca8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04ca8-124">-WhatIf</span></span>
<span data-ttu-id="04ca8-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04ca8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04ca8-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="04ca8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04ca8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ca8-127">CommonParameters</span></span>
<span data-ttu-id="04ca8-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04ca8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ca8-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04ca8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ca8-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04ca8-130">INPUTS</span></span>

### <span data-ttu-id="04ca8-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="04ca8-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="04ca8-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04ca8-132">OUTPUTS</span></span>

### <span data-ttu-id="04ca8-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="04ca8-133">System.Void</span></span>

## <span data-ttu-id="04ca8-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="04ca8-134">NOTES</span></span>
<span data-ttu-id="04ca8-135">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="04ca8-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="04ca8-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04ca8-136">RELATED LINKS</span></span>
