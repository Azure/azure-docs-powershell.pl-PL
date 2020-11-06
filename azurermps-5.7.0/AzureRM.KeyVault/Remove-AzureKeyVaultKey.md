---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
ms.openlocfilehash: 5244ed9a8803be07a46c50a15553a4863f7907d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544283"
---
# <span data-ttu-id="b3f75-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b3f75-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="b3f75-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3f75-102">SYNOPSIS</span></span>
<span data-ttu-id="b3f75-103">Usuwa klucz w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="b3f75-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3f75-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3f75-104">SYNTAX</span></span>

### <span data-ttu-id="b3f75-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b3f75-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3f75-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b3f75-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3f75-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b3f75-107">DESCRIPTION</span></span>
<span data-ttu-id="b3f75-108">Polecenie cmdlet Remove-AzureKeyVaultKey usuwa klucz w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="b3f75-108">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="b3f75-109">Jeśli usunięto przypadkowo klucz, można go odzyskać przy użyciu Undo-AzureKeyVaultKeyRemoval przez użytkownika ze specjalnymi uprawnieniami "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="b3f75-109">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="b3f75-110">To polecenie cmdlet ma wartość High dla właściwości **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="b3f75-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="b3f75-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3f75-111">EXAMPLES</span></span>

### <span data-ttu-id="b3f75-112">Przykład 1: Usuwanie klucza z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="b3f75-112">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="b3f75-113">To polecenie usuwa klucz o nazwie ITSoftware z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="b3f75-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="b3f75-114">Przykład 2: Usuwanie klucza bez potwierdzenia użytkownika</span><span class="sxs-lookup"><span data-stu-id="b3f75-114">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="b3f75-115">To polecenie usuwa klucz o nazwie ITSoftware z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="b3f75-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="b3f75-116">W poleceniu określono parametry *Force* i *Confirm* , a w związku z tym polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b3f75-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="b3f75-117">Przykład 3: trwałe przeczyszczanie usuniętego klucza z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="b3f75-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="b3f75-118">To polecenie usuwa klucz o nazwie ITSoftware z magazynu kluczy o nazwie contoso — trwałe.</span><span class="sxs-lookup"><span data-stu-id="b3f75-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="b3f75-119">Wykonanie tego polecenia cmdlet wymaga uprawnienia "Wyczyść", które musi być wcześniej i wyraźnie udzielone użytkownikowi dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="b3f75-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="b3f75-120">Przykład 4: usuwanie kluczy za pomocą operatora potoku</span><span class="sxs-lookup"><span data-stu-id="b3f75-120">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="b3f75-121">To polecenie pobiera wszystkie klucze w magazynie kluczy o nazwie Contoso i przekazuje je do polecenia cmdlet **WHERE-Object** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="b3f75-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b3f75-122">Polecenie cmdlet przekazuje klucze, których atrybut **Enabled** jest wartością $false dla bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3f75-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="b3f75-123">Te klucze są usuwane przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3f75-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="b3f75-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3f75-124">PARAMETERS</span></span>

### <span data-ttu-id="b3f75-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3f75-125">-DefaultProfile</span></span>
<span data-ttu-id="b3f75-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b3f75-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3f75-127">-Force</span><span class="sxs-lookup"><span data-stu-id="b3f75-127">-Force</span></span>
<span data-ttu-id="b3f75-128">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b3f75-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b3f75-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b3f75-129">-InputObject</span></span>
<span data-ttu-id="b3f75-130">Obiekt pakietu</span><span class="sxs-lookup"><span data-stu-id="b3f75-130">KeyBundle Object</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f75-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="b3f75-131">-InRemovedState</span></span>
<span data-ttu-id="b3f75-132">Trwałe usunięcie wcześniej usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="b3f75-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="b3f75-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b3f75-133">-Name</span></span>
<span data-ttu-id="b3f75-134">Określa nazwę klucza, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="b3f75-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="b3f75-135">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza na podstawie nazwy, jaką określa ten parametr, nazwy magazynu kluczy i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="b3f75-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f75-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3f75-136">-PassThru</span></span>
<span data-ttu-id="b3f75-137">Wskazuje, że to polecenie cmdlet zwróci element **Microsoft. Azure. Commands** . objecting. models</span><span class="sxs-lookup"><span data-stu-id="b3f75-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="b3f75-138">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b3f75-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b3f75-139">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="b3f75-139">-VaultName</span></span>
<span data-ttu-id="b3f75-140">Określa nazwę magazynu kluczy, z którego należy usunąć klucz.</span><span class="sxs-lookup"><span data-stu-id="b3f75-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="b3f75-141">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="b3f75-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f75-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3f75-142">-Confirm</span></span>
<span data-ttu-id="b3f75-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3f75-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3f75-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3f75-144">-WhatIf</span></span>
<span data-ttu-id="b3f75-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3f75-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3f75-146">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3f75-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3f75-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b3f75-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3f75-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3f75-148">CommonParameters</span></span>
<span data-ttu-id="b3f75-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3f75-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3f75-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3f75-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3f75-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3f75-151">INPUTS</span></span>

### <span data-ttu-id="b3f75-152">Ciąg</span><span class="sxs-lookup"><span data-stu-id="b3f75-152">String</span></span>

## <span data-ttu-id="b3f75-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3f75-153">OUTPUTS</span></span>

### <span data-ttu-id="b3f75-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b3f75-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>
<span data-ttu-id="b3f75-155">To polecenie cmdlet zwraca wartość tylko wtedy, gdy określisz parametr *PassThru* .</span><span class="sxs-lookup"><span data-stu-id="b3f75-155">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="b3f75-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3f75-156">NOTES</span></span>

## <span data-ttu-id="b3f75-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3f75-157">RELATED LINKS</span></span>

[<span data-ttu-id="b3f75-158">Dodaj-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b3f75-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="b3f75-159">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b3f75-159">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="b3f75-160">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="b3f75-160">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="b3f75-161">Cofanie — AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="b3f75-161">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

