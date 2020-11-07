---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
ms.openlocfilehash: d8b8a333b4d009ee1b40a8b4ddc6ed49850f1a11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867543"
---
# <span data-ttu-id="de7fb-101">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="de7fb-101">Get-AzMlOpClusterKey</span></span>

## <span data-ttu-id="de7fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de7fb-102">SYNOPSIS</span></span>
<span data-ttu-id="de7fb-103">Pobiera klucze dostępu skojarzone z klastrem usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="de7fb-103">Gets the access keys associated with an operationalization cluster.</span></span>

## <span data-ttu-id="de7fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de7fb-104">SYNTAX</span></span>

### <span data-ttu-id="de7fb-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="de7fb-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de7fb-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="de7fb-106">GetByInputObject</span></span>
```
Get-AzMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de7fb-107">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="de7fb-107">GetByResourceId</span></span>
```
Get-AzMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de7fb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="de7fb-108">DESCRIPTION</span></span>
<span data-ttu-id="de7fb-109">Klucze dla konta magazynu, rejestru kontenera i innych usług skojarzonych z klastrem operationalization nie są zwracane podczas uzyskiwania właściwości klastra.</span><span class="sxs-lookup"><span data-stu-id="de7fb-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="de7fb-110">Należy wprowadzić określone połączenie, aby pobrać klucze, ponieważ są to informacje poufne.</span><span class="sxs-lookup"><span data-stu-id="de7fb-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="de7fb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de7fb-111">EXAMPLES</span></span>

### <span data-ttu-id="de7fb-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="de7fb-112">Example 1</span></span>
```
PS C:\> Get-AzMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="de7fb-113">Zwraca klucze tajne dla usług skojarzonych z klastrem operationalization.</span><span class="sxs-lookup"><span data-stu-id="de7fb-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="de7fb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de7fb-114">PARAMETERS</span></span>

### <span data-ttu-id="de7fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de7fb-115">-DefaultProfile</span></span>
<span data-ttu-id="de7fb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de7fb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de7fb-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="de7fb-117">-InputObject</span></span>
<span data-ttu-id="de7fb-118">Obiekt klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="de7fb-118">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: GetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de7fb-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="de7fb-119">-Name</span></span>
<span data-ttu-id="de7fb-120">Nazwa klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="de7fb-120">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de7fb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de7fb-121">-ResourceGroupName</span></span>
<span data-ttu-id="de7fb-122">Nazwa grupy zasobów dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="de7fb-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de7fb-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de7fb-123">-ResourceId</span></span>
<span data-ttu-id="de7fb-124">Identyfikator zasobu platformy Azure dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="de7fb-124">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de7fb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de7fb-125">CommonParameters</span></span>
<span data-ttu-id="de7fb-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de7fb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de7fb-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de7fb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de7fb-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de7fb-128">INPUTS</span></span>

### <span data-ttu-id="de7fb-129">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="de7fb-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="de7fb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="de7fb-130">System.String</span></span>

## <span data-ttu-id="de7fb-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de7fb-131">OUTPUTS</span></span>

### <span data-ttu-id="de7fb-132">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="de7fb-132">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="de7fb-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de7fb-133">NOTES</span></span>

## <span data-ttu-id="de7fb-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de7fb-134">RELATED LINKS</span></span>
