---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: 0c3fe2ffc9e5ce74c991e182ef1112629f05b88a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873052"
---
# <span data-ttu-id="3e836-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="3e836-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="3e836-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e836-102">SYNOPSIS</span></span>
<span data-ttu-id="3e836-103">To polecenie używa certyfikatów, które zostały podane, lub system wygenerował certyfikaty z podpisem własnym, aby skonfigurować nowy klaster programu Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="3e836-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="3e836-104">Może on używać szablonu domyślnego lub szablonu niestandardowego, który jest udostępniany.</span><span class="sxs-lookup"><span data-stu-id="3e836-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="3e836-105">Możesz określić folder do eksportowania certyfikatów z podpisem własnym lub pobrać je później z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="3e836-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

## <span data-ttu-id="3e836-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e836-106">SYNTAX</span></span>

### <span data-ttu-id="3e836-107">ByDefaultArmTemplate (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3e836-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e836-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="3e836-108">ByExistingKeyVault</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e836-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="3e836-109">ByNewPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>]
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateSubjectName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e836-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="3e836-110">ByExistingPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e836-111">Opis</span><span class="sxs-lookup"><span data-stu-id="3e836-111">DESCRIPTION</span></span>
<span data-ttu-id="3e836-112">W poleceniu **New-AzServiceFabricCluster** są używane certyfikaty, które zostały podane, lub system wygenerował certyfikaty z podpisem własnym, aby skonfigurować nowy klaster programu Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="3e836-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="3e836-113">Szablon, którego używasz, może być szablonem domyślnym lub szablonem niestandardowym.</span><span class="sxs-lookup"><span data-stu-id="3e836-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="3e836-114">Możesz określić folder do eksportowania certyfikatów z podpisem własnym lub pobrać je później z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="3e836-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="3e836-115">Jeśli określisz szablon niestandardowy i plik parametrów, nie musisz dostarczać informacji o certyfikacie w pliku parametru, system wypełni te parametry.</span><span class="sxs-lookup"><span data-stu-id="3e836-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="3e836-116">Poniżej wymieniono cztery opcje.</span><span class="sxs-lookup"><span data-stu-id="3e836-116">The four options are detailed below.</span></span> <span data-ttu-id="3e836-117">Przewiń w dół, aby zapoznać się z objaśnieniami każdego z parametrów.</span><span class="sxs-lookup"><span data-stu-id="3e836-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="3e836-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e836-118">EXAMPLES</span></span>

### <span data-ttu-id="3e836-119">Przykład 1: Określ tylko rozmiar klastra, nazwę podmiotu certyfikatu oraz system operacyjny, aby wdrożyć klaster.</span><span class="sxs-lookup"><span data-stu-id="3e836-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="c:\certs"

Write-Output "Create cluster in '$clusterloc' with cert subject name '$subname' and cert output path '$pfxfolder'"

New-AzServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 5 -VmPassword $pass -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="3e836-120">To polecenie umożliwia określenie rozmiaru klastra, nazwy podmiotu certyfikatu i systemu operacyjnego w celu wdrożenia klastra.</span><span class="sxs-lookup"><span data-stu-id="3e836-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="3e836-121">Przykład 2: Określanie istniejącego zasobu certyfikatu w magazynie kluczy oraz szablonu niestandardowego do wdrożenia klastra</span><span class="sxs-lookup"><span data-stu-id="3e836-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secretId
```

<span data-ttu-id="3e836-122">To polecenie umożliwia określenie istniejącego zasobu certyfikatu w magazynie kluczy oraz szablonu niestandardowego do wdrożenia klastra.</span><span class="sxs-lookup"><span data-stu-id="3e836-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="3e836-123">Przykład 3: Tworzenie nowego klastra przy użyciu szablonu niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="3e836-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="3e836-124">Określanie innej nazwy grupy zasobów dla magazynu kluczy oraz przekazywanie przez system nowego certyfikatu</span><span class="sxs-lookup"><span data-stu-id="3e836-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.$clusterloc.cloudapp.azure.com" -f $RGName, $clusterloc
$pfxfolder="~\Documents"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -KeyVaultResourceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="3e836-125">To polecenie tworzy nowy klaster przy użyciu szablonu niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="3e836-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="3e836-126">Określanie innej nazwy grupy zasobów dla magazynu kluczy oraz przekazywanie przez system nowego certyfikatu</span><span class="sxs-lookup"><span data-stu-id="3e836-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="3e836-127">Przykład 4: przenoszenie własnego certyfikatu i szablonu niestandardowego oraz tworzenie nowego klastra</span><span class="sxs-lookup"><span data-stu-id="3e836-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateFile $pfxsourcefile -CertificatePassword $pass -KeyVaultResourceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="3e836-128">To polecenie umożliwia przeprowadzenie własnego certyfikatu i szablonu niestandardowego oraz utworzenie nowego klastra.</span><span class="sxs-lookup"><span data-stu-id="3e836-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="3e836-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e836-129">PARAMETERS</span></span>

### <span data-ttu-id="3e836-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="3e836-130">-CertificateCommonName</span></span>
<span data-ttu-id="3e836-131">Nazwa pospolita certyfikatu</span><span class="sxs-lookup"><span data-stu-id="3e836-131">Certificate common name</span></span>

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

### <span data-ttu-id="3e836-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="3e836-132">-CertificateFile</span></span>
<span data-ttu-id="3e836-133">Istniejąca ścieżka do pliku certyfikatu podstawowego klastra</span><span class="sxs-lookup"><span data-stu-id="3e836-133">The existing certificate file path for the primary cluster certificate</span></span>

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

### <span data-ttu-id="3e836-134">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="3e836-134">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="3e836-135">Odcisk palca wystawcy certyfikatu, oddzielony przecinkami, jeśli więcej niż jeden</span><span class="sxs-lookup"><span data-stu-id="3e836-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="3e836-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="3e836-136">-CertificateOutputFolder</span></span>
<span data-ttu-id="3e836-137">Folder nowego pliku certyfikatu do utworzenia</span><span class="sxs-lookup"><span data-stu-id="3e836-137">The folder of the new certificate file to be created</span></span>

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

### <span data-ttu-id="3e836-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="3e836-138">-CertificatePassword</span></span>
<span data-ttu-id="3e836-139">Hasło pliku certyfikatu</span><span class="sxs-lookup"><span data-stu-id="3e836-139">The password of the certificate file</span></span>

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

### <span data-ttu-id="3e836-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="3e836-140">-CertificateSubjectName</span></span>
<span data-ttu-id="3e836-141">Nazwa podmiotu certyfikatu do utworzenia</span><span class="sxs-lookup"><span data-stu-id="3e836-141">The subject name of the certificate to be created</span></span>

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

### <span data-ttu-id="3e836-142">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="3e836-142">-ClusterSize</span></span>
<span data-ttu-id="3e836-143">Liczba węzłów w klastrze.</span><span class="sxs-lookup"><span data-stu-id="3e836-143">The number of nodes in the cluster.</span></span>
<span data-ttu-id="3e836-144">Domyślnie 5 węzłów</span><span class="sxs-lookup"><span data-stu-id="3e836-144">Default are 5 nodes</span></span>

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

### <span data-ttu-id="3e836-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e836-145">-DefaultProfile</span></span>
<span data-ttu-id="3e836-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e836-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e836-147">-Thebinding</span><span class="sxs-lookup"><span data-stu-id="3e836-147">-KeyVaultName</span></span>
<span data-ttu-id="3e836-148">Nazwa magazynu kluczy platformy Azure, jeśli nie została określona, zostanie przeszukana domyślnie w nazwie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3e836-148">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="3e836-149">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e836-149">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="3e836-150">Nazwa grupy zasobów magazynu kluczy platformy Azure, jeśli nie została podana, zostanie domyślnie określona jako nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3e836-150">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="3e836-151">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3e836-151">-Location</span></span>
<span data-ttu-id="3e836-152">Lokalizacja grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3e836-152">The resource group location</span></span>

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

### <span data-ttu-id="3e836-153">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3e836-153">-Name</span></span>
<span data-ttu-id="3e836-154">Określ nazwę klastra, jeśli nie jest podana, jest taka sama jak nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3e836-154">Specify the name of the cluster, if not given it will be same as resource group name</span></span>

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

### <span data-ttu-id="3e836-155">-OS</span><span class="sxs-lookup"><span data-stu-id="3e836-155">-OS</span></span>
<span data-ttu-id="3e836-156">System operacyjny maszyn wirtualnych, które tworzą klaster.</span><span class="sxs-lookup"><span data-stu-id="3e836-156">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="3e836-157">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="3e836-157">-ParameterFile</span></span>
<span data-ttu-id="3e836-158">Ścieżka do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="3e836-158">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="3e836-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e836-159">-ResourceGroupName</span></span>
<span data-ttu-id="3e836-160">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3e836-160">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="3e836-161">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="3e836-161">-SecondaryCertificateFile</span></span>
<span data-ttu-id="3e836-162">Istniejąca ścieżka pliku certyfikatu dla pomocniczego certyfikatu klastra</span><span class="sxs-lookup"><span data-stu-id="3e836-162">The existing certificate file path for the secondary cluster certificate</span></span>

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

### <span data-ttu-id="3e836-163">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="3e836-163">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="3e836-164">Hasło pliku certyfikatu</span><span class="sxs-lookup"><span data-stu-id="3e836-164">The password of the certificate file</span></span>

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

### <span data-ttu-id="3e836-165">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="3e836-165">-SecretIdentifier</span></span>
<span data-ttu-id="3e836-166">Istniejący tajny adres URL magazynu kluczy platformy Azure, na przykład ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="3e836-166">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="3e836-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="3e836-167">-TemplateFile</span></span>
<span data-ttu-id="3e836-168">Ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="3e836-168">The path to the template file.</span></span>

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

### <span data-ttu-id="3e836-169">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="3e836-169">-VmPassword</span></span>
<span data-ttu-id="3e836-170">Hasło maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3e836-170">The password of the Vm.</span></span>

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

### <span data-ttu-id="3e836-171">-VmSku</span><span class="sxs-lookup"><span data-stu-id="3e836-171">-VmSku</span></span>
<span data-ttu-id="3e836-172">Wersja SKU maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="3e836-172">The Vm Sku</span></span>

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

### <span data-ttu-id="3e836-173">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="3e836-173">-VmUserName</span></span>
<span data-ttu-id="3e836-174">Nazwa użytkownika służąca do logowania się do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="3e836-174">The user name for logging to Vm</span></span>

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

### <span data-ttu-id="3e836-175">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e836-175">-Confirm</span></span>
<span data-ttu-id="3e836-176">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e836-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e836-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e836-177">-WhatIf</span></span>
<span data-ttu-id="3e836-178">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e836-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e836-179">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3e836-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e836-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e836-180">CommonParameters</span></span>
<span data-ttu-id="3e836-181">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e836-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e836-182">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e836-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e836-183">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e836-183">INPUTS</span></span>

### <span data-ttu-id="3e836-184">System. String</span><span class="sxs-lookup"><span data-stu-id="3e836-184">System.String</span></span>

### <span data-ttu-id="3e836-185">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="3e836-185">System.Security.SecureString</span></span>

### <span data-ttu-id="3e836-186">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3e836-186">System.Int32</span></span>

### <span data-ttu-id="3e836-187">Microsoft. Azure. Commands. servicefabric. MODELES. OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="3e836-187">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="3e836-188">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e836-188">OUTPUTS</span></span>

### <span data-ttu-id="3e836-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="3e836-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="3e836-190">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e836-190">NOTES</span></span>

## <span data-ttu-id="3e836-191">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e836-191">RELATED LINKS</span></span>
