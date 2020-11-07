---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 8912717f718bff7c669752e5e49c2796ee94b05b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719664"
---
# <span data-ttu-id="9d0c7-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="9d0c7-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="9d0c7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d0c7-102">SYNOPSIS</span></span>
<span data-ttu-id="9d0c7-103">Pobiera dane metryczne dla środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="9d0c7-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d0c7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d0c7-104">SYNTAX</span></span>

### <span data-ttu-id="9d0c7-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9d0c7-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="9d0c7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9d0c7-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
```

### <span data-ttu-id="9d0c7-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="9d0c7-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="9d0c7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9d0c7-108">DESCRIPTION</span></span>
<span data-ttu-id="9d0c7-109">Polecenie cmdlet Get-AzureRmDataFactoryV2IntegrationRuntimeMetric pobiera dane metryczne dotyczące środowiska programu integracyjnego w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="9d0c7-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="9d0c7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d0c7-110">EXAMPLES</span></span>

### <span data-ttu-id="9d0c7-111">Przykład 1: uzyskiwanie metryki środowiska uruchomieniowego integracji</span><span class="sxs-lookup"><span data-stu-id="9d0c7-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="9d0c7-112">To polecenie wyświetla dane metryczne dotyczące środowiska wykonawczego integracji o nazwie "test-SelfHost-IR" w subskrypcji grupy zasobów o nazwie "RG-test-dfv2" i fabryki danych o nazwie "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="9d0c7-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="9d0c7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d0c7-113">PARAMETERS</span></span>

### <span data-ttu-id="9d0c7-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="9d0c7-114">-DataFactoryName</span></span>
<span data-ttu-id="9d0c7-115">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="9d0c7-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0c7-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9d0c7-116">-InputObject</span></span>
<span data-ttu-id="9d0c7-117">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="9d0c7-117">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0c7-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9d0c7-118">-Name</span></span>
<span data-ttu-id="9d0c7-119">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="9d0c7-119">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0c7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d0c7-120">-ResourceGroupName</span></span>
<span data-ttu-id="9d0c7-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9d0c7-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0c7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d0c7-122">-ResourceId</span></span>
<span data-ttu-id="9d0c7-123">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9d0c7-123">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="9d0c7-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d0c7-124">INPUTS</span></span>

### <span data-ttu-id="9d0c7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9d0c7-125">System.String</span></span>
<span data-ttu-id="9d0c7-126">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9d0c7-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="9d0c7-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d0c7-127">OUTPUTS</span></span>

### <span data-ttu-id="9d0c7-128">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="9d0c7-128">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>


## <span data-ttu-id="9d0c7-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d0c7-129">NOTES</span></span>

## <span data-ttu-id="9d0c7-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d0c7-130">RELATED LINKS</span></span>
[<span data-ttu-id="9d0c7-131">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9d0c7-131">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

