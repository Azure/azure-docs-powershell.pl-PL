---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
ms.openlocfilehash: f2ed1813859f92624696eef7fa4f881f3eba1628
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498162"
---
# <span data-ttu-id="605b9-101">New-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="605b9-101">New-AzVMWareCluster</span></span>

## <span data-ttu-id="605b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="605b9-102">SYNOPSIS</span></span>
<span data-ttu-id="605b9-103">Tworzenie lub aktualizowanie klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="605b9-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="605b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="605b9-104">SYNTAX</span></span>

```
New-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -ClusterSize <Int32>
 -SkuName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="605b9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="605b9-105">DESCRIPTION</span></span>
<span data-ttu-id="605b9-106">Tworzenie lub aktualizowanie klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="605b9-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="605b9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="605b9-107">EXAMPLES</span></span>

### <span data-ttu-id="605b9-108">Przykład 1: Tworzenie klastra</span><span class="sxs-lookup"><span data-stu-id="605b9-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="605b9-109">Utwórz klaster</span><span class="sxs-lookup"><span data-stu-id="605b9-109">Create cluster</span></span>

## <span data-ttu-id="605b9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="605b9-110">PARAMETERS</span></span>

### <span data-ttu-id="605b9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="605b9-111">-AsJob</span></span>
<span data-ttu-id="605b9-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="605b9-112">Run the command as a job</span></span>

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

### <span data-ttu-id="605b9-113">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="605b9-113">-ClusterSize</span></span>
<span data-ttu-id="605b9-114">Rozmiar klastra</span><span class="sxs-lookup"><span data-stu-id="605b9-114">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="605b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="605b9-115">-DefaultProfile</span></span>
<span data-ttu-id="605b9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="605b9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="605b9-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="605b9-117">-Name</span></span>
<span data-ttu-id="605b9-118">Nazwa klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="605b9-118">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="605b9-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="605b9-119">-NoWait</span></span>
<span data-ttu-id="605b9-120">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="605b9-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="605b9-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="605b9-121">-PrivateCloudName</span></span>
<span data-ttu-id="605b9-122">Nazwa prywatnej chmury.</span><span class="sxs-lookup"><span data-stu-id="605b9-122">The name of the private cloud.</span></span>

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

### <span data-ttu-id="605b9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="605b9-123">-ResourceGroupName</span></span>
<span data-ttu-id="605b9-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="605b9-124">The name of the resource group.</span></span>
<span data-ttu-id="605b9-125">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="605b9-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="605b9-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="605b9-126">-SkuName</span></span>
<span data-ttu-id="605b9-127">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="605b9-127">The name of the SKU.</span></span>

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

### <span data-ttu-id="605b9-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="605b9-128">-SubscriptionId</span></span>
<span data-ttu-id="605b9-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="605b9-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="605b9-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="605b9-130">-Confirm</span></span>
<span data-ttu-id="605b9-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="605b9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="605b9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="605b9-132">-WhatIf</span></span>
<span data-ttu-id="605b9-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="605b9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="605b9-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="605b9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="605b9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="605b9-135">CommonParameters</span></span>
<span data-ttu-id="605b9-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="605b9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="605b9-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="605b9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="605b9-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="605b9-138">INPUTS</span></span>

## <span data-ttu-id="605b9-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="605b9-139">OUTPUTS</span></span>

### <span data-ttu-id="605b9-140">Microsoft. Azure. PowerShell. cmdlet. VMWare. modele. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="605b9-140">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="605b9-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="605b9-141">NOTES</span></span>

<span data-ttu-id="605b9-142">PISUJE</span><span class="sxs-lookup"><span data-stu-id="605b9-142">ALIASES</span></span>

## <span data-ttu-id="605b9-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="605b9-143">RELATED LINKS</span></span>

