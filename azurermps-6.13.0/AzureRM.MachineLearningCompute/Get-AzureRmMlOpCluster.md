---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: 746dde8dd3460add5eb6a20e4a9b771873dac0e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545152"
---
# <span data-ttu-id="30fce-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="30fce-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="30fce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30fce-102">SYNOPSIS</span></span>
<span data-ttu-id="30fce-103">Pobiera obiekt klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="30fce-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30fce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30fce-104">SYNTAX</span></span>

### <span data-ttu-id="30fce-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="30fce-105">GetByName</span></span>
```
Get-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="30fce-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="30fce-106">GetByResourceGroup</span></span>
```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30fce-107">Opis</span><span class="sxs-lookup"><span data-stu-id="30fce-107">DESCRIPTION</span></span>
<span data-ttu-id="30fce-108">Pobiera obiekt klastra operationalization według nazwy lub według grupy zasobów lub abonamentu.</span><span class="sxs-lookup"><span data-stu-id="30fce-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="30fce-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30fce-109">EXAMPLES</span></span>

### <span data-ttu-id="30fce-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="30fce-110">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="30fce-111">Pobiera określony klaster operationalization według nazwy.</span><span class="sxs-lookup"><span data-stu-id="30fce-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="30fce-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="30fce-112">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="30fce-113">Pobiera wszystkie klastry operationalization w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="30fce-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="30fce-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="30fce-114">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="30fce-115">Pobiera wszystkie klastry usługi operationalization w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="30fce-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="30fce-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30fce-116">PARAMETERS</span></span>

### <span data-ttu-id="30fce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30fce-117">-DefaultProfile</span></span>
<span data-ttu-id="30fce-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="30fce-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30fce-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="30fce-119">-Name</span></span>
<span data-ttu-id="30fce-120">Nazwa klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="30fce-120">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30fce-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30fce-121">-ResourceGroupName</span></span>
<span data-ttu-id="30fce-122">Nazwa grupy zasobów dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="30fce-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30fce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30fce-123">CommonParameters</span></span>
<span data-ttu-id="30fce-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30fce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30fce-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30fce-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30fce-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30fce-126">INPUTS</span></span>

### <span data-ttu-id="30fce-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="30fce-127">None</span></span>

## <span data-ttu-id="30fce-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30fce-128">OUTPUTS</span></span>

### <span data-ttu-id="30fce-129">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="30fce-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="30fce-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30fce-130">NOTES</span></span>

## <span data-ttu-id="30fce-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30fce-131">RELATED LINKS</span></span>
