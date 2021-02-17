---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: 75d781527a9783c81eba5bd2aacf07d237ef4f8f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412082"
---
# <span data-ttu-id="c2500-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c2500-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="c2500-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2500-102">SYNOPSIS</span></span>
<span data-ttu-id="c2500-103">Usuwa klucz z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="c2500-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="c2500-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c2500-104">SYNTAX</span></span>

### <span data-ttu-id="c2500-105">ByVaultName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="c2500-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2500-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c2500-106">ByInputObject</span></span>
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2500-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c2500-107">DESCRIPTION</span></span>
<span data-ttu-id="c2500-108">Polecenie Remove-AzKeyVaultKey cmdlet usuwa klucz z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="c2500-108">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="c2500-109">Jeśli klucz został przypadkowo usunięty, może zostać odzyskany za Undo-AzKeyVaultKeyRemoval użytkownika ze specjalnymi uprawnieniami do odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c2500-109">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="c2500-110">To polecenie cmdlet ma wartość wysoką dla właściwości **ConfirmImpact.**</span><span class="sxs-lookup"><span data-stu-id="c2500-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="c2500-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c2500-111">EXAMPLES</span></span>

### <span data-ttu-id="c2500-112">Przykład 1. Usuwanie klucza z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="c2500-112">Example 1: Remove a key from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

Vault Name           : contoso
Name                 : key2
Id                   : https://contoso.vault.azure.net:443/keys/itsoftware/fdad15793ba0437e960497908ef9eb32
Deleted Date         : 5/24/2018 11:28:25 PM
Scheduled Purge Date : 8/22/2018 11:28:25 PM
Enabled              : False
Expires              : 10/11/2018 11:32:49 PM
Not Before           : 4/11/2018 11:22:49 PM
Created              : 4/12/2018 10:16:38 PM
Updated              : 4/12/2018 10:16:38 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="c2500-113">To polecenie usuwa klucz o nazwie ITSoftware z magazynu kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="c2500-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="c2500-114">Przykład 2. Usuwanie klucza bez potwierdzenia użytkownika</span><span class="sxs-lookup"><span data-stu-id="c2500-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="c2500-115">To polecenie usuwa klucz o nazwie ITSoftware z magazynu kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="c2500-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="c2500-116">Polecenie określa parametr *Force,* dlatego polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c2500-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="c2500-117">Przykład 3. Trwałe przeczyszczanie usuniętego klucza z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="c2500-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="c2500-118">To polecenie trwale usuwa klucz o nazwie ITSoftware z magazynu kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="c2500-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="c2500-119">Wykonanie tego polecenia cmdlet wymaga uprawnienia "przeczyszczania", które musi być wcześniej i jawnie udzielone użytkownikowi dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="c2500-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="c2500-120">Przykład 4. Usuwanie kluczy przy użyciu operatora potoku</span><span class="sxs-lookup"><span data-stu-id="c2500-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="c2500-121">To polecenie pobiera wszystkie klucze z magazynu kluczy o nazwie Contoso i przekazuje je do polecenia cmdlet **Where-Object** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="c2500-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c2500-122">To polecenie cmdlet przekazuje do bieżącego polecenia cmdlet klawisze o wartości $False **atrybutu Enabled.**</span><span class="sxs-lookup"><span data-stu-id="c2500-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="c2500-123">To polecenie cmdlet usuwa te klawisze.</span><span class="sxs-lookup"><span data-stu-id="c2500-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="c2500-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2500-124">PARAMETERS</span></span>

### <span data-ttu-id="c2500-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2500-125">-DefaultProfile</span></span>
<span data-ttu-id="c2500-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c2500-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2500-127">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c2500-127">-Force</span></span>
<span data-ttu-id="c2500-128">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c2500-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c2500-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2500-129">-InputObject</span></span>
<span data-ttu-id="c2500-130">Obiekt Key Przechowaj</span><span class="sxs-lookup"><span data-stu-id="c2500-130">KeyBundle Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2500-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="c2500-131">-InRemovedState</span></span>
<span data-ttu-id="c2500-132">Usuń trwale usunięty wcześniej klucz.</span><span class="sxs-lookup"><span data-stu-id="c2500-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="c2500-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c2500-133">-Name</span></span>
<span data-ttu-id="c2500-134">Określa nazwę klucza do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c2500-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="c2500-135">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza na podstawie nazwy, która jest określana przez ten parametr, nazwy magazynu kluczy i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="c2500-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2500-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2500-136">-PassThru</span></span>
<span data-ttu-id="c2500-137">Wskazuje, że to polecenie cmdlet zwraca obiekt **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey.**</span><span class="sxs-lookup"><span data-stu-id="c2500-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="c2500-138">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c2500-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c2500-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c2500-139">-VaultName</span></span>
<span data-ttu-id="c2500-140">Określa nazwę magazynu kluczy, z którego ma być usuwany klucz.</span><span class="sxs-lookup"><span data-stu-id="c2500-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="c2500-141">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, która jest określana przez ten parametr i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="c2500-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2500-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2500-142">-Confirm</span></span>
<span data-ttu-id="c2500-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c2500-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2500-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2500-144">-WhatIf</span></span>
<span data-ttu-id="c2500-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2500-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2500-146">Polecenie cmdlet nie zostanie uruchomione. Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2500-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2500-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c2500-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2500-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2500-148">CommonParameters</span></span>
<span data-ttu-id="c2500-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2500-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2500-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2500-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2500-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2500-151">INPUTS</span></span>

### <span data-ttu-id="c2500-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c2500-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="c2500-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2500-153">OUTPUTS</span></span>

### <span data-ttu-id="c2500-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c2500-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="c2500-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c2500-155">NOTES</span></span>

## <span data-ttu-id="c2500-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2500-156">RELATED LINKS</span></span>

[<span data-ttu-id="c2500-157">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c2500-157">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="c2500-158">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c2500-158">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)


[<span data-ttu-id="c2500-159">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="c2500-159">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

