---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: 0e9eecf16a26be5367df5d8ad8b45a40e0050da3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717110"
---
# <span data-ttu-id="376ce-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="376ce-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="376ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="376ce-102">SYNOPSIS</span></span>
<span data-ttu-id="376ce-103">Pobiera obiekt klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="376ce-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="376ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="376ce-104">SYNTAX</span></span>

### <span data-ttu-id="376ce-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="376ce-105">GetByName</span></span>
```
Get-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="376ce-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="376ce-106">GetByResourceGroup</span></span>
```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="376ce-107">Opis</span><span class="sxs-lookup"><span data-stu-id="376ce-107">DESCRIPTION</span></span>
<span data-ttu-id="376ce-108">Pobiera obiekt klastra operationalization według nazwy lub według grupy zasobów lub abonamentu.</span><span class="sxs-lookup"><span data-stu-id="376ce-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="376ce-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="376ce-109">EXAMPLES</span></span>

### <span data-ttu-id="376ce-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="376ce-110">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="376ce-111">Pobiera określony klaster operationalization według nazwy.</span><span class="sxs-lookup"><span data-stu-id="376ce-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="376ce-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="376ce-112">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="376ce-113">Pobiera wszystkie klastry operationalization w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="376ce-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="376ce-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="376ce-114">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="376ce-115">Pobiera wszystkie klastry usługi operationalization w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="376ce-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="376ce-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="376ce-116">PARAMETERS</span></span>

### <span data-ttu-id="376ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="376ce-117">-DefaultProfile</span></span>
<span data-ttu-id="376ce-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="376ce-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="376ce-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="376ce-119">-Name</span></span>
<span data-ttu-id="376ce-120">Nazwa klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="376ce-120">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="376ce-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="376ce-121">-ResourceGroupName</span></span>
<span data-ttu-id="376ce-122">Nazwa grupy zasobów dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="376ce-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="376ce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="376ce-123">CommonParameters</span></span>
<span data-ttu-id="376ce-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="376ce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="376ce-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="376ce-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="376ce-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="376ce-126">INPUTS</span></span>

### <span data-ttu-id="376ce-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="376ce-127">None</span></span>

## <span data-ttu-id="376ce-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="376ce-128">OUTPUTS</span></span>

### <span data-ttu-id="376ce-129">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="376ce-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="376ce-130">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. MachineLearningCompute. MODELES. PSOperationalizationCluster, Microsoft. Azure. Commands. MachineLearningCompute, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="376ce-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster, Microsoft.Azure.Commands.MachineLearningCompute, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="376ce-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="376ce-131">NOTES</span></span>

## <span data-ttu-id="376ce-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="376ce-132">RELATED LINKS</span></span>

