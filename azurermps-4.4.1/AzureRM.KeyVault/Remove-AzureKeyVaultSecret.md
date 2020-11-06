---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://go.microsoft.com/fwlink/?LinkId=690300
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: e5ec1e2377b9a1c04fc10ce976bd800227baabed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551855"
---
# <span data-ttu-id="f22eb-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f22eb-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="f22eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f22eb-102">SYNOPSIS</span></span>
<span data-ttu-id="f22eb-103">Usuwa klucz tajny w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="f22eb-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f22eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f22eb-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f22eb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f22eb-105">DESCRIPTION</span></span>
<span data-ttu-id="f22eb-106">Polecenie cmdlet Remove-AzureKeyVaultSecret usuwa klucz tajny w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="f22eb-106">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="f22eb-107">Jeśli klucz tajny został przypadkowo usunięty, klucz tajny można odzyskać przy użyciu Undo-AzureKeyVaultSecretRemoval przez użytkownika ze specjalnymi uprawnieniami "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="f22eb-107">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="f22eb-108">To polecenie cmdlet ma wartość High dla właściwości **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="f22eb-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="f22eb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f22eb-109">EXAMPLES</span></span>

### <span data-ttu-id="f22eb-110">Przykład 1: Usuwanie klucza tajnego z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="f22eb-110">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="f22eb-111">To polecenie usuwa klucz tajny o nazwie FinanceSecret z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="f22eb-111">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="f22eb-112">Przykład 2: Usuwanie klucza tajnego z magazynu kluczy bez potwierdzenia użytkownika</span><span class="sxs-lookup"><span data-stu-id="f22eb-112">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="f22eb-113">To polecenie usuwa hasło o nazwie FinanceSecret z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="f22eb-113">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="f22eb-114">W poleceniu określono parametry *Force* i *Confirm* , a w związku z tym polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f22eb-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="f22eb-115">Przykład 3: trwałe przeczyszczanie usuniętego klucza tajnego w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="f22eb-115">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="f22eb-116">Polecenie to powoduje, że tajne o nazwie FinanceSecret jest przenoszone na stałe z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="f22eb-116">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="f22eb-117">Wykonanie tego polecenia cmdlet wymaga uprawnienia "Wyczyść", które musi być wcześniej i wyraźnie udzielone użytkownikowi dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f22eb-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="f22eb-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f22eb-118">PARAMETERS</span></span>

### <span data-ttu-id="f22eb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f22eb-119">-Force</span></span>
<span data-ttu-id="f22eb-120">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f22eb-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f22eb-121">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="f22eb-121">-InRemovedState</span></span>
<span data-ttu-id="f22eb-122">Jeśli jest obecny, usuwa uprzednio usunięte tajne hasło.</span><span class="sxs-lookup"><span data-stu-id="f22eb-122">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="f22eb-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f22eb-123">-Name</span></span>
<span data-ttu-id="f22eb-124">Określa nazwę wpisu tajnego.</span><span class="sxs-lookup"><span data-stu-id="f22eb-124">Specifies the name of a secret.</span></span>
<span data-ttu-id="f22eb-125">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza tajnego na podstawie nazwy, jaką ten parametr określa, nazwę magazynu kluczy i obecne środowisko.</span><span class="sxs-lookup"><span data-stu-id="f22eb-125">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f22eb-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f22eb-126">-PassThru</span></span>
<span data-ttu-id="f22eb-127">Wskazuje, że to polecenie cmdlet zwróci obiekt **Microsoft. Azure. Commands** .Attribute. model. models. Secret.</span><span class="sxs-lookup"><span data-stu-id="f22eb-127">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="f22eb-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f22eb-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f22eb-129">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="f22eb-129">-VaultName</span></span>
<span data-ttu-id="f22eb-130">Określa nazwę magazynu kluczy, do którego należy odpowiedni klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="f22eb-130">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="f22eb-131">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="f22eb-131">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f22eb-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f22eb-132">-Confirm</span></span>
<span data-ttu-id="f22eb-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f22eb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f22eb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f22eb-134">-WhatIf</span></span>
<span data-ttu-id="f22eb-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f22eb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f22eb-136">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f22eb-136">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f22eb-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f22eb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f22eb-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f22eb-138">-DefaultProfile</span></span>
<span data-ttu-id="f22eb-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f22eb-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f22eb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f22eb-140">CommonParameters</span></span>
<span data-ttu-id="f22eb-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f22eb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f22eb-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f22eb-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f22eb-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f22eb-143">INPUTS</span></span>

### <span data-ttu-id="f22eb-144">Ciąg</span><span class="sxs-lookup"><span data-stu-id="f22eb-144">String</span></span>

## <span data-ttu-id="f22eb-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f22eb-145">OUTPUTS</span></span>

### <span data-ttu-id="f22eb-146">Microsoft. Azure. Commands. platforming. models. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="f22eb-146">Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>
<span data-ttu-id="f22eb-147">To polecenie cmdlet zwraca wartość tylko wtedy, gdy określisz parametr *PassThru* .</span><span class="sxs-lookup"><span data-stu-id="f22eb-147">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="f22eb-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f22eb-148">NOTES</span></span>

## <span data-ttu-id="f22eb-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f22eb-149">RELATED LINKS</span></span>

[<span data-ttu-id="f22eb-150">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f22eb-150">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="f22eb-151">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f22eb-151">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="f22eb-152">Cofanie — AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="f22eb-152">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

