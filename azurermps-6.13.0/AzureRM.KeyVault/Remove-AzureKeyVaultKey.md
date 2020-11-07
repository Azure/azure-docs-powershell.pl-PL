---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
ms.openlocfilehash: ff7e5a02899d806633e485f06f419a6f1f2082a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546583"
---
# <span data-ttu-id="4d11b-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4d11b-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="4d11b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d11b-102">SYNOPSIS</span></span>
<span data-ttu-id="4d11b-103">Usuwa klucz w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="4d11b-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d11b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d11b-104">SYNTAX</span></span>

### <span data-ttu-id="4d11b-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4d11b-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d11b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4d11b-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d11b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4d11b-107">DESCRIPTION</span></span>
<span data-ttu-id="4d11b-108">Polecenie cmdlet Remove-AzureKeyVaultKey usuwa klucz w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="4d11b-108">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="4d11b-109">Jeśli usunięto przypadkowo klucz, można go odzyskać przy użyciu Undo-AzureKeyVaultKeyRemoval przez użytkownika ze specjalnymi uprawnieniami "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="4d11b-109">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="4d11b-110">To polecenie cmdlet ma wartość High dla właściwości **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="4d11b-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="4d11b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d11b-111">EXAMPLES</span></span>

### <span data-ttu-id="4d11b-112">Przykład 1: Usuwanie klucza z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="4d11b-112">Example 1: Remove a key from a key vault</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

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

<span data-ttu-id="4d11b-113">To polecenie usuwa klucz o nazwie ITSoftware z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="4d11b-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="4d11b-114">Przykład 2: Usuwanie klucza bez potwierdzenia użytkownika</span><span class="sxs-lookup"><span data-stu-id="4d11b-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="4d11b-115">To polecenie usuwa klucz o nazwie ITSoftware z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="4d11b-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="4d11b-116">Polecenie określa parametr *Force* , dlatego polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4d11b-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="4d11b-117">Przykład 3: trwałe przeczyszczanie usuniętego klucza z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="4d11b-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="4d11b-118">To polecenie usuwa klucz o nazwie ITSoftware z magazynu kluczy o nazwie contoso — trwałe.</span><span class="sxs-lookup"><span data-stu-id="4d11b-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="4d11b-119">Wykonanie tego polecenia cmdlet wymaga uprawnienia "Wyczyść", które musi być wcześniej i wyraźnie udzielone użytkownikowi dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="4d11b-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="4d11b-120">Przykład 4: usuwanie kluczy za pomocą operatora potoku</span><span class="sxs-lookup"><span data-stu-id="4d11b-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="4d11b-121">To polecenie pobiera wszystkie klucze w magazynie kluczy o nazwie Contoso i przekazuje je do polecenia cmdlet **WHERE-Object** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="4d11b-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4d11b-122">Polecenie cmdlet przekazuje klucze, których atrybut **Enabled** jest wartością $false dla bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d11b-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="4d11b-123">Te klucze są usuwane przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d11b-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="4d11b-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d11b-124">PARAMETERS</span></span>

### <span data-ttu-id="4d11b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d11b-125">-DefaultProfile</span></span>
<span data-ttu-id="4d11b-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4d11b-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d11b-127">-Force</span><span class="sxs-lookup"><span data-stu-id="4d11b-127">-Force</span></span>
<span data-ttu-id="4d11b-128">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4d11b-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4d11b-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4d11b-129">-InputObject</span></span>
<span data-ttu-id="4d11b-130">Obiekt pakietu</span><span class="sxs-lookup"><span data-stu-id="4d11b-130">KeyBundle Object</span></span>

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

### <span data-ttu-id="4d11b-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="4d11b-131">-InRemovedState</span></span>
<span data-ttu-id="4d11b-132">Trwałe usunięcie wcześniej usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="4d11b-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="4d11b-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4d11b-133">-Name</span></span>
<span data-ttu-id="4d11b-134">Określa nazwę klucza, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="4d11b-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="4d11b-135">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza na podstawie nazwy, jaką określa ten parametr, nazwy magazynu kluczy i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="4d11b-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="4d11b-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d11b-136">-PassThru</span></span>
<span data-ttu-id="4d11b-137">Wskazuje, że to polecenie cmdlet zwróci obiekt **Microsoft. Azure. Commands. DataModel. models. PSKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="4d11b-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="4d11b-138">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="4d11b-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4d11b-139">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="4d11b-139">-VaultName</span></span>
<span data-ttu-id="4d11b-140">Określa nazwę magazynu kluczy, z którego należy usunąć klucz.</span><span class="sxs-lookup"><span data-stu-id="4d11b-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="4d11b-141">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="4d11b-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="4d11b-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d11b-142">-Confirm</span></span>
<span data-ttu-id="4d11b-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d11b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d11b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d11b-144">-WhatIf</span></span>
<span data-ttu-id="4d11b-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d11b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d11b-146">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d11b-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d11b-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4d11b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d11b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d11b-148">CommonParameters</span></span>
<span data-ttu-id="4d11b-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d11b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d11b-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d11b-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d11b-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d11b-151">INPUTS</span></span>

### <span data-ttu-id="4d11b-152">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4d11b-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>
<span data-ttu-id="4d11b-153">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4d11b-153">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4d11b-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d11b-154">OUTPUTS</span></span>

### <span data-ttu-id="4d11b-155">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4d11b-155">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="4d11b-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d11b-156">NOTES</span></span>

## <span data-ttu-id="4d11b-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d11b-157">RELATED LINKS</span></span>

[<span data-ttu-id="4d11b-158">Dodaj-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4d11b-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="4d11b-159">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4d11b-159">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="4d11b-160">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="4d11b-160">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="4d11b-161">Cofanie — AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="4d11b-161">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)
