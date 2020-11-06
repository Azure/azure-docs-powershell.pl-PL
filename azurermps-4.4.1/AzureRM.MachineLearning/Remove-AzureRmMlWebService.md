---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: f05d4142efab5a95cfef43fbc44cf57d0e1e2cf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549159"
---
# <span data-ttu-id="91cbc-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="91cbc-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="91cbc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="91cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="91cbc-103">Usuwa usługę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="91cbc-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91cbc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="91cbc-104">SYNTAX</span></span>

### <span data-ttu-id="91cbc-105">Usuń usługę sieci Web usługi Azure ML Resouce według nazwy i grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="91cbc-105">Remove an Azure ML web service resouce by name and resource group.</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91cbc-106">Usuń usługę sieci Web Azure ML określoną jako obiekt.</span><span class="sxs-lookup"><span data-stu-id="91cbc-106">Remove an Azure ML web service specified as an object.</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91cbc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="91cbc-107">DESCRIPTION</span></span>
<span data-ttu-id="91cbc-108">Usuwa usługę sieci Web Azure Machine Learning, do której odwołuje się grupa zasobów i nazwa.</span><span class="sxs-lookup"><span data-stu-id="91cbc-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="91cbc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="91cbc-109">EXAMPLES</span></span>

### <span data-ttu-id="91cbc-110">--------------------------Przykład 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="91cbc-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="91cbc-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="91cbc-111">@{paragraph=PS C:\\\>}</span></span>





```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="91cbc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91cbc-112">PARAMETERS</span></span>

### <span data-ttu-id="91cbc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="91cbc-113">-Force</span></span>
<span data-ttu-id="91cbc-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="91cbc-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="91cbc-115">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="91cbc-115">-MlWebService</span></span>
<span data-ttu-id="91cbc-116">Usługa sieci Web, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="91cbc-116">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Remove an Azure ML web service specified as an object.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91cbc-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="91cbc-117">-Name</span></span>
<span data-ttu-id="91cbc-118">Nazwa usługi sieci Web, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="91cbc-118">The name of the web service to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91cbc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91cbc-119">-ResourceGroupName</span></span>
<span data-ttu-id="91cbc-120">Grupa zasobów usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="91cbc-120">The resource group of the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91cbc-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="91cbc-121">-Confirm</span></span>
<span data-ttu-id="91cbc-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91cbc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91cbc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91cbc-123">-WhatIf</span></span>
<span data-ttu-id="91cbc-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91cbc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91cbc-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="91cbc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91cbc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91cbc-126">-DefaultProfile</span></span>
<span data-ttu-id="91cbc-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="91cbc-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91cbc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91cbc-128">CommonParameters</span></span>
<span data-ttu-id="91cbc-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91cbc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91cbc-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91cbc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91cbc-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91cbc-131">INPUTS</span></span>

### <span data-ttu-id="91cbc-132">Usług</span><span class="sxs-lookup"><span data-stu-id="91cbc-132">WebService</span></span>
<span data-ttu-id="91cbc-133">Parametr "MlWebService" akceptuje wartość typu "WebService" z procesu</span><span class="sxs-lookup"><span data-stu-id="91cbc-133">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="91cbc-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="91cbc-134">OUTPUTS</span></span>

### <span data-ttu-id="91cbc-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="91cbc-135">None</span></span>

## <span data-ttu-id="91cbc-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="91cbc-136">NOTES</span></span>
<span data-ttu-id="91cbc-137">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="91cbc-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="91cbc-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91cbc-138">RELATED LINKS</span></span>

