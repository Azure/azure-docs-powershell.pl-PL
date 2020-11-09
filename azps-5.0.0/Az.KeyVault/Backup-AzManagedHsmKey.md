---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
ms.openlocfilehash: 9e75b6de483f0103103434518d31b472660f4a70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304626"
---
# <span data-ttu-id="0ade3-101">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0ade3-101">Backup-AzManagedHsmKey</span></span>

## <span data-ttu-id="0ade3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ade3-102">SYNOPSIS</span></span>
<span data-ttu-id="0ade3-103">Wykonywanie kopii zapasowej klucza w zarządzanym modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="0ade3-103">Backs up a key in a managed HSM.</span></span>

## <span data-ttu-id="0ade3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ade3-104">SYNTAX</span></span>

### <span data-ttu-id="0ade3-105">ByKeyName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0ade3-105">ByKeyName (Default)</span></span>
```
Backup-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ade3-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="0ade3-106">ByKey</span></span>
```
Backup-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ade3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0ade3-107">DESCRIPTION</span></span>
<span data-ttu-id="0ade3-108">Polecenie cmdlet **Backup-AzManagedHsmKey** wykonuje kopię zapasową określonego klucza w zarządzanym modułu HSM przez pobranie go i zapisanie go w pliku.</span><span class="sxs-lookup"><span data-stu-id="0ade3-108">The **Backup-AzManagedHsmKey** cmdlet backs up a specified key in a managed HSM by downloading it and storing it in a file.</span></span>
<span data-ttu-id="0ade3-109">Jeśli istnieje wiele wersji klucza, wszystkie wersje są uwzględniane w kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="0ade3-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="0ade3-110">Ponieważ pobrana zawartość jest szyfrowana, nie można jej użyć poza oknem HSM zarządzanym na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="0ade3-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Managed HSM.</span></span>
<span data-ttu-id="0ade3-111">Klucz kopii zapasowej można przywrócić do dowolnego zarządzanego modułu HSM w subskrypcji, z której wykonano kopię zapasową.</span><span class="sxs-lookup"><span data-stu-id="0ade3-111">You can restore a backed-up key to any managed HSM in the subscription that it was backed up from.</span></span>
<span data-ttu-id="0ade3-112">Typowe przyczyny korzystania z tego polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0ade3-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="0ade3-113">Chcesz zalogować się do kopii klucza, aby uzyskać kopię w trybie offline, na wypadek przypadkowego usunięcia klucza z zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="0ade3-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your managed HSM.</span></span>
 
- <span data-ttu-id="0ade3-114">Utworzono klucz przy użyciu zarządzanego modułu HSM i teraz chcę sklonować klucz do innego obszaru platformy Azure, aby można go było używać we wszystkich wystąpieniach aplikacji rozproszonej.</span><span class="sxs-lookup"><span data-stu-id="0ade3-114">You created a key using Managed HSM and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="0ade3-115">Użyj polecenia cmdlet **Backup-AzManagedHsmKey** , aby pobrać klucz w zaszyfrowanym formacie, a następnie użyj polecenia cmdlet Restore-AzManagedHsmKey i określeniu zarządzanego modułu HSM w drugim regionie.</span><span class="sxs-lookup"><span data-stu-id="0ade3-115">Use the **Backup-AzManagedHsmKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzManagedHsmKey cmdlet and specify a managed HSM in the second region.</span></span>

## <span data-ttu-id="0ade3-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ade3-116">EXAMPLES</span></span>

### <span data-ttu-id="0ade3-117">Przykład 1. Tworzenie kopii zapasowej klucza z automatycznie wygenerowaną nazwą pliku</span><span class="sxs-lookup"><span data-stu-id="0ade3-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzManagedHsmKey -HsmName testmhsm -Name testkey

C:\Users\username\testmhsm-testkey-1602664728.7106073
```

<span data-ttu-id="0ade3-118">To polecenie pobiera klucz o nazwie TestKey z zarządzanego modułu HSM o nazwie testmhsm i zapisuje kopię zapasową tego klucza w pliku, którego nazwa jest automatycznie nazywana, i wyświetla nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="0ade3-118">This command retrieves the key named testkey from the managed HSM named testmhsm and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

## <span data-ttu-id="0ade3-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ade3-119">PARAMETERS</span></span>

### <span data-ttu-id="0ade3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ade3-120">-DefaultProfile</span></span>
<span data-ttu-id="0ade3-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ade3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ade3-122">-Force</span><span class="sxs-lookup"><span data-stu-id="0ade3-122">-Force</span></span>
<span data-ttu-id="0ade3-123">Zastąpienie danego pliku, jeśli istnieje</span><span class="sxs-lookup"><span data-stu-id="0ade3-123">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="0ade3-124">-HsmName</span><span class="sxs-lookup"><span data-stu-id="0ade3-124">-HsmName</span></span>
<span data-ttu-id="0ade3-125">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="0ade3-125">HSM name.</span></span> <span data-ttu-id="0ade3-126">Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="0ade3-126">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ade3-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0ade3-127">-InputObject</span></span>
<span data-ttu-id="0ade3-128">Kluczowy pakiet do utworzenia kopii zapasowej, który połączył się z wyników rozmowy o pobraniu.</span><span class="sxs-lookup"><span data-stu-id="0ade3-128">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ade3-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0ade3-129">-Name</span></span>
<span data-ttu-id="0ade3-130">Nazwa klucza.</span><span class="sxs-lookup"><span data-stu-id="0ade3-130">Key name.</span></span>
<span data-ttu-id="0ade3-131">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie nazwa zarządzanego modułu HSM, obecnie wybranego środowiska i nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="0ade3-131">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ade3-132">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="0ade3-132">-OutputFile</span></span>
<span data-ttu-id="0ade3-133">Plik wyjściowy.</span><span class="sxs-lookup"><span data-stu-id="0ade3-133">Output file.</span></span>
<span data-ttu-id="0ade3-134">Plik wyjściowy, w którym ma zostać zapisany obiekt BLOB klucza kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="0ade3-134">The output file to store the backed up key blob in.</span></span>
<span data-ttu-id="0ade3-135">Jeśli nie jest obecny, wybierana jest domyślna nazwa pliku.</span><span class="sxs-lookup"><span data-stu-id="0ade3-135">If not present, a default filename is chosen.</span></span>

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

### <span data-ttu-id="0ade3-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0ade3-136">-Confirm</span></span>
<span data-ttu-id="0ade3-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ade3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ade3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ade3-138">-WhatIf</span></span>
<span data-ttu-id="0ade3-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ade3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ade3-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0ade3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ade3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ade3-141">CommonParameters</span></span>
<span data-ttu-id="0ade3-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ade3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ade3-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ade3-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ade3-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ade3-144">INPUTS</span></span>

### <span data-ttu-id="0ade3-145">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0ade3-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="0ade3-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ade3-146">OUTPUTS</span></span>

### <span data-ttu-id="0ade3-147">System. String</span><span class="sxs-lookup"><span data-stu-id="0ade3-147">System.String</span></span>

## <span data-ttu-id="0ade3-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ade3-148">NOTES</span></span>

## <span data-ttu-id="0ade3-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ade3-149">RELATED LINKS</span></span>

[<span data-ttu-id="0ade3-150">Dodaj-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0ade3-150">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="0ade3-151">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0ade3-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="0ade3-152">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0ade3-152">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="0ade3-153">Cofanie — AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="0ade3-153">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="0ade3-154">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0ade3-154">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="0ade3-155">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0ade3-155">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)