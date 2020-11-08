---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
ms.openlocfilehash: f2ed1813859f92624696eef7fa4f881f3eba1628
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221430"
---
# <span data-ttu-id="a730a-101">New-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="a730a-101">New-AzVMWareCluster</span></span>

## <span data-ttu-id="a730a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a730a-102">SYNOPSIS</span></span>
<span data-ttu-id="a730a-103">Tworzenie lub aktualizowanie klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="a730a-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="a730a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a730a-104">SYNTAX</span></span>

```
New-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -ClusterSize <Int32>
 -SkuName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a730a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a730a-105">DESCRIPTION</span></span>
<span data-ttu-id="a730a-106">Tworzenie lub aktualizowanie klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="a730a-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="a730a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a730a-107">EXAMPLES</span></span>

### <span data-ttu-id="a730a-108">Przykład 1: Tworzenie klastra</span><span class="sxs-lookup"><span data-stu-id="a730a-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="a730a-109">Utwórz klaster</span><span class="sxs-lookup"><span data-stu-id="a730a-109">Create cluster</span></span>

## <span data-ttu-id="a730a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a730a-110">PARAMETERS</span></span>

### <span data-ttu-id="a730a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a730a-111">-AsJob</span></span>
<span data-ttu-id="a730a-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="a730a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a730a-113">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="a730a-113">-ClusterSize</span></span>
<span data-ttu-id="a730a-114">Rozmiar klastra</span><span class="sxs-lookup"><span data-stu-id="a730a-114">The cluster size</span></span>

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

### <span data-ttu-id="a730a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a730a-115">-DefaultProfile</span></span>
<span data-ttu-id="a730a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a730a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a730a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a730a-117">-Name</span></span>
<span data-ttu-id="a730a-118">Nazwa klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="a730a-118">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="a730a-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a730a-119">-NoWait</span></span>
<span data-ttu-id="a730a-120">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="a730a-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a730a-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="a730a-121">-PrivateCloudName</span></span>
<span data-ttu-id="a730a-122">Nazwa prywatnej chmury.</span><span class="sxs-lookup"><span data-stu-id="a730a-122">The name of the private cloud.</span></span>

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

### <span data-ttu-id="a730a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a730a-123">-ResourceGroupName</span></span>
<span data-ttu-id="a730a-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a730a-124">The name of the resource group.</span></span>
<span data-ttu-id="a730a-125">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="a730a-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a730a-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a730a-126">-SkuName</span></span>
<span data-ttu-id="a730a-127">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="a730a-127">The name of the SKU.</span></span>

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

### <span data-ttu-id="a730a-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a730a-128">-SubscriptionId</span></span>
<span data-ttu-id="a730a-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="a730a-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a730a-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a730a-130">-Confirm</span></span>
<span data-ttu-id="a730a-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a730a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a730a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a730a-132">-WhatIf</span></span>
<span data-ttu-id="a730a-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a730a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a730a-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a730a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a730a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a730a-135">CommonParameters</span></span>
<span data-ttu-id="a730a-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a730a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a730a-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a730a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a730a-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a730a-138">INPUTS</span></span>

## <span data-ttu-id="a730a-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a730a-139">OUTPUTS</span></span>

### <span data-ttu-id="a730a-140">Microsoft. Azure. PowerShell. cmdlet. VMWare. modele. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="a730a-140">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="a730a-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a730a-141">NOTES</span></span>

<span data-ttu-id="a730a-142">PISUJE</span><span class="sxs-lookup"><span data-stu-id="a730a-142">ALIASES</span></span>

## <span data-ttu-id="a730a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a730a-143">RELATED LINKS</span></span>

