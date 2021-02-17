---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: d9a3e5488fe55a1d5090fb21ffb211e6fcec53c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191146"
---
# <span data-ttu-id="d128e-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d128e-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="d128e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d128e-102">SYNOPSIS</span></span>
<span data-ttu-id="d128e-103">Remvoe client certificate by thumbprint or common name.</span><span class="sxs-lookup"><span data-stu-id="d128e-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="d128e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d128e-104">SYNTAX</span></span>

### <span data-ttu-id="d128e-105">ClientCertByTpByObj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d128e-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d128e-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="d128e-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d128e-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="d128e-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d128e-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="d128e-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d128e-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="d128e-109">DESCRIPTION</span></span>
<span data-ttu-id="d128e-110">Remvoe client certificate by thumbprint or common name.</span><span class="sxs-lookup"><span data-stu-id="d128e-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="d128e-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d128e-111">EXAMPLES</span></span>

### <span data-ttu-id="d128e-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d128e-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="d128e-113">Usuń certyfikat klienta za pomocą popularnej nazwy.</span><span class="sxs-lookup"><span data-stu-id="d128e-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="d128e-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d128e-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="d128e-115">Usuń certyfikat klienta za pomocą kciuka.</span><span class="sxs-lookup"><span data-stu-id="d128e-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="d128e-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d128e-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="d128e-117">Usuń certyfikat klienta za pomocą funkcji usbprint za pomocą funkcji pipingu.</span><span class="sxs-lookup"><span data-stu-id="d128e-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="d128e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d128e-118">PARAMETERS</span></span>

### <span data-ttu-id="d128e-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d128e-119">-AsJob</span></span>
<span data-ttu-id="d128e-120">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="d128e-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d128e-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="d128e-121">-CommonName</span></span>
<span data-ttu-id="d128e-122">Nazwa pospolita certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="d128e-122">Client certificate common name.</span></span>

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

### <span data-ttu-id="d128e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d128e-123">-DefaultProfile</span></span>
<span data-ttu-id="d128e-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d128e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d128e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d128e-125">-InputObject</span></span>
<span data-ttu-id="d128e-126">Zarządzany zasób klastrów</span><span class="sxs-lookup"><span data-stu-id="d128e-126">Managed cluster resource</span></span>

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

### <span data-ttu-id="d128e-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d128e-127">-Name</span></span>
<span data-ttu-id="d128e-128">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="d128e-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d128e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d128e-129">-PassThru</span></span>
<span data-ttu-id="d128e-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="d128e-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d128e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d128e-131">-ResourceGroupName</span></span>
<span data-ttu-id="d128e-132">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d128e-132">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d128e-133">- Thumbprint</span><span class="sxs-lookup"><span data-stu-id="d128e-133">-Thumbprint</span></span>
<span data-ttu-id="d128e-134">Thumbprint certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="d128e-134">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="d128e-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d128e-135">-Confirm</span></span>
<span data-ttu-id="d128e-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d128e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d128e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d128e-137">-WhatIf</span></span>
<span data-ttu-id="d128e-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d128e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d128e-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d128e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d128e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d128e-140">CommonParameters</span></span>
<span data-ttu-id="d128e-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d128e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d128e-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d128e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d128e-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d128e-143">INPUTS</span></span>

### <span data-ttu-id="d128e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d128e-144">System.String</span></span>

## <span data-ttu-id="d128e-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d128e-145">OUTPUTS</span></span>

### <span data-ttu-id="d128e-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="d128e-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="d128e-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d128e-147">NOTES</span></span>

## <span data-ttu-id="d128e-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d128e-148">RELATED LINKS</span></span>
