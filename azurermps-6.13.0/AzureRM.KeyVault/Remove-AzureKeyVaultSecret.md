---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: bff9c08a0c36fb7a4d89fb86d9c219491f3642b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545212"
---
# <span data-ttu-id="35616-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="35616-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="35616-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="35616-102">SYNOPSIS</span></span>
<span data-ttu-id="35616-103">Usuwa klucz tajny w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="35616-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35616-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="35616-104">SYNTAX</span></span>

### <span data-ttu-id="35616-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="35616-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35616-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="35616-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35616-107">Opis</span><span class="sxs-lookup"><span data-stu-id="35616-107">DESCRIPTION</span></span>
<span data-ttu-id="35616-108">Polecenie cmdlet Remove-AzureKeyVaultSecret usuwa klucz tajny w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="35616-108">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="35616-109">Jeśli klucz tajny został przypadkowo usunięty, klucz tajny można odzyskać przy użyciu Undo-AzureKeyVaultSecretRemoval przez użytkownika ze specjalnymi uprawnieniami "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="35616-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="35616-110">To polecenie cmdlet ma wartość High dla właściwości **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="35616-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="35616-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="35616-111">EXAMPLES</span></span>

### <span data-ttu-id="35616-112">Przykład 1: Usuwanie klucza tajnego z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="35616-112">Example 1: Remove a secret from a key vault</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru

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

<span data-ttu-id="35616-113">To polecenie usuwa klucz tajny o nazwie FinanceSecret z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="35616-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="35616-114">Przykład 2: Usuwanie klucza tajnego z magazynu kluczy bez potwierdzenia użytkownika</span><span class="sxs-lookup"><span data-stu-id="35616-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru -Force

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

<span data-ttu-id="35616-115">To polecenie usuwa hasło o nazwie FinanceSecret z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="35616-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="35616-116">W poleceniu określono parametry *Force* i *Confirm* , a w związku z tym polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="35616-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="35616-117">Przykład 3: trwałe przeczyszczanie usuniętego klucza tajnego w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="35616-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="35616-118">Polecenie to powoduje, że tajne o nazwie FinanceSecret jest przenoszone na stałe z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="35616-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="35616-119">Wykonanie tego polecenia cmdlet wymaga uprawnienia "Wyczyść", które musi być wcześniej i wyraźnie udzielone użytkownikowi dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="35616-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="35616-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35616-120">PARAMETERS</span></span>

### <span data-ttu-id="35616-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35616-121">-DefaultProfile</span></span>
<span data-ttu-id="35616-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="35616-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35616-123">-Force</span><span class="sxs-lookup"><span data-stu-id="35616-123">-Force</span></span>
<span data-ttu-id="35616-124">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="35616-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="35616-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="35616-125">-InputObject</span></span>
<span data-ttu-id="35616-126">Obiekt tajny magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="35616-126">Key Vault Secret Object</span></span>

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

### <span data-ttu-id="35616-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="35616-127">-InRemovedState</span></span>
<span data-ttu-id="35616-128">Jeśli jest obecny, usuwa uprzednio usunięte tajne hasło.</span><span class="sxs-lookup"><span data-stu-id="35616-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="35616-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="35616-129">-Name</span></span>
<span data-ttu-id="35616-130">Określa nazwę wpisu tajnego.</span><span class="sxs-lookup"><span data-stu-id="35616-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="35616-131">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza tajnego na podstawie nazwy, jaką ten parametr określa, nazwę magazynu kluczy i obecne środowisko.</span><span class="sxs-lookup"><span data-stu-id="35616-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="35616-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35616-132">-PassThru</span></span>
<span data-ttu-id="35616-133">Wskazuje, że to polecenie cmdlet zwróci obiekt **Microsoft. Azure. Commands** .Attribute. model. models. Secret.</span><span class="sxs-lookup"><span data-stu-id="35616-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="35616-134">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="35616-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="35616-135">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="35616-135">-VaultName</span></span>
<span data-ttu-id="35616-136">Określa nazwę magazynu kluczy, do którego należy odpowiedni klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="35616-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="35616-137">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="35616-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="35616-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="35616-138">-Confirm</span></span>
<span data-ttu-id="35616-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35616-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35616-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35616-140">-WhatIf</span></span>
<span data-ttu-id="35616-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35616-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35616-142">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35616-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35616-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="35616-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35616-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35616-144">CommonParameters</span></span>
<span data-ttu-id="35616-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35616-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35616-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35616-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35616-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35616-147">INPUTS</span></span>

### <span data-ttu-id="35616-148">Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="35616-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="35616-149">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="35616-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="35616-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="35616-150">OUTPUTS</span></span>

### <span data-ttu-id="35616-151">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="35616-151">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="35616-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="35616-152">NOTES</span></span>

## <span data-ttu-id="35616-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35616-153">RELATED LINKS</span></span>

[<span data-ttu-id="35616-154">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="35616-154">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="35616-155">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="35616-155">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="35616-156">Cofanie — AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="35616-156">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

