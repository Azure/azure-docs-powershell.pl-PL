---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: 51d322ea738a56e4b1fa24cccdb7bb59a6cd0d21
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234701"
---
# <span data-ttu-id="aa08f-101">Backup-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="aa08f-101">Backup-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="aa08f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa08f-102">SYNOPSIS</span></span>
<span data-ttu-id="aa08f-103">Wykonywanie kopii zapasowej certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="aa08f-103">Backs up a certificate in a key vault.</span></span>

## <span data-ttu-id="aa08f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa08f-104">SYNTAX</span></span>

### <span data-ttu-id="aa08f-105">ByCertificateName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aa08f-105">ByCertificateName (Default)</span></span>
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa08f-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="aa08f-106">ByCertificate</span></span>
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa08f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="aa08f-107">DESCRIPTION</span></span>
<span data-ttu-id="aa08f-108">Polecenie cmdlet **Backup-AzKeyVaultCertificate** wykonuje kopię zapasową określonego certyfikatu w magazynie kluczy przez pobranie go i zapisanie go w pliku.</span><span class="sxs-lookup"><span data-stu-id="aa08f-108">The **Backup-AzKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="aa08f-109">Jeśli certyfikat zawiera wiele wersji, wszystkie jego wersje zostaną uwzględnione w kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="aa08f-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="aa08f-110">Ponieważ pobrana zawartość jest szyfrowana, nie można jej użyć poza magazynem kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="aa08f-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="aa08f-111">Możesz przywrócić kopię zapasową certyfikatu do dowolnego magazynu kluczy w subskrypcji, z której wykonano kopię zapasową, o ile magazyn znajduje się w tej samej geograficznej platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="aa08f-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="aa08f-112">Typowe przyczyny korzystania z tego polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="aa08f-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="aa08f-113">Chcesz zachować kopię certyfikatu w trybie offline na wypadek przypadkowego usunięcia oryginału z magazynu.</span><span class="sxs-lookup"><span data-stu-id="aa08f-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="aa08f-114">Utworzono certyfikat przy użyciu magazynu kluczy, a teraz chcę sklonować obiekt do innego obszaru platformy Azure, aby można go było używać we wszystkich wystąpieniach aplikacji rozproszonej.</span><span class="sxs-lookup"><span data-stu-id="aa08f-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="aa08f-115">Użyj polecenia cmdlet **Backup-AzKeyVaultCertificate** , aby pobrać certyfikat w formacie zaszyfrowanym, a następnie użyj polecenia cmdlet **Restore-AzKeyVaultCertificate** i określ Magazyn kluczy w drugim regionie.</span><span class="sxs-lookup"><span data-stu-id="aa08f-115">Use the **Backup-AzKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="aa08f-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa08f-116">EXAMPLES</span></span>

### <span data-ttu-id="aa08f-117">Przykład 1. wykonywanie kopii zapasowej certyfikatu z automatycznie wygenerowaną nazwą pliku</span><span class="sxs-lookup"><span data-stu-id="aa08f-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="aa08f-118">To polecenie pobiera certyfikat o nazwie CERT z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego certyfikatu do pliku, którego nazwa jest automatycznie nazywana, i wyświetla nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="aa08f-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="aa08f-119">Przykład 2: wykonywanie kopii zapasowej certyfikatu pod określoną nazwą pliku</span><span class="sxs-lookup"><span data-stu-id="aa08f-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="aa08f-120">To polecenie pobiera certyfikat o nazwie CERT z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego certyfikatu do pliku o nazwie Backup. blob.</span><span class="sxs-lookup"><span data-stu-id="aa08f-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="aa08f-121">Przykład 3: wykonywanie kopii zapasowej uprzednio pobranego certyfikatu do określonej nazwy pliku, zastępując plik docelowy bez monitowania.</span><span class="sxs-lookup"><span data-stu-id="aa08f-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="aa08f-122">To polecenie tworzy kopię zapasową certyfikatu o nazwie $cert. Nazwa w magazynie o nazwie $cert. Element magazynname do pliku o nazwie Backup. blob, w cichym zastępowaniu pliku, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="aa08f-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="aa08f-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa08f-123">PARAMETERS</span></span>

### <span data-ttu-id="aa08f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa08f-124">-DefaultProfile</span></span>
<span data-ttu-id="aa08f-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa08f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa08f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="aa08f-126">-Force</span></span>
<span data-ttu-id="aa08f-127">Zastąpienie danego pliku, jeśli istnieje</span><span class="sxs-lookup"><span data-stu-id="aa08f-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="aa08f-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aa08f-128">-InputObject</span></span>
<span data-ttu-id="aa08f-129">Nie można utworzyć kopii zapasowej, która została przetworzona na podstawie danych wyjściowych rozmowy.</span><span class="sxs-lookup"><span data-stu-id="aa08f-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="aa08f-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aa08f-130">-Name</span></span>
<span data-ttu-id="aa08f-131">Nazwa tajna.</span><span class="sxs-lookup"><span data-stu-id="aa08f-131">Secret name.</span></span>
<span data-ttu-id="aa08f-132">Polecenie cmdlet tworzy nazwę FQDN wpisu tajnego na podstawie nazwy magazynu, obecnie wybranej nazwy środowiska i sekretu.</span><span class="sxs-lookup"><span data-stu-id="aa08f-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="aa08f-133">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="aa08f-133">-OutputFile</span></span>
<span data-ttu-id="aa08f-134">Plik wyjściowy.</span><span class="sxs-lookup"><span data-stu-id="aa08f-134">Output file.</span></span>
<span data-ttu-id="aa08f-135">Plik wyjściowy, w którym ma być przechowywana kopia zapasowa certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="aa08f-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="aa08f-136">Jeśli nie podano tego parametru, zostanie wygenerowana domyślna nazwa pliku.</span><span class="sxs-lookup"><span data-stu-id="aa08f-136">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="aa08f-137">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="aa08f-137">-VaultName</span></span>
<span data-ttu-id="aa08f-138">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="aa08f-138">Vault name.</span></span>
<span data-ttu-id="aa08f-139">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="aa08f-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="aa08f-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa08f-140">-Confirm</span></span>
<span data-ttu-id="aa08f-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa08f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa08f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa08f-142">-WhatIf</span></span>
<span data-ttu-id="aa08f-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa08f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa08f-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aa08f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa08f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa08f-145">CommonParameters</span></span>
<span data-ttu-id="aa08f-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa08f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa08f-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa08f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa08f-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa08f-148">INPUTS</span></span>

### <span data-ttu-id="aa08f-149">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="aa08f-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="aa08f-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa08f-150">OUTPUTS</span></span>

### <span data-ttu-id="aa08f-151">System. String</span><span class="sxs-lookup"><span data-stu-id="aa08f-151">System.String</span></span>

## <span data-ttu-id="aa08f-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa08f-152">NOTES</span></span>

## <span data-ttu-id="aa08f-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa08f-153">RELATED LINKS</span></span>
