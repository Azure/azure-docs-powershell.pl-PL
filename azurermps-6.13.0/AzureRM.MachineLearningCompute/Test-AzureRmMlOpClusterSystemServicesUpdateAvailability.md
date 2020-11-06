---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/test-azurermmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 9832faaaaf1097f53aff841f8a455680b2a40a2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545143"
---
# <span data-ttu-id="77d3c-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="77d3c-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="77d3c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77d3c-102">SYNOPSIS</span></span>
<span data-ttu-id="77d3c-103">Sprawdza, czy są dostępne aktualizacje dla usług systemowych skojarzonych z klastrem usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="77d3c-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77d3c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77d3c-104">SYNTAX</span></span>

### <span data-ttu-id="77d3c-105">TestByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="77d3c-105">TestByNameAndResourceGroup</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77d3c-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="77d3c-106">TestByInputObject</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77d3c-107">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="77d3c-107">TestByResourceId</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77d3c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="77d3c-108">DESCRIPTION</span></span>
<span data-ttu-id="77d3c-109">Usługi systemowe odbierają aktualizacje niezależnie od klastra programu operationalization.</span><span class="sxs-lookup"><span data-stu-id="77d3c-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="77d3c-110">Użycie tego polecenia cmdlet umożliwi użytkownikowi zapoznanie się z informacją, czy funkcja Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span><span class="sxs-lookup"><span data-stu-id="77d3c-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="77d3c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77d3c-111">EXAMPLES</span></span>

### <span data-ttu-id="77d3c-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77d3c-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="77d3c-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="77d3c-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="77d3c-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="77d3c-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="77d3c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77d3c-115">PARAMETERS</span></span>

### <span data-ttu-id="77d3c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77d3c-116">-DefaultProfile</span></span>
<span data-ttu-id="77d3c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77d3c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77d3c-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="77d3c-118">-InputObject</span></span>
<span data-ttu-id="77d3c-119">Obiekt klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="77d3c-119">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: TestByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77d3c-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77d3c-120">-Name</span></span>
<span data-ttu-id="77d3c-121">Nazwa klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="77d3c-121">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77d3c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77d3c-122">-ResourceGroupName</span></span>
<span data-ttu-id="77d3c-123">Nazwa grupy zasobów dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="77d3c-123">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77d3c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77d3c-124">-ResourceId</span></span>
<span data-ttu-id="77d3c-125">Identyfikator zasobu platformy Azure dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="77d3c-125">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77d3c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77d3c-126">CommonParameters</span></span>
<span data-ttu-id="77d3c-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77d3c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77d3c-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77d3c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77d3c-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77d3c-129">INPUTS</span></span>

### <span data-ttu-id="77d3c-130">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="77d3c-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="77d3c-131">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="77d3c-131">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="77d3c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="77d3c-132">System.String</span></span>

## <span data-ttu-id="77d3c-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77d3c-133">OUTPUTS</span></span>

### <span data-ttu-id="77d3c-134">Microsoft. Azure. Commands. MachineLearningCompute. models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="77d3c-134">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="77d3c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77d3c-135">NOTES</span></span>

## <span data-ttu-id="77d3c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77d3c-136">RELATED LINKS</span></span>
