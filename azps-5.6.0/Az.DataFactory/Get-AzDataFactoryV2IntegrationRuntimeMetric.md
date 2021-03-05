---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 12810756f1ebe3e3bf345519d981b660f4c61aa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975249"
---
# <span data-ttu-id="fbba8-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="fbba8-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="fbba8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbba8-102">SYNOPSIS</span></span>
<span data-ttu-id="fbba8-103">Pobiera dane metryczne dla środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="fbba8-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="fbba8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fbba8-104">SYNTAX</span></span>

### <span data-ttu-id="fbba8-105">ByIntegrationRuntimeName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="fbba8-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbba8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fbba8-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fbba8-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="fbba8-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbba8-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fbba8-108">DESCRIPTION</span></span>
<span data-ttu-id="fbba8-109">Polecenie Get-AzDataFactoryV2IntegrationRuntimeMetric pobiera dane metryczne dotyczące środowiska uruchomieniowego integracji w zakładzie danych.</span><span class="sxs-lookup"><span data-stu-id="fbba8-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="fbba8-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fbba8-110">EXAMPLES</span></span>

### <span data-ttu-id="fbba8-111">Przykład 1. Uzyskaj metrykę środowiska uruchomieniowego integracji</span><span class="sxs-lookup"><span data-stu-id="fbba8-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="fbba8-112">To polecenie wyświetla dane metryczne dotyczące środowiska uruchomieniowego integracji o nazwie "test-selfhost-ir" w subskrypcji dla grupy zasobów o nazwach "rg-test-dfv2" i data factory o nazwie "test-df-eu2".</span><span class="sxs-lookup"><span data-stu-id="fbba8-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="fbba8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbba8-113">PARAMETERS</span></span>

### <span data-ttu-id="fbba8-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fbba8-114">-DataFactoryName</span></span>
<span data-ttu-id="fbba8-115">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="fbba8-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbba8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbba8-116">-DefaultProfile</span></span>
<span data-ttu-id="fbba8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fbba8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbba8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbba8-118">-InputObject</span></span>
<span data-ttu-id="fbba8-119">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="fbba8-119">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbba8-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fbba8-120">-Name</span></span>
<span data-ttu-id="fbba8-121">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="fbba8-121">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbba8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbba8-122">-ResourceGroupName</span></span>
<span data-ttu-id="fbba8-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fbba8-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbba8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbba8-124">-ResourceId</span></span>
<span data-ttu-id="fbba8-125">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="fbba8-125">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbba8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbba8-126">CommonParameters</span></span>
<span data-ttu-id="fbba8-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbba8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbba8-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbba8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbba8-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbba8-129">INPUTS</span></span>

### <span data-ttu-id="fbba8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fbba8-130">System.String</span></span>

### <span data-ttu-id="fbba8-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fbba8-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="fbba8-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbba8-132">OUTPUTS</span></span>

### <span data-ttu-id="fbba8-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="fbba8-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="fbba8-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fbba8-134">NOTES</span></span>

## <span data-ttu-id="fbba8-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbba8-135">RELATED LINKS</span></span>

[<span data-ttu-id="fbba8-136">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fbba8-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

