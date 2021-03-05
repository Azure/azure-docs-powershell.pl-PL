---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: f0ba5cb4d461bbc70ba742ae46ba4b9489923545
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005482"
---
# <span data-ttu-id="b0abd-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b0abd-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="b0abd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0abd-102">SYNOPSIS</span></span>
<span data-ttu-id="b0abd-103">Remvoe client certificate by thumbprint or common name.</span><span class="sxs-lookup"><span data-stu-id="b0abd-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="b0abd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b0abd-104">SYNTAX</span></span>

### <span data-ttu-id="b0abd-105">ClientCertByTpByObj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b0abd-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0abd-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="b0abd-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0abd-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="b0abd-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0abd-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="b0abd-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0abd-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="b0abd-109">DESCRIPTION</span></span>
<span data-ttu-id="b0abd-110">Remvoe client certificate by thumbprint or common name.</span><span class="sxs-lookup"><span data-stu-id="b0abd-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="b0abd-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b0abd-111">EXAMPLES</span></span>

### <span data-ttu-id="b0abd-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b0abd-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="b0abd-113">Usuwanie certyfikatu klienta za pomocą nazwy wspólnej.</span><span class="sxs-lookup"><span data-stu-id="b0abd-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="b0abd-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b0abd-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="b0abd-115">Usuń certyfikat klienta za pomocą kciuka.</span><span class="sxs-lookup"><span data-stu-id="b0abd-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="b0abd-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b0abd-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="b0abd-117">Usuń certyfikat klienta za pomocą funkcji usbprint za pomocą funkcji pipingu.</span><span class="sxs-lookup"><span data-stu-id="b0abd-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="b0abd-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0abd-118">PARAMETERS</span></span>

### <span data-ttu-id="b0abd-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b0abd-119">-AsJob</span></span>
<span data-ttu-id="b0abd-120">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="b0abd-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b0abd-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="b0abd-121">-CommonName</span></span>
<span data-ttu-id="b0abd-122">Nazwa pospolita certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="b0abd-122">Client certificate common name.</span></span>

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

### <span data-ttu-id="b0abd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0abd-123">-DefaultProfile</span></span>
<span data-ttu-id="b0abd-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0abd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0abd-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0abd-125">-InputObject</span></span>
<span data-ttu-id="b0abd-126">Zarządzany zasób klastrów</span><span class="sxs-lookup"><span data-stu-id="b0abd-126">Managed cluster resource</span></span>

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

### <span data-ttu-id="b0abd-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b0abd-127">-Name</span></span>
<span data-ttu-id="b0abd-128">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="b0abd-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b0abd-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0abd-129">-PassThru</span></span>
<span data-ttu-id="b0abd-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="b0abd-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="b0abd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0abd-131">-ResourceGroupName</span></span>
<span data-ttu-id="b0abd-132">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b0abd-132">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b0abd-133">- Thumbprint</span><span class="sxs-lookup"><span data-stu-id="b0abd-133">-Thumbprint</span></span>
<span data-ttu-id="b0abd-134">Thumbprint certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="b0abd-134">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="b0abd-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b0abd-135">-Confirm</span></span>
<span data-ttu-id="b0abd-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b0abd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0abd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0abd-137">-WhatIf</span></span>
<span data-ttu-id="b0abd-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0abd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0abd-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b0abd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0abd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0abd-140">CommonParameters</span></span>
<span data-ttu-id="b0abd-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0abd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0abd-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0abd-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0abd-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0abd-143">INPUTS</span></span>

### <span data-ttu-id="b0abd-144">System.String</span><span class="sxs-lookup"><span data-stu-id="b0abd-144">System.String</span></span>

## <span data-ttu-id="b0abd-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0abd-145">OUTPUTS</span></span>

### <span data-ttu-id="b0abd-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="b0abd-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="b0abd-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b0abd-147">NOTES</span></span>

## <span data-ttu-id="b0abd-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0abd-148">RELATED LINKS</span></span>
