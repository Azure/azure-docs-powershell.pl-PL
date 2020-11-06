---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
ms.openlocfilehash: 24f12a0e95ab7c233a08ec1ad0f4dc330583dd3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554344"
---
# <span data-ttu-id="02dd2-101">Add-AzureRmMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="02dd2-101">Add-AzureRmMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="02dd2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="02dd2-103">Tworzy właściwości regionalne usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="02dd2-103">Creates regional web service properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02dd2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02dd2-104">SYNTAX</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02dd2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="02dd2-105">DESCRIPTION</span></span>
<span data-ttu-id="02dd2-106">Tworzy właściwości regionalne Azure Machine Learning dla istniejącej usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="02dd2-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="02dd2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02dd2-107">EXAMPLES</span></span>

### <span data-ttu-id="02dd2-108">--------------------------Przykład 1: Dodawanie nowych właściwości regionalnych dla Stanów Zjednoczonych--------------------------zachodniego</span><span class="sxs-lookup"><span data-stu-id="02dd2-108">--------------------------  Example 1: Add new regional properties for West Central US  --------------------------</span></span>
<span data-ttu-id="02dd2-109">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="02dd2-109">@{paragraph=PS C:\\\>}</span></span>



```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="02dd2-110">To polecenie przykładowe tworzy właściwość regionalną dla usługi sieci Web w regionie "Zachodnia Centrala Amerykańska".</span><span class="sxs-lookup"><span data-stu-id="02dd2-110">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="02dd2-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02dd2-111">PARAMETERS</span></span>

### <span data-ttu-id="02dd2-112">-Force</span><span class="sxs-lookup"><span data-stu-id="02dd2-112">-Force</span></span>
<span data-ttu-id="02dd2-113">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="02dd2-113">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="02dd2-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="02dd2-114">-Name</span></span>
<span data-ttu-id="02dd2-115">Nazwa usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="02dd2-115">The name for the web service.</span></span>

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

### <span data-ttu-id="02dd2-116">-Region</span><span class="sxs-lookup"><span data-stu-id="02dd2-116">-Region</span></span>
<span data-ttu-id="02dd2-117">Region, w którym mają zostać utworzone właściwości usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="02dd2-117">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="02dd2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02dd2-118">-ResourceGroupName</span></span>
<span data-ttu-id="02dd2-119">Grupa zasobów, do której należy usługa sieci Web.</span><span class="sxs-lookup"><span data-stu-id="02dd2-119">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="02dd2-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02dd2-120">-Confirm</span></span>
<span data-ttu-id="02dd2-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02dd2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02dd2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02dd2-122">-WhatIf</span></span>
<span data-ttu-id="02dd2-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02dd2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02dd2-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="02dd2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02dd2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02dd2-125">-DefaultProfile</span></span>
<span data-ttu-id="02dd2-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02dd2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02dd2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02dd2-127">CommonParameters</span></span>
<span data-ttu-id="02dd2-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02dd2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02dd2-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02dd2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02dd2-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02dd2-130">INPUTS</span></span>

## <span data-ttu-id="02dd2-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02dd2-131">OUTPUTS</span></span>

### <span data-ttu-id="02dd2-132">Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService</span><span class="sxs-lookup"><span data-stu-id="02dd2-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="02dd2-133">Skrócony opis usługi sieci Web Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="02dd2-133">A summary description of the Azure Machine Learning web service.</span></span>

## <span data-ttu-id="02dd2-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02dd2-134">NOTES</span></span>
<span data-ttu-id="02dd2-135">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="02dd2-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="02dd2-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02dd2-136">RELATED LINKS</span></span>

