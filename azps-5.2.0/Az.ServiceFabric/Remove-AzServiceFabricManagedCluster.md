---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
ms.openlocfilehash: d676958948b9197a64a08646e837287299107bfa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343333"
---
# <span data-ttu-id="557e7-101">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="557e7-101">Remove-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="557e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="557e7-102">SYNOPSIS</span></span>
<span data-ttu-id="557e7-103">Usuń zasób klastra.</span><span class="sxs-lookup"><span data-stu-id="557e7-103">Remove cluster resource.</span></span>

## <span data-ttu-id="557e7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="557e7-104">SYNTAX</span></span>

### <span data-ttu-id="557e7-105">ByObj (domyślny)</span><span class="sxs-lookup"><span data-stu-id="557e7-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="557e7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="557e7-106">ByName</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="557e7-107">ById</span><span class="sxs-lookup"><span data-stu-id="557e7-107">ById</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="557e7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="557e7-108">DESCRIPTION</span></span>
<span data-ttu-id="557e7-109">Usuń klaster spowoduje to również usunięcie typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="557e7-109">Remove cluster this will remove the node types under the cluster too.</span></span>

## <span data-ttu-id="557e7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="557e7-110">EXAMPLES</span></span>

### <span data-ttu-id="557e7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="557e7-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedCluster -ResourceGroupName sfmcalsantamps -ClusterName sfmcalsantamps
```

<span data-ttu-id="557e7-112">Usuń klaster.</span><span class="sxs-lookup"><span data-stu-id="557e7-112">Remove cluster.</span></span>

### <span data-ttu-id="557e7-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="557e7-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedCluster
```

<span data-ttu-id="557e7-114">Usuń klaster z potokiem.</span><span class="sxs-lookup"><span data-stu-id="557e7-114">Remove cluster, with piping.</span></span>

## <span data-ttu-id="557e7-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="557e7-115">PARAMETERS</span></span>

### <span data-ttu-id="557e7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="557e7-116">-AsJob</span></span>
<span data-ttu-id="557e7-117">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="557e7-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="557e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="557e7-118">-DefaultProfile</span></span>
<span data-ttu-id="557e7-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="557e7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="557e7-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="557e7-120">-InputObject</span></span>
<span data-ttu-id="557e7-121">Zarządzany zasób klastra</span><span class="sxs-lookup"><span data-stu-id="557e7-121">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="557e7-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="557e7-122">-Name</span></span>
<span data-ttu-id="557e7-123">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="557e7-123">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="557e7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="557e7-124">-PassThru</span></span>
<span data-ttu-id="557e7-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="557e7-125">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="557e7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="557e7-126">-ResourceGroupName</span></span>
<span data-ttu-id="557e7-127">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="557e7-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="557e7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="557e7-128">-ResourceId</span></span>
<span data-ttu-id="557e7-129">Identyfikator zarządzanego zasobu klastra</span><span class="sxs-lookup"><span data-stu-id="557e7-129">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="557e7-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="557e7-130">-Confirm</span></span>
<span data-ttu-id="557e7-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="557e7-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="557e7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="557e7-132">-WhatIf</span></span>
<span data-ttu-id="557e7-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="557e7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="557e7-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="557e7-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="557e7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="557e7-135">CommonParameters</span></span>
<span data-ttu-id="557e7-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="557e7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="557e7-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="557e7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="557e7-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="557e7-138">INPUTS</span></span>

### <span data-ttu-id="557e7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="557e7-139">System.String</span></span>

## <span data-ttu-id="557e7-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="557e7-140">OUTPUTS</span></span>

### <span data-ttu-id="557e7-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="557e7-141">System.Boolean</span></span>

## <span data-ttu-id="557e7-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="557e7-142">NOTES</span></span>

## <span data-ttu-id="557e7-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="557e7-143">RELATED LINKS</span></span>
