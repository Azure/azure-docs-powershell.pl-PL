---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 4636dc8f8c8efdf9dae5f7d2094fd3432528f043
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231491"
---
# <span data-ttu-id="01efe-101">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="01efe-101">Set-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="01efe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01efe-102">SYNOPSIS</span></span>
<span data-ttu-id="01efe-103">Ustawianie właściwości zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="01efe-103">Set cluster resource properties.</span></span>

## <span data-ttu-id="01efe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01efe-104">SYNTAX</span></span>

### <span data-ttu-id="01efe-105">ByObj (domyślny)</span><span class="sxs-lookup"><span data-stu-id="01efe-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01efe-106">WithPramsByName</span><span class="sxs-lookup"><span data-stu-id="01efe-106">WithPramsByName</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>]
 [-ClientConnectionPort <Int32>] [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01efe-107">ByNameById</span><span class="sxs-lookup"><span data-stu-id="01efe-107">ByNameById</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceId] <String> [-UpgradeMode <ClusterUpgradeMode>]
 [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01efe-108">Opis</span><span class="sxs-lookup"><span data-stu-id="01efe-108">DESCRIPTION</span></span>
<span data-ttu-id="01efe-109">Ustawianie właściwości zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="01efe-109">Set cluster resource properties.</span></span>

## <span data-ttu-id="01efe-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01efe-110">EXAMPLES</span></span>

### <span data-ttu-id="01efe-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="01efe-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Update-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName -DnsName testnewdns -ClientConnectionPort 50000 -Verbose
```

<span data-ttu-id="01efe-112">Zaktualizuj nazwę DNS i port połączenia klienta dla klastra.</span><span class="sxs-lookup"><span data-stu-id="01efe-112">Update dns name and client connection port for the cluster.</span></span>

### <span data-ttu-id="01efe-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="01efe-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster.DnsName = "testnewdns"
$cluster.ClientConnectionPort = 50000
$cluster | Set-AzServiceFabricManagedCluster
```

<span data-ttu-id="01efe-114">Zaktualizuj nazwę DNS i port połączenia klienta dla klastra przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="01efe-114">Update dns name and client connection port for the cluster, with piping.</span></span>

## <span data-ttu-id="01efe-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01efe-115">PARAMETERS</span></span>

### <span data-ttu-id="01efe-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01efe-116">-AsJob</span></span>
<span data-ttu-id="01efe-117">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="01efe-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="01efe-118">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="01efe-118">-ClientConnectionPort</span></span>
<span data-ttu-id="01efe-119">Port służący do połączeń klientów z klastrem.</span><span class="sxs-lookup"><span data-stu-id="01efe-119">Port used for client connections to the cluster.</span></span> <span data-ttu-id="01efe-120">Wartość domyślna: 19000.</span><span class="sxs-lookup"><span data-stu-id="01efe-120">Default: 19000.</span></span>

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

### <span data-ttu-id="01efe-121">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="01efe-121">-CodeVersion</span></span>
<span data-ttu-id="01efe-122">Wersja kodu klastra.</span><span class="sxs-lookup"><span data-stu-id="01efe-122">Cluster code version.</span></span> <span data-ttu-id="01efe-123">Używaj tylko trybu uaktualniania ręcznego.</span><span class="sxs-lookup"><span data-stu-id="01efe-123">Only use if upgrade mode is Manual.</span></span>

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

### <span data-ttu-id="01efe-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01efe-124">-DefaultProfile</span></span>
<span data-ttu-id="01efe-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="01efe-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01efe-126">-DnsName</span><span class="sxs-lookup"><span data-stu-id="01efe-126">-DnsName</span></span>
<span data-ttu-id="01efe-127">Nazwa DNS klastra.</span><span class="sxs-lookup"><span data-stu-id="01efe-127">Cluster's dns name.</span></span>

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

### <span data-ttu-id="01efe-128">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="01efe-128">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="01efe-129">Port służący do połączeń HTTP z klastrem.</span><span class="sxs-lookup"><span data-stu-id="01efe-129">Port used for http connections to the cluster.</span></span> <span data-ttu-id="01efe-130">Wartość domyślna: 19080.</span><span class="sxs-lookup"><span data-stu-id="01efe-130">Default: 19080.</span></span>

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

### <span data-ttu-id="01efe-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="01efe-131">-InputObject</span></span>
<span data-ttu-id="01efe-132">Zarządzany zasób klastra</span><span class="sxs-lookup"><span data-stu-id="01efe-132">Managed Cluster resource</span></span>

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

### <span data-ttu-id="01efe-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="01efe-133">-Name</span></span>
<span data-ttu-id="01efe-134">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="01efe-134">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="01efe-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01efe-135">-ResourceGroupName</span></span>
<span data-ttu-id="01efe-136">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="01efe-136">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="01efe-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01efe-137">-ResourceId</span></span>
<span data-ttu-id="01efe-138">Identyfikator zarządzanego zasobu klastra</span><span class="sxs-lookup"><span data-stu-id="01efe-138">Managed Cluster resource id</span></span>

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

### <span data-ttu-id="01efe-139">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="01efe-139">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="01efe-140">Punkt końcowy używany przez odwrotny serwer proxy.</span><span class="sxs-lookup"><span data-stu-id="01efe-140">Endpoint used by reverse proxy.</span></span>

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

### <span data-ttu-id="01efe-141">-Upgrademode</span><span class="sxs-lookup"><span data-stu-id="01efe-141">-UpgradeMode</span></span>
<span data-ttu-id="01efe-142">Tryb uaktualniania wersji kodu klastra.</span><span class="sxs-lookup"><span data-stu-id="01efe-142">Cluster code version upgrade mode.</span></span> <span data-ttu-id="01efe-143">Automatyczne lub ręczne.</span><span class="sxs-lookup"><span data-stu-id="01efe-143">Automatic or Manual.</span></span>

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

### <span data-ttu-id="01efe-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="01efe-144">-Confirm</span></span>
<span data-ttu-id="01efe-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01efe-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01efe-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01efe-146">-WhatIf</span></span>
<span data-ttu-id="01efe-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01efe-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01efe-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="01efe-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01efe-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01efe-149">CommonParameters</span></span>
<span data-ttu-id="01efe-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01efe-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01efe-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01efe-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01efe-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01efe-152">INPUTS</span></span>

### <span data-ttu-id="01efe-153">System. String</span><span class="sxs-lookup"><span data-stu-id="01efe-153">System.String</span></span>

## <span data-ttu-id="01efe-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01efe-154">OUTPUTS</span></span>

### <span data-ttu-id="01efe-155">Microsoft. Azure. Commands. servicefabric. MODELES. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="01efe-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="01efe-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01efe-156">NOTES</span></span>

## <span data-ttu-id="01efe-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01efe-157">RELATED LINKS</span></span>
