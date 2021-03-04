---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: 675107a27774cf2fe44ef328cdb0d7a3569e8abb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952490"
---
# <span data-ttu-id="58d92-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="58d92-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="58d92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58d92-102">SYNOPSIS</span></span>
<span data-ttu-id="58d92-103">Usuwa klucz tajny z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="58d92-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="58d92-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="58d92-104">SYNTAX</span></span>

### <span data-ttu-id="58d92-105">ByVaultName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="58d92-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58d92-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="58d92-106">ByInputObject</span></span>
```
Remove-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58d92-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="58d92-107">DESCRIPTION</span></span>
<span data-ttu-id="58d92-108">Polecenie Remove-AzKeyVaultSecret cmdlet usuwa klucz tajny w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="58d92-108">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="58d92-109">Jeśli tajna tajemnica została przypadkowo usunięta, może zostać odzyskana Undo-AzKeyVaultSecretRemoval użytkownika ze specjalnymi uprawnieniami do odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="58d92-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="58d92-110">To polecenie cmdlet ma wartość wysoką dla **właściwości ConfirmImpact.**</span><span class="sxs-lookup"><span data-stu-id="58d92-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="58d92-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="58d92-111">EXAMPLES</span></span>

### <span data-ttu-id="58d92-112">Przykład 1. Usuwanie klucza tajnego z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="58d92-112">Example 1: Remove a secret from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="58d92-113">To polecenie usuwa klucz tajny o nazwie FinanseSecret z magazynu kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="58d92-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="58d92-114">Przykład 2. Usunięcie klucza tajnego z magazynu kluczy bez potwierdzenia użytkownika</span><span class="sxs-lookup"><span data-stu-id="58d92-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru -Force

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="58d92-115">To polecenie usuwa klucz tajny o nazwie FinanseSecret z magazynu kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="58d92-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="58d92-116">To polecenie określa parametry *Force (Wymuszaj)* *i Confirm* (Potwierdź), dlatego polecenie cmdlet nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="58d92-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="58d92-117">Przykład 3. Trwałe czyszczenie usuniętego klucza tajnego z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="58d92-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="58d92-118">To polecenie trwale przesłoni klucz tajny o nazwie FinanseSecret z magazynu kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="58d92-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="58d92-119">Wykonanie tego polecenia cmdlet wymaga uprawnienia "przeczyszczania", które musi być wcześniej i jawnie udzielone użytkownikowi dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="58d92-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="58d92-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58d92-120">PARAMETERS</span></span>

### <span data-ttu-id="58d92-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58d92-121">-DefaultProfile</span></span>
<span data-ttu-id="58d92-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="58d92-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58d92-123">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="58d92-123">-Force</span></span>
<span data-ttu-id="58d92-124">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="58d92-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="58d92-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58d92-125">-InputObject</span></span>
<span data-ttu-id="58d92-126">Tajny obiekt magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="58d92-126">Key Vault Secret Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58d92-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="58d92-127">-InRemovedState</span></span>
<span data-ttu-id="58d92-128">Jeśli występuje, usuwa usunięty wcześniej klucz tajny na stałe.</span><span class="sxs-lookup"><span data-stu-id="58d92-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="58d92-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="58d92-129">-Name</span></span>
<span data-ttu-id="58d92-130">Określa nazwę tajemnicy.</span><span class="sxs-lookup"><span data-stu-id="58d92-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="58d92-131">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza tajnego na podstawie nazwy, która jest określana przez ten parametr, nazwy magazynu kluczy i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="58d92-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d92-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58d92-132">-PassThru</span></span>
<span data-ttu-id="58d92-133">Wskazuje, że to polecenie cmdlet zwraca obiekt **Microsoft.Azure.Commands.KeyVault.Models.Secret.**</span><span class="sxs-lookup"><span data-stu-id="58d92-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="58d92-134">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="58d92-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="58d92-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="58d92-135">-VaultName</span></span>
<span data-ttu-id="58d92-136">Określa nazwę magazynu kluczy, do którego należy klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="58d92-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="58d92-137">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, która jest określana przez ten parametr i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="58d92-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="58d92-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58d92-138">-Confirm</span></span>
<span data-ttu-id="58d92-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="58d92-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58d92-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58d92-140">-WhatIf</span></span>
<span data-ttu-id="58d92-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58d92-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58d92-142">Polecenie cmdlet nie zostanie uruchomione. Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58d92-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58d92-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="58d92-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58d92-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58d92-144">CommonParameters</span></span>
<span data-ttu-id="58d92-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58d92-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58d92-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58d92-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58d92-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58d92-147">INPUTS</span></span>

### <span data-ttu-id="58d92-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="58d92-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="58d92-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58d92-149">OUTPUTS</span></span>

### <span data-ttu-id="58d92-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="58d92-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="58d92-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="58d92-151">NOTES</span></span>

## <span data-ttu-id="58d92-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58d92-152">RELATED LINKS</span></span>

[<span data-ttu-id="58d92-153">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="58d92-153">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="58d92-154">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="58d92-154">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="58d92-155">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="58d92-155">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

