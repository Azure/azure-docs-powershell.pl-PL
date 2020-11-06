---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 6b5797d67b709e9c44756dad018a47eb416ed174
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545151"
---
# <span data-ttu-id="8e0ec-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="8e0ec-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="8e0ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e0ec-102">SYNOPSIS</span></span>
<span data-ttu-id="8e0ec-103">Pobiera klucze dostępu skojarzone z klastrem usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="8e0ec-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e0ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e0ec-104">SYNTAX</span></span>

### <span data-ttu-id="8e0ec-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8e0ec-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e0ec-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="8e0ec-106">GetByInputObject</span></span>
```
Get-AzureRmMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e0ec-107">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e0ec-107">GetByResourceId</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e0ec-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8e0ec-108">DESCRIPTION</span></span>
<span data-ttu-id="8e0ec-109">Klucze dla konta magazynu, rejestru kontenera i innych usług skojarzonych z klastrem operationalization nie są zwracane podczas uzyskiwania właściwości klastra.</span><span class="sxs-lookup"><span data-stu-id="8e0ec-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="8e0ec-110">Należy wprowadzić określone połączenie, aby pobrać klucze, ponieważ są to informacje poufne.</span><span class="sxs-lookup"><span data-stu-id="8e0ec-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="8e0ec-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e0ec-111">EXAMPLES</span></span>

### <span data-ttu-id="8e0ec-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8e0ec-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="8e0ec-113">Zwraca klucze tajne dla usług skojarzonych z klastrem operationalization.</span><span class="sxs-lookup"><span data-stu-id="8e0ec-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="8e0ec-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e0ec-114">PARAMETERS</span></span>

### <span data-ttu-id="8e0ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e0ec-115">-DefaultProfile</span></span>
<span data-ttu-id="8e0ec-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e0ec-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e0ec-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8e0ec-117">-InputObject</span></span>
<span data-ttu-id="8e0ec-118">Obiekt klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="8e0ec-118">The operationalization cluster object.</span></span>

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

### <span data-ttu-id="8e0ec-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8e0ec-119">-Name</span></span>
<span data-ttu-id="8e0ec-120">Nazwa klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="8e0ec-120">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="8e0ec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e0ec-121">-ResourceGroupName</span></span>
<span data-ttu-id="8e0ec-122">Nazwa grupy zasobów dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="8e0ec-122">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="8e0ec-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e0ec-123">-ResourceId</span></span>
<span data-ttu-id="8e0ec-124">Identyfikator zasobu platformy Azure dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="8e0ec-124">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="8e0ec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e0ec-125">CommonParameters</span></span>
<span data-ttu-id="8e0ec-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e0ec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e0ec-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e0ec-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e0ec-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e0ec-128">INPUTS</span></span>

### <span data-ttu-id="8e0ec-129">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="8e0ec-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="8e0ec-130">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8e0ec-130">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="8e0ec-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8e0ec-131">System.String</span></span>

## <span data-ttu-id="8e0ec-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e0ec-132">OUTPUTS</span></span>

### <span data-ttu-id="8e0ec-133">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="8e0ec-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="8e0ec-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e0ec-134">NOTES</span></span>

## <span data-ttu-id="8e0ec-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e0ec-135">RELATED LINKS</span></span>
