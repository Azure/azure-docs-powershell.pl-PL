---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 9b82d302bba1c2f51de3748fb9c335dd0db2699d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306270"
---
# <span data-ttu-id="acc4c-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="acc4c-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="acc4c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="acc4c-102">SYNOPSIS</span></span>
<span data-ttu-id="acc4c-103">Pobiera dane metryczne dla środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="acc4c-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="acc4c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="acc4c-104">SYNTAX</span></span>

### <span data-ttu-id="acc4c-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="acc4c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acc4c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="acc4c-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="acc4c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="acc4c-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acc4c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="acc4c-108">DESCRIPTION</span></span>
<span data-ttu-id="acc4c-109">Polecenie cmdlet Get-AzDataFactoryV2IntegrationRuntimeMetric pobiera dane metryczne dotyczące środowiska programu integracyjnego w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="acc4c-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="acc4c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="acc4c-110">EXAMPLES</span></span>

### <span data-ttu-id="acc4c-111">Przykład 1: uzyskiwanie metryki środowiska uruchomieniowego integracji</span><span class="sxs-lookup"><span data-stu-id="acc4c-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="acc4c-112">To polecenie wyświetla dane metryczne dotyczące środowiska wykonawczego integracji o nazwie "test-SelfHost-IR" w subskrypcji grupy zasobów o nazwie "RG-test-dfv2" i fabryki danych o nazwie "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="acc4c-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="acc4c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="acc4c-113">PARAMETERS</span></span>

### <span data-ttu-id="acc4c-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="acc4c-114">-DataFactoryName</span></span>
<span data-ttu-id="acc4c-115">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="acc4c-115">The data factory name.</span></span>

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

### <span data-ttu-id="acc4c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc4c-116">-DefaultProfile</span></span>
<span data-ttu-id="acc4c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="acc4c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acc4c-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="acc4c-118">-InputObject</span></span>
<span data-ttu-id="acc4c-119">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="acc4c-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="acc4c-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="acc4c-120">-Name</span></span>
<span data-ttu-id="acc4c-121">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="acc4c-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="acc4c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc4c-122">-ResourceGroupName</span></span>
<span data-ttu-id="acc4c-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="acc4c-123">The resource group name.</span></span>

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

### <span data-ttu-id="acc4c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acc4c-124">-ResourceId</span></span>
<span data-ttu-id="acc4c-125">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="acc4c-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="acc4c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc4c-126">CommonParameters</span></span>
<span data-ttu-id="acc4c-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acc4c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc4c-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acc4c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc4c-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="acc4c-129">INPUTS</span></span>

### <span data-ttu-id="acc4c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="acc4c-130">System.String</span></span>

### <span data-ttu-id="acc4c-131">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="acc4c-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="acc4c-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="acc4c-132">OUTPUTS</span></span>

### <span data-ttu-id="acc4c-133">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="acc4c-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="acc4c-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="acc4c-134">NOTES</span></span>

## <span data-ttu-id="acc4c-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="acc4c-135">RELATED LINKS</span></span>

[<span data-ttu-id="acc4c-136">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="acc4c-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

