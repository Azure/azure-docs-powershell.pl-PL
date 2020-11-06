---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: aba54b47a5d335bb4f6ef1fbbf7bef66fa694aaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527681"
---
# <span data-ttu-id="10af6-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="10af6-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="10af6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10af6-102">SYNOPSIS</span></span>
<span data-ttu-id="10af6-103">Pobiera dane metryczne dla środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="10af6-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10af6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10af6-104">SYNTAX</span></span>

### <span data-ttu-id="10af6-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="10af6-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10af6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="10af6-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10af6-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="10af6-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10af6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="10af6-108">DESCRIPTION</span></span>
<span data-ttu-id="10af6-109">Polecenie cmdlet Get-AzureRmDataFactoryV2IntegrationRuntimeMetric pobiera dane metryczne dotyczące środowiska programu integracyjnego w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="10af6-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="10af6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10af6-110">EXAMPLES</span></span>

### <span data-ttu-id="10af6-111">Przykład 1: uzyskiwanie metryki środowiska uruchomieniowego integracji</span><span class="sxs-lookup"><span data-stu-id="10af6-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="10af6-112">To polecenie wyświetla dane metryczne dotyczące środowiska wykonawczego integracji o nazwie "test-SelfHost-IR" w subskrypcji grupy zasobów o nazwie "RG-test-dfv2" i fabryki danych o nazwie "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="10af6-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="10af6-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10af6-113">PARAMETERS</span></span>

### <span data-ttu-id="10af6-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="10af6-114">-DataFactoryName</span></span>
<span data-ttu-id="10af6-115">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="10af6-115">The data factory name.</span></span>

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

### <span data-ttu-id="10af6-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="10af6-116">-InputObject</span></span>
<span data-ttu-id="10af6-117">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="10af6-117">The integration runtime object.</span></span>

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

### <span data-ttu-id="10af6-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="10af6-118">-Name</span></span>
<span data-ttu-id="10af6-119">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="10af6-119">The integration runtime name.</span></span>

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

### <span data-ttu-id="10af6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10af6-120">-ResourceGroupName</span></span>
<span data-ttu-id="10af6-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="10af6-121">The resource group name.</span></span>

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

### <span data-ttu-id="10af6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10af6-122">-ResourceId</span></span>
<span data-ttu-id="10af6-123">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="10af6-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="10af6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10af6-124">-DefaultProfile</span></span>
<span data-ttu-id="10af6-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="10af6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10af6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10af6-126">CommonParameters</span></span>
<span data-ttu-id="10af6-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10af6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10af6-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10af6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10af6-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10af6-129">INPUTS</span></span>

### <span data-ttu-id="10af6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="10af6-130">System.String</span></span>
<span data-ttu-id="10af6-131">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="10af6-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="10af6-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10af6-132">OUTPUTS</span></span>

### <span data-ttu-id="10af6-133">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="10af6-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="10af6-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10af6-134">NOTES</span></span>

## <span data-ttu-id="10af6-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10af6-135">RELATED LINKS</span></span>

[<span data-ttu-id="10af6-136">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="10af6-136">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

