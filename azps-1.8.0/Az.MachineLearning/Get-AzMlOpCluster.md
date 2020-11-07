---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
ms.openlocfilehash: 24400b7a2c882cef81d818c5f5b94fca4235ec83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867548"
---
# <span data-ttu-id="3a90f-101">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="3a90f-101">Get-AzMlOpCluster</span></span>

## <span data-ttu-id="3a90f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a90f-102">SYNOPSIS</span></span>
<span data-ttu-id="3a90f-103">Pobiera obiekt klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="3a90f-103">Gets an operationalization cluster object.</span></span>

## <span data-ttu-id="3a90f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a90f-104">SYNTAX</span></span>

### <span data-ttu-id="3a90f-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="3a90f-105">GetByName</span></span>
```
Get-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a90f-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3a90f-106">GetByResourceGroup</span></span>
```
Get-AzMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a90f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3a90f-107">DESCRIPTION</span></span>
<span data-ttu-id="3a90f-108">Pobiera obiekt klastra operationalization według nazwy lub według grupy zasobów lub abonamentu.</span><span class="sxs-lookup"><span data-stu-id="3a90f-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="3a90f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a90f-109">EXAMPLES</span></span>

### <span data-ttu-id="3a90f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3a90f-110">Example 1</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="3a90f-111">Pobiera określony klaster operationalization według nazwy.</span><span class="sxs-lookup"><span data-stu-id="3a90f-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="3a90f-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3a90f-112">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="3a90f-113">Pobiera wszystkie klastry operationalization w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a90f-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="3a90f-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="3a90f-114">Example 3</span></span>
```
PS C:\> Get-AzMlOpCluster
```

<span data-ttu-id="3a90f-115">Pobiera wszystkie klastry usługi operationalization w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3a90f-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="3a90f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a90f-116">PARAMETERS</span></span>

### <span data-ttu-id="3a90f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a90f-117">-DefaultProfile</span></span>
<span data-ttu-id="3a90f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a90f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a90f-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a90f-119">-Name</span></span>
<span data-ttu-id="3a90f-120">Nazwa klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="3a90f-120">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="3a90f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a90f-121">-ResourceGroupName</span></span>
<span data-ttu-id="3a90f-122">Nazwa grupy zasobów dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="3a90f-122">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="3a90f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a90f-123">CommonParameters</span></span>
<span data-ttu-id="3a90f-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a90f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a90f-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a90f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a90f-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a90f-126">INPUTS</span></span>

### <span data-ttu-id="3a90f-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3a90f-127">None</span></span>

## <span data-ttu-id="3a90f-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a90f-128">OUTPUTS</span></span>

### <span data-ttu-id="3a90f-129">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="3a90f-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="3a90f-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a90f-130">NOTES</span></span>

## <span data-ttu-id="3a90f-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a90f-131">RELATED LINKS</span></span>
