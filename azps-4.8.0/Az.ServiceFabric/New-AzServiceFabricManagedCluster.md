---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 9dd54f0f1ca56a8bedf3550e238a4308b519925d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221118"
---
# <span data-ttu-id="6adad-101">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="6adad-101">New-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="6adad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6adad-102">SYNOPSIS</span></span>
<span data-ttu-id="6adad-103">Tworzenie nowego zarządzanego klastra.</span><span class="sxs-lookup"><span data-stu-id="6adad-103">Create new managed cluster.</span></span>

## <span data-ttu-id="6adad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6adad-104">SYNTAX</span></span>

### <span data-ttu-id="6adad-105">ClientCertByTp (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6adad-105">ClientCertByTp (Default)</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertThumbprint <String> -AdminPassword <SecureString> [-AdminUserName <String>]
 [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>] [-DnsName <String>]
 [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6adad-106">ClientCertByCn</span><span class="sxs-lookup"><span data-stu-id="6adad-106">ClientCertByCn</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertCommonName <String> [-ClientCertIssuerThumbprint <String[]>] -AdminPassword <SecureString>
 [-AdminUserName <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6adad-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6adad-107">DESCRIPTION</span></span>
<span data-ttu-id="6adad-108">To polecenie cmdlet utworzy zarządzany zasób klastra bez typów węzłów.</span><span class="sxs-lookup"><span data-stu-id="6adad-108">This cmdlet will create a managed cluster resource without node types.</span></span> <span data-ttu-id="6adad-109">Aby zainicjować Inicjowanie klastra, należy dodać podstawowy typ węzła użyj [nowych-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span><span class="sxs-lookup"><span data-stu-id="6adad-109">To bootstrap the cluster A primary node type needs to be added use [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span></span>

## <span data-ttu-id="6adad-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6adad-110">EXAMPLES</span></span>

### <span data-ttu-id="6adad-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6adad-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -AdminPassword $password -Verbose
```

<span data-ttu-id="6adad-112">To polecenie tworzy zasób klastra mający domyślną podstawową jednostkę SKU.</span><span class="sxs-lookup"><span data-stu-id="6adad-112">This command creates a cluster resource with default basic sku.</span></span>

### <span data-ttu-id="6adad-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6adad-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -ClientCertThumbprint XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX -ClientCertIsAdmin -AdminPassword $password -Sku Standard -Verbose
```

<span data-ttu-id="6adad-114">To polecenie tworzy zasób klastra w centraluseuap za pomocą początkowego certyfikatu klienta administratora i standardowej jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="6adad-114">This command creates a cluster resource in centraluseuap with an initial admin client certificate and standard sku.</span></span>

## <span data-ttu-id="6adad-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6adad-115">PARAMETERS</span></span>

### <span data-ttu-id="6adad-116">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="6adad-116">-AdminPassword</span></span>
<span data-ttu-id="6adad-117">Hasło administratora używane przez maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="6adad-117">Admin password used for the virtual machines.</span></span>

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

### <span data-ttu-id="6adad-118">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="6adad-118">-AdminUserName</span></span>
<span data-ttu-id="6adad-119">Hasło administratora używane przez maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="6adad-119">Admin password used for the virtual machines.</span></span>
<span data-ttu-id="6adad-120">Wartość domyślna: vmadmin.</span><span class="sxs-lookup"><span data-stu-id="6adad-120">Default: vmadmin.</span></span>

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

### <span data-ttu-id="6adad-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6adad-121">-AsJob</span></span>
<span data-ttu-id="6adad-122">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="6adad-122">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6adad-123">-ClientCertCommonName</span><span class="sxs-lookup"><span data-stu-id="6adad-123">-ClientCertCommonName</span></span>
<span data-ttu-id="6adad-124">Nazwa pospolita certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="6adad-124">Client certificate common name.</span></span>

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

### <span data-ttu-id="6adad-125">-ClientCertIsAdmin</span><span class="sxs-lookup"><span data-stu-id="6adad-125">-ClientCertIsAdmin</span></span>
<span data-ttu-id="6adad-126">Umożliwia określenie, czy certyfikat klienta ma poziom administratora.</span><span class="sxs-lookup"><span data-stu-id="6adad-126">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="6adad-127">-ClientCertIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="6adad-127">-ClientCertIssuerThumbprint</span></span>
<span data-ttu-id="6adad-128">Lista odcisków palców wystawcy dla certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="6adad-128">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="6adad-129">Używaj tylko w połączeniu z ClientCertCommonName.</span><span class="sxs-lookup"><span data-stu-id="6adad-129">Only use in combination with ClientCertCommonName.</span></span>

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

### <span data-ttu-id="6adad-130">-ClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="6adad-130">-ClientCertThumbprint</span></span>
<span data-ttu-id="6adad-131">Odcisk palca certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="6adad-131">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="6adad-132">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="6adad-132">-ClientConnectionPort</span></span>
<span data-ttu-id="6adad-133">Port służący do połączeń klientów z klastrem.</span><span class="sxs-lookup"><span data-stu-id="6adad-133">Port used for client connections to the cluster.</span></span>
<span data-ttu-id="6adad-134">Wartość domyślna: 19000.</span><span class="sxs-lookup"><span data-stu-id="6adad-134">Default: 19000.</span></span>

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

### <span data-ttu-id="6adad-135">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="6adad-135">-CodeVersion</span></span>
<span data-ttu-id="6adad-136">Wersja kodu sieci szkieletowej usługi klastrowania.</span><span class="sxs-lookup"><span data-stu-id="6adad-136">Cluster service fabric code version.</span></span>
<span data-ttu-id="6adad-137">Używaj tylko trybu uaktualniania ręcznego.</span><span class="sxs-lookup"><span data-stu-id="6adad-137">Only use if upgrade mode is Manual.</span></span>

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

### <span data-ttu-id="6adad-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6adad-138">-DefaultProfile</span></span>
<span data-ttu-id="6adad-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6adad-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6adad-140">-DnsName</span><span class="sxs-lookup"><span data-stu-id="6adad-140">-DnsName</span></span>
<span data-ttu-id="6adad-141">Nazwa DNS klastra.</span><span class="sxs-lookup"><span data-stu-id="6adad-141">Cluster's dns name.</span></span>

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

### <span data-ttu-id="6adad-142">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="6adad-142">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="6adad-143">Port służący do połączeń HTTP z klastrem.</span><span class="sxs-lookup"><span data-stu-id="6adad-143">Port used for http connections to the cluster.</span></span>
<span data-ttu-id="6adad-144">Wartość domyślna: 19080.</span><span class="sxs-lookup"><span data-stu-id="6adad-144">Default: 19080.</span></span>

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

### <span data-ttu-id="6adad-145">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6adad-145">-Location</span></span>
<span data-ttu-id="6adad-146">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="6adad-146">The resource location</span></span>

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

### <span data-ttu-id="6adad-147">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6adad-147">-Name</span></span>
<span data-ttu-id="6adad-148">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="6adad-148">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="6adad-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6adad-149">-ResourceGroupName</span></span>
<span data-ttu-id="6adad-150">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6adad-150">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="6adad-151">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="6adad-151">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="6adad-152">Punkt końcowy używany przez odwrotny serwer proxy.</span><span class="sxs-lookup"><span data-stu-id="6adad-152">Endpoint used by reverse proxy.</span></span>

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

### <span data-ttu-id="6adad-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="6adad-153">-Sku</span></span>
<span data-ttu-id="6adad-154">SKU klastra, dostępne są następujące opcje: co najmniej 3 węzły dosienne i dozwolone jest tylko 1 węzeł i standard: będzie zawierać co najmniej 5 węzłów rozrzutu i umożliwia korzystanie z wielu typów węzłów.</span><span class="sxs-lookup"><span data-stu-id="6adad-154">Cluster's Sku, the options are Basic: it will have a minimum of 3 seed nodes and only allows 1 node type and Standard: it will have a minimum of 5 seed nodes and allows multiple node types.</span></span>

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

### <span data-ttu-id="6adad-155">-Upgrademode</span><span class="sxs-lookup"><span data-stu-id="6adad-155">-UpgradeMode</span></span>
<span data-ttu-id="6adad-156">Tryb uaktualniania wersji kodu sieci szkieletowej usługi klastrowania.</span><span class="sxs-lookup"><span data-stu-id="6adad-156">Cluster service fabric code version upgrade mode.</span></span>
<span data-ttu-id="6adad-157">Automatyczne lub ręczne.</span><span class="sxs-lookup"><span data-stu-id="6adad-157">Automatic or Manual.</span></span>

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

### <span data-ttu-id="6adad-158">-UseTestExtension</span><span class="sxs-lookup"><span data-stu-id="6adad-158">-UseTestExtension</span></span>
<span data-ttu-id="6adad-159">Jeśli określisz, klaster zostanie wyposażony w rozszerzenie VMSS test usługi.</span><span class="sxs-lookup"><span data-stu-id="6adad-159">If Specify The cluster will be crated with service test vmss extension.</span></span>

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

### <span data-ttu-id="6adad-160">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6adad-160">-Confirm</span></span>
<span data-ttu-id="6adad-161">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6adad-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6adad-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6adad-162">-WhatIf</span></span>
<span data-ttu-id="6adad-163">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6adad-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6adad-164">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6adad-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6adad-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6adad-165">CommonParameters</span></span>
<span data-ttu-id="6adad-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6adad-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6adad-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6adad-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6adad-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6adad-168">INPUTS</span></span>

### <span data-ttu-id="6adad-169">System. String</span><span class="sxs-lookup"><span data-stu-id="6adad-169">System.String</span></span>

## <span data-ttu-id="6adad-170">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6adad-170">OUTPUTS</span></span>

### <span data-ttu-id="6adad-171">Microsoft. Azure. Commands. servicefabric. MODELES. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="6adad-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="6adad-172">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6adad-172">NOTES</span></span>

## <span data-ttu-id="6adad-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6adad-173">RELATED LINKS</span></span>

[<span data-ttu-id="6adad-174">Nowe — AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="6adad-174">New-AzServiceFabricManagedNodeType</span></span>](./New-AzServiceFabricManagedNodeType.md)