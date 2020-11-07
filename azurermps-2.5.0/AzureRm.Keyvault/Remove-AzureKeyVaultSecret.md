---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: 56cc6b11c517379f1d13ebe2dbf2cee00f18211b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897365"
---
# <span data-ttu-id="d0795-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d0795-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="d0795-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0795-102">SYNOPSIS</span></span>
<span data-ttu-id="d0795-103">Usuwa klucz tajny w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="d0795-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0795-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0795-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0795-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d0795-105">DESCRIPTION</span></span>
<span data-ttu-id="d0795-106">Polecenie cmdlet Remove-AzureKeyVaultSecret usuwa klucz tajny w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="d0795-106">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="d0795-107">Jeśli klucz tajny został przypadkowo usunięty, klucz tajny można odzyskać przy użyciu Undo-AzureKeyVaultSecretRemoval przez użytkownika ze specjalnymi uprawnieniami "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="d0795-107">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="d0795-108">To polecenie cmdlet ma wartość High dla właściwości **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="d0795-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="d0795-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0795-109">EXAMPLES</span></span>

### <span data-ttu-id="d0795-110">Przykład 1: Usuwanie klucza tajnego z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="d0795-110">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="d0795-111">To polecenie usuwa klucz tajny o nazwie FinanceSecret z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="d0795-111">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="d0795-112">Przykład 2: Usuwanie klucza tajnego z magazynu kluczy bez potwierdzenia użytkownika</span><span class="sxs-lookup"><span data-stu-id="d0795-112">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="d0795-113">To polecenie usuwa hasło o nazwie FinanceSecret z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="d0795-113">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="d0795-114">W poleceniu określono parametry *Force* i *Confirm* , a w związku z tym polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d0795-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="d0795-115">Przykład 3: trwałe przeczyszczanie usuniętego klucza tajnego w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="d0795-115">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="d0795-116">Polecenie to powoduje, że tajne o nazwie FinanceSecret jest przenoszone na stałe z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="d0795-116">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="d0795-117">Wykonanie tego polecenia cmdlet wymaga uprawnienia "Wyczyść", które musi być wcześniej i wyraźnie udzielone użytkownikowi dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d0795-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="d0795-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0795-118">PARAMETERS</span></span>

### <span data-ttu-id="d0795-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0795-119">-DefaultProfile</span></span>
<span data-ttu-id="d0795-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d0795-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0795-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d0795-121">-Force</span></span>
<span data-ttu-id="d0795-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d0795-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0795-123">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="d0795-123">-InRemovedState</span></span>
<span data-ttu-id="d0795-124">Jeśli jest obecny, usuwa uprzednio usunięte tajne hasło.</span><span class="sxs-lookup"><span data-stu-id="d0795-124">If present, removes the previously deleted secret permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0795-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d0795-125">-Name</span></span>
<span data-ttu-id="d0795-126">Określa nazwę wpisu tajnego.</span><span class="sxs-lookup"><span data-stu-id="d0795-126">Specifies the name of a secret.</span></span>
<span data-ttu-id="d0795-127">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza tajnego na podstawie nazwy, jaką ten parametr określa, nazwę magazynu kluczy i obecne środowisko.</span><span class="sxs-lookup"><span data-stu-id="d0795-127">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0795-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0795-128">-PassThru</span></span>
<span data-ttu-id="d0795-129">Wskazuje, że to polecenie cmdlet zwróci obiekt **Microsoft. Azure. Commands** .Attribute. model. models. Secret.</span><span class="sxs-lookup"><span data-stu-id="d0795-129">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="d0795-130">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d0795-130">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0795-131">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="d0795-131">-VaultName</span></span>
<span data-ttu-id="d0795-132">Określa nazwę magazynu kluczy, do którego należy odpowiedni klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="d0795-132">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="d0795-133">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="d0795-133">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="d0795-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d0795-134">-Confirm</span></span>
<span data-ttu-id="d0795-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0795-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0795-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0795-136">-WhatIf</span></span>
<span data-ttu-id="d0795-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0795-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0795-138">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0795-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0795-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d0795-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0795-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0795-140">CommonParameters</span></span>
<span data-ttu-id="d0795-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0795-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0795-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0795-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0795-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0795-143">INPUTS</span></span>

### <span data-ttu-id="d0795-144">Ciąg</span><span class="sxs-lookup"><span data-stu-id="d0795-144">String</span></span>

## <span data-ttu-id="d0795-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0795-145">OUTPUTS</span></span>

### <span data-ttu-id="d0795-146">Microsoft. Azure. Commands. platforming. models. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="d0795-146">Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>
<span data-ttu-id="d0795-147">To polecenie cmdlet zwraca wartość tylko wtedy, gdy określisz parametr *PassThru* .</span><span class="sxs-lookup"><span data-stu-id="d0795-147">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="d0795-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0795-148">NOTES</span></span>

## <span data-ttu-id="d0795-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0795-149">RELATED LINKS</span></span>

[<span data-ttu-id="d0795-150">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d0795-150">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="d0795-151">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d0795-151">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="d0795-152">Cofanie — AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="d0795-152">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

