---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 4636dc8f8c8efdf9dae5f7d2094fd3432528f043
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197810"
---
# <span data-ttu-id="49e54-101">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="49e54-101">Set-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="49e54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49e54-102">SYNOPSIS</span></span>
<span data-ttu-id="49e54-103">Ustawianie właściwości zasobów klastrów.</span><span class="sxs-lookup"><span data-stu-id="49e54-103">Set cluster resource properties.</span></span>

## <span data-ttu-id="49e54-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="49e54-104">SYNTAX</span></span>

### <span data-ttu-id="49e54-105">ByObj (Domyślnie)</span><span class="sxs-lookup"><span data-stu-id="49e54-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49e54-106">WithErmsByName</span><span class="sxs-lookup"><span data-stu-id="49e54-106">WithPramsByName</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>]
 [-ClientConnectionPort <Int32>] [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49e54-107">ByNameById</span><span class="sxs-lookup"><span data-stu-id="49e54-107">ByNameById</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceId] <String> [-UpgradeMode <ClusterUpgradeMode>]
 [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49e54-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="49e54-108">DESCRIPTION</span></span>
<span data-ttu-id="49e54-109">Ustawianie właściwości zasobów klastrów.</span><span class="sxs-lookup"><span data-stu-id="49e54-109">Set cluster resource properties.</span></span>

## <span data-ttu-id="49e54-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="49e54-110">EXAMPLES</span></span>

### <span data-ttu-id="49e54-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="49e54-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Update-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName -DnsName testnewdns -ClientConnectionPort 50000 -Verbose
```

<span data-ttu-id="49e54-112">Zaktualizuj nazwę DNS i port połączenia klienta dla klastra.</span><span class="sxs-lookup"><span data-stu-id="49e54-112">Update dns name and client connection port for the cluster.</span></span>

### <span data-ttu-id="49e54-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="49e54-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster.DnsName = "testnewdns"
$cluster.ClientConnectionPort = 50000
$cluster | Set-AzServiceFabricManagedCluster
```

<span data-ttu-id="49e54-114">Aktualizowanie portu połączenia dns i połączenia klienta dla klastrów za pomocą połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="49e54-114">Update dns name and client connection port for the cluster, with piping.</span></span>

## <span data-ttu-id="49e54-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49e54-115">PARAMETERS</span></span>

### <span data-ttu-id="49e54-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="49e54-116">-AsJob</span></span>
<span data-ttu-id="49e54-117">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="49e54-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="49e54-118">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="49e54-118">-ClientConnectionPort</span></span>
<span data-ttu-id="49e54-119">Port używany do obsługi połączeń klienta z klastrem.</span><span class="sxs-lookup"><span data-stu-id="49e54-119">Port used for client connections to the cluster.</span></span> <span data-ttu-id="49e54-120">Wartość domyślna: 19000.</span><span class="sxs-lookup"><span data-stu-id="49e54-120">Default: 19000.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e54-121">- CodeVersion</span><span class="sxs-lookup"><span data-stu-id="49e54-121">-CodeVersion</span></span>
<span data-ttu-id="49e54-122">Wersja kodu klastrowego.</span><span class="sxs-lookup"><span data-stu-id="49e54-122">Cluster code version.</span></span> <span data-ttu-id="49e54-123">Użyj tylko wtedy, gdy tryb uaktualniania jest ręczny.</span><span class="sxs-lookup"><span data-stu-id="49e54-123">Only use if upgrade mode is Manual.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e54-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49e54-124">-DefaultProfile</span></span>
<span data-ttu-id="49e54-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="49e54-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49e54-126">-DnsName</span><span class="sxs-lookup"><span data-stu-id="49e54-126">-DnsName</span></span>
<span data-ttu-id="49e54-127">Nazwa DNS klastrów.</span><span class="sxs-lookup"><span data-stu-id="49e54-127">Cluster's dns name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e54-128">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="49e54-128">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="49e54-129">Port używany na połączeniach http z klastrem.</span><span class="sxs-lookup"><span data-stu-id="49e54-129">Port used for http connections to the cluster.</span></span> <span data-ttu-id="49e54-130">Domyślne: 19080.</span><span class="sxs-lookup"><span data-stu-id="49e54-130">Default: 19080.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e54-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49e54-131">-InputObject</span></span>
<span data-ttu-id="49e54-132">Zasób zarządzany klastrów</span><span class="sxs-lookup"><span data-stu-id="49e54-132">Managed Cluster resource</span></span>

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

### <span data-ttu-id="49e54-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="49e54-133">-Name</span></span>
<span data-ttu-id="49e54-134">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="49e54-134">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49e54-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49e54-135">-ResourceGroupName</span></span>
<span data-ttu-id="49e54-136">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="49e54-136">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49e54-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49e54-137">-ResourceId</span></span>
<span data-ttu-id="49e54-138">Identyfikator zasobu zarządzanego klastra</span><span class="sxs-lookup"><span data-stu-id="49e54-138">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49e54-139">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="49e54-139">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="49e54-140">Punkt końcowy używany przez odwrotny serwer proxy.</span><span class="sxs-lookup"><span data-stu-id="49e54-140">Endpoint used by reverse proxy.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e54-141">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="49e54-141">-UpgradeMode</span></span>
<span data-ttu-id="49e54-142">Tryb uaktualniania wersji kodu klastrowego.</span><span class="sxs-lookup"><span data-stu-id="49e54-142">Cluster code version upgrade mode.</span></span> <span data-ttu-id="49e54-143">Automatyczne lub ręczne.</span><span class="sxs-lookup"><span data-stu-id="49e54-143">Automatic or Manual.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode]
Parameter Sets: WithPramsByName, ByNameById
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49e54-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49e54-144">-Confirm</span></span>
<span data-ttu-id="49e54-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="49e54-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49e54-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49e54-146">-WhatIf</span></span>
<span data-ttu-id="49e54-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49e54-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49e54-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="49e54-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49e54-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49e54-149">CommonParameters</span></span>
<span data-ttu-id="49e54-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49e54-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49e54-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49e54-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49e54-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49e54-152">INPUTS</span></span>

### <span data-ttu-id="49e54-153">System.String</span><span class="sxs-lookup"><span data-stu-id="49e54-153">System.String</span></span>

## <span data-ttu-id="49e54-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="49e54-154">OUTPUTS</span></span>

### <span data-ttu-id="49e54-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="49e54-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="49e54-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="49e54-156">NOTES</span></span>

## <span data-ttu-id="49e54-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49e54-157">RELATED LINKS</span></span>
