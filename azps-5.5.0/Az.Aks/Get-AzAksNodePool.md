---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 5c690b377d658e3ebc4eddaf49d546efd503a01c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199874"
---
# <span data-ttu-id="123c2-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="123c2-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="123c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="123c2-102">SYNOPSIS</span></span>
<span data-ttu-id="123c2-103">Utwórz pulę notek w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="123c2-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="123c2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="123c2-104">SYNTAX</span></span>

### <span data-ttu-id="123c2-105">NameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="123c2-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="123c2-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="123c2-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="123c2-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="123c2-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="123c2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="123c2-108">DESCRIPTION</span></span>
<span data-ttu-id="123c2-109">Utwórz pulę notek w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="123c2-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="123c2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="123c2-110">EXAMPLES</span></span>

### <span data-ttu-id="123c2-111">Pobierz wszystkie pule węzła w określonym klastrze</span><span class="sxs-lookup"><span data-stu-id="123c2-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="123c2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="123c2-112">PARAMETERS</span></span>

### <span data-ttu-id="123c2-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="123c2-113">-ClusterName</span></span>
<span data-ttu-id="123c2-114">Nazwa zarządzanego zasobu klastrów.</span><span class="sxs-lookup"><span data-stu-id="123c2-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="123c2-115">- ClusterObject</span><span class="sxs-lookup"><span data-stu-id="123c2-115">-ClusterObject</span></span>
<span data-ttu-id="123c2-116">Obiekt klasterowy.</span><span class="sxs-lookup"><span data-stu-id="123c2-116">The cluster object.</span></span>

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

### <span data-ttu-id="123c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="123c2-117">-DefaultProfile</span></span>
<span data-ttu-id="123c2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="123c2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="123c2-119">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="123c2-119">-Id</span></span>
<span data-ttu-id="123c2-120">Identyfikator puli węzła w zarządzanym klastrze Kubernetes</span><span class="sxs-lookup"><span data-stu-id="123c2-120">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="123c2-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="123c2-121">-Name</span></span>
<span data-ttu-id="123c2-122">Nazwa puli węzła.</span><span class="sxs-lookup"><span data-stu-id="123c2-122">The name of the node pool.</span></span>

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

### <span data-ttu-id="123c2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="123c2-123">-ResourceGroupName</span></span>
<span data-ttu-id="123c2-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="123c2-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="123c2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="123c2-125">CommonParameters</span></span>
<span data-ttu-id="123c2-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="123c2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="123c2-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="123c2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="123c2-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="123c2-128">INPUTS</span></span>

### <span data-ttu-id="123c2-129">System.String</span><span class="sxs-lookup"><span data-stu-id="123c2-129">System.String</span></span>

## <span data-ttu-id="123c2-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="123c2-130">OUTPUTS</span></span>

### <span data-ttu-id="123c2-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="123c2-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="123c2-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="123c2-132">NOTES</span></span>

## <span data-ttu-id="123c2-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="123c2-133">RELATED LINKS</span></span>
