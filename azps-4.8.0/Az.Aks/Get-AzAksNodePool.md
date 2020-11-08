---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 5c690b377d658e3ebc4eddaf49d546efd503a01c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222379"
---
# <span data-ttu-id="48a59-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="48a59-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="48a59-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48a59-102">SYNOPSIS</span></span>
<span data-ttu-id="48a59-103">Tworzenie puli notatek w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="48a59-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="48a59-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48a59-104">SYNTAX</span></span>

### <span data-ttu-id="48a59-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="48a59-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48a59-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48a59-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48a59-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48a59-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48a59-108">Opis</span><span class="sxs-lookup"><span data-stu-id="48a59-108">DESCRIPTION</span></span>
<span data-ttu-id="48a59-109">Tworzenie puli notatek w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="48a59-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="48a59-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48a59-110">EXAMPLES</span></span>

### <span data-ttu-id="48a59-111">Pobieranie wszystkich pul węzłów w określonym klastrze</span><span class="sxs-lookup"><span data-stu-id="48a59-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="48a59-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48a59-112">PARAMETERS</span></span>

### <span data-ttu-id="48a59-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="48a59-113">-ClusterName</span></span>
<span data-ttu-id="48a59-114">Nazwa zarządzanego zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="48a59-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48a59-115">-Clusterobject</span><span class="sxs-lookup"><span data-stu-id="48a59-115">-ClusterObject</span></span>
<span data-ttu-id="48a59-116">Obiekt klastra.</span><span class="sxs-lookup"><span data-stu-id="48a59-116">The cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48a59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48a59-117">-DefaultProfile</span></span>
<span data-ttu-id="48a59-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="48a59-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48a59-119">-ID</span><span class="sxs-lookup"><span data-stu-id="48a59-119">-Id</span></span>
<span data-ttu-id="48a59-120">Identyfikator puli węzłów w klastrze zarządzanych Kubernetes</span><span class="sxs-lookup"><span data-stu-id="48a59-120">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48a59-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="48a59-121">-Name</span></span>
<span data-ttu-id="48a59-122">Nazwa puli węzłów.</span><span class="sxs-lookup"><span data-stu-id="48a59-122">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48a59-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48a59-123">-ResourceGroupName</span></span>
<span data-ttu-id="48a59-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="48a59-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48a59-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48a59-125">CommonParameters</span></span>
<span data-ttu-id="48a59-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48a59-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48a59-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48a59-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48a59-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48a59-128">INPUTS</span></span>

### <span data-ttu-id="48a59-129">System. String</span><span class="sxs-lookup"><span data-stu-id="48a59-129">System.String</span></span>

## <span data-ttu-id="48a59-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48a59-130">OUTPUTS</span></span>

### <span data-ttu-id="48a59-131">Microsoft. Azure. Commands. AKS. models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="48a59-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="48a59-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48a59-132">NOTES</span></span>

## <span data-ttu-id="48a59-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48a59-133">RELATED LINKS</span></span>
