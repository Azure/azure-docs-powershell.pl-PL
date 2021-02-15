---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: 9e5ba2d2ee228da30a887c0c7b318dd9d270d763
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242090"
---
# <span data-ttu-id="1d7d9-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="1d7d9-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="1d7d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d7d9-102">SYNOPSIS</span></span>

<span data-ttu-id="1d7d9-103">To polecenie używa certyfikatów, które ty dostarczasz, lub certyfikatów wygenerowanych przez system z podpisem własnym w celu skonfigurowania nowego klastru materiału usługowego.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="1d7d9-104">Może on używać szablonu domyślnego lub niestandardowego, który możesz udostępnić.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="1d7d9-105">Możesz określić folder, aby wyeksportować certyfikaty z podpisem własnym lub pobrać je później z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

## <span data-ttu-id="1d7d9-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1d7d9-106">SYNTAX</span></span>

### <span data-ttu-id="1d7d9-107">ByDefaultArmTemplate (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="1d7d9-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d7d9-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="1d7d9-108">ByExistingKeyVault</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-Thumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d7d9-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="1d7d9-109">ByNewPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>]
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateSubjectName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1d7d9-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="1d7d9-110">ByExistingPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d7d9-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="1d7d9-111">DESCRIPTION</span></span>

<span data-ttu-id="1d7d9-112">Polecenie **New-AzServiceFabricCluster** używa certyfikatów, które dostarczasz, lub certyfikatów wygenerowanych przez system w celu skonfigurowania nowego klastru struktury usług.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="1d7d9-113">Używanym szablonem może być szablon domyślny lub szablon niestandardowy, który możesz udostępnić.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="1d7d9-114">Możesz określić folder, aby wyeksportować certyfikaty z podpisem własnym lub pobrać je później z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="1d7d9-115">Jeśli określasz niestandardowy szablon i plik parametru, nie musisz poświadczeń w pliku parametrów, system wypełni te parametry.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="1d7d9-116">Poniżej przedstawiono cztery opcje.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-116">The four options are detailed below.</span></span> <span data-ttu-id="1d7d9-117">Przewiń w dół, aby uzyskać objaśnienia poszczególnych parametrów.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="1d7d9-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1d7d9-118">EXAMPLES</span></span>

### <span data-ttu-id="1d7d9-119">Przykład 1. Określanie tylko rozmiaru klastrów, nazwy podmiotu certyfikatu i systemu operacyjnego do wdrożenia klastrów</span><span class="sxs-lookup"><span data-stu-id="1d7d9-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -f $resourceGroupName, $azureRegion
$localCertificateFolder = "c:\certs"

Write-Output "Create cluster in '$azureRegion' with cert subject name '$clusterDnsName' and cert output path '$localCertificateFolder'"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -Location $azureRegion -ClusterSize 5 -VmPassword $password -CertificateSubjectName $clusterDnsName -CertificateOutputFolder $localCertificateFolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="1d7d9-120">To polecenie określa tylko rozmiar klastrów, nazwę podmiotu certyfikatu i system operacyjny do wdrożenia klastrów.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="1d7d9-121">Przykład 2. Określanie istniejącego zasobu certyfikatu w magazynie kluczy i szablonu niestandardowego w celu wdrożenia klastrów</span><span class="sxs-lookup"><span data-stu-id="1d7d9-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>

```powershell
$resourceGroupName = "test20"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId = "https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -SecretIdentifier $secretId
```

<span data-ttu-id="1d7d9-122">To polecenie określa istniejący zasób certyfikatu w magazynie kluczy i szablon niestandardowy do wdrażania klastrów.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="1d7d9-123">Przykład 3. Tworzenie nowego klastra przy użyciu szablonu niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="1d7d9-124">Określanie innej nazwy grupy zasobów dla magazynu kluczy i przekazywanie do systemu nowego certyfikatu</span><span class="sxs-lookup"><span data-stu-id="1d7d9-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$keyVaultResourceGroupName = " quickstart-kv-group"
$keyVaultName = "quickstart-kv"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -F $resourceGroupName, $azureRegion
$localCertificateFolder = "~\Documents"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateOutputFolder $localCertificateFolder -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName  -KeyVaultName $keyVaultName -CertificateSubjectName $clusterDnsName
```

<span data-ttu-id="1d7d9-125">To polecenie tworzy nowy klaster przy użyciu szablonu niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="1d7d9-126">Określanie innej nazwy grupy zasobów dla magazynu kluczy i przekazywanie do systemu nowego certyfikatu</span><span class="sxs-lookup"><span data-stu-id="1d7d9-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="1d7d9-127">Przykład 4. Przynieź własny certyfikat i szablon niestandardowy i utwórz nowy klaster</span><span class="sxs-lookup"><span data-stu-id="1d7d9-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "test20"
$keyVaultResourceGroupName = "test20kvrg"
$keyVaultName = "test20kv"
$localCertificateFile = "c:\Mycertificates\my2017Prodcert.pfx"
$templateParameterFile = "~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateFile $localCertificateFile -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName -KeyVaultName $keyVaultName
```

<span data-ttu-id="1d7d9-128">To polecenie umożliwia przyniesienie własnego certyfikatu i szablonu niestandardowego oraz utworzenie nowego klastra.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="1d7d9-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d7d9-129">PARAMETERS</span></span>

### <span data-ttu-id="1d7d9-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="1d7d9-130">-CertificateCommonName</span></span>

<span data-ttu-id="1d7d9-131">Nazwa pospolita certyfikatu</span><span class="sxs-lookup"><span data-stu-id="1d7d9-131">Certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertCommonName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="1d7d9-132">-CertificateFile</span></span>

<span data-ttu-id="1d7d9-133">Istniejąca ścieżka pliku certyfikatu dla certyfikatu klastrów podstawowych</span><span class="sxs-lookup"><span data-stu-id="1d7d9-133">The existing certificate file path for the primary cluster certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-134">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="1d7d9-134">-CertificateIssuerThumbprint</span></span>

<span data-ttu-id="1d7d9-135">Thumbprint wystawcy certyfikatu oddzielony przecinkami, jeśli jest ich więcej niż jeden</span><span class="sxs-lookup"><span data-stu-id="1d7d9-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertIssuerThumbprint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="1d7d9-136">-CertificateOutputFolder</span></span>

<span data-ttu-id="1d7d9-137">Folder nowego pliku certyfikatu, który ma zostać utworzony</span><span class="sxs-lookup"><span data-stu-id="1d7d9-137">The folder of the new certificate file to be created</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="1d7d9-138">-CertificatePassword</span></span>

<span data-ttu-id="1d7d9-139">Hasło pliku certyfikatu</span><span class="sxs-lookup"><span data-stu-id="1d7d9-139">The password of the certificate file</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="1d7d9-140">-CertificateSubjectName</span></span>

<span data-ttu-id="1d7d9-141">Nazwa podmiotu certyfikatu do utworzenia</span><span class="sxs-lookup"><span data-stu-id="1d7d9-141">The subject name of the certificate to be created</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Subject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-142">- ClusterSize</span><span class="sxs-lookup"><span data-stu-id="1d7d9-142">-ClusterSize</span></span>

<span data-ttu-id="1d7d9-143">Liczba węzłów w klastrze.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-143">The number of nodes in the cluster.</span></span>
<span data-ttu-id="1d7d9-144">Wartością domyślną jest 5 węzłów</span><span class="sxs-lookup"><span data-stu-id="1d7d9-144">Default are 5 nodes</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d7d9-145">-DefaultProfile</span></span>

<span data-ttu-id="1d7d9-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d7d9-147">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="1d7d9-147">-KeyVaultName</span></span>

<span data-ttu-id="1d7d9-148">Nazwa magazynu kluczy platformy Azure, jeśli nie zostanie nadana, zostanie domyślnie nadana nazwie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1d7d9-148">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-149">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d7d9-149">-KeyVaultResourceGroupName</span></span>

<span data-ttu-id="1d7d9-150">Nazwa grupy zasobów magazynu klucza platformy Azure, jeśli nie zostanie nadana, zostanie domyślnie nadana nazwie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1d7d9-150">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-151">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1d7d9-151">-Location</span></span>

<span data-ttu-id="1d7d9-152">Lokalizacja grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1d7d9-152">The resource group location</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-153">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1d7d9-153">-Name</span></span>

<span data-ttu-id="1d7d9-154">Określanie nazwy klastra, jeśli nie zostanie nadana, będzie taka sama jak nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1d7d9-154">Specify the name of the cluster, if not given it will be same as resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: ClusterName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-155">— system operacyjny</span><span class="sxs-lookup"><span data-stu-id="1d7d9-155">-OS</span></span>

<span data-ttu-id="1d7d9-156">System operacyjny maszyn wirtualnych, które są klasterem.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-156">The Operating System of the VMs that make up the cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem
Parameter Sets: ByDefaultArmTemplate
Aliases: VmImage
Accepted values: WindowsServer2012R2Datacenter, WindowsServer2016Datacenter, WindowsServer2016DatacenterwithContainers, UbuntuServer1604

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-157">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="1d7d9-157">-ParameterFile</span></span>

<span data-ttu-id="1d7d9-158">Ścieżka do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-158">The path to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d7d9-159">-ResourceGroupName</span></span>

<span data-ttu-id="1d7d9-160">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-160">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1d7d9-161">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="1d7d9-161">-SecondaryCertificateFile</span></span>

<span data-ttu-id="1d7d9-162">Istniejąca ścieżka pliku certyfikatu dla certyfikatu klasteru pomocniczego</span><span class="sxs-lookup"><span data-stu-id="1d7d9-162">The existing certificate file path for the secondary cluster certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecSource

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-163">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="1d7d9-163">-SecondaryCertificatePassword</span></span>

<span data-ttu-id="1d7d9-164">Hasło pliku certyfikatu</span><span class="sxs-lookup"><span data-stu-id="1d7d9-164">The password of the certificate file</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecCertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-165">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="1d7d9-165">-SecretIdentifier</span></span>

<span data-ttu-id="1d7d9-166">Istniejący tajny adres URL magazynu kluczy platformy Azure, na przykład https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="1d7d9-166">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="1d7d9-167">-TemplateFile</span></span>

<span data-ttu-id="1d7d9-168">Ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-168">The path to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-169">- Thumbprint</span><span class="sxs-lookup"><span data-stu-id="1d7d9-169">-Thumbprint</span></span>
<span data-ttu-id="1d7d9-170">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-170">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="1d7d9-171">Użyj tego polecenia, jeśli certyfikat nie jest zarządzany, ponieważ magazyn kluczy będzie przechowywać tylko certyfikat jako tajny i polecenie cmdlet nie może ponownie przechować kciuka.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-171">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-172">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="1d7d9-172">-VmPassword</span></span>

<span data-ttu-id="1d7d9-173">Hasło maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-173">The password of the Vm.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-174">-VmSku</span><span class="sxs-lookup"><span data-stu-id="1d7d9-174">-VmSku</span></span>

<span data-ttu-id="1d7d9-175">SKU maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1d7d9-175">The Vm Sku</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: Sku

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-176">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="1d7d9-176">-VmUserName</span></span>

<span data-ttu-id="1d7d9-177">Nazwa użytkownika dla rejestrowania do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1d7d9-177">The user name for logging to Vm</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d9-178">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1d7d9-178">-Confirm</span></span>

<span data-ttu-id="1d7d9-179">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d7d9-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d7d9-180">-WhatIf</span></span>

<span data-ttu-id="1d7d9-181">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d7d9-182">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d7d9-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d7d9-183">CommonParameters</span></span>
<span data-ttu-id="1d7d9-184">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d7d9-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d7d9-185">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d7d9-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d7d9-186">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d7d9-186">INPUTS</span></span>

### <span data-ttu-id="1d7d9-187">System.String</span><span class="sxs-lookup"><span data-stu-id="1d7d9-187">System.String</span></span>

### <span data-ttu-id="1d7d9-188">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="1d7d9-188">System.Security.SecureString</span></span>

### <span data-ttu-id="1d7d9-189">System.Int32</span><span class="sxs-lookup"><span data-stu-id="1d7d9-189">System.Int32</span></span>

### <span data-ttu-id="1d7d9-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="1d7d9-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="1d7d9-191">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d7d9-191">OUTPUTS</span></span>

### <span data-ttu-id="1d7d9-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="1d7d9-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="1d7d9-193">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1d7d9-193">NOTES</span></span>

## <span data-ttu-id="1d7d9-194">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d7d9-194">RELATED LINKS</span></span>
