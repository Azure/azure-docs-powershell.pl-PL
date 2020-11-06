---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/add-azurermmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
ms.openlocfilehash: be43e56b8106cfde357f1a6c8609cee497158308
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546548"
---
# <span data-ttu-id="62f28-101">Add-AzureRmMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="62f28-101">Add-AzureRmMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="62f28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62f28-102">SYNOPSIS</span></span>
<span data-ttu-id="62f28-103">Tworzy właściwości regionalne usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="62f28-103">Creates regional web service properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62f28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62f28-104">SYNTAX</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62f28-105">Opis</span><span class="sxs-lookup"><span data-stu-id="62f28-105">DESCRIPTION</span></span>
<span data-ttu-id="62f28-106">Tworzy właściwości regionalne Azure Machine Learning dla istniejącej usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="62f28-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="62f28-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62f28-107">EXAMPLES</span></span>

### <span data-ttu-id="62f28-108">Przykład 1: Dodawanie nowych właściwości regionalnych dla Polski centralnego</span><span class="sxs-lookup"><span data-stu-id="62f28-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="62f28-109">To polecenie przykładowe tworzy właściwość regionalną dla usługi sieci Web w regionie "Zachodnia Centrala Amerykańska".</span><span class="sxs-lookup"><span data-stu-id="62f28-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="62f28-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62f28-110">PARAMETERS</span></span>

### <span data-ttu-id="62f28-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62f28-111">-DefaultProfile</span></span>
<span data-ttu-id="62f28-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="62f28-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62f28-113">-Force</span><span class="sxs-lookup"><span data-stu-id="62f28-113">-Force</span></span>
<span data-ttu-id="62f28-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="62f28-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="62f28-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="62f28-115">-Name</span></span>
<span data-ttu-id="62f28-116">Nazwa usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="62f28-116">The name for the web service.</span></span>

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

### <span data-ttu-id="62f28-117">-Region</span><span class="sxs-lookup"><span data-stu-id="62f28-117">-Region</span></span>
<span data-ttu-id="62f28-118">Region, w którym mają zostać utworzone właściwości usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="62f28-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="62f28-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62f28-119">-ResourceGroupName</span></span>
<span data-ttu-id="62f28-120">Grupa zasobów, do której należy usługa sieci Web.</span><span class="sxs-lookup"><span data-stu-id="62f28-120">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="62f28-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62f28-121">-Confirm</span></span>
<span data-ttu-id="62f28-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62f28-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62f28-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62f28-123">-WhatIf</span></span>
<span data-ttu-id="62f28-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62f28-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62f28-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="62f28-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62f28-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62f28-126">CommonParameters</span></span>
<span data-ttu-id="62f28-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62f28-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62f28-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62f28-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62f28-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62f28-129">INPUTS</span></span>

### <span data-ttu-id="62f28-130">System. String</span><span class="sxs-lookup"><span data-stu-id="62f28-130">System.String</span></span>

## <span data-ttu-id="62f28-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62f28-131">OUTPUTS</span></span>

### <span data-ttu-id="62f28-132">Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService</span><span class="sxs-lookup"><span data-stu-id="62f28-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="62f28-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62f28-133">NOTES</span></span>
<span data-ttu-id="62f28-134">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="62f28-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="62f28-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62f28-135">RELATED LINKS</span></span>
