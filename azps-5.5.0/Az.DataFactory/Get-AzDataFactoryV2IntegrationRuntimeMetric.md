---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 9b82d302bba1c2f51de3748fb9c335dd0db2699d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242818"
---
# <span data-ttu-id="920d5-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="920d5-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="920d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="920d5-102">SYNOPSIS</span></span>
<span data-ttu-id="920d5-103">Pobiera dane metryczne dla środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="920d5-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="920d5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="920d5-104">SYNTAX</span></span>

### <span data-ttu-id="920d5-105">ByIntegrationRuntimeName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="920d5-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="920d5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="920d5-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="920d5-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="920d5-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="920d5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="920d5-108">DESCRIPTION</span></span>
<span data-ttu-id="920d5-109">Polecenie Get-AzDataFactoryV2IntegrationRuntimeMetric pobiera dane metryczne dotyczące środowiska uruchomieniowego integracji w zakładzie danych.</span><span class="sxs-lookup"><span data-stu-id="920d5-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="920d5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="920d5-110">EXAMPLES</span></span>

### <span data-ttu-id="920d5-111">Przykład 1. Uzyskaj metrykę środowiska uruchomieniowego integracji</span><span class="sxs-lookup"><span data-stu-id="920d5-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="920d5-112">To polecenie wyświetla dane metryczne dotyczące środowiska uruchomieniowego integracji o nazwie "test-selfhost-ir" w subskrypcji dla grupy zasobów o nazwach "rg-test-dfv2" i data factory o nazwie "test-df-eu2".</span><span class="sxs-lookup"><span data-stu-id="920d5-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="920d5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="920d5-113">PARAMETERS</span></span>

### <span data-ttu-id="920d5-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="920d5-114">-DataFactoryName</span></span>
<span data-ttu-id="920d5-115">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="920d5-115">The data factory name.</span></span>

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

### <span data-ttu-id="920d5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="920d5-116">-DefaultProfile</span></span>
<span data-ttu-id="920d5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="920d5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="920d5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="920d5-118">-InputObject</span></span>
<span data-ttu-id="920d5-119">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="920d5-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="920d5-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="920d5-120">-Name</span></span>
<span data-ttu-id="920d5-121">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="920d5-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="920d5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="920d5-122">-ResourceGroupName</span></span>
<span data-ttu-id="920d5-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="920d5-123">The resource group name.</span></span>

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

### <span data-ttu-id="920d5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="920d5-124">-ResourceId</span></span>
<span data-ttu-id="920d5-125">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="920d5-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="920d5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="920d5-126">CommonParameters</span></span>
<span data-ttu-id="920d5-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="920d5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="920d5-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="920d5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="920d5-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="920d5-129">INPUTS</span></span>

### <span data-ttu-id="920d5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="920d5-130">System.String</span></span>

### <span data-ttu-id="920d5-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="920d5-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="920d5-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="920d5-132">OUTPUTS</span></span>

### <span data-ttu-id="920d5-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="920d5-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="920d5-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="920d5-134">NOTES</span></span>

## <span data-ttu-id="920d5-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="920d5-135">RELATED LINKS</span></span>

[<span data-ttu-id="920d5-136">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="920d5-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

