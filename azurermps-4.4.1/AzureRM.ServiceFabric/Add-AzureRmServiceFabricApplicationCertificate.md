---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
ms.openlocfilehash: 6d77c795415bca1a8bffbed6d09062f394782e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552343"
---
# <span data-ttu-id="f34f8-101">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="f34f8-101">Add-AzureRmServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="f34f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f34f8-102">SYNOPSIS</span></span>
<span data-ttu-id="f34f8-103">Dodaj nowy certyfikat do zestawów skali maszyny wirtualnej, które tworzą klaster.</span><span class="sxs-lookup"><span data-stu-id="f34f8-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="f34f8-104">Certyfikat jest przeznaczony do użytku jako certyfikat aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f34f8-104">The certificate is intended to be used as an application certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f34f8-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f34f8-105">SYNTAX</span></span>

### <span data-ttu-id="f34f8-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="f34f8-106">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f34f8-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="f34f8-107">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f34f8-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="f34f8-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f34f8-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f34f8-109">DESCRIPTION</span></span>
<span data-ttu-id="f34f8-110">Użyj **dodatku Add-AzureRmServiceFabricApplicationCertificate** , aby zainstalować certyfikat we wszystkich węzłach w klastrze.</span><span class="sxs-lookup"><span data-stu-id="f34f8-110">Use **Add-AzureRmServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="f34f8-111">Możesz określić certyfikat, który już masz, lub który wygenerował nowy system, i przekazać go do nowego lub istniejącego magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f34f8-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="f34f8-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f34f8-112">EXAMPLES</span></span>

### <span data-ttu-id="f34f8-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f34f8-113">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="f34f8-114">To polecenie spowoduje dodanie certyfikatu z istniejącego magazynu kluczy platformy Azure do wszystkich typów węzłów klastra.</span><span class="sxs-lookup"><span data-stu-id="f34f8-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="f34f8-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f34f8-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="f34f8-116">To polecenie utworzy certyfikat z podpisem własnym w magazynie kluczy platformy Azure z nazwą grupy zasobów magazynu kluczy i nazwą magazynu kluczy, zostanie zainstalowany na wszystkich typach węzłów klastra i pobierze certyfikat w obszarze folder "c:\Test".</span><span class="sxs-lookup"><span data-stu-id="f34f8-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="f34f8-117">Nazwa pobranego certyfikatu jest taka sama jak nazwa certyfikatu magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f34f8-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="f34f8-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f34f8-118">PARAMETERS</span></span>

### <span data-ttu-id="f34f8-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f34f8-119">-CertificateFile</span></span>
<span data-ttu-id="f34f8-120">Istniejąca ścieżka pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f34f8-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="f34f8-121">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="f34f8-121">-CertificateOutputFolder</span></span>
<span data-ttu-id="f34f8-122">Ścieżka folderu nowego certyfikatu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="f34f8-122">The folder path of the new certificate to be created.</span></span>

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

### <span data-ttu-id="f34f8-123">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f34f8-123">-CertificatePassword</span></span>
<span data-ttu-id="f34f8-124">Hasło pliku PFX.</span><span class="sxs-lookup"><span data-stu-id="f34f8-124">The password of the pfx file.</span></span>

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

### <span data-ttu-id="f34f8-125">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="f34f8-125">-CertificateSubjectName</span></span>
<span data-ttu-id="f34f8-126">Nazwa DNS certyfikatu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="f34f8-126">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="f34f8-127">-Thebinding</span><span class="sxs-lookup"><span data-stu-id="f34f8-127">-KeyVaultName</span></span>
<span data-ttu-id="f34f8-128">Nazwa magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f34f8-128">Azure key vault name.</span></span>

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

### <span data-ttu-id="f34f8-129">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="f34f8-129">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="f34f8-130">Nazwa grupy zasobów magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f34f8-130">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="f34f8-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f34f8-131">-Name</span></span>
<span data-ttu-id="f34f8-132">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="f34f8-132">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="f34f8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f34f8-133">-ResourceGroupName</span></span>
<span data-ttu-id="f34f8-134">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f34f8-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="f34f8-135">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="f34f8-135">-SecretIdentifier</span></span>
<span data-ttu-id="f34f8-136">Istniejący identyfikator URI tajnego magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f34f8-136">The existing Azure key vault secret uri.</span></span>

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

### <span data-ttu-id="f34f8-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f34f8-137">-Confirm</span></span>
<span data-ttu-id="f34f8-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f34f8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f34f8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f34f8-139">-WhatIf</span></span>
<span data-ttu-id="f34f8-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f34f8-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f34f8-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f34f8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f34f8-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f34f8-142">-DefaultProfile</span></span>
<span data-ttu-id="f34f8-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f34f8-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f34f8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f34f8-144">CommonParameters</span></span>
<span data-ttu-id="f34f8-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f34f8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f34f8-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f34f8-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f34f8-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f34f8-147">INPUTS</span></span>

### <span data-ttu-id="f34f8-148">System. String</span><span class="sxs-lookup"><span data-stu-id="f34f8-148">System.String</span></span>

## <span data-ttu-id="f34f8-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f34f8-149">OUTPUTS</span></span>

### <span data-ttu-id="f34f8-150">Microsoft. Azure. Commands. servicefabric. MODELES. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f34f8-150">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="f34f8-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f34f8-151">NOTES</span></span>

## <span data-ttu-id="f34f8-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f34f8-152">RELATED LINKS</span></span>

[<span data-ttu-id="f34f8-153">Dodaj-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f34f8-153">Add-AzureRmServiceFabricClusterCertificate</span></span>](./Add-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="f34f8-154">Nowe — AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="f34f8-154">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)
