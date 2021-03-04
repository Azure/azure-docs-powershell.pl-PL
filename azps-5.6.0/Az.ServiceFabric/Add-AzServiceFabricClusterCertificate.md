---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 379bd710413fee83a2fdb6b10dc7fb42f0f207bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969873"
---
# <span data-ttu-id="6ceda-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6ceda-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="6ceda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ceda-102">SYNOPSIS</span></span>
<span data-ttu-id="6ceda-103">Dodawanie certyfikatu klasteru pomocniczego do klastrów.</span><span class="sxs-lookup"><span data-stu-id="6ceda-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="6ceda-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6ceda-104">SYNTAX</span></span>

### <span data-ttu-id="6ceda-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="6ceda-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-Thumbprint <String>] [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ceda-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="6ceda-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ceda-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="6ceda-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ceda-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6ceda-108">DESCRIPTION</span></span>
<span data-ttu-id="6ceda-109">Użyj dodatku **AzServiceFabricClusterCertificate,** aby dodać certyfikat klasteru pomocniczego z istniejącego magazynu kluczy platformy Azure lub tworząc nowy magazyn kluczy platformy Azure przy użyciu istniejącego certyfikatu dostarczonego lub na podstawie nowo utworzonego certyfikatu z podpisem własnym.</span><span class="sxs-lookup"><span data-stu-id="6ceda-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="6ceda-110">Jeśli istnieje, zastąpi on klaster pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="6ceda-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="6ceda-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6ceda-111">EXAMPLES</span></span>

### <span data-ttu-id="6ceda-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6ceda-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="6ceda-113">To polecenie spowoduje dodanie certyfikatu w istniejącym magazynie kluczy platformy Azure jako certyfikatu klasteru pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="6ceda-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="6ceda-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6ceda-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="6ceda-115">To polecenie utworzy certyfikat z podpisem własnym w magazynie kluczy platformy Azure i uaktualni klaster, aby użyć go jako certyfikatu klasteru pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="6ceda-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="6ceda-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ceda-116">PARAMETERS</span></span>

### <span data-ttu-id="6ceda-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="6ceda-117">-CertificateCommonName</span></span>
<span data-ttu-id="6ceda-118">Nazwa pospolita certyfikatu</span><span class="sxs-lookup"><span data-stu-id="6ceda-118">Certificate common name</span></span>

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

### <span data-ttu-id="6ceda-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="6ceda-119">-CertificateFile</span></span>
<span data-ttu-id="6ceda-120">Ścieżka do istniejącego certyfikatu</span><span class="sxs-lookup"><span data-stu-id="6ceda-120">The path to the existing certificate</span></span>

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

### <span data-ttu-id="6ceda-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="6ceda-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="6ceda-122">Thumbprint wystawcy certyfikatu oddzielony przecinkami, jeśli jest ich więcej niż jeden</span><span class="sxs-lookup"><span data-stu-id="6ceda-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="6ceda-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="6ceda-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="6ceda-124">Folder, do którego należy pobrać nowy certyfikat.</span><span class="sxs-lookup"><span data-stu-id="6ceda-124">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="6ceda-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="6ceda-125">-CertificatePassword</span></span>
<span data-ttu-id="6ceda-126">Hasło certyfikatu</span><span class="sxs-lookup"><span data-stu-id="6ceda-126">The password of the certificate</span></span>

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

### <span data-ttu-id="6ceda-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="6ceda-127">-CertificateSubjectName</span></span>
<span data-ttu-id="6ceda-128">Nazwa podmiotu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="6ceda-128">The subject name of the certificate</span></span>

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

### <span data-ttu-id="6ceda-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ceda-129">-DefaultProfile</span></span>
<span data-ttu-id="6ceda-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ceda-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ceda-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="6ceda-131">-KeyVaultName</span></span>
<span data-ttu-id="6ceda-132">Nazwa magazynu kluczy platformy Azure, jeśli nie zostanie nadana, zostanie domyślnie nadana nazwie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6ceda-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="6ceda-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ceda-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="6ceda-134">Nazwa grupy zasobów magazynu klucza platformy Azure, jeśli nie zostanie nadana, zostanie domyślnie nadana nazwie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6ceda-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="6ceda-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6ceda-135">-Name</span></span>
<span data-ttu-id="6ceda-136">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="6ceda-136">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="6ceda-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ceda-137">-ResourceGroupName</span></span>
<span data-ttu-id="6ceda-138">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6ceda-138">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="6ceda-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="6ceda-139">-SecretIdentifier</span></span>
<span data-ttu-id="6ceda-140">Istniejący tajny adres URL magazynu kluczy platformy Azure, na przykład https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="6ceda-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="6ceda-141">- Thumbprint</span><span class="sxs-lookup"><span data-stu-id="6ceda-141">-Thumbprint</span></span>
<span data-ttu-id="6ceda-142">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span><span class="sxs-lookup"><span data-stu-id="6ceda-142">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="6ceda-143">Użyj tego polecenia, jeśli certyfikat nie jest zarządzany, ponieważ magazyn kluczy będzie przechowywać tylko certyfikat jako tajny i polecenie cmdlet nie może ponownie przechować kciuka.</span><span class="sxs-lookup"><span data-stu-id="6ceda-143">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

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

### <span data-ttu-id="6ceda-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ceda-144">-Confirm</span></span>
<span data-ttu-id="6ceda-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6ceda-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ceda-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ceda-146">-WhatIf</span></span>
<span data-ttu-id="6ceda-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ceda-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ceda-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6ceda-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ceda-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ceda-149">CommonParameters</span></span>
<span data-ttu-id="6ceda-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ceda-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ceda-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ceda-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ceda-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ceda-152">INPUTS</span></span>

### <span data-ttu-id="6ceda-153">System.String</span><span class="sxs-lookup"><span data-stu-id="6ceda-153">System.String</span></span>

### <span data-ttu-id="6ceda-154">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="6ceda-154">System.Security.SecureString</span></span>

## <span data-ttu-id="6ceda-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ceda-155">OUTPUTS</span></span>

### <span data-ttu-id="6ceda-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="6ceda-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="6ceda-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6ceda-157">NOTES</span></span>

## <span data-ttu-id="6ceda-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ceda-158">RELATED LINKS</span></span>

[<span data-ttu-id="6ceda-159">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6ceda-159">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="6ceda-160">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="6ceda-160">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
