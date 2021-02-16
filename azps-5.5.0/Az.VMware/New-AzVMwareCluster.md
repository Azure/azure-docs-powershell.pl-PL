---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
ms.openlocfilehash: d654b2fa012a793ce48dff2cc5bfb9ade4f99d34
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182546"
---
# <span data-ttu-id="ea989-101">New-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="ea989-101">New-AzVMwareCluster</span></span>

## <span data-ttu-id="ea989-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea989-102">SYNOPSIS</span></span>
<span data-ttu-id="ea989-103">Tworzenie lub aktualizowanie klastrów w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="ea989-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="ea989-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ea989-104">SYNTAX</span></span>

```
New-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -SkuName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ea989-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ea989-105">DESCRIPTION</span></span>
<span data-ttu-id="ea989-106">Tworzenie lub aktualizowanie klastrów w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="ea989-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="ea989-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ea989-107">EXAMPLES</span></span>

### <span data-ttu-id="ea989-108">Przykład 1. Tworzenie klastrów</span><span class="sxs-lookup"><span data-stu-id="ea989-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="ea989-109">Tworzenie klastrów</span><span class="sxs-lookup"><span data-stu-id="ea989-109">Create cluster</span></span>

## <span data-ttu-id="ea989-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea989-110">PARAMETERS</span></span>

### <span data-ttu-id="ea989-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ea989-111">-AsJob</span></span>
<span data-ttu-id="ea989-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="ea989-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ea989-113">- ClusterSize</span><span class="sxs-lookup"><span data-stu-id="ea989-113">-ClusterSize</span></span>
<span data-ttu-id="ea989-114">Rozmiar klastrów</span><span class="sxs-lookup"><span data-stu-id="ea989-114">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea989-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea989-115">-DefaultProfile</span></span>
<span data-ttu-id="ea989-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea989-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea989-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ea989-117">-Name</span></span>
<span data-ttu-id="ea989-118">Nazwa klastra w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="ea989-118">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea989-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ea989-119">-NoWait</span></span>
<span data-ttu-id="ea989-120">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="ea989-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ea989-121">- PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="ea989-121">-PrivateCloudName</span></span>
<span data-ttu-id="ea989-122">Nazwa chmury prywatnej.</span><span class="sxs-lookup"><span data-stu-id="ea989-122">The name of the private cloud.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea989-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea989-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea989-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea989-124">The name of the resource group.</span></span>
<span data-ttu-id="ea989-125">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="ea989-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea989-126">-SKUName</span><span class="sxs-lookup"><span data-stu-id="ea989-126">-SkuName</span></span>
<span data-ttu-id="ea989-127">Nazwa sku.</span><span class="sxs-lookup"><span data-stu-id="ea989-127">The name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea989-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea989-128">-SubscriptionId</span></span>
<span data-ttu-id="ea989-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ea989-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea989-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea989-130">-Confirm</span></span>
<span data-ttu-id="ea989-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ea989-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea989-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea989-132">-WhatIf</span></span>
<span data-ttu-id="ea989-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea989-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea989-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ea989-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea989-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea989-135">CommonParameters</span></span>
<span data-ttu-id="ea989-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea989-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea989-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea989-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea989-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea989-138">INPUTS</span></span>

## <span data-ttu-id="ea989-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ea989-139">OUTPUTS</span></span>

### <span data-ttu-id="ea989-140">Microsoft.Azure.PowerShell.Cmdlet.VCmdlet.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="ea989-140">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="ea989-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ea989-141">NOTES</span></span>

<span data-ttu-id="ea989-142">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ea989-142">ALIASES</span></span>

## <span data-ttu-id="ea989-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea989-143">RELATED LINKS</span></span>

