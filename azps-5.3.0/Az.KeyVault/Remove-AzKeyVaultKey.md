---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: e78b6729061efe5a83f31bd25b9e542c09627ca3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503363"
---
# <span data-ttu-id="cfec7-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cfec7-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="cfec7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cfec7-102">SYNOPSIS</span></span>
<span data-ttu-id="cfec7-103">Usuwa klucz w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="cfec7-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="cfec7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cfec7-104">SYNTAX</span></span>

### <span data-ttu-id="cfec7-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cfec7-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfec7-106">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="cfec7-106">HsmByVaultName</span></span>
```
Remove-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfec7-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cfec7-107">ByInputObject</span></span>
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfec7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cfec7-108">DESCRIPTION</span></span>
<span data-ttu-id="cfec7-109">Polecenie cmdlet Remove-AzKeyVaultKey usuwa klucz w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="cfec7-109">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="cfec7-110">Jeśli usunięto przypadkowo klucz, można go odzyskać przy użyciu Undo-AzKeyVaultKeyRemoval przez użytkownika ze specjalnymi uprawnieniami "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="cfec7-110">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="cfec7-111">To polecenie cmdlet ma wartość High dla właściwości **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="cfec7-111">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="cfec7-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cfec7-112">EXAMPLES</span></span>

### <span data-ttu-id="cfec7-113">Przykład 1: Usuwanie klucza z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="cfec7-113">Example 1: Remove a key from a key vault</span></span>
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

<span data-ttu-id="cfec7-114">To polecenie usuwa klucz o nazwie ITSoftware z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="cfec7-114">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="cfec7-115">Przykład 2: Usuwanie klucza bez potwierdzenia użytkownika</span><span class="sxs-lookup"><span data-stu-id="cfec7-115">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="cfec7-116">To polecenie usuwa klucz o nazwie ITSoftware z magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="cfec7-116">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="cfec7-117">Polecenie określa parametr *Force* , dlatego polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cfec7-117">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="cfec7-118">Przykład 3: trwałe przeczyszczanie usuniętego klucza z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="cfec7-118">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="cfec7-119">To polecenie usuwa klucz o nazwie ITSoftware z magazynu kluczy o nazwie contoso — trwałe.</span><span class="sxs-lookup"><span data-stu-id="cfec7-119">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="cfec7-120">Wykonanie tego polecenia cmdlet wymaga uprawnienia "Wyczyść", które musi być wcześniej i wyraźnie udzielone użytkownikowi dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="cfec7-120">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="cfec7-121">Przykład 4: usuwanie kluczy za pomocą operatora potoku</span><span class="sxs-lookup"><span data-stu-id="cfec7-121">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="cfec7-122">To polecenie pobiera wszystkie klucze w magazynie kluczy o nazwie Contoso i przekazuje je do polecenia cmdlet **WHERE-Object** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="cfec7-122">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cfec7-123">Polecenie cmdlet przekazuje klucze, których atrybut **Enabled** jest wartością $false dla bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfec7-123">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="cfec7-124">Te klucze są usuwane przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfec7-124">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="cfec7-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cfec7-125">PARAMETERS</span></span>

### <span data-ttu-id="cfec7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfec7-126">-DefaultProfile</span></span>
<span data-ttu-id="cfec7-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cfec7-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cfec7-128">-Force</span><span class="sxs-lookup"><span data-stu-id="cfec7-128">-Force</span></span>
<span data-ttu-id="cfec7-129">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cfec7-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cfec7-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="cfec7-130">-HsmName</span></span>
<span data-ttu-id="cfec7-131">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="cfec7-131">HSM name.</span></span> <span data-ttu-id="cfec7-132">Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="cfec7-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfec7-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cfec7-133">-InputObject</span></span>
<span data-ttu-id="cfec7-134">Obiekt pakietu</span><span class="sxs-lookup"><span data-stu-id="cfec7-134">KeyBundle Object</span></span>

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

### <span data-ttu-id="cfec7-135">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="cfec7-135">-InRemovedState</span></span>
<span data-ttu-id="cfec7-136">Trwałe usunięcie wcześniej usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="cfec7-136">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="cfec7-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cfec7-137">-Name</span></span>
<span data-ttu-id="cfec7-138">Określa nazwę klucza, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="cfec7-138">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="cfec7-139">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza na podstawie nazwy, jaką określa ten parametr, nazwy magazynu kluczy i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="cfec7-139">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, HsmByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfec7-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cfec7-140">-PassThru</span></span>
<span data-ttu-id="cfec7-141">Wskazuje, że to polecenie cmdlet zwróci obiekt **Microsoft. Azure. Commands. DataModel. models. PSKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="cfec7-141">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="cfec7-142">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="cfec7-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cfec7-143">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="cfec7-143">-VaultName</span></span>
<span data-ttu-id="cfec7-144">Określa nazwę magazynu kluczy, z którego należy usunąć klucz.</span><span class="sxs-lookup"><span data-stu-id="cfec7-144">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="cfec7-145">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="cfec7-145">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="cfec7-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cfec7-146">-Confirm</span></span>
<span data-ttu-id="cfec7-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfec7-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfec7-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfec7-148">-WhatIf</span></span>
<span data-ttu-id="cfec7-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfec7-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfec7-150">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfec7-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfec7-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cfec7-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfec7-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfec7-152">CommonParameters</span></span>
<span data-ttu-id="cfec7-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfec7-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfec7-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfec7-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfec7-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cfec7-155">INPUTS</span></span>

### <span data-ttu-id="cfec7-156">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="cfec7-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="cfec7-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cfec7-157">OUTPUTS</span></span>

### <span data-ttu-id="cfec7-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cfec7-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="cfec7-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cfec7-159">NOTES</span></span>

## <span data-ttu-id="cfec7-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cfec7-160">RELATED LINKS</span></span>

[<span data-ttu-id="cfec7-161">Dodaj-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cfec7-161">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="cfec7-162">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cfec7-162">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="cfec7-163">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="cfec7-163">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

[<span data-ttu-id="cfec7-164">Cofanie — AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="cfec7-164">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

