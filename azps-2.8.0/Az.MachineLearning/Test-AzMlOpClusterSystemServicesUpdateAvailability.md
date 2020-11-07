---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/test-azmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Test-AzMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Test-AzMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: d05f8b746dbd212c834e3554639340fa6075c216
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704922"
---
# <span data-ttu-id="2fbd0-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="2fbd0-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="2fbd0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2fbd0-102">SYNOPSIS</span></span>
<span data-ttu-id="2fbd0-103">Sprawdza, czy są dostępne aktualizacje dla usług systemowych skojarzonych z klastrem usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="2fbd0-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

## <span data-ttu-id="2fbd0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2fbd0-104">SYNTAX</span></span>

### <span data-ttu-id="2fbd0-105">TestByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2fbd0-105">TestByNameAndResourceGroup</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fbd0-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="2fbd0-106">TestByInputObject</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fbd0-107">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="2fbd0-107">TestByResourceId</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fbd0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2fbd0-108">DESCRIPTION</span></span>
<span data-ttu-id="2fbd0-109">Usługi systemowe odbierają aktualizacje niezależnie od klastra programu operationalization.</span><span class="sxs-lookup"><span data-stu-id="2fbd0-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="2fbd0-110">Użycie tego polecenia cmdlet umożliwi użytkownikowi zapoznanie się z informacją, czy funkcja Invoke-AzMlOpClusterSystemServicesUpdate.</span><span class="sxs-lookup"><span data-stu-id="2fbd0-110">Using this cmdlet will let the user know if Invoke-AzMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="2fbd0-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2fbd0-111">EXAMPLES</span></span>

### <span data-ttu-id="2fbd0-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2fbd0-112">Example 1</span></span>
```
PS C:\> Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="2fbd0-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2fbd0-113">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="2fbd0-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="2fbd0-114">Example 3</span></span>
```
PS C:\> Find-AzResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="2fbd0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2fbd0-115">PARAMETERS</span></span>

### <span data-ttu-id="2fbd0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fbd0-116">-DefaultProfile</span></span>
<span data-ttu-id="2fbd0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2fbd0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fbd0-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2fbd0-118">-InputObject</span></span>
<span data-ttu-id="2fbd0-119">Obiekt klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="2fbd0-119">The operationalization cluster object.</span></span>

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

### <span data-ttu-id="2fbd0-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2fbd0-120">-Name</span></span>
<span data-ttu-id="2fbd0-121">Nazwa klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="2fbd0-121">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="2fbd0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fbd0-122">-ResourceGroupName</span></span>
<span data-ttu-id="2fbd0-123">Nazwa grupy zasobów dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="2fbd0-123">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="2fbd0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fbd0-124">-ResourceId</span></span>
<span data-ttu-id="2fbd0-125">Identyfikator zasobu platformy Azure dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="2fbd0-125">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="2fbd0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fbd0-126">CommonParameters</span></span>
<span data-ttu-id="2fbd0-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fbd0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fbd0-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fbd0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fbd0-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fbd0-129">INPUTS</span></span>

### <span data-ttu-id="2fbd0-130">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="2fbd0-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="2fbd0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2fbd0-131">System.String</span></span>

## <span data-ttu-id="2fbd0-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2fbd0-132">OUTPUTS</span></span>

### <span data-ttu-id="2fbd0-133">Microsoft. Azure. Commands. MachineLearningCompute. models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="2fbd0-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="2fbd0-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2fbd0-134">NOTES</span></span>

## <span data-ttu-id="2fbd0-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2fbd0-135">RELATED LINKS</span></span>
