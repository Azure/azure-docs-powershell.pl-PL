---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: 4d7365a2a7a8d11fc1032f182409bd462931be3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545659"
---
# <span data-ttu-id="6da69-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="6da69-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="6da69-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6da69-102">SYNOPSIS</span></span>
<span data-ttu-id="6da69-103">Usuwa usługę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="6da69-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6da69-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6da69-104">SYNTAX</span></span>

### <span data-ttu-id="6da69-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6da69-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6da69-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="6da69-106">RemoveByObject</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6da69-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6da69-107">DESCRIPTION</span></span>
<span data-ttu-id="6da69-108">Usuwa usługę sieci Web Azure Machine Learning, do której odwołuje się grupa zasobów i nazwa.</span><span class="sxs-lookup"><span data-stu-id="6da69-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="6da69-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6da69-109">EXAMPLES</span></span>

### <span data-ttu-id="6da69-110">--------------------------Przykład 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6da69-110">--------------------------  Example 1  --------------------------</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="6da69-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6da69-111">PARAMETERS</span></span>

### <span data-ttu-id="6da69-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6da69-112">-DefaultProfile</span></span>
<span data-ttu-id="6da69-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6da69-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da69-114">-Force</span><span class="sxs-lookup"><span data-stu-id="6da69-114">-Force</span></span>
<span data-ttu-id="6da69-115">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6da69-115">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da69-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="6da69-116">-MlWebService</span></span>
<span data-ttu-id="6da69-117">Usługa sieci Web, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="6da69-117">The web service to be removed.</span></span>

```yaml
Type: WebService
Parameter Sets: RemoveByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6da69-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6da69-118">-Name</span></span>
<span data-ttu-id="6da69-119">Nazwa usługi sieci Web, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="6da69-119">The name of the web service to be removed.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da69-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6da69-120">-ResourceGroupName</span></span>
<span data-ttu-id="6da69-121">Grupa zasobów usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="6da69-121">The resource group of the web service.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da69-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6da69-122">-Confirm</span></span>
<span data-ttu-id="6da69-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6da69-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6da69-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6da69-124">-WhatIf</span></span>
<span data-ttu-id="6da69-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6da69-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6da69-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6da69-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6da69-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6da69-127">CommonParameters</span></span>
<span data-ttu-id="6da69-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6da69-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6da69-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6da69-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6da69-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6da69-130">INPUTS</span></span>

### <span data-ttu-id="6da69-131">Usług</span><span class="sxs-lookup"><span data-stu-id="6da69-131">WebService</span></span>
<span data-ttu-id="6da69-132">Parametr "MlWebService" akceptuje wartość typu "WebService" z procesu</span><span class="sxs-lookup"><span data-stu-id="6da69-132">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="6da69-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6da69-133">OUTPUTS</span></span>

### <span data-ttu-id="6da69-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6da69-134">None</span></span>

## <span data-ttu-id="6da69-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6da69-135">NOTES</span></span>
<span data-ttu-id="6da69-136">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="6da69-136">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="6da69-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6da69-137">RELATED LINKS</span></span>

