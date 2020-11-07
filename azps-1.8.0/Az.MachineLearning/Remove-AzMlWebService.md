---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 2ade770ea51f3b9cb83ff04fc5edf604cab5bb71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867503"
---
# <span data-ttu-id="8ddb6-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="8ddb6-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="8ddb6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ddb6-102">SYNOPSIS</span></span>
<span data-ttu-id="8ddb6-103">Usuwa usługę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="8ddb6-103">Deletes a web service.</span></span>

## <span data-ttu-id="8ddb6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ddb6-104">SYNTAX</span></span>

### <span data-ttu-id="8ddb6-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8ddb6-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ddb6-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="8ddb6-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ddb6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8ddb6-107">DESCRIPTION</span></span>
<span data-ttu-id="8ddb6-108">Usuwa usługę sieci Web Azure Machine Learning, do której odwołuje się grupa zasobów i nazwa.</span><span class="sxs-lookup"><span data-stu-id="8ddb6-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="8ddb6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ddb6-109">EXAMPLES</span></span>

### <span data-ttu-id="8ddb6-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8ddb6-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="8ddb6-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ddb6-111">PARAMETERS</span></span>

### <span data-ttu-id="8ddb6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ddb6-112">-DefaultProfile</span></span>
<span data-ttu-id="8ddb6-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8ddb6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ddb6-114">-Force</span><span class="sxs-lookup"><span data-stu-id="8ddb6-114">-Force</span></span>
<span data-ttu-id="8ddb6-115">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8ddb6-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8ddb6-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="8ddb6-116">-MlWebService</span></span>
<span data-ttu-id="8ddb6-117">Usługa sieci Web, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="8ddb6-117">The web service to be removed.</span></span>

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

### <span data-ttu-id="8ddb6-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8ddb6-118">-Name</span></span>
<span data-ttu-id="8ddb6-119">Nazwa usługi sieci Web, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="8ddb6-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="8ddb6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ddb6-120">-ResourceGroupName</span></span>
<span data-ttu-id="8ddb6-121">Grupa zasobów usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="8ddb6-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="8ddb6-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8ddb6-122">-Confirm</span></span>
<span data-ttu-id="8ddb6-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ddb6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ddb6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ddb6-124">-WhatIf</span></span>
<span data-ttu-id="8ddb6-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ddb6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ddb6-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8ddb6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ddb6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ddb6-127">CommonParameters</span></span>
<span data-ttu-id="8ddb6-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ddb6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ddb6-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ddb6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ddb6-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ddb6-130">INPUTS</span></span>

### <span data-ttu-id="8ddb6-131">Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService</span><span class="sxs-lookup"><span data-stu-id="8ddb6-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="8ddb6-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ddb6-132">OUTPUTS</span></span>

### <span data-ttu-id="8ddb6-133">System. void</span><span class="sxs-lookup"><span data-stu-id="8ddb6-133">System.Void</span></span>

## <span data-ttu-id="8ddb6-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ddb6-134">NOTES</span></span>
<span data-ttu-id="8ddb6-135">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="8ddb6-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="8ddb6-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ddb6-136">RELATED LINKS</span></span>
