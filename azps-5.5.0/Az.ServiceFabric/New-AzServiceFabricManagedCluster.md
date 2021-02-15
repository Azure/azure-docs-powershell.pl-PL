---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 9dd54f0f1ca56a8bedf3550e238a4308b519925d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242083"
---
# <span data-ttu-id="d18f0-101">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="d18f0-101">New-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="d18f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d18f0-102">SYNOPSIS</span></span>
<span data-ttu-id="d18f0-103">Tworzenie nowego klastru zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="d18f0-103">Create new managed cluster.</span></span>

## <span data-ttu-id="d18f0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d18f0-104">SYNTAX</span></span>

### <span data-ttu-id="d18f0-105">ClientCertByTp (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d18f0-105">ClientCertByTp (Default)</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertThumbprint <String> -AdminPassword <SecureString> [-AdminUserName <String>]
 [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>] [-DnsName <String>]
 [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d18f0-106">ClientCertByCn</span><span class="sxs-lookup"><span data-stu-id="d18f0-106">ClientCertByCn</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertCommonName <String> [-ClientCertIssuerThumbprint <String[]>] -AdminPassword <SecureString>
 [-AdminUserName <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d18f0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d18f0-107">DESCRIPTION</span></span>
<span data-ttu-id="d18f0-108">To polecenie cmdlet utworzy zarządzany zasób klastrów bez typów węzłów.</span><span class="sxs-lookup"><span data-stu-id="d18f0-108">This cmdlet will create a managed cluster resource without node types.</span></span> <span data-ttu-id="d18f0-109">Aby maskować klaster podstawowy typ węzła musi zostać dodany, użyj [właściwości New-AzServiceFabricManagedNodeType.](./New-AzServiceFabricManagedNodeType.md)</span><span class="sxs-lookup"><span data-stu-id="d18f0-109">To bootstrap the cluster A primary node type needs to be added use [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span></span>

## <span data-ttu-id="d18f0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d18f0-110">EXAMPLES</span></span>

### <span data-ttu-id="d18f0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d18f0-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -AdminPassword $password -Verbose
```

<span data-ttu-id="d18f0-112">To polecenie tworzy zasób klastrów z domyślną podstawową bazą danych.</span><span class="sxs-lookup"><span data-stu-id="d18f0-112">This command creates a cluster resource with default basic sku.</span></span>

### <span data-ttu-id="d18f0-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d18f0-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -ClientCertThumbprint XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX -ClientCertIsAdmin -AdminPassword $password -Sku Standard -Verbose
```

<span data-ttu-id="d18f0-114">To polecenie tworzy zasób klastrów w centraluseuap z początkowym certyfikatem klienta administratora i standardową skojarzeniami.</span><span class="sxs-lookup"><span data-stu-id="d18f0-114">This command creates a cluster resource in centraluseuap with an initial admin client certificate and standard sku.</span></span>

## <span data-ttu-id="d18f0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d18f0-115">PARAMETERS</span></span>

### <span data-ttu-id="d18f0-116">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="d18f0-116">-AdminPassword</span></span>
<span data-ttu-id="d18f0-117">Hasło administratora używane dla maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="d18f0-117">Admin password used for the virtual machines.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18f0-118">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="d18f0-118">-AdminUserName</span></span>
<span data-ttu-id="d18f0-119">Hasło administratora używane dla maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="d18f0-119">Admin password used for the virtual machines.</span></span>
<span data-ttu-id="d18f0-120">Domyślne: administrator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d18f0-120">Default: vmadmin.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "vmadmin"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18f0-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d18f0-121">-AsJob</span></span>
<span data-ttu-id="d18f0-122">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="d18f0-122">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d18f0-123">-ClientCertCommonName</span><span class="sxs-lookup"><span data-stu-id="d18f0-123">-ClientCertCommonName</span></span>
<span data-ttu-id="d18f0-124">Nazwa pospolita certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="d18f0-124">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18f0-125">-ClientCertIsAdmin</span><span class="sxs-lookup"><span data-stu-id="d18f0-125">-ClientCertIsAdmin</span></span>
<span data-ttu-id="d18f0-126">Umożliwia określenie, czy certyfikat klienta ma poziom administratora.</span><span class="sxs-lookup"><span data-stu-id="d18f0-126">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="d18f0-127">-ClientCertIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="d18f0-127">-ClientCertIssuerThumbprint</span></span>
<span data-ttu-id="d18f0-128">List of Issuer thumbprints for the client certificate.</span><span class="sxs-lookup"><span data-stu-id="d18f0-128">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="d18f0-129">Używaj tylko w połączeniu z parametrem ClientCertCommonName.</span><span class="sxs-lookup"><span data-stu-id="d18f0-129">Only use in combination with ClientCertCommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18f0-130">-ClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="d18f0-130">-ClientCertThumbprint</span></span>
<span data-ttu-id="d18f0-131">Thumbprint certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="d18f0-131">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18f0-132">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="d18f0-132">-ClientConnectionPort</span></span>
<span data-ttu-id="d18f0-133">Port używany do obsługi połączeń klienta z klastrem.</span><span class="sxs-lookup"><span data-stu-id="d18f0-133">Port used for client connections to the cluster.</span></span>
<span data-ttu-id="d18f0-134">Wartość domyślna: 19000.</span><span class="sxs-lookup"><span data-stu-id="d18f0-134">Default: 19000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18f0-135">- CodeVersion</span><span class="sxs-lookup"><span data-stu-id="d18f0-135">-CodeVersion</span></span>
<span data-ttu-id="d18f0-136">Wersja kodu szkieletowego usługi klastrowej.</span><span class="sxs-lookup"><span data-stu-id="d18f0-136">Cluster service fabric code version.</span></span>
<span data-ttu-id="d18f0-137">Użyj tylko wtedy, gdy tryb uaktualniania jest ręczny.</span><span class="sxs-lookup"><span data-stu-id="d18f0-137">Only use if upgrade mode is Manual.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18f0-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d18f0-138">-DefaultProfile</span></span>
<span data-ttu-id="d18f0-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d18f0-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d18f0-140">-DnsName</span><span class="sxs-lookup"><span data-stu-id="d18f0-140">-DnsName</span></span>
<span data-ttu-id="d18f0-141">Nazwa DNS klastrów.</span><span class="sxs-lookup"><span data-stu-id="d18f0-141">Cluster's dns name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18f0-142">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="d18f0-142">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="d18f0-143">Port używany dla połączeń http z klastrem.</span><span class="sxs-lookup"><span data-stu-id="d18f0-143">Port used for http connections to the cluster.</span></span>
<span data-ttu-id="d18f0-144">Domyślne: 19080.</span><span class="sxs-lookup"><span data-stu-id="d18f0-144">Default: 19080.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19080
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18f0-145">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d18f0-145">-Location</span></span>
<span data-ttu-id="d18f0-146">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="d18f0-146">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d18f0-147">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d18f0-147">-Name</span></span>
<span data-ttu-id="d18f0-148">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="d18f0-148">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d18f0-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d18f0-149">-ResourceGroupName</span></span>
<span data-ttu-id="d18f0-150">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d18f0-150">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d18f0-151">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="d18f0-151">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="d18f0-152">Punkt końcowy używany przez odwrotny serwer proxy.</span><span class="sxs-lookup"><span data-stu-id="d18f0-152">Endpoint used by reverse proxy.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18f0-153">- SKU</span><span class="sxs-lookup"><span data-stu-id="d18f0-153">-Sku</span></span>
<span data-ttu-id="d18f0-154">SKU klastrów, opcje są podstawowe: będą mieć co najmniej 3 węzły iniekcyjną i zezwalają tylko na 1 typ węzła i standardowo: będą mieć co najmniej 5 węzłów iniekcjonu i dopuszczają wiele typów węzłów.</span><span class="sxs-lookup"><span data-stu-id="d18f0-154">Cluster's Sku, the options are Basic: it will have a minimum of 3 seed nodes and only allows 1 node type and Standard: it will have a minimum of 5 seed nodes and allows multiple node types.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ManagedClusterSku
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: Basic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18f0-155">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="d18f0-155">-UpgradeMode</span></span>
<span data-ttu-id="d18f0-156">Tryb uaktualniania wersji kodu szkieletowego usługi klastrowej.</span><span class="sxs-lookup"><span data-stu-id="d18f0-156">Cluster service fabric code version upgrade mode.</span></span>
<span data-ttu-id="d18f0-157">Automatyczne lub ręczne.</span><span class="sxs-lookup"><span data-stu-id="d18f0-157">Automatic or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18f0-158">-UseTestExtension</span><span class="sxs-lookup"><span data-stu-id="d18f0-158">-UseTestExtension</span></span>
<span data-ttu-id="d18f0-159">If Specify The cluster will be crated with service test vmss extension.</span><span class="sxs-lookup"><span data-stu-id="d18f0-159">If Specify The cluster will be crated with service test vmss extension.</span></span>

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

### <span data-ttu-id="d18f0-160">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d18f0-160">-Confirm</span></span>
<span data-ttu-id="d18f0-161">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d18f0-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d18f0-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d18f0-162">-WhatIf</span></span>
<span data-ttu-id="d18f0-163">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d18f0-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d18f0-164">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d18f0-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d18f0-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d18f0-165">CommonParameters</span></span>
<span data-ttu-id="d18f0-166">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d18f0-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d18f0-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d18f0-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d18f0-168">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d18f0-168">INPUTS</span></span>

### <span data-ttu-id="d18f0-169">System.String</span><span class="sxs-lookup"><span data-stu-id="d18f0-169">System.String</span></span>

## <span data-ttu-id="d18f0-170">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d18f0-170">OUTPUTS</span></span>

### <span data-ttu-id="d18f0-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="d18f0-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="d18f0-172">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d18f0-172">NOTES</span></span>

## <span data-ttu-id="d18f0-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d18f0-173">RELATED LINKS</span></span>

[<span data-ttu-id="d18f0-174">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="d18f0-174">New-AzServiceFabricManagedNodeType</span></span>](./New-AzServiceFabricManagedNodeType.md)