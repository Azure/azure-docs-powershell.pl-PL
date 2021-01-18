---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: d9a3e5488fe55a1d5090fb21ffb211e6fcec53c2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502792"
---
# <span data-ttu-id="6f96d-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6f96d-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="6f96d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6f96d-102">SYNOPSIS</span></span>
<span data-ttu-id="6f96d-103">Remvoe certyfikat klienta według odcisku palca lub nazwy pospolitej.</span><span class="sxs-lookup"><span data-stu-id="6f96d-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="6f96d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6f96d-104">SYNTAX</span></span>

### <span data-ttu-id="6f96d-105">ClientCertByTpByObj (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6f96d-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f96d-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="6f96d-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f96d-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="6f96d-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f96d-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="6f96d-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f96d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6f96d-109">DESCRIPTION</span></span>
<span data-ttu-id="6f96d-110">Remvoe certyfikat klienta według odcisku palca lub nazwy pospolitej.</span><span class="sxs-lookup"><span data-stu-id="6f96d-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="6f96d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6f96d-111">EXAMPLES</span></span>

### <span data-ttu-id="6f96d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6f96d-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="6f96d-113">Usuń certyfikat klienta według nazwy pospolitej.</span><span class="sxs-lookup"><span data-stu-id="6f96d-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="6f96d-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6f96d-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="6f96d-115">Usuń certyfikat klienta według odcisku palca.</span><span class="sxs-lookup"><span data-stu-id="6f96d-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="6f96d-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="6f96d-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="6f96d-117">Usuń certyfikat klienta według odcisku palca z potokiem.</span><span class="sxs-lookup"><span data-stu-id="6f96d-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="6f96d-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6f96d-118">PARAMETERS</span></span>

### <span data-ttu-id="6f96d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f96d-119">-AsJob</span></span>
<span data-ttu-id="6f96d-120">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="6f96d-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6f96d-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="6f96d-121">-CommonName</span></span>
<span data-ttu-id="6f96d-122">Nazwa pospolita certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="6f96d-122">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f96d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f96d-123">-DefaultProfile</span></span>
<span data-ttu-id="6f96d-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6f96d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f96d-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6f96d-125">-InputObject</span></span>
<span data-ttu-id="6f96d-126">Zarządzany zasób klastra</span><span class="sxs-lookup"><span data-stu-id="6f96d-126">Managed cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ClientCertByTpByObj, ClientCertByCnByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f96d-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6f96d-127">-Name</span></span>
<span data-ttu-id="6f96d-128">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="6f96d-128">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f96d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f96d-129">-PassThru</span></span>
<span data-ttu-id="6f96d-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6f96d-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="6f96d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f96d-131">-ResourceGroupName</span></span>
<span data-ttu-id="6f96d-132">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6f96d-132">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f96d-133">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="6f96d-133">-Thumbprint</span></span>
<span data-ttu-id="6f96d-134">Odcisk palca certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="6f96d-134">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByCnTpName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f96d-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6f96d-135">-Confirm</span></span>
<span data-ttu-id="6f96d-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f96d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f96d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f96d-137">-WhatIf</span></span>
<span data-ttu-id="6f96d-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f96d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f96d-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6f96d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f96d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f96d-140">CommonParameters</span></span>
<span data-ttu-id="6f96d-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f96d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f96d-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f96d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f96d-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f96d-143">INPUTS</span></span>

### <span data-ttu-id="6f96d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6f96d-144">System.String</span></span>

## <span data-ttu-id="6f96d-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6f96d-145">OUTPUTS</span></span>

### <span data-ttu-id="6f96d-146">Microsoft. Azure. Commands. servicefabric. MODELES. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="6f96d-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="6f96d-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6f96d-147">NOTES</span></span>

## <span data-ttu-id="6f96d-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f96d-148">RELATED LINKS</span></span>
