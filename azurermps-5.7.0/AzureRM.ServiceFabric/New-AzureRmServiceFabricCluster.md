---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/new-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 5da8d1f48a50cafc970278d59b99750f283a9414
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549547"
---
# <span data-ttu-id="b8ea3-101">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="b8ea3-101">New-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="b8ea3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ea3-103">To polecenie używa certyfikatów, które zostały podane, lub system wygenerował certyfikaty z podpisem własnym, aby skonfigurować nowy klaster programu Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="b8ea3-104">Może on używać szablonu domyślnego lub szablonu niestandardowego, który jest udostępniany.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="b8ea3-105">Możesz określić folder do eksportowania certyfikatów z podpisem własnym lub pobrać je później z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8ea3-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8ea3-106">SYNTAX</span></span>

### <span data-ttu-id="b8ea3-107">ByDefaultArmTemplate (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b8ea3-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8ea3-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="b8ea3-108">ByExistingKeyVault</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-VmPassword <SecureString>] -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8ea3-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="b8ea3-109">ByNewPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>]
 [-KeyVaultName <String>] [-CertificateSubjectName <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8ea3-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="b8ea3-110">ByExistingPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8ea3-111">Opis</span><span class="sxs-lookup"><span data-stu-id="b8ea3-111">DESCRIPTION</span></span>
<span data-ttu-id="b8ea3-112">W poleceniu **New-AzureRmServiceFabricCluster** są używane certyfikaty, które zostały podane, lub system wygenerował certyfikaty z podpisem własnym, aby skonfigurować nowy klaster programu Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-112">The **New-AzureRmServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="b8ea3-113">Szablon, którego używasz, może być szablonem domyślnym lub szablonem niestandardowym.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="b8ea3-114">Możesz określić folder do eksportowania certyfikatów z podpisem własnym lub pobrać je później z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>

<span data-ttu-id="b8ea3-115">Jeśli określisz szablon niestandardowy i plik parametrów, nie musisz dostarczać informacji o certyfikacie w pliku parametru, system wypełni te parametry.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>

<span data-ttu-id="b8ea3-116">Poniżej wymieniono cztery opcje.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-116">The four options are detailed below.</span></span> <span data-ttu-id="b8ea3-117">Przewiń w dół, aby zapoznać się z objaśnieniami każdego z parametrów.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="b8ea3-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8ea3-118">EXAMPLES</span></span>

### <span data-ttu-id="b8ea3-119">Przykład 1: Określ tylko rozmiar klastra, nazwę podmiotu certyfikatu oraz system operacyjny, aby wdrożyć klaster.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="~\Documents"

Write-Output "Create cluster in '$clusterloc' with cert subject name '$subname' and cert output path '$pfxfolder'"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 3 -VmPassword $pass -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="b8ea3-120">To polecenie umożliwia określenie rozmiaru klastra, nazwy podmiotu certyfikatu i systemu operacyjnego w celu wdrożenia klastra.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="b8ea3-121">Przykład 2: Określanie istniejącego zasobu certyfikatu w magazynie kluczy oraz szablonu niestandardowego do wdrożenia klastra</span><span class="sxs-lookup"><span data-stu-id="b8ea3-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secretId
```

<span data-ttu-id="b8ea3-122">To polecenie umożliwia określenie istniejącego zasobu certyfikatu w magazynie kluczy oraz szablonu niestandardowego do wdrożenia klastra.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="b8ea3-123">Przykład 3: Tworzenie nowego klastra przy użyciu szablonu niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="b8ea3-124">Określanie innej nazwy grupy zasobów dla magazynu kluczy oraz przekazywanie przez system nowego certyfikatu</span><span class="sxs-lookup"><span data-stu-id="b8ea3-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>
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

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="b8ea3-125">To polecenie tworzy nowy klaster przy użyciu szablonu niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="b8ea3-126">Określanie innej nazwy grupy zasobów dla magazynu kluczy oraz przekazywanie przez system nowego certyfikatu</span><span class="sxs-lookup"><span data-stu-id="b8ea3-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="b8ea3-127">Przykład 4: przenoszenie własnego certyfikatu i szablonu niestandardowego oraz tworzenie nowego klastra</span><span class="sxs-lookup"><span data-stu-id="b8ea3-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateFile $pfxsourcefile -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="b8ea3-128">To polecenie umożliwia przeprowadzenie własnego certyfikatu i szablonu niestandardowego oraz utworzenie nowego klastra.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="b8ea3-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8ea3-129">PARAMETERS</span></span>

### <span data-ttu-id="b8ea3-130">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b8ea3-130">-CertificateFile</span></span>
<span data-ttu-id="b8ea3-131">Istniejąca ścieżka pliku certyfikatu podstawowego certyfikatu klastra.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-131">The existing certificate file path for the primary cluster certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-132">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="b8ea3-132">-CertificateOutputFolder</span></span>
<span data-ttu-id="b8ea3-133">Folder nowego pliku certyfikatu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-133">The folder of the new certificate file to be created.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-134">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="b8ea3-134">-CertificatePassword</span></span>
<span data-ttu-id="b8ea3-135">Hasło pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-135">The password of the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-136">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="b8ea3-136">-CertificateSubjectName</span></span>
<span data-ttu-id="b8ea3-137">Nazwa podmiotu certyfikatu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-137">The subject name of the certificate to be created.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Subject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-138">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="b8ea3-138">-ClusterSize</span></span>
<span data-ttu-id="b8ea3-139">Liczba węzłów w klastrze.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-139">The number of nodes in the cluster.</span></span> <span data-ttu-id="b8ea3-140">Domyślna to 5 węzłów.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-140">Default are 5 nodes.</span></span>

```yaml
Type: Int32
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8ea3-141">-DefaultProfile</span></span>
<span data-ttu-id="b8ea3-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-143">-Thebinding</span><span class="sxs-lookup"><span data-stu-id="b8ea3-143">-KeyVaultName</span></span>
<span data-ttu-id="b8ea3-144">Nazwa magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-144">Azure key vault name.</span></span> <span data-ttu-id="b8ea3-145">Jeśli nie zostanie podany, zostanie ona przyszukana domyślnie do nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-145">If not given, it will be defaulted to the resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-146">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8ea3-146">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="b8ea3-147">Nazwa grupy zasobów magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-147">Azure key vault resource group name.</span></span> <span data-ttu-id="b8ea3-148">Jeśli nie zostanie podany, zostanie ona przyszukana domyślnie do nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-148">If not given, it will be defaulted to resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-149">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b8ea3-149">-Location</span></span>
<span data-ttu-id="b8ea3-150">Lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-150">The resource group location.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-151">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b8ea3-151">-Name</span></span>
<span data-ttu-id="b8ea3-152">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-152">Specify the name of the cluster.</span></span> <span data-ttu-id="b8ea3-153">Jeśli nie zostanie podany, będzie taka sama jak nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-153">If not given, it will be same as resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: ClusterName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-154">-OS</span><span class="sxs-lookup"><span data-stu-id="b8ea3-154">-OS</span></span>
<span data-ttu-id="b8ea3-155">System operacyjny maszyn wirtualnych, które tworzą klaster.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-155">The Operating System of the VMs that make up the cluster.</span></span>

```yaml
Type: OperatingSystem
Parameter Sets: ByDefaultArmTemplate
Aliases: VmImage
Accepted values: WindowsServer2012R2Datacenter, WindowsServer2016Datacenter, WindowsServer2016DatacenterwithContainers, UbuntuServer1604

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-156">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="b8ea3-156">-ParameterFile</span></span>
<span data-ttu-id="b8ea3-157">Ścieżka do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-157">The path to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8ea3-158">-ResourceGroupName</span></span>
<span data-ttu-id="b8ea3-159">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-159">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-160">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="b8ea3-160">-SecondaryCertificateFile</span></span>
<span data-ttu-id="b8ea3-161">Istniejąca ścieżka pliku certyfikatu dla pomocniczego certyfikatu klastra.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-161">The existing certificate file path for the secondary cluster certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecSource

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-162">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="b8ea3-162">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="b8ea3-163">Hasło pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-163">The password of the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecCertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-164">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="b8ea3-164">-SecretIdentifier</span></span>
<span data-ttu-id="b8ea3-165">Istniejący tajny adres URL magazynu kluczy platformy Azure, na przykład: ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-165">The existing Azure key vault secret URL, for example: 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingKeyVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-166">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="b8ea3-166">-TemplateFile</span></span>
<span data-ttu-id="b8ea3-167">Ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-167">The path to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-168">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="b8ea3-168">-VmPassword</span></span>
<span data-ttu-id="b8ea3-169">Hasło maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-169">The password of the Vm.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: SecureString
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-170">-VmSku</span><span class="sxs-lookup"><span data-stu-id="b8ea3-170">-VmSku</span></span>
<span data-ttu-id="b8ea3-171">Wersja SKU maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-171">The Vm Sku.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: Sku

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-172">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="b8ea3-172">-VmUserName</span></span>
<span data-ttu-id="b8ea3-173">Nazwa użytkownika służąca do logowania się do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-173">The user name for logging to Vm.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-174">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b8ea3-174">-Confirm</span></span>
<span data-ttu-id="b8ea3-175">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8ea3-176">-WhatIf</span></span>
<span data-ttu-id="b8ea3-177">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-177">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8ea3-178">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-178">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ea3-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ea3-179">CommonParameters</span></span>
<span data-ttu-id="b8ea3-180">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8ea3-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ea3-181">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8ea3-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ea3-182">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8ea3-182">INPUTS</span></span>

### <span data-ttu-id="b8ea3-183">System. String</span><span class="sxs-lookup"><span data-stu-id="b8ea3-183">System.String</span></span>
<span data-ttu-id="b8ea3-184">System. Security. SecureString system. Int32 Microsoft. Azure. Commands. servicefabric. MODELES. OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="b8ea3-184">System.Security.SecureString System.Int32 Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="b8ea3-185">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8ea3-185">OUTPUTS</span></span>

### <span data-ttu-id="b8ea3-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="b8ea3-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="b8ea3-187">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8ea3-187">NOTES</span></span>

## <span data-ttu-id="b8ea3-188">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8ea3-188">RELATED LINKS</span></span>

