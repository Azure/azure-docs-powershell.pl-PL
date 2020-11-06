---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/add-azurermmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
ms.openlocfilehash: 8b2f881b57639a83227c2f590ffd260b78509a54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552896"
---
# <span data-ttu-id="08de1-101">Add-AzureRmMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="08de1-101">Add-AzureRmMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="08de1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08de1-102">SYNOPSIS</span></span>
<span data-ttu-id="08de1-103">Tworzy właściwości regionalne usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="08de1-103">Creates regional web service properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08de1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08de1-104">SYNTAX</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08de1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="08de1-105">DESCRIPTION</span></span>
<span data-ttu-id="08de1-106">Tworzy właściwości regionalne Azure Machine Learning dla istniejącej usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="08de1-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="08de1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08de1-107">EXAMPLES</span></span>

### <span data-ttu-id="08de1-108">--------------------------Przykład 1: Dodawanie nowych właściwości regionalnych dla Stanów Zjednoczonych--------------------------zachodniego</span><span class="sxs-lookup"><span data-stu-id="08de1-108">--------------------------  Example 1: Add new regional properties for West Central US  --------------------------</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="08de1-109">To polecenie przykładowe tworzy właściwość regionalną dla usługi sieci Web w regionie "Zachodnia Centrala Amerykańska".</span><span class="sxs-lookup"><span data-stu-id="08de1-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="08de1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08de1-110">PARAMETERS</span></span>

### <span data-ttu-id="08de1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08de1-111">-DefaultProfile</span></span>
<span data-ttu-id="08de1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="08de1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08de1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="08de1-113">-Force</span></span>
<span data-ttu-id="08de1-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="08de1-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="08de1-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="08de1-115">-Name</span></span>
<span data-ttu-id="08de1-116">Nazwa usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="08de1-116">The name for the web service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08de1-117">-Region</span><span class="sxs-lookup"><span data-stu-id="08de1-117">-Region</span></span>
<span data-ttu-id="08de1-118">Region, w którym mają zostać utworzone właściwości usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="08de1-118">The region in which to create the web service properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08de1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08de1-119">-ResourceGroupName</span></span>
<span data-ttu-id="08de1-120">Grupa zasobów, do której należy usługa sieci Web.</span><span class="sxs-lookup"><span data-stu-id="08de1-120">The resource group in which the web service belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08de1-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08de1-121">-Confirm</span></span>
<span data-ttu-id="08de1-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08de1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08de1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08de1-123">-WhatIf</span></span>
<span data-ttu-id="08de1-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08de1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08de1-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="08de1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08de1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08de1-126">CommonParameters</span></span>
<span data-ttu-id="08de1-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08de1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08de1-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08de1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08de1-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08de1-129">INPUTS</span></span>

### <span data-ttu-id="08de1-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="08de1-130">None</span></span>
<span data-ttu-id="08de1-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="08de1-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="08de1-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08de1-132">OUTPUTS</span></span>

### <span data-ttu-id="08de1-133">Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService</span><span class="sxs-lookup"><span data-stu-id="08de1-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="08de1-134">Skrócony opis usługi sieci Web Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="08de1-134">A summary description of the Azure Machine Learning web service.</span></span>

## <span data-ttu-id="08de1-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08de1-135">NOTES</span></span>
<span data-ttu-id="08de1-136">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="08de1-136">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="08de1-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08de1-137">RELATED LINKS</span></span>

