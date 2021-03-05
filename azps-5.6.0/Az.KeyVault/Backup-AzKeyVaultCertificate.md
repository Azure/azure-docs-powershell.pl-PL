---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: e4692d9b623ce285a2be50d51a450fd8da39a5ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968961"
---
# <span data-ttu-id="c12cf-101">Backup-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c12cf-101">Backup-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="c12cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c12cf-102">SYNOPSIS</span></span>
<span data-ttu-id="c12cf-103">Kopii zapasowej certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="c12cf-103">Backs up a certificate in a key vault.</span></span>

## <span data-ttu-id="c12cf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c12cf-104">SYNTAX</span></span>

### <span data-ttu-id="c12cf-105">ByCertificateName (Default)</span><span class="sxs-lookup"><span data-stu-id="c12cf-105">ByCertificateName (Default)</span></span>
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c12cf-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="c12cf-106">ByCertificate</span></span>
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c12cf-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c12cf-107">DESCRIPTION</span></span>
<span data-ttu-id="c12cf-108">Polecenie **cmdlet Backup-AzKeyVaultCertificate** kopii zapasowej określonego certyfikatu w magazynie kluczy, pobierając go i przechowując w pliku.</span><span class="sxs-lookup"><span data-stu-id="c12cf-108">The **Backup-AzKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="c12cf-109">Jeśli certyfikat ma wiele wersji, wszystkie jego wersje zostaną uwzględnione w kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="c12cf-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="c12cf-110">Pobrana zawartość jest zaszyfrowana, więc nie można jej używać poza magazynem kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c12cf-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="c12cf-111">Kopię zapasową certyfikatu możesz przywrócić do dowolnego magazynu kluczy w subskrypcji, z których został on kopii zapasowej, o ile magazyn znajduje się w tej samej lokalizacji geograficznej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c12cf-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="c12cf-112">Typowe powody, dla których należy używać tego polecenia cmdlet, to:</span><span class="sxs-lookup"><span data-stu-id="c12cf-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="c12cf-113">Chcesz zachować kopię certyfikatu w trybie offline na wypadek przypadkowego usunięcia oryginału z magazynu.</span><span class="sxs-lookup"><span data-stu-id="c12cf-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="c12cf-114">Certyfikat został utworzony przy użyciu magazynu kluczy, a teraz chcesz sklonować obiekt w innym regionie platformy Azure, aby można było go używać ze wszystkich wystąpień aplikacji rozproszonej.</span><span class="sxs-lookup"><span data-stu-id="c12cf-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="c12cf-115">Użyj polecenia cmdlet **Backup-AzKeyVaultCertificate,** aby pobrać certyfikat w postaci zaszyfrowanej, a następnie użyj polecenia cmdlet **Restore-AzKeyVaultCertificate** i określ magazyn kluczy w drugim regionie.</span><span class="sxs-lookup"><span data-stu-id="c12cf-115">Use the **Backup-AzKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="c12cf-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c12cf-116">EXAMPLES</span></span>

### <span data-ttu-id="c12cf-117">Przykład 1. Tworzy kopię zapasową certyfikatu z automatycznie wygenerowaną nazwą pliku</span><span class="sxs-lookup"><span data-stu-id="c12cf-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="c12cf-118">To polecenie pobiera certyfikat o nazwie MyCert z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego certyfikatu w pliku, który jest automatycznie nazwany dla Ciebie, i wyświetla nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="c12cf-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="c12cf-119">Przykład 2. Kopii zapasowej certyfikatu pod określoną nazwą pliku</span><span class="sxs-lookup"><span data-stu-id="c12cf-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="c12cf-120">To polecenie pobiera certyfikat o nazwie MyCert z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego certyfikatu w pliku o nazwie Backup.blob.</span><span class="sxs-lookup"><span data-stu-id="c12cf-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="c12cf-121">Przykład 3. Należy zrobić kopię zapasową poprzednio pobranego certyfikatu pod określoną nazwą pliku, która nie wyświetla monitu w pliku docelowym.</span><span class="sxs-lookup"><span data-stu-id="c12cf-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="c12cf-122">To polecenie tworzy kopię zapasową certyfikatu o nazwie $cert. Nazwa w magazynie o nazwie $cert. Nazwa magazynu do pliku o nazwie Backup.blob, bezgłośnie nadpisując plik, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="c12cf-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="c12cf-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c12cf-123">PARAMETERS</span></span>

### <span data-ttu-id="c12cf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c12cf-124">-DefaultProfile</span></span>
<span data-ttu-id="c12cf-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c12cf-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c12cf-126">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c12cf-126">-Force</span></span>
<span data-ttu-id="c12cf-127">Zastępowanie danego pliku, jeśli istnieje</span><span class="sxs-lookup"><span data-stu-id="c12cf-127">Overwrite the given file if it exists</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c12cf-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c12cf-128">-InputObject</span></span>
<span data-ttu-id="c12cf-129">Tajna, aby mieć kopię zapasową, potokowana na wyniku połączenia pobierania.</span><span class="sxs-lookup"><span data-stu-id="c12cf-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c12cf-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c12cf-130">-Name</span></span>
<span data-ttu-id="c12cf-131">Tajna nazwa.</span><span class="sxs-lookup"><span data-stu-id="c12cf-131">Secret name.</span></span>
<span data-ttu-id="c12cf-132">Polecenie cmdlet konstruuje nazwę FQDN tajemnicy przed nazwą magazynu, obecnie wybranym środowiskiem i nazwą tajną.</span><span class="sxs-lookup"><span data-stu-id="c12cf-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c12cf-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="c12cf-133">-OutputFile</span></span>
<span data-ttu-id="c12cf-134">Plik wyjściowy.</span><span class="sxs-lookup"><span data-stu-id="c12cf-134">Output file.</span></span>
<span data-ttu-id="c12cf-135">Plik wyjściowy do przechowywania kopii zapasowej certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="c12cf-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="c12cf-136">Jeśli nie zostanie określona, zostanie wygenerowana domyślna nazwa pliku.</span><span class="sxs-lookup"><span data-stu-id="c12cf-136">If not specified, a default filename will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c12cf-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c12cf-137">-VaultName</span></span>
<span data-ttu-id="c12cf-138">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="c12cf-138">Vault name.</span></span>
<span data-ttu-id="c12cf-139">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="c12cf-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c12cf-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c12cf-140">-Confirm</span></span>
<span data-ttu-id="c12cf-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c12cf-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c12cf-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c12cf-142">-WhatIf</span></span>
<span data-ttu-id="c12cf-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c12cf-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c12cf-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c12cf-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c12cf-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c12cf-145">CommonParameters</span></span>
<span data-ttu-id="c12cf-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c12cf-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c12cf-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c12cf-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c12cf-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c12cf-148">INPUTS</span></span>

### <span data-ttu-id="c12cf-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c12cf-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="c12cf-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c12cf-150">OUTPUTS</span></span>

### <span data-ttu-id="c12cf-151">System.String</span><span class="sxs-lookup"><span data-stu-id="c12cf-151">System.String</span></span>

## <span data-ttu-id="c12cf-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c12cf-152">NOTES</span></span>

## <span data-ttu-id="c12cf-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c12cf-153">RELATED LINKS</span></span>
