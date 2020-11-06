---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://go.microsoft.com/fwlink/?LinkId=690299
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
ms.openlocfilehash: b5f2917da71e8c4539660dbb91dd81f3fb5d7959
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551868"
---
# <span data-ttu-id="fd4ac-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fd4ac-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="fd4ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd4ac-102">SYNOPSIS</span></span>
<span data-ttu-id="fd4ac-103">Usuwa klucz w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd4ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd4ac-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd4ac-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fd4ac-105">DESCRIPTION</span></span>
<span data-ttu-id="fd4ac-106">Polecenie cmdlet Remove-AzureKeyVaultKey usuwa klucz w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-106">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="fd4ac-107">Jeśli usunięto przypadkowo klucz, można go odzyskać przy użyciu Undo-AzureKeyVaultKeyRemoval przez użytkownika ze specjalnymi uprawnieniami "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="fd4ac-107">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="fd4ac-108">To polecenie cmdlet ma wartość High dla właściwości **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="fd4ac-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="fd4ac-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd4ac-109">EXAMPLES</span></span>

### <span data-ttu-id="fd4ac-110">Przykład 1: Usuwanie klucza z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="fd4ac-110">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="fd4ac-111">To polecenie usuwa klucz o nazwie ITSoftware z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-111">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="fd4ac-112">Przykład 2: Usuwanie klucza bez potwierdzenia użytkownika</span><span class="sxs-lookup"><span data-stu-id="fd4ac-112">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="fd4ac-113">To polecenie usuwa klucz o nazwie ITSoftware z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="fd4ac-114">W poleceniu określono parametry *Force* i *Confirm* , a w związku z tym polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="fd4ac-115">Przykład 3: trwałe przeczyszczanie usuniętego klucza z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="fd4ac-115">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="fd4ac-116">To polecenie usuwa klucz o nazwie ITSoftware z magazynu kluczy o nazwie contoso — trwałe.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-116">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="fd4ac-117">Wykonanie tego polecenia cmdlet wymaga uprawnienia "Wyczyść", które musi być wcześniej i wyraźnie udzielone użytkownikowi dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="fd4ac-118">Przykład 4: usuwanie kluczy za pomocą operatora potoku</span><span class="sxs-lookup"><span data-stu-id="fd4ac-118">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="fd4ac-119">To polecenie pobiera wszystkie klucze w magazynie kluczy o nazwie Contoso i przekazuje je do polecenia cmdlet **WHERE-Object** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-119">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fd4ac-120">Polecenie cmdlet przekazuje klucze, których atrybut **Enabled** jest wartością $false dla bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-120">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="fd4ac-121">Te klucze są usuwane przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-121">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="fd4ac-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd4ac-122">PARAMETERS</span></span>

### <span data-ttu-id="fd4ac-123">-Force</span><span class="sxs-lookup"><span data-stu-id="fd4ac-123">-Force</span></span>
<span data-ttu-id="fd4ac-124">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fd4ac-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="fd4ac-125">-InRemovedState</span></span>
<span data-ttu-id="fd4ac-126">Trwałe usunięcie wcześniej usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-126">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="fd4ac-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fd4ac-127">-Name</span></span>
<span data-ttu-id="fd4ac-128">Określa nazwę klucza, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-128">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="fd4ac-129">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza na podstawie nazwy, jaką określa ten parametr, nazwy magazynu kluczy i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-129">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd4ac-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd4ac-130">-PassThru</span></span>
<span data-ttu-id="fd4ac-131">Wskazuje, że to polecenie cmdlet zwróci element **Microsoft. Azure. Commands** . objecting. models</span><span class="sxs-lookup"><span data-stu-id="fd4ac-131">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="fd4ac-132">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fd4ac-133">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="fd4ac-133">-VaultName</span></span>
<span data-ttu-id="fd4ac-134">Określa nazwę magazynu kluczy, z którego należy usunąć klucz.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-134">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="fd4ac-135">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-135">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="fd4ac-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd4ac-136">-Confirm</span></span>
<span data-ttu-id="fd4ac-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd4ac-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd4ac-138">-WhatIf</span></span>
<span data-ttu-id="fd4ac-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd4ac-140">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-140">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd4ac-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd4ac-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd4ac-142">-DefaultProfile</span></span>
<span data-ttu-id="fd4ac-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd4ac-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd4ac-144">CommonParameters</span></span>
<span data-ttu-id="fd4ac-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd4ac-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd4ac-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd4ac-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd4ac-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd4ac-147">INPUTS</span></span>

### <span data-ttu-id="fd4ac-148">Ciąg</span><span class="sxs-lookup"><span data-stu-id="fd4ac-148">String</span></span>

## <span data-ttu-id="fd4ac-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd4ac-149">OUTPUTS</span></span>

### <span data-ttu-id="fd4ac-150">Microsoft. Azure. Commands. platforming. models. DeletedKeyBundle</span><span class="sxs-lookup"><span data-stu-id="fd4ac-150">Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>
<span data-ttu-id="fd4ac-151">To polecenie cmdlet zwraca wartość tylko wtedy, gdy określisz parametr *PassThru* .</span><span class="sxs-lookup"><span data-stu-id="fd4ac-151">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="fd4ac-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd4ac-152">NOTES</span></span>

## <span data-ttu-id="fd4ac-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd4ac-153">RELATED LINKS</span></span>

[<span data-ttu-id="fd4ac-154">Dodaj-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fd4ac-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="fd4ac-155">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fd4ac-155">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="fd4ac-156">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="fd4ac-156">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="fd4ac-157">Cofanie — AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="fd4ac-157">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

