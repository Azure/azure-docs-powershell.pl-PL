---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: f13b00ff0d9b0d3340cb0159714f1162cf5d0011
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873067"
---
# <span data-ttu-id="b0e7c-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="b0e7c-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="b0e7c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b0e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e7c-103">Dodaj pomocniczy certyfikat klastra do klastra.</span><span class="sxs-lookup"><span data-stu-id="b0e7c-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="b0e7c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b0e7c-104">SYNTAX</span></span>

### <span data-ttu-id="b0e7c-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="b0e7c-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0e7c-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="b0e7c-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0e7c-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="b0e7c-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0e7c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b0e7c-108">DESCRIPTION</span></span>
<span data-ttu-id="b0e7c-109">Użyj polecenia **Add-AzServiceFabricClusterCertificate** , aby dodać pomocniczy certyfikat klastra z istniejącego magazynu kluczy platformy Azure lub utworzyć nowy magazyn kluczy platformy Azure przy użyciu istniejącego certyfikatu lub z utworzonego nowego certyfikatu z podpisem własnym.</span><span class="sxs-lookup"><span data-stu-id="b0e7c-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="b0e7c-110">Spowoduje to zastąpienie klastra pomocniczego, jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="b0e7c-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="b0e7c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b0e7c-111">EXAMPLES</span></span>

### <span data-ttu-id="b0e7c-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b0e7c-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="b0e7c-113">To polecenie spowoduje dodanie certyfikatu w istniejącym magazynie kluczy platformy Azure jako pomocniczy certyfikat klastra.</span><span class="sxs-lookup"><span data-stu-id="b0e7c-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="b0e7c-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b0e7c-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="b0e7c-115">To polecenie utworzy certyfikat z podpisem własnym w magazynie kluczy usługi Azure i uaktualni klaster, aby używać go jako pomocniczego certyfikatu klastra.</span><span class="sxs-lookup"><span data-stu-id="b0e7c-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="b0e7c-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0e7c-116">PARAMETERS</span></span>

### <span data-ttu-id="b0e7c-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="b0e7c-117">-CertificateCommonName</span></span>
<span data-ttu-id="b0e7c-118">Nazwa pospolita certyfikatu</span><span class="sxs-lookup"><span data-stu-id="b0e7c-118">Certificate common name</span></span>

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

### <span data-ttu-id="b0e7c-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b0e7c-119">-CertificateFile</span></span>
<span data-ttu-id="b0e7c-120">Ścieżka do istniejącego certyfikatu</span><span class="sxs-lookup"><span data-stu-id="b0e7c-120">The path to the existing certificate</span></span>

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

### <span data-ttu-id="b0e7c-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="b0e7c-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="b0e7c-122">Odcisk palca wystawcy certyfikatu, oddzielony przecinkami, jeśli więcej niż jeden</span><span class="sxs-lookup"><span data-stu-id="b0e7c-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="b0e7c-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="b0e7c-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="b0e7c-124">Folder, w którym należy pobrać nowy certyfikat.</span><span class="sxs-lookup"><span data-stu-id="b0e7c-124">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="b0e7c-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="b0e7c-125">-CertificatePassword</span></span>
<span data-ttu-id="b0e7c-126">Hasło certyfikatu</span><span class="sxs-lookup"><span data-stu-id="b0e7c-126">The password of the certificate</span></span>

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

### <span data-ttu-id="b0e7c-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="b0e7c-127">-CertificateSubjectName</span></span>
<span data-ttu-id="b0e7c-128">Nazwa podmiotu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="b0e7c-128">The subject name of the certificate</span></span>

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

### <span data-ttu-id="b0e7c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0e7c-129">-DefaultProfile</span></span>
<span data-ttu-id="b0e7c-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0e7c-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0e7c-131">-Thebinding</span><span class="sxs-lookup"><span data-stu-id="b0e7c-131">-KeyVaultName</span></span>
<span data-ttu-id="b0e7c-132">Nazwa magazynu kluczy platformy Azure, jeśli nie została określona, zostanie przeszukana domyślnie w nazwie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b0e7c-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="b0e7c-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0e7c-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="b0e7c-134">Nazwa grupy zasobów magazynu kluczy platformy Azure, jeśli nie została podana, zostanie domyślnie określona jako nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b0e7c-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0e7c-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b0e7c-135">-Name</span></span>
<span data-ttu-id="b0e7c-136">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="b0e7c-136">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="b0e7c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0e7c-137">-ResourceGroupName</span></span>
<span data-ttu-id="b0e7c-138">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b0e7c-138">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b0e7c-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="b0e7c-139">-SecretIdentifier</span></span>
<span data-ttu-id="b0e7c-140">Istniejący tajny adres URL magazynu kluczy platformy Azure, na przykład ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="b0e7c-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="b0e7c-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b0e7c-141">-Confirm</span></span>
<span data-ttu-id="b0e7c-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0e7c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0e7c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0e7c-143">-WhatIf</span></span>
<span data-ttu-id="b0e7c-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0e7c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0e7c-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b0e7c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0e7c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e7c-146">CommonParameters</span></span>
<span data-ttu-id="b0e7c-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0e7c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e7c-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0e7c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e7c-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0e7c-149">INPUTS</span></span>

### <span data-ttu-id="b0e7c-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b0e7c-150">System.String</span></span>

### <span data-ttu-id="b0e7c-151">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="b0e7c-151">System.Security.SecureString</span></span>

## <span data-ttu-id="b0e7c-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b0e7c-152">OUTPUTS</span></span>

### <span data-ttu-id="b0e7c-153">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="b0e7c-153">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b0e7c-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b0e7c-154">NOTES</span></span>

## <span data-ttu-id="b0e7c-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0e7c-155">RELATED LINKS</span></span>

[<span data-ttu-id="b0e7c-156">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="b0e7c-156">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="b0e7c-157">Nowe — AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="b0e7c-157">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)

[<span data-ttu-id="b0e7c-158">Dodaj-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="b0e7c-158">Add-AzServiceFabricApplicationCertificate</span></span>](./Add-AzServiceFabricApplicationCertificate.md)
