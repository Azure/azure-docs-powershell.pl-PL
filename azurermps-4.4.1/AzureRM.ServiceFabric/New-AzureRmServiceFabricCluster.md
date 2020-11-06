---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
ms.openlocfilehash: c1f6dea6c4fb103107a052d64a82ad81eafdb8c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553757"
---
# <span data-ttu-id="b27ae-101">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="b27ae-101">New-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="b27ae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b27ae-102">SYNOPSIS</span></span>
<span data-ttu-id="b27ae-103">To polecenie używa certyfikatów, które zostały podane, lub system wygenerował certyfikaty z podpisem własnym, aby skonfigurować nowy klaster programu Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="b27ae-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="b27ae-104">Może on używać szablonu domyślnego lub szablonu niestandardowego, który jest udostępniany.</span><span class="sxs-lookup"><span data-stu-id="b27ae-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="b27ae-105">Możesz określić folder do eksportowania certyfikatów z podpisem własnym lub pobrać je później z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="b27ae-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b27ae-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b27ae-106">SYNTAX</span></span>

### <span data-ttu-id="b27ae-107">ByDefaultArmTemplate (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b27ae-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b27ae-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="b27ae-108">ByExistingKeyVault</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b27ae-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="b27ae-109">ByNewPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>]
 [-KeyVaultName <String>] [-CertificateSubjectName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b27ae-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="b27ae-110">ByExistingPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b27ae-111">Opis</span><span class="sxs-lookup"><span data-stu-id="b27ae-111">DESCRIPTION</span></span>
<span data-ttu-id="b27ae-112">W poleceniu **New-AzureRmServiceFabricCluster** są używane certyfikaty, które zostały podane, lub system wygenerował certyfikaty z podpisem własnym, aby skonfigurować nowy klaster programu Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="b27ae-112">The **New-AzureRmServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="b27ae-113">Szablon, którego używasz, może być szablonem domyślnym lub szablonem niestandardowym.</span><span class="sxs-lookup"><span data-stu-id="b27ae-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="b27ae-114">Możesz określić folder do eksportowania certyfikatów z podpisem własnym lub pobrać je później z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="b27ae-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>

<span data-ttu-id="b27ae-115">Jeśli określisz szablon niestandardowy i plik parametrów, nie musisz dostarczać informacji o certyfikacie w pliku parametru, system wypełni te parametry.</span><span class="sxs-lookup"><span data-stu-id="b27ae-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>

<span data-ttu-id="b27ae-116">Poniżej wymieniono cztery opcje.</span><span class="sxs-lookup"><span data-stu-id="b27ae-116">The four options are detailed below.</span></span> <span data-ttu-id="b27ae-117">Przewiń w dół, aby zapoznać się z objaśnieniami każdego z parametrów.</span><span class="sxs-lookup"><span data-stu-id="b27ae-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="b27ae-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b27ae-118">EXAMPLES</span></span>

### <span data-ttu-id="b27ae-119">Przykład 1: Określ tylko rozmiar klastra, nazwę podmiotu certyfikatu oraz system operacyjny, aby wdrożyć klaster.</span><span class="sxs-lookup"><span data-stu-id="b27ae-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="~\Documents"

Write-Output "create cluster in " $clusterloc "subject name for cert " $subname "and output the cert into " $pfxfolder

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 3 -VmPassword $pwd -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pwd -OS WindowsServer2016Datacenter
```

<span data-ttu-id="b27ae-120">To polecenie umożliwia określenie rozmiaru klastra, nazwy podmiotu certyfikatu i systemu operacyjnego w celu wdrożenia klastra.</span><span class="sxs-lookup"><span data-stu-id="b27ae-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="b27ae-121">Przykład 2: Określanie istniejącego zasobu certyfikatu w magazynie kluczy oraz szablonu niestandardowego do wdrożenia klastra</span><span class="sxs-lookup"><span data-stu-id="b27ae-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secertId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secertId
```

<span data-ttu-id="b27ae-122">To polecenie umożliwia określenie istniejącego zasobu certyfikatu w magazynie kluczy oraz szablonu niestandardowego do wdrożenia klastra.</span><span class="sxs-lookup"><span data-stu-id="b27ae-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="b27ae-123">Przykład 3: Tworzenie nowego klastra przy użyciu szablonu niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="b27ae-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="b27ae-124">Określanie innej nazwy RG dla magazynu kluczy i załadowanie do niego certyfikatu przez system.</span><span class="sxs-lookup"><span data-stu-id="b27ae-124">Specify the different RG name for the key vault and have the system upload the certificate to it</span></span>
```
$pwd="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.$clusterloc.cloudapp.azure.com" -f $RGName, $clusterloc
$pfxfolder="~\Documents"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secertId="https://test1.vault.azure.net:443/secrets/testcertificate4/55ec7c4dc61a462bbc645ffc9b4b225f"
$thumprint="C2D7E11DD35153A702A51D10A424A3014B9B6E8B"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pwd -KeyVaultResouceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="b27ae-125">To polecenie tworzy nowy klaster przy użyciu szablonu niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="b27ae-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="b27ae-126">Określ inną nazwę RG dla magazynu kluczy, a system przekaże certyfikat.</span><span class="sxs-lookup"><span data-stu-id="b27ae-126">Specify the different RG name for the key vault and have the system upload the certificate to it.</span></span>

### <span data-ttu-id="b27ae-127">Przykład 4: przenoszenie własnego certyfikatu i szablonu niestandardowego oraz tworzenie nowego klastra</span><span class="sxs-lookup"><span data-stu-id="b27ae-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$certPwd="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateSourceFile $pfxsourcefile -CertificatePassword $certpwd -KeyVaultResouceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="b27ae-128">To polecenie umożliwia przeprowadzenie własnego certyfikatu i szablonu niestandardowego oraz utworzenie nowego klastra.</span><span class="sxs-lookup"><span data-stu-id="b27ae-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="b27ae-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b27ae-129">PARAMETERS</span></span>

### <span data-ttu-id="b27ae-130">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b27ae-130">-CertificateFile</span></span>
<span data-ttu-id="b27ae-131">Istniejąca ścieżka pliku certyfikatu podstawowego certyfikatu klastra.</span><span class="sxs-lookup"><span data-stu-id="b27ae-131">The existing certificate file path for the primary cluster certificate.</span></span>

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

### <span data-ttu-id="b27ae-132">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="b27ae-132">-CertificateOutputFolder</span></span>
<span data-ttu-id="b27ae-133">Folder nowego pliku certyfikatu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="b27ae-133">The folder of the new certificate file to be created.</span></span>

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

### <span data-ttu-id="b27ae-134">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="b27ae-134">-CertificatePassword</span></span>
<span data-ttu-id="b27ae-135">Hasło pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b27ae-135">The password of the certificate file.</span></span>

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

### <span data-ttu-id="b27ae-136">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="b27ae-136">-CertificateSubjectName</span></span>
<span data-ttu-id="b27ae-137">Nazwa podmiotu certyfikatu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="b27ae-137">The subject name of the certificate to be created.</span></span>

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

### <span data-ttu-id="b27ae-138">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="b27ae-138">-ClusterSize</span></span>
<span data-ttu-id="b27ae-139">Liczba węzłów w klastrze.</span><span class="sxs-lookup"><span data-stu-id="b27ae-139">The number of nodes in the cluster.</span></span> <span data-ttu-id="b27ae-140">Domyślna to 5 węzłów.</span><span class="sxs-lookup"><span data-stu-id="b27ae-140">Default are 5 nodes.</span></span>

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

### <span data-ttu-id="b27ae-141">-Thebinding</span><span class="sxs-lookup"><span data-stu-id="b27ae-141">-KeyVaultName</span></span>
<span data-ttu-id="b27ae-142">Nazwa magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b27ae-142">Azure key vault name.</span></span> <span data-ttu-id="b27ae-143">Jeśli nie zostanie podany, zostanie ona przyszukana domyślnie do nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b27ae-143">If not given, it will be defaulted to the resource group name.</span></span>

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

### <span data-ttu-id="b27ae-144">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="b27ae-144">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="b27ae-145">Nazwa grupy zasobów magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b27ae-145">Azure key vault resource group name.</span></span> <span data-ttu-id="b27ae-146">Jeśli nie zostanie podany, zostanie ona przyszukana domyślnie do nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b27ae-146">If not given, it will be defaulted to resource group name.</span></span>

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

### <span data-ttu-id="b27ae-147">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b27ae-147">-Location</span></span>
<span data-ttu-id="b27ae-148">Lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b27ae-148">The resource group location.</span></span>

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

### <span data-ttu-id="b27ae-149">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b27ae-149">-Name</span></span>
<span data-ttu-id="b27ae-150">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="b27ae-150">Specify the name of the cluster.</span></span> <span data-ttu-id="b27ae-151">Jeśli nie zostanie podany, będzie taka sama jak nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b27ae-151">If not given, it will be same as resource group name.</span></span>

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

### <span data-ttu-id="b27ae-152">-OS</span><span class="sxs-lookup"><span data-stu-id="b27ae-152">-OS</span></span>
<span data-ttu-id="b27ae-153">System operacyjny maszyn wirtualnych, które tworzą klaster.</span><span class="sxs-lookup"><span data-stu-id="b27ae-153">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="b27ae-154">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="b27ae-154">-ParameterFile</span></span>
<span data-ttu-id="b27ae-155">Ścieżka do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="b27ae-155">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="b27ae-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b27ae-156">-ResourceGroupName</span></span>
<span data-ttu-id="b27ae-157">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b27ae-157">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b27ae-158">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="b27ae-158">-SecondaryCertificateFile</span></span>
<span data-ttu-id="b27ae-159">Istniejąca ścieżka pliku certyfikatu dla pomocniczego certyfikatu klastra.</span><span class="sxs-lookup"><span data-stu-id="b27ae-159">The existing certificate file path for the secondary cluster certificate.</span></span>

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

### <span data-ttu-id="b27ae-160">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="b27ae-160">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="b27ae-161">Hasło pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b27ae-161">The password of the certificate file.</span></span>

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

### <span data-ttu-id="b27ae-162">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="b27ae-162">-SecretIdentifier</span></span>
<span data-ttu-id="b27ae-163">Istniejący tajny adres URL magazynu kluczy platformy Azure, na przykład: ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '.</span><span class="sxs-lookup"><span data-stu-id="b27ae-163">The existing Azure key vault secret URL, for example: 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'.</span></span>

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

### <span data-ttu-id="b27ae-164">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="b27ae-164">-TemplateFile</span></span>
<span data-ttu-id="b27ae-165">Ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="b27ae-165">The path to the template file.</span></span>

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

### <span data-ttu-id="b27ae-166">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="b27ae-166">-VmPassword</span></span>
<span data-ttu-id="b27ae-167">Hasło maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b27ae-167">The password of the Vm.</span></span>

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

### <span data-ttu-id="b27ae-168">-VmSku</span><span class="sxs-lookup"><span data-stu-id="b27ae-168">-VmSku</span></span>
<span data-ttu-id="b27ae-169">Wersja SKU maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b27ae-169">The Vm Sku.</span></span>

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

### <span data-ttu-id="b27ae-170">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="b27ae-170">-VmUserName</span></span>
<span data-ttu-id="b27ae-171">Nazwa użytkownika służąca do logowania się do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b27ae-171">The user name for logging to Vm.</span></span>

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

### <span data-ttu-id="b27ae-172">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b27ae-172">-Confirm</span></span>
<span data-ttu-id="b27ae-173">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b27ae-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b27ae-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b27ae-174">-WhatIf</span></span>
<span data-ttu-id="b27ae-175">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b27ae-175">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b27ae-176">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b27ae-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b27ae-177">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b27ae-177">-DefaultProfile</span></span>
<span data-ttu-id="b27ae-178">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b27ae-178">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27ae-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b27ae-179">CommonParameters</span></span>
<span data-ttu-id="b27ae-180">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b27ae-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b27ae-181">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b27ae-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b27ae-182">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b27ae-182">INPUTS</span></span>

### <span data-ttu-id="b27ae-183">System. String</span><span class="sxs-lookup"><span data-stu-id="b27ae-183">System.String</span></span>
<span data-ttu-id="b27ae-184">System. Security. SecureString system. Int32 Microsoft. Azure. Commands. servicefabric. MODELES. OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="b27ae-184">System.Security.SecureString System.Int32 Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="b27ae-185">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b27ae-185">OUTPUTS</span></span>

### <span data-ttu-id="b27ae-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="b27ae-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="b27ae-187">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b27ae-187">NOTES</span></span>

## <span data-ttu-id="b27ae-188">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b27ae-188">RELATED LINKS</span></span>

