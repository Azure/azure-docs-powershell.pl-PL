---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
ms.openlocfilehash: 58547205bc0edae3ea1ab9ff56d3df1ef71214f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708092"
---
# <span data-ttu-id="306f6-101">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="306f6-101">Add-AzServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="306f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="306f6-102">SYNOPSIS</span></span>
<span data-ttu-id="306f6-103">Dodaj nowy certyfikat do zestawów skali maszyny wirtualnej, które tworzą klaster.</span><span class="sxs-lookup"><span data-stu-id="306f6-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="306f6-104">Certyfikat jest przeznaczony do użytku jako certyfikat aplikacji.</span><span class="sxs-lookup"><span data-stu-id="306f6-104">The certificate is intended to be used as an application certificate.</span></span>

## <span data-ttu-id="306f6-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="306f6-105">SYNTAX</span></span>

### <span data-ttu-id="306f6-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="306f6-106">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="306f6-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="306f6-107">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="306f6-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="306f6-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="306f6-109">Opis</span><span class="sxs-lookup"><span data-stu-id="306f6-109">DESCRIPTION</span></span>
<span data-ttu-id="306f6-110">Użyj **dodatku Add-AzServiceFabricApplicationCertificate** , aby zainstalować certyfikat we wszystkich węzłach w klastrze.</span><span class="sxs-lookup"><span data-stu-id="306f6-110">Use **Add-AzServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="306f6-111">Możesz określić certyfikat, który już masz, lub który wygenerował nowy system, i przekazać go do nowego lub istniejącego magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="306f6-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="306f6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="306f6-112">EXAMPLES</span></span>

### <span data-ttu-id="306f6-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="306f6-113">Example 1</span></span>
```
PS c:> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="306f6-114">To polecenie spowoduje dodanie certyfikatu z istniejącego magazynu kluczy platformy Azure do wszystkich typów węzłów klastra.</span><span class="sxs-lookup"><span data-stu-id="306f6-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="306f6-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="306f6-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="306f6-116">To polecenie utworzy certyfikat z podpisem własnym w magazynie kluczy platformy Azure z nazwą grupy zasobów magazynu kluczy i nazwą magazynu kluczy, zostanie zainstalowany na wszystkich typach węzłów klastra i pobierze certyfikat w obszarze folder "c:\Test".</span><span class="sxs-lookup"><span data-stu-id="306f6-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="306f6-117">Nazwa pobranego certyfikatu jest taka sama jak nazwa certyfikatu magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="306f6-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="306f6-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="306f6-118">PARAMETERS</span></span>

### <span data-ttu-id="306f6-119">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="306f6-119">-CertificateCommonName</span></span>
<span data-ttu-id="306f6-120">Nazwa pospolita certyfikatu</span><span class="sxs-lookup"><span data-stu-id="306f6-120">Certificate common name</span></span>

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

### <span data-ttu-id="306f6-121">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="306f6-121">-CertificateFile</span></span>
<span data-ttu-id="306f6-122">Istniejąca ścieżka pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="306f6-122">The existing certificate file path.</span></span>

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

### <span data-ttu-id="306f6-123">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="306f6-123">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="306f6-124">Odcisk palca wystawcy certyfikatu, oddzielony przecinkami, jeśli więcej niż jeden</span><span class="sxs-lookup"><span data-stu-id="306f6-124">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="306f6-125">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="306f6-125">-CertificateOutputFolder</span></span>
<span data-ttu-id="306f6-126">Ścieżka folderu nowego certyfikatu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="306f6-126">The folder path of the new certificate to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="306f6-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="306f6-127">-CertificatePassword</span></span>
<span data-ttu-id="306f6-128">Hasło pliku PFX.</span><span class="sxs-lookup"><span data-stu-id="306f6-128">The password of the pfx file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="306f6-129">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="306f6-129">-CertificateSubjectName</span></span>
<span data-ttu-id="306f6-130">Nazwa DNS certyfikatu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="306f6-130">The Dns name of the certificate to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Subject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="306f6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="306f6-131">-DefaultProfile</span></span>
<span data-ttu-id="306f6-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="306f6-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="306f6-133">-Thebinding</span><span class="sxs-lookup"><span data-stu-id="306f6-133">-KeyVaultName</span></span>
<span data-ttu-id="306f6-134">Nazwa magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="306f6-134">Azure key vault name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="306f6-135">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="306f6-135">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="306f6-136">Nazwa grupy zasobów magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="306f6-136">Azure key vault resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="306f6-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="306f6-137">-Name</span></span>
<span data-ttu-id="306f6-138">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="306f6-138">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="306f6-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="306f6-139">-ResourceGroupName</span></span>
<span data-ttu-id="306f6-140">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="306f6-140">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="306f6-141">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="306f6-141">-SecretIdentifier</span></span>
<span data-ttu-id="306f6-142">Istniejący identyfikator URI tajnego magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="306f6-142">The existing Azure key vault secret uri.</span></span>

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

### <span data-ttu-id="306f6-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="306f6-143">-Confirm</span></span>
<span data-ttu-id="306f6-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="306f6-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="306f6-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="306f6-145">-WhatIf</span></span>
<span data-ttu-id="306f6-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="306f6-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="306f6-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="306f6-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="306f6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="306f6-148">CommonParameters</span></span>
<span data-ttu-id="306f6-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="306f6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="306f6-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="306f6-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="306f6-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="306f6-151">INPUTS</span></span>

### <span data-ttu-id="306f6-152">System. String</span><span class="sxs-lookup"><span data-stu-id="306f6-152">System.String</span></span>

### <span data-ttu-id="306f6-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="306f6-153">System.Security.SecureString</span></span>

## <span data-ttu-id="306f6-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="306f6-154">OUTPUTS</span></span>

### <span data-ttu-id="306f6-155">Microsoft. Azure. Commands. servicefabric. MODELES. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="306f6-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="306f6-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="306f6-156">NOTES</span></span>

## <span data-ttu-id="306f6-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="306f6-157">RELATED LINKS</span></span>

[<span data-ttu-id="306f6-158">Dodaj-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="306f6-158">Add-AzServiceFabricClusterCertificate</span></span>](./Add-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="306f6-159">Nowe — AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="306f6-159">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
