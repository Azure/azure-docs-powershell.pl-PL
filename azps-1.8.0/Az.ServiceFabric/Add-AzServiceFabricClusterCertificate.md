---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: bf96b4a21e12e41ce067d669b50c05831a162a8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708091"
---
# <span data-ttu-id="e0b95-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="e0b95-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="e0b95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e0b95-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b95-103">Dodaj pomocniczy certyfikat klastra do klastra.</span><span class="sxs-lookup"><span data-stu-id="e0b95-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="e0b95-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e0b95-104">SYNTAX</span></span>

### <span data-ttu-id="e0b95-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="e0b95-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0b95-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="e0b95-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0b95-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="e0b95-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0b95-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e0b95-108">DESCRIPTION</span></span>
<span data-ttu-id="e0b95-109">Użyj polecenia **Add-AzServiceFabricClusterCertificate** , aby dodać pomocniczy certyfikat klastra z istniejącego magazynu kluczy platformy Azure lub utworzyć nowy magazyn kluczy platformy Azure przy użyciu istniejącego certyfikatu lub z utworzonego nowego certyfikatu z podpisem własnym.</span><span class="sxs-lookup"><span data-stu-id="e0b95-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="e0b95-110">Spowoduje to zastąpienie klastra pomocniczego, jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="e0b95-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="e0b95-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e0b95-111">EXAMPLES</span></span>

### <span data-ttu-id="e0b95-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e0b95-112">Example 1</span></span>
```
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="e0b95-113">To polecenie spowoduje dodanie certyfikatu w istniejącym magazynie kluczy platformy Azure jako pomocniczy certyfikat klastra.</span><span class="sxs-lookup"><span data-stu-id="e0b95-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="e0b95-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e0b95-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="e0b95-115">To polecenie utworzy certyfikat z podpisem własnym w magazynie kluczy usługi Azure i uaktualni klaster, aby używać go jako pomocniczego certyfikatu klastra.</span><span class="sxs-lookup"><span data-stu-id="e0b95-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="e0b95-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0b95-116">PARAMETERS</span></span>

### <span data-ttu-id="e0b95-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="e0b95-117">-CertificateCommonName</span></span>
<span data-ttu-id="e0b95-118">Nazwa pospolita certyfikatu</span><span class="sxs-lookup"><span data-stu-id="e0b95-118">Certificate common name</span></span>

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

### <span data-ttu-id="e0b95-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e0b95-119">-CertificateFile</span></span>
<span data-ttu-id="e0b95-120">Istniejąca ścieżka pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="e0b95-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="e0b95-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="e0b95-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="e0b95-122">Odcisk palca wystawcy certyfikatu, oddzielony przecinkami, jeśli więcej niż jeden</span><span class="sxs-lookup"><span data-stu-id="e0b95-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="e0b95-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="e0b95-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="e0b95-124">Folder nowego certyfikatu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="e0b95-124">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="e0b95-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e0b95-125">-CertificatePassword</span></span>
<span data-ttu-id="e0b95-126">Hasło pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="e0b95-126">The password of the certificate file.</span></span>

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

### <span data-ttu-id="e0b95-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="e0b95-127">-CertificateSubjectName</span></span>
<span data-ttu-id="e0b95-128">Nazwa DNS certyfikatu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="e0b95-128">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="e0b95-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b95-129">-DefaultProfile</span></span>
<span data-ttu-id="e0b95-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0b95-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0b95-131">-Thebinding</span><span class="sxs-lookup"><span data-stu-id="e0b95-131">-KeyVaultName</span></span>
<span data-ttu-id="e0b95-132">Nazwa magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0b95-132">Azure key vault name.</span></span>

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

### <span data-ttu-id="e0b95-133">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0b95-133">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="e0b95-134">Nazwa grupy zasobów magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0b95-134">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="e0b95-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e0b95-135">-Name</span></span>
<span data-ttu-id="e0b95-136">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="e0b95-136">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e0b95-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0b95-137">-ResourceGroupName</span></span>
<span data-ttu-id="e0b95-138">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0b95-138">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e0b95-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="e0b95-139">-SecretIdentifier</span></span>
<span data-ttu-id="e0b95-140">Istniejący tajny adres URL magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0b95-140">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="e0b95-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e0b95-141">-Confirm</span></span>
<span data-ttu-id="e0b95-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0b95-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0b95-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0b95-143">-WhatIf</span></span>
<span data-ttu-id="e0b95-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0b95-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0b95-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e0b95-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0b95-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b95-146">CommonParameters</span></span>
<span data-ttu-id="e0b95-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0b95-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b95-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0b95-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b95-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0b95-149">INPUTS</span></span>

### <span data-ttu-id="e0b95-150">System. String</span><span class="sxs-lookup"><span data-stu-id="e0b95-150">System.String</span></span>

### <span data-ttu-id="e0b95-151">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="e0b95-151">System.Security.SecureString</span></span>

## <span data-ttu-id="e0b95-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e0b95-152">OUTPUTS</span></span>

### <span data-ttu-id="e0b95-153">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="e0b95-153">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="e0b95-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e0b95-154">NOTES</span></span>

## <span data-ttu-id="e0b95-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0b95-155">RELATED LINKS</span></span>

[<span data-ttu-id="e0b95-156">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="e0b95-156">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="e0b95-157">Nowe — AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="e0b95-157">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)

[<span data-ttu-id="e0b95-158">Dodaj-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="e0b95-158">Add-AzServiceFabricApplicationCertificate</span></span>](./Add-AzServiceFabricApplicationCertificate.md)
