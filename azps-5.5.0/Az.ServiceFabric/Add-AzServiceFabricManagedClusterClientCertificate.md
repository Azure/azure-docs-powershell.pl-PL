---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: e948acb179a0ae6a338fa02f01d1cb7d6efbd4fe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189106"
---
# <span data-ttu-id="814c8-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="814c8-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="814c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="814c8-102">SYNOPSIS</span></span>
<span data-ttu-id="814c8-103">Dodaj nazwę pospolitą certyfikatu lub thumbprint do klastra.</span><span class="sxs-lookup"><span data-stu-id="814c8-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="814c8-104">Spowoduje to zarejestrowanie certyfikatu ponownie dla klastrów na potrzeby uwierzytelniania klienta.</span><span class="sxs-lookup"><span data-stu-id="814c8-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="814c8-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="814c8-105">SYNTAX</span></span>

### <span data-ttu-id="814c8-106">ClientCertByTpByObj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="814c8-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="814c8-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="814c8-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="814c8-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="814c8-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="814c8-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="814c8-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="814c8-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="814c8-110">DESCRIPTION</span></span>
<span data-ttu-id="814c8-111">Dodaj nazwę pospolitą certyfikatu lub thumbprint do klastra.</span><span class="sxs-lookup"><span data-stu-id="814c8-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="814c8-112">Spowoduje to zarejestrowanie certyfikatu ponownie dla klastrów na potrzeby uwierzytelniania klienta.</span><span class="sxs-lookup"><span data-stu-id="814c8-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="814c8-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="814c8-113">EXAMPLES</span></span>

### <span data-ttu-id="814c8-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="814c8-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="814c8-115">To polecenie spowoduje dodanie certyfikatu z kciukiem "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" do klastrów, dzięki czemu klient może używać tego certyfikatu jako administrator do komunikowania się z klasterem.</span><span class="sxs-lookup"><span data-stu-id="814c8-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="814c8-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="814c8-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="814c8-117">To polecenie spowoduje dodanie certyfikatu klienta tylko do odczytu z nazwą pospolitą "Contoso.com" i 2 wystawcami.</span><span class="sxs-lookup"><span data-stu-id="814c8-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="814c8-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="814c8-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="814c8-119">To polecenie spowoduje dodanie certyfikatu klienta tylko do odczytu z nazwą pospolitą "Contoso.com" i 2 wystawców, z rurami.</span><span class="sxs-lookup"><span data-stu-id="814c8-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="814c8-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="814c8-120">PARAMETERS</span></span>

### <span data-ttu-id="814c8-121">— Administrator</span><span class="sxs-lookup"><span data-stu-id="814c8-121">-Admin</span></span>
<span data-ttu-id="814c8-122">Umożliwia określenie, czy certyfikat klienta ma poziom administratora.</span><span class="sxs-lookup"><span data-stu-id="814c8-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="814c8-123">— AsJob</span><span class="sxs-lookup"><span data-stu-id="814c8-123">-AsJob</span></span>
<span data-ttu-id="814c8-124">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="814c8-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="814c8-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="814c8-125">-CommonName</span></span>
<span data-ttu-id="814c8-126">Nazwa pospolita certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="814c8-126">Client certificate common name.</span></span>

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

### <span data-ttu-id="814c8-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="814c8-127">-DefaultProfile</span></span>
<span data-ttu-id="814c8-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="814c8-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="814c8-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="814c8-129">-InputObject</span></span>
<span data-ttu-id="814c8-130">Zarządzany zasób klastrów</span><span class="sxs-lookup"><span data-stu-id="814c8-130">Managed cluster resource</span></span>

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

### <span data-ttu-id="814c8-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="814c8-131">-IssuerThumbprint</span></span>
<span data-ttu-id="814c8-132">List of Issuer thumbprints for the client certificate.</span><span class="sxs-lookup"><span data-stu-id="814c8-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="814c8-133">Używaj tylko w połączeniu z commonname.</span><span class="sxs-lookup"><span data-stu-id="814c8-133">Only use in combination with CommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="814c8-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="814c8-134">-Name</span></span>
<span data-ttu-id="814c8-135">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="814c8-135">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="814c8-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="814c8-136">-ResourceGroupName</span></span>
<span data-ttu-id="814c8-137">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="814c8-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="814c8-138">- Thumbprint</span><span class="sxs-lookup"><span data-stu-id="814c8-138">-Thumbprint</span></span>
<span data-ttu-id="814c8-139">Thumbprint certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="814c8-139">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByTpByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="814c8-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="814c8-140">-Confirm</span></span>
<span data-ttu-id="814c8-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="814c8-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="814c8-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="814c8-142">-WhatIf</span></span>
<span data-ttu-id="814c8-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="814c8-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="814c8-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="814c8-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="814c8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="814c8-145">CommonParameters</span></span>
<span data-ttu-id="814c8-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="814c8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="814c8-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="814c8-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="814c8-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="814c8-148">INPUTS</span></span>

### <span data-ttu-id="814c8-149">System.String</span><span class="sxs-lookup"><span data-stu-id="814c8-149">System.String</span></span>

## <span data-ttu-id="814c8-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="814c8-150">OUTPUTS</span></span>

### <span data-ttu-id="814c8-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="814c8-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="814c8-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="814c8-152">NOTES</span></span>

## <span data-ttu-id="814c8-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="814c8-153">RELATED LINKS</span></span>
