---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
ms.openlocfilehash: fb52675187cda4ffd87b7198a4ffb98c2f4e4734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550543"
---
# <span data-ttu-id="fb4c6-101">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="fb4c6-101">Add-AzureRmServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="fb4c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb4c6-102">SYNOPSIS</span></span>
<span data-ttu-id="fb4c6-103">Dodaj nowy certyfikat do zestawów skali maszyny wirtualnej, które tworzą klaster.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="fb4c6-104">Certyfikat jest przeznaczony do użytku jako certyfikat aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-104">The certificate is intended to be used as an application certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb4c6-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb4c6-105">SYNTAX</span></span>

### <span data-ttu-id="fb4c6-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="fb4c6-106">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb4c6-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="fb4c6-107">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb4c6-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="fb4c6-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb4c6-109">Opis</span><span class="sxs-lookup"><span data-stu-id="fb4c6-109">DESCRIPTION</span></span>
<span data-ttu-id="fb4c6-110">Użyj **dodatku Add-AzureRmServiceFabricApplicationCertificate** , aby zainstalować certyfikat we wszystkich węzłach w klastrze.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-110">Use **Add-AzureRmServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="fb4c6-111">Możesz określić certyfikat, który już masz, lub który wygenerował nowy system, i przekazać go do nowego lub istniejącego magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="fb4c6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb4c6-112">EXAMPLES</span></span>

### <span data-ttu-id="fb4c6-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fb4c6-113">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="fb4c6-114">To polecenie spowoduje dodanie certyfikatu z istniejącego magazynu kluczy platformy Azure do wszystkich typów węzłów klastra.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="fb4c6-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fb4c6-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="fb4c6-116">To polecenie utworzy certyfikat z podpisem własnym w magazynie kluczy platformy Azure z nazwą grupy zasobów magazynu kluczy i nazwą magazynu kluczy, zostanie zainstalowany na wszystkich typach węzłów klastra i pobierze certyfikat w obszarze folder "c:\Test".</span><span class="sxs-lookup"><span data-stu-id="fb4c6-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="fb4c6-117">Nazwa pobranego certyfikatu jest taka sama jak nazwa certyfikatu magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="fb4c6-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb4c6-118">PARAMETERS</span></span>

### <span data-ttu-id="fb4c6-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="fb4c6-119">-CertificateFile</span></span>
<span data-ttu-id="fb4c6-120">Istniejąca ścieżka pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="fb4c6-121">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="fb4c6-121">-CertificateOutputFolder</span></span>
<span data-ttu-id="fb4c6-122">Ścieżka folderu nowego certyfikatu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-122">The folder path of the new certificate to be created.</span></span>

```yaml
Type: String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4c6-123">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="fb4c6-123">-CertificatePassword</span></span>
<span data-ttu-id="fb4c6-124">Hasło pliku PFX.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-124">The password of the pfx file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4c6-125">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="fb4c6-125">-CertificateSubjectName</span></span>
<span data-ttu-id="fb4c6-126">Nazwa DNS certyfikatu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-126">The Dns name of the certificate to be created.</span></span>

```yaml
Type: String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Subject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4c6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb4c6-127">-DefaultProfile</span></span>
<span data-ttu-id="fb4c6-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb4c6-129">-Thebinding</span><span class="sxs-lookup"><span data-stu-id="fb4c6-129">-KeyVaultName</span></span>
<span data-ttu-id="fb4c6-130">Nazwa magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-130">Azure key vault name.</span></span>

```yaml
Type: String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4c6-131">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb4c6-131">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="fb4c6-132">Nazwa grupy zasobów magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-132">Azure key vault resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4c6-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fb4c6-133">-Name</span></span>
<span data-ttu-id="fb4c6-134">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-134">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4c6-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb4c6-135">-ResourceGroupName</span></span>
<span data-ttu-id="fb4c6-136">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-136">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="fb4c6-137">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="fb4c6-137">-SecretIdentifier</span></span>
<span data-ttu-id="fb4c6-138">Istniejący identyfikator URI tajnego magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-138">The existing Azure key vault secret uri.</span></span>

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

### <span data-ttu-id="fb4c6-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fb4c6-139">-Confirm</span></span>
<span data-ttu-id="fb4c6-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb4c6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb4c6-141">-WhatIf</span></span>
<span data-ttu-id="fb4c6-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb4c6-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb4c6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb4c6-144">CommonParameters</span></span>
<span data-ttu-id="fb4c6-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb4c6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb4c6-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb4c6-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb4c6-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb4c6-147">INPUTS</span></span>

### <span data-ttu-id="fb4c6-148">System. String</span><span class="sxs-lookup"><span data-stu-id="fb4c6-148">System.String</span></span>

## <span data-ttu-id="fb4c6-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb4c6-149">OUTPUTS</span></span>

### <span data-ttu-id="fb4c6-150">Microsoft. Azure. Commands. servicefabric. MODELES. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="fb4c6-150">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="fb4c6-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb4c6-151">NOTES</span></span>

## <span data-ttu-id="fb4c6-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb4c6-152">RELATED LINKS</span></span>

[<span data-ttu-id="fb4c6-153">Dodaj-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="fb4c6-153">Add-AzureRmServiceFabricClusterCertificate</span></span>](./Add-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="fb4c6-154">Nowe — AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="fb4c6-154">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)
