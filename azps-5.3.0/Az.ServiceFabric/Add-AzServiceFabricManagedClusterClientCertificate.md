---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: e948acb179a0ae6a338fa02f01d1cb7d6efbd4fe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502844"
---
# <span data-ttu-id="0d70a-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0d70a-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="0d70a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d70a-102">SYNOPSIS</span></span>
<span data-ttu-id="0d70a-103">Dodawanie nazwy pospolitej certyfikatu lub odcisku palca do klastra.</span><span class="sxs-lookup"><span data-stu-id="0d70a-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="0d70a-104">Spowoduje to ponowne zarejestrowanie certyfikatu w celu uwierzytelnienia klienta.</span><span class="sxs-lookup"><span data-stu-id="0d70a-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="0d70a-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d70a-105">SYNTAX</span></span>

### <span data-ttu-id="0d70a-106">ClientCertByTpByObj (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0d70a-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d70a-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="0d70a-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d70a-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="0d70a-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d70a-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="0d70a-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d70a-110">Opis</span><span class="sxs-lookup"><span data-stu-id="0d70a-110">DESCRIPTION</span></span>
<span data-ttu-id="0d70a-111">Dodawanie nazwy pospolitej certyfikatu lub odcisku palca do klastra.</span><span class="sxs-lookup"><span data-stu-id="0d70a-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="0d70a-112">Spowoduje to ponowne zarejestrowanie certyfikatu w celu uwierzytelnienia klienta.</span><span class="sxs-lookup"><span data-stu-id="0d70a-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="0d70a-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d70a-113">EXAMPLES</span></span>

### <span data-ttu-id="0d70a-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0d70a-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="0d70a-115">To polecenie doda certyfikat z odciskiem palca "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" do klastra, więc klient może użyć tego certyfikatu jako administratora do komunikacji z klastrem.</span><span class="sxs-lookup"><span data-stu-id="0d70a-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="0d70a-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0d70a-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="0d70a-117">To polecenie doda certyfikat klienta tylko do odczytu z nazwą pospolitą "Contoso.com" i 2 wystawcami.</span><span class="sxs-lookup"><span data-stu-id="0d70a-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="0d70a-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0d70a-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="0d70a-119">To polecenie doda certyfikat klienta tylko do odczytu z nazwą pospolitą "Contoso.com" i 2 wystawcami, korzystając z połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="0d70a-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="0d70a-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d70a-120">PARAMETERS</span></span>

### <span data-ttu-id="0d70a-121">-Administrator</span><span class="sxs-lookup"><span data-stu-id="0d70a-121">-Admin</span></span>
<span data-ttu-id="0d70a-122">Umożliwia określenie, czy certyfikat klienta ma poziom administratora.</span><span class="sxs-lookup"><span data-stu-id="0d70a-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="0d70a-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d70a-123">-AsJob</span></span>
<span data-ttu-id="0d70a-124">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="0d70a-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0d70a-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="0d70a-125">-CommonName</span></span>
<span data-ttu-id="0d70a-126">Nazwa pospolita certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="0d70a-126">Client certificate common name.</span></span>

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

### <span data-ttu-id="0d70a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d70a-127">-DefaultProfile</span></span>
<span data-ttu-id="0d70a-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d70a-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d70a-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0d70a-129">-InputObject</span></span>
<span data-ttu-id="0d70a-130">Zarządzany zasób klastra</span><span class="sxs-lookup"><span data-stu-id="0d70a-130">Managed cluster resource</span></span>

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

### <span data-ttu-id="0d70a-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="0d70a-131">-IssuerThumbprint</span></span>
<span data-ttu-id="0d70a-132">Lista odcisków palców wystawcy dla certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="0d70a-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="0d70a-133">Używaj tylko w połączeniu z funkcją CommonName.</span><span class="sxs-lookup"><span data-stu-id="0d70a-133">Only use in combination with CommonName.</span></span>

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

### <span data-ttu-id="0d70a-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0d70a-134">-Name</span></span>
<span data-ttu-id="0d70a-135">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="0d70a-135">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0d70a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d70a-136">-ResourceGroupName</span></span>
<span data-ttu-id="0d70a-137">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0d70a-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0d70a-138">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="0d70a-138">-Thumbprint</span></span>
<span data-ttu-id="0d70a-139">Odcisk palca certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="0d70a-139">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="0d70a-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0d70a-140">-Confirm</span></span>
<span data-ttu-id="0d70a-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d70a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d70a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d70a-142">-WhatIf</span></span>
<span data-ttu-id="0d70a-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d70a-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d70a-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0d70a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d70a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d70a-145">CommonParameters</span></span>
<span data-ttu-id="0d70a-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d70a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d70a-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d70a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d70a-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d70a-148">INPUTS</span></span>

### <span data-ttu-id="0d70a-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0d70a-149">System.String</span></span>

## <span data-ttu-id="0d70a-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d70a-150">OUTPUTS</span></span>

### <span data-ttu-id="0d70a-151">Microsoft. Azure. Commands. servicefabric. MODELES. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="0d70a-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="0d70a-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d70a-152">NOTES</span></span>

## <span data-ttu-id="0d70a-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d70a-153">RELATED LINKS</span></span>
