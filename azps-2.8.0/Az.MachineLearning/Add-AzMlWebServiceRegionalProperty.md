---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: 877ef93dbecf3510887a24cb0b5dfe65948658f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704958"
---
# <span data-ttu-id="b8d9e-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="b8d9e-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="b8d9e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8d9e-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d9e-103">Tworzy właściwości regionalne usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b8d9e-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="b8d9e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8d9e-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8d9e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b8d9e-105">DESCRIPTION</span></span>
<span data-ttu-id="b8d9e-106">Tworzy właściwości regionalne Azure Machine Learning dla istniejącej usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b8d9e-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="b8d9e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8d9e-107">EXAMPLES</span></span>

### <span data-ttu-id="b8d9e-108">Przykład 1: Dodawanie nowych właściwości regionalnych dla Polski centralnego</span><span class="sxs-lookup"><span data-stu-id="b8d9e-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="b8d9e-109">To polecenie przykładowe tworzy właściwość regionalną dla usługi sieci Web w regionie "Zachodnia Centrala Amerykańska".</span><span class="sxs-lookup"><span data-stu-id="b8d9e-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="b8d9e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8d9e-110">PARAMETERS</span></span>

### <span data-ttu-id="b8d9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d9e-111">-DefaultProfile</span></span>
<span data-ttu-id="b8d9e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b8d9e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8d9e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b8d9e-113">-Force</span></span>
<span data-ttu-id="b8d9e-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b8d9e-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b8d9e-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b8d9e-115">-Name</span></span>
<span data-ttu-id="b8d9e-116">Nazwa usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b8d9e-116">The name for the web service.</span></span>

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

### <span data-ttu-id="b8d9e-117">-Region</span><span class="sxs-lookup"><span data-stu-id="b8d9e-117">-Region</span></span>
<span data-ttu-id="b8d9e-118">Region, w którym mają zostać utworzone właściwości usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b8d9e-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="b8d9e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8d9e-119">-ResourceGroupName</span></span>
<span data-ttu-id="b8d9e-120">Grupa zasobów, do której należy usługa sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b8d9e-120">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="b8d9e-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b8d9e-121">-Confirm</span></span>
<span data-ttu-id="b8d9e-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8d9e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8d9e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8d9e-123">-WhatIf</span></span>
<span data-ttu-id="b8d9e-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8d9e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8d9e-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b8d9e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8d9e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d9e-126">CommonParameters</span></span>
<span data-ttu-id="b8d9e-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8d9e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d9e-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8d9e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d9e-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8d9e-129">INPUTS</span></span>

### <span data-ttu-id="b8d9e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b8d9e-130">System.String</span></span>

## <span data-ttu-id="b8d9e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8d9e-131">OUTPUTS</span></span>

### <span data-ttu-id="b8d9e-132">Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService</span><span class="sxs-lookup"><span data-stu-id="b8d9e-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="b8d9e-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8d9e-133">NOTES</span></span>
<span data-ttu-id="b8d9e-134">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="b8d9e-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b8d9e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8d9e-135">RELATED LINKS</span></span>
