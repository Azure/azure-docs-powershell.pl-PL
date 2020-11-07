---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultkey
schema: 2.0.0
ms.openlocfilehash: 911ea06fdfa9d4d90f8c9935e3e98c026c70cce5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897374"
---
# <span data-ttu-id="3312f-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3312f-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="3312f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3312f-102">SYNOPSIS</span></span>
<span data-ttu-id="3312f-103">Usuwa klucz w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="3312f-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3312f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3312f-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3312f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3312f-105">DESCRIPTION</span></span>
<span data-ttu-id="3312f-106">Polecenie cmdlet Remove-AzureKeyVaultKey usuwa klucz w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="3312f-106">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="3312f-107">Jeśli usunięto przypadkowo klucz, można go odzyskać przy użyciu Undo-AzureKeyVaultKeyRemoval przez użytkownika ze specjalnymi uprawnieniami "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="3312f-107">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="3312f-108">To polecenie cmdlet ma wartość High dla właściwości **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="3312f-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="3312f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3312f-109">EXAMPLES</span></span>

### <span data-ttu-id="3312f-110">Przykład 1: Usuwanie klucza z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="3312f-110">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="3312f-111">To polecenie usuwa klucz o nazwie ITSoftware z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="3312f-111">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="3312f-112">Przykład 2: Usuwanie klucza bez potwierdzenia użytkownika</span><span class="sxs-lookup"><span data-stu-id="3312f-112">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="3312f-113">To polecenie usuwa klucz o nazwie ITSoftware z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="3312f-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="3312f-114">W poleceniu określono parametry *Force* i *Confirm* , a w związku z tym polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3312f-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="3312f-115">Przykład 3: trwałe przeczyszczanie usuniętego klucza z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="3312f-115">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="3312f-116">To polecenie usuwa klucz o nazwie ITSoftware z magazynu kluczy o nazwie contoso — trwałe.</span><span class="sxs-lookup"><span data-stu-id="3312f-116">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="3312f-117">Wykonanie tego polecenia cmdlet wymaga uprawnienia "Wyczyść", które musi być wcześniej i wyraźnie udzielone użytkownikowi dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="3312f-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="3312f-118">Przykład 4: usuwanie kluczy za pomocą operatora potoku</span><span class="sxs-lookup"><span data-stu-id="3312f-118">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="3312f-119">To polecenie pobiera wszystkie klucze w magazynie kluczy o nazwie Contoso i przekazuje je do polecenia cmdlet **WHERE-Object** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="3312f-119">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3312f-120">Polecenie cmdlet przekazuje klucze, których atrybut **Enabled** jest wartością $false dla bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3312f-120">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="3312f-121">Te klucze są usuwane przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3312f-121">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="3312f-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3312f-122">PARAMETERS</span></span>

### <span data-ttu-id="3312f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3312f-123">-DefaultProfile</span></span>
<span data-ttu-id="3312f-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3312f-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3312f-125">-Force</span><span class="sxs-lookup"><span data-stu-id="3312f-125">-Force</span></span>
<span data-ttu-id="3312f-126">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3312f-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3312f-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="3312f-127">-InRemovedState</span></span>
<span data-ttu-id="3312f-128">Trwałe usunięcie wcześniej usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="3312f-128">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="3312f-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3312f-129">-Name</span></span>
<span data-ttu-id="3312f-130">Określa nazwę klucza, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="3312f-130">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="3312f-131">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza na podstawie nazwy, jaką określa ten parametr, nazwy magazynu kluczy i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="3312f-131">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3312f-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3312f-132">-PassThru</span></span>
<span data-ttu-id="3312f-133">Wskazuje, że to polecenie cmdlet zwróci element **Microsoft. Azure. Commands** . objecting. models</span><span class="sxs-lookup"><span data-stu-id="3312f-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="3312f-134">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3312f-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3312f-135">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="3312f-135">-VaultName</span></span>
<span data-ttu-id="3312f-136">Określa nazwę magazynu kluczy, z którego należy usunąć klucz.</span><span class="sxs-lookup"><span data-stu-id="3312f-136">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="3312f-137">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="3312f-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="3312f-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3312f-138">-Confirm</span></span>
<span data-ttu-id="3312f-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3312f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3312f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3312f-140">-WhatIf</span></span>
<span data-ttu-id="3312f-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3312f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3312f-142">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3312f-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3312f-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3312f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3312f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3312f-144">CommonParameters</span></span>
<span data-ttu-id="3312f-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3312f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3312f-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3312f-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3312f-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3312f-147">INPUTS</span></span>

### <span data-ttu-id="3312f-148">Ciąg</span><span class="sxs-lookup"><span data-stu-id="3312f-148">String</span></span>

## <span data-ttu-id="3312f-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3312f-149">OUTPUTS</span></span>

### <span data-ttu-id="3312f-150">Microsoft. Azure. Commands. platforming. models. DeletedKeyBundle</span><span class="sxs-lookup"><span data-stu-id="3312f-150">Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>
<span data-ttu-id="3312f-151">To polecenie cmdlet zwraca wartość tylko wtedy, gdy określisz parametr *PassThru* .</span><span class="sxs-lookup"><span data-stu-id="3312f-151">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="3312f-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3312f-152">NOTES</span></span>

## <span data-ttu-id="3312f-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3312f-153">RELATED LINKS</span></span>

[<span data-ttu-id="3312f-154">Dodaj-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3312f-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="3312f-155">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3312f-155">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="3312f-156">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="3312f-156">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="3312f-157">Cofanie — AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="3312f-157">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

