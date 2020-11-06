---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: fa357a4f5b8e599858ce5aff3e0aa11121833ba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546455"
---
# <span data-ttu-id="496e0-101">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="496e0-101">Add-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="496e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="496e0-102">SYNOPSIS</span></span>
<span data-ttu-id="496e0-103">Dodaj pomocniczy certyfikat klastra do klastra.</span><span class="sxs-lookup"><span data-stu-id="496e0-103">Add a secondary cluster certificate to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="496e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="496e0-104">SYNTAX</span></span>

### <span data-ttu-id="496e0-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="496e0-105">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="496e0-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="496e0-106">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="496e0-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="496e0-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="496e0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="496e0-108">DESCRIPTION</span></span>
<span data-ttu-id="496e0-109">Użyj polecenia **Add-AzureRmServiceFabricClusterCertificate** , aby dodać pomocniczy certyfikat klastra z istniejącego magazynu kluczy platformy Azure lub utworzyć nowy magazyn kluczy platformy Azure przy użyciu istniejącego certyfikatu lub z utworzonego nowego certyfikatu z podpisem własnym.</span><span class="sxs-lookup"><span data-stu-id="496e0-109">Use **Add-AzureRmServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="496e0-110">Spowoduje to zastąpienie klastra pomocniczego, jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="496e0-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="496e0-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="496e0-111">EXAMPLES</span></span>

### <span data-ttu-id="496e0-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="496e0-112">Example 1</span></span>
```
Add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="496e0-113">To polecenie spowoduje dodanie certyfikatu w istniejącym magazynie kluczy platformy Azure jako pomocniczy certyfikat klastra.</span><span class="sxs-lookup"><span data-stu-id="496e0-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="496e0-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="496e0-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="496e0-115">To polecenie utworzy certyfikat z podpisem własnym w magazynie kluczy usługi Azure i uaktualni klaster, aby używać go jako pomocniczego certyfikatu klastra.</span><span class="sxs-lookup"><span data-stu-id="496e0-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="496e0-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="496e0-116">PARAMETERS</span></span>

### <span data-ttu-id="496e0-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="496e0-117">-CertificateFile</span></span>
<span data-ttu-id="496e0-118">Istniejąca ścieżka pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="496e0-118">The existing certificate file path.</span></span>

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

### <span data-ttu-id="496e0-119">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="496e0-119">-CertificateOutputFolder</span></span>
<span data-ttu-id="496e0-120">Folder nowego certyfikatu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="496e0-120">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="496e0-121">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="496e0-121">-CertificatePassword</span></span>
<span data-ttu-id="496e0-122">Hasło pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="496e0-122">The password of the certificate file.</span></span>

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

### <span data-ttu-id="496e0-123">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="496e0-123">-CertificateSubjectName</span></span>
<span data-ttu-id="496e0-124">Nazwa DNS certyfikatu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="496e0-124">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="496e0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="496e0-125">-DefaultProfile</span></span>
<span data-ttu-id="496e0-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="496e0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="496e0-127">-Thebinding</span><span class="sxs-lookup"><span data-stu-id="496e0-127">-KeyVaultName</span></span>
<span data-ttu-id="496e0-128">Nazwa magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="496e0-128">Azure key vault name.</span></span>

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

### <span data-ttu-id="496e0-129">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="496e0-129">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="496e0-130">Nazwa grupy zasobów magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="496e0-130">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="496e0-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="496e0-131">-Name</span></span>
<span data-ttu-id="496e0-132">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="496e0-132">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="496e0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="496e0-133">-ResourceGroupName</span></span>
<span data-ttu-id="496e0-134">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="496e0-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="496e0-135">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="496e0-135">-SecretIdentifier</span></span>
<span data-ttu-id="496e0-136">Istniejący tajny adres URL magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="496e0-136">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="496e0-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="496e0-137">-Confirm</span></span>
<span data-ttu-id="496e0-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="496e0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="496e0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="496e0-139">-WhatIf</span></span>
<span data-ttu-id="496e0-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="496e0-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="496e0-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="496e0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="496e0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="496e0-142">CommonParameters</span></span>
<span data-ttu-id="496e0-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="496e0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="496e0-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="496e0-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="496e0-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="496e0-145">INPUTS</span></span>

### <span data-ttu-id="496e0-146">System. String</span><span class="sxs-lookup"><span data-stu-id="496e0-146">System.String</span></span>
<span data-ttu-id="496e0-147">Parametry: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), (ByValue), KeyVaultResouceGroupName (ByValue), SecretIdentifier (ByValue)</span><span class="sxs-lookup"><span data-stu-id="496e0-147">Parameters: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), KeyVaultName (ByValue), KeyVaultResouceGroupName (ByValue), SecretIdentifier (ByValue)</span></span>

### <span data-ttu-id="496e0-148">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="496e0-148">System.Security.SecureString</span></span>
<span data-ttu-id="496e0-149">Parametry: CertificatePassword (ByValue)</span><span class="sxs-lookup"><span data-stu-id="496e0-149">Parameters: CertificatePassword (ByValue)</span></span>

## <span data-ttu-id="496e0-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="496e0-150">OUTPUTS</span></span>

### <span data-ttu-id="496e0-151">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="496e0-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="496e0-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="496e0-152">NOTES</span></span>

## <span data-ttu-id="496e0-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="496e0-153">RELATED LINKS</span></span>

[<span data-ttu-id="496e0-154">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="496e0-154">Remove-AzureRmServiceFabricClusterCertificate</span></span>](./Remove-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="496e0-155">Nowe — AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="496e0-155">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)

[<span data-ttu-id="496e0-156">Dodaj-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="496e0-156">Add-AzureRmServiceFabricApplicationCertificate</span></span>](./Add-AzureRmServiceFabricApplicationCertificate.md)
