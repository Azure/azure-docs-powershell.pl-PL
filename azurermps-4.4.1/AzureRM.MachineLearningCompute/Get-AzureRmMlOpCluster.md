---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: e37aff4f6f79a3aa0420c98811bc47b951bb4d3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549984"
---
# <span data-ttu-id="db39b-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="db39b-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="db39b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db39b-102">SYNOPSIS</span></span>
<span data-ttu-id="db39b-103">Pobiera obiekt klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="db39b-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db39b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db39b-104">SYNTAX</span></span>

```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db39b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="db39b-105">DESCRIPTION</span></span>
<span data-ttu-id="db39b-106">Pobiera obiekt klastra operationalization według nazwy lub według grupy zasobów lub abonamentu.</span><span class="sxs-lookup"><span data-stu-id="db39b-106">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="db39b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db39b-107">EXAMPLES</span></span>

### <span data-ttu-id="db39b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="db39b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="db39b-109">Pobiera określony klaster operationalization według nazwy.</span><span class="sxs-lookup"><span data-stu-id="db39b-109">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="db39b-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="db39b-110">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="db39b-111">Pobiera wszystkie klastry operationalization w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="db39b-111">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="db39b-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="db39b-112">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="db39b-113">Pobiera wszystkie klastry usługi operationalization w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="db39b-113">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="db39b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db39b-114">PARAMETERS</span></span>

### <span data-ttu-id="db39b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db39b-115">-DefaultProfile</span></span>
<span data-ttu-id="db39b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="db39b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db39b-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="db39b-117">-Name</span></span>
<span data-ttu-id="db39b-118">Nazwa klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="db39b-118">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get an operationalization cluster by its name.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db39b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db39b-119">-ResourceGroupName</span></span>
<span data-ttu-id="db39b-120">Nazwa grupy zasobów dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="db39b-120">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db39b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db39b-121">CommonParameters</span></span>
<span data-ttu-id="db39b-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db39b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db39b-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db39b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db39b-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db39b-124">INPUTS</span></span>

### <span data-ttu-id="db39b-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="db39b-125">None</span></span>

## <span data-ttu-id="db39b-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db39b-126">OUTPUTS</span></span>

### <span data-ttu-id="db39b-127">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="db39b-127">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="db39b-128">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. MachineLearningCompute. MODELES. PSOperationalizationCluster, Microsoft. Azure. Commands. MachineLearningCompute, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="db39b-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster, Microsoft.Azure.Commands.MachineLearningCompute, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="db39b-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db39b-129">NOTES</span></span>

## <span data-ttu-id="db39b-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db39b-130">RELATED LINKS</span></span>

