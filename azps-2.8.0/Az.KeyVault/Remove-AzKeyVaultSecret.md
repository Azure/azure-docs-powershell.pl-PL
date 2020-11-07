---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: 2c52d6cbd5a3e027baf41959d28816f63062b046
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705127"
---
# <span data-ttu-id="2f99b-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2f99b-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="2f99b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f99b-102">SYNOPSIS</span></span>
<span data-ttu-id="2f99b-103">Usuwa klucz tajny w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="2f99b-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="2f99b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f99b-104">SYNTAX</span></span>

### <span data-ttu-id="2f99b-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2f99b-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f99b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2f99b-106">ByInputObject</span></span>
```
Remove-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f99b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2f99b-107">DESCRIPTION</span></span>
<span data-ttu-id="2f99b-108">Polecenie cmdlet Remove-AzKeyVaultSecret usuwa klucz tajny w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="2f99b-108">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="2f99b-109">Jeśli klucz tajny został przypadkowo usunięty, klucz tajny można odzyskać przy użyciu Undo-AzKeyVaultSecretRemoval przez użytkownika ze specjalnymi uprawnieniami "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="2f99b-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="2f99b-110">To polecenie cmdlet ma wartość High dla właściwości **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="2f99b-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="2f99b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f99b-111">EXAMPLES</span></span>

### <span data-ttu-id="2f99b-112">Przykład 1: Usuwanie klucza tajnego z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="2f99b-112">Example 1: Remove a secret from a key vault</span></span>
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

<span data-ttu-id="2f99b-113">To polecenie usuwa klucz tajny o nazwie FinanceSecret z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="2f99b-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="2f99b-114">Przykład 2: Usuwanie klucza tajnego z magazynu kluczy bez potwierdzenia użytkownika</span><span class="sxs-lookup"><span data-stu-id="2f99b-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
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

<span data-ttu-id="2f99b-115">To polecenie usuwa hasło o nazwie FinanceSecret z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="2f99b-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="2f99b-116">W poleceniu określono parametry *Force* i *Confirm* , a w związku z tym polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2f99b-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="2f99b-117">Przykład 3: trwałe przeczyszczanie usuniętego klucza tajnego w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="2f99b-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="2f99b-118">Polecenie to powoduje, że tajne o nazwie FinanceSecret jest przenoszone na stałe z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="2f99b-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="2f99b-119">Wykonanie tego polecenia cmdlet wymaga uprawnienia "Wyczyść", które musi być wcześniej i wyraźnie udzielone użytkownikowi dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="2f99b-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="2f99b-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f99b-120">PARAMETERS</span></span>

### <span data-ttu-id="2f99b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f99b-121">-DefaultProfile</span></span>
<span data-ttu-id="2f99b-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2f99b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f99b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="2f99b-123">-Force</span></span>
<span data-ttu-id="2f99b-124">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2f99b-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2f99b-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2f99b-125">-InputObject</span></span>
<span data-ttu-id="2f99b-126">Obiekt tajny magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="2f99b-126">Key Vault Secret Object</span></span>

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

### <span data-ttu-id="2f99b-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="2f99b-127">-InRemovedState</span></span>
<span data-ttu-id="2f99b-128">Jeśli jest obecny, usuwa uprzednio usunięte tajne hasło.</span><span class="sxs-lookup"><span data-stu-id="2f99b-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="2f99b-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2f99b-129">-Name</span></span>
<span data-ttu-id="2f99b-130">Określa nazwę wpisu tajnego.</span><span class="sxs-lookup"><span data-stu-id="2f99b-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="2f99b-131">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza tajnego na podstawie nazwy, jaką ten parametr określa, nazwę magazynu kluczy i obecne środowisko.</span><span class="sxs-lookup"><span data-stu-id="2f99b-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="2f99b-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f99b-132">-PassThru</span></span>
<span data-ttu-id="2f99b-133">Wskazuje, że to polecenie cmdlet zwróci obiekt **Microsoft. Azure. Commands** .Attribute. model. models. Secret.</span><span class="sxs-lookup"><span data-stu-id="2f99b-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="2f99b-134">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="2f99b-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2f99b-135">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="2f99b-135">-VaultName</span></span>
<span data-ttu-id="2f99b-136">Określa nazwę magazynu kluczy, do którego należy odpowiedni klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="2f99b-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="2f99b-137">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="2f99b-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="2f99b-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f99b-138">-Confirm</span></span>
<span data-ttu-id="2f99b-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f99b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f99b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f99b-140">-WhatIf</span></span>
<span data-ttu-id="2f99b-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f99b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f99b-142">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f99b-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f99b-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2f99b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f99b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f99b-144">CommonParameters</span></span>
<span data-ttu-id="2f99b-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f99b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f99b-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f99b-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f99b-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f99b-147">INPUTS</span></span>

### <span data-ttu-id="2f99b-148">Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="2f99b-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="2f99b-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f99b-149">OUTPUTS</span></span>

### <span data-ttu-id="2f99b-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2f99b-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="2f99b-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f99b-151">NOTES</span></span>

## <span data-ttu-id="2f99b-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f99b-152">RELATED LINKS</span></span>

[<span data-ttu-id="2f99b-153">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2f99b-153">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="2f99b-154">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2f99b-154">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="2f99b-155">Cofanie — AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="2f99b-155">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)
