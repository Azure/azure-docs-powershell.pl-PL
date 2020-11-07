---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: e78912d2a8ab0ce4f5e990e69e236853a85019c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708086"
---
# <span data-ttu-id="758d3-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="758d3-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="758d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="758d3-102">SYNOPSIS</span></span>
<span data-ttu-id="758d3-103">To polecenie używa certyfikatów, które zostały podane, lub system wygenerował certyfikaty z podpisem własnym, aby skonfigurować nowy klaster programu Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="758d3-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="758d3-104">Może on używać szablonu domyślnego lub szablonu niestandardowego, który jest udostępniany.</span><span class="sxs-lookup"><span data-stu-id="758d3-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="758d3-105">Możesz określić folder do eksportowania certyfikatów z podpisem własnym lub pobrać je później z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="758d3-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

## <span data-ttu-id="758d3-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="758d3-106">SYNTAX</span></span>

### <span data-ttu-id="758d3-107">ByDefaultArmTemplate (domyślny)</span><span class="sxs-lookup"><span data-stu-id="758d3-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="758d3-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="758d3-108">ByExistingKeyVault</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="758d3-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="758d3-109">ByNewPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>]
 [-KeyVaultName <String>] [-CertificateSubjectName <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="758d3-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="758d3-110">ByExistingPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="758d3-111">Opis</span><span class="sxs-lookup"><span data-stu-id="758d3-111">DESCRIPTION</span></span>
<span data-ttu-id="758d3-112">W poleceniu **New-AzServiceFabricCluster** są używane certyfikaty, które zostały podane, lub system wygenerował certyfikaty z podpisem własnym, aby skonfigurować nowy klaster programu Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="758d3-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="758d3-113">Szablon, którego używasz, może być szablonem domyślnym lub szablonem niestandardowym.</span><span class="sxs-lookup"><span data-stu-id="758d3-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="758d3-114">Możesz określić folder do eksportowania certyfikatów z podpisem własnym lub pobrać je później z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="758d3-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="758d3-115">Jeśli określisz szablon niestandardowy i plik parametrów, nie musisz dostarczać informacji o certyfikacie w pliku parametru, system wypełni te parametry.</span><span class="sxs-lookup"><span data-stu-id="758d3-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="758d3-116">Poniżej wymieniono cztery opcje.</span><span class="sxs-lookup"><span data-stu-id="758d3-116">The four options are detailed below.</span></span> <span data-ttu-id="758d3-117">Przewiń w dół, aby zapoznać się z objaśnieniami każdego z parametrów.</span><span class="sxs-lookup"><span data-stu-id="758d3-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="758d3-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="758d3-118">EXAMPLES</span></span>

### <span data-ttu-id="758d3-119">Przykład 1: Określ tylko rozmiar klastra, nazwę podmiotu certyfikatu oraz system operacyjny, aby wdrożyć klaster.</span><span class="sxs-lookup"><span data-stu-id="758d3-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="c:\certs"

Write-Output "Create cluster in '$clusterloc' with cert subject name '$subname' and cert output path '$pfxfolder'"

New-AzServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 5 -VmPassword $pass -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="758d3-120">To polecenie umożliwia określenie rozmiaru klastra, nazwy podmiotu certyfikatu i systemu operacyjnego w celu wdrożenia klastra.</span><span class="sxs-lookup"><span data-stu-id="758d3-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="758d3-121">Przykład 2: Określanie istniejącego zasobu certyfikatu w magazynie kluczy oraz szablonu niestandardowego do wdrożenia klastra</span><span class="sxs-lookup"><span data-stu-id="758d3-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secretId
```

<span data-ttu-id="758d3-122">To polecenie umożliwia określenie istniejącego zasobu certyfikatu w magazynie kluczy oraz szablonu niestandardowego do wdrożenia klastra.</span><span class="sxs-lookup"><span data-stu-id="758d3-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="758d3-123">Przykład 3: Tworzenie nowego klastra przy użyciu szablonu niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="758d3-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="758d3-124">Określanie innej nazwy grupy zasobów dla magazynu kluczy oraz przekazywanie przez system nowego certyfikatu</span><span class="sxs-lookup"><span data-stu-id="758d3-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>
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

New-AzServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="758d3-125">To polecenie tworzy nowy klaster przy użyciu szablonu niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="758d3-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="758d3-126">Określanie innej nazwy grupy zasobów dla magazynu kluczy oraz przekazywanie przez system nowego certyfikatu</span><span class="sxs-lookup"><span data-stu-id="758d3-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="758d3-127">Przykład 4: przenoszenie własnego certyfikatu i szablonu niestandardowego oraz tworzenie nowego klastra</span><span class="sxs-lookup"><span data-stu-id="758d3-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateFile $pfxsourcefile -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="758d3-128">To polecenie umożliwia przeprowadzenie własnego certyfikatu i szablonu niestandardowego oraz utworzenie nowego klastra.</span><span class="sxs-lookup"><span data-stu-id="758d3-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="758d3-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="758d3-129">PARAMETERS</span></span>

### <span data-ttu-id="758d3-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="758d3-130">-CertificateCommonName</span></span>
<span data-ttu-id="758d3-131">Nazwa pospolita certyfikatu</span><span class="sxs-lookup"><span data-stu-id="758d3-131">Certificate common name</span></span>

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

### <span data-ttu-id="758d3-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="758d3-132">-CertificateFile</span></span>
<span data-ttu-id="758d3-133">Istniejąca ścieżka pliku certyfikatu podstawowego certyfikatu klastra.</span><span class="sxs-lookup"><span data-stu-id="758d3-133">The existing certificate file path for the primary cluster certificate.</span></span>

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

### <span data-ttu-id="758d3-134">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="758d3-134">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="758d3-135">Odcisk palca wystawcy certyfikatu, oddzielony przecinkami, jeśli więcej niż jeden</span><span class="sxs-lookup"><span data-stu-id="758d3-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="758d3-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="758d3-136">-CertificateOutputFolder</span></span>
<span data-ttu-id="758d3-137">Folder nowego pliku certyfikatu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="758d3-137">The folder of the new certificate file to be created.</span></span>

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

### <span data-ttu-id="758d3-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="758d3-138">-CertificatePassword</span></span>
<span data-ttu-id="758d3-139">Hasło pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="758d3-139">The password of the certificate file.</span></span>

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

### <span data-ttu-id="758d3-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="758d3-140">-CertificateSubjectName</span></span>
<span data-ttu-id="758d3-141">Nazwa podmiotu certyfikatu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="758d3-141">The subject name of the certificate to be created.</span></span>

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

### <span data-ttu-id="758d3-142">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="758d3-142">-ClusterSize</span></span>
<span data-ttu-id="758d3-143">Liczba węzłów w klastrze.</span><span class="sxs-lookup"><span data-stu-id="758d3-143">The number of nodes in the cluster.</span></span> <span data-ttu-id="758d3-144">Domyślna to 5 węzłów.</span><span class="sxs-lookup"><span data-stu-id="758d3-144">Default are 5 nodes.</span></span>

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

### <span data-ttu-id="758d3-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="758d3-145">-DefaultProfile</span></span>
<span data-ttu-id="758d3-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="758d3-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="758d3-147">-Thebinding</span><span class="sxs-lookup"><span data-stu-id="758d3-147">-KeyVaultName</span></span>
<span data-ttu-id="758d3-148">Nazwa magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="758d3-148">Azure key vault name.</span></span> <span data-ttu-id="758d3-149">Jeśli nie zostanie podany, zostanie ona przyszukana domyślnie do nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="758d3-149">If not given, it will be defaulted to the resource group name.</span></span>

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

### <span data-ttu-id="758d3-150">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="758d3-150">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="758d3-151">Nazwa grupy zasobów magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="758d3-151">Azure key vault resource group name.</span></span> <span data-ttu-id="758d3-152">Jeśli nie zostanie podany, zostanie ona przyszukana domyślnie do nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="758d3-152">If not given, it will be defaulted to resource group name.</span></span>

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

### <span data-ttu-id="758d3-153">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="758d3-153">-Location</span></span>
<span data-ttu-id="758d3-154">Lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="758d3-154">The resource group location.</span></span>

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

### <span data-ttu-id="758d3-155">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="758d3-155">-Name</span></span>
<span data-ttu-id="758d3-156">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="758d3-156">Specify the name of the cluster.</span></span> <span data-ttu-id="758d3-157">Jeśli nie zostanie podany, będzie taka sama jak nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="758d3-157">If not given, it will be same as resource group name.</span></span>

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

### <span data-ttu-id="758d3-158">-OS</span><span class="sxs-lookup"><span data-stu-id="758d3-158">-OS</span></span>
<span data-ttu-id="758d3-159">System operacyjny maszyn wirtualnych, które tworzą klaster.</span><span class="sxs-lookup"><span data-stu-id="758d3-159">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="758d3-160">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="758d3-160">-ParameterFile</span></span>
<span data-ttu-id="758d3-161">Ścieżka do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="758d3-161">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="758d3-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="758d3-162">-ResourceGroupName</span></span>
<span data-ttu-id="758d3-163">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="758d3-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="758d3-164">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="758d3-164">-SecondaryCertificateFile</span></span>
<span data-ttu-id="758d3-165">Istniejąca ścieżka pliku certyfikatu dla pomocniczego certyfikatu klastra.</span><span class="sxs-lookup"><span data-stu-id="758d3-165">The existing certificate file path for the secondary cluster certificate.</span></span>

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

### <span data-ttu-id="758d3-166">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="758d3-166">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="758d3-167">Hasło pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="758d3-167">The password of the certificate file.</span></span>

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

### <span data-ttu-id="758d3-168">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="758d3-168">-SecretIdentifier</span></span>
<span data-ttu-id="758d3-169">Istniejący tajny adres URL magazynu kluczy platformy Azure, na przykład: ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '.</span><span class="sxs-lookup"><span data-stu-id="758d3-169">The existing Azure key vault secret URL, for example: 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'.</span></span>

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

### <span data-ttu-id="758d3-170">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="758d3-170">-TemplateFile</span></span>
<span data-ttu-id="758d3-171">Ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="758d3-171">The path to the template file.</span></span>

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

### <span data-ttu-id="758d3-172">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="758d3-172">-VmPassword</span></span>
<span data-ttu-id="758d3-173">Hasło maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="758d3-173">The password of the Vm.</span></span>

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

### <span data-ttu-id="758d3-174">-VmSku</span><span class="sxs-lookup"><span data-stu-id="758d3-174">-VmSku</span></span>
<span data-ttu-id="758d3-175">Wersja SKU maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="758d3-175">The Vm Sku.</span></span>

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

### <span data-ttu-id="758d3-176">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="758d3-176">-VmUserName</span></span>
<span data-ttu-id="758d3-177">Nazwa użytkownika służąca do logowania się do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="758d3-177">The user name for logging to Vm.</span></span>

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

### <span data-ttu-id="758d3-178">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="758d3-178">-Confirm</span></span>
<span data-ttu-id="758d3-179">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="758d3-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="758d3-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="758d3-180">-WhatIf</span></span>
<span data-ttu-id="758d3-181">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="758d3-181">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="758d3-182">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="758d3-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="758d3-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="758d3-183">CommonParameters</span></span>
<span data-ttu-id="758d3-184">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="758d3-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="758d3-185">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="758d3-185">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="758d3-186">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="758d3-186">INPUTS</span></span>

### <span data-ttu-id="758d3-187">System. String</span><span class="sxs-lookup"><span data-stu-id="758d3-187">System.String</span></span>

### <span data-ttu-id="758d3-188">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="758d3-188">System.Security.SecureString</span></span>

### <span data-ttu-id="758d3-189">System. Int32</span><span class="sxs-lookup"><span data-stu-id="758d3-189">System.Int32</span></span>

### <span data-ttu-id="758d3-190">Microsoft. Azure. Commands. servicefabric. MODELES. OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="758d3-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="758d3-191">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="758d3-191">OUTPUTS</span></span>

### <span data-ttu-id="758d3-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="758d3-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="758d3-193">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="758d3-193">NOTES</span></span>

## <span data-ttu-id="758d3-194">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="758d3-194">RELATED LINKS</span></span>
