---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
ms.openlocfilehash: 15a9466dd0caac6ebe7497942de36e832b89ee55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224255"
---
# <span data-ttu-id="660f9-101">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="660f9-101">Remove-AzManagedHsmKey</span></span>

## <span data-ttu-id="660f9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="660f9-102">SYNOPSIS</span></span>
<span data-ttu-id="660f9-103">Usuwa klucz z zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="660f9-103">Deletes a key in a managed HSM.</span></span>

## <span data-ttu-id="660f9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="660f9-104">SYNTAX</span></span>

### <span data-ttu-id="660f9-105">RemoveByKeyNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="660f9-105">RemoveByKeyNameParameterSet (Default)</span></span>
```
Remove-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="660f9-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="660f9-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="660f9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="660f9-107">DESCRIPTION</span></span>
<span data-ttu-id="660f9-108">Polecenie cmdlet Remove-AzManagedHsmKey usuwa klucz z zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="660f9-108">The Remove-AzManagedHsmKey cmdlet deletes a key in a managed HSM.</span></span>
<span data-ttu-id="660f9-109">Jeśli usunięto przypadkowo klucz, można go odzyskać przy użyciu Undo-AzManagedHsmKeyRemoval przez użytkownika ze specjalnymi uprawnieniami "Odzyskaj".</span><span class="sxs-lookup"><span data-stu-id="660f9-109">If the key was accidentally deleted the key can be recovered using Undo-AzManagedHsmKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="660f9-110">To polecenie cmdlet ma wartość High dla właściwości **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="660f9-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="660f9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="660f9-111">EXAMPLES</span></span>

### <span data-ttu-id="660f9-112">Przykład 1: Usuwanie klucza z zarządzanego modułu HSM</span><span class="sxs-lookup"><span data-stu-id="660f9-112">Example 1: Remove a key from a managed HSM</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -PassThru

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:35:06 AM
Scheduled Purge Date : 1/12/2021 9:35:06 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="660f9-113">To polecenie usuwa klucz o nazwie TestKey z zarządzanego modułu HSM o nazwie testmhsm.</span><span class="sxs-lookup"><span data-stu-id="660f9-113">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="660f9-114">Przykład 2: Usuwanie klucza bez potwierdzenia użytkownika</span><span class="sxs-lookup"><span data-stu-id="660f9-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -Force
```

<span data-ttu-id="660f9-115">To polecenie usuwa klucz o nazwie TestKey z zarządzanego modułu HSM o nazwie testmhsm.</span><span class="sxs-lookup"><span data-stu-id="660f9-115">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>
<span data-ttu-id="660f9-116">Polecenie określa parametr *Force* , dlatego polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="660f9-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="660f9-117">Przykład 3: trwałe przeczyszczanie usuniętego klucza z zarządzanego modułu HSM</span><span class="sxs-lookup"><span data-stu-id="660f9-117">Example 3: Purge a deleted key from the managed HSM permanently</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState
```

<span data-ttu-id="660f9-118">To polecenie usuwa klucz o nazwie TestKey z zarządzanego modułu HSM o nazwie testmhsm na stałe.</span><span class="sxs-lookup"><span data-stu-id="660f9-118">This command removes the key named testkey from the managed HSM named testmhsm permanently.</span></span>
<span data-ttu-id="660f9-119">Wykonanie tego polecenia cmdlet wymaga uprawnienia "Wyczyść", które musi być wcześniej i wyraźnie udzielone użytkownikowi w ramach zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="660f9-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this managed HSM.</span></span>

### <span data-ttu-id="660f9-120">Przykład 4: usuwanie kluczy za pomocą operatora potoku</span><span class="sxs-lookup"><span data-stu-id="660f9-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzManagedHsmKey
```

<span data-ttu-id="660f9-121">To polecenie pobiera wszystkie klucze w zarządzanym modułu HSM o nazwie testmhsm i przekazuje je do polecenia cmdlet **WHERE-Object** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="660f9-121">This command gets all the keys in the managed HSM named testmhsm and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="660f9-122">Polecenie cmdlet przekazuje klucze, których atrybut **Enabled** jest wartością $false dla bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="660f9-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="660f9-123">Te klucze są usuwane przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="660f9-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="660f9-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="660f9-124">PARAMETERS</span></span>

### <span data-ttu-id="660f9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="660f9-125">-DefaultProfile</span></span>
<span data-ttu-id="660f9-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="660f9-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="660f9-127">-Force</span><span class="sxs-lookup"><span data-stu-id="660f9-127">-Force</span></span>
<span data-ttu-id="660f9-128">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="660f9-128">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="660f9-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="660f9-129">-HsmName</span></span>
<span data-ttu-id="660f9-130">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="660f9-130">HSM name.</span></span> <span data-ttu-id="660f9-131">Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="660f9-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="660f9-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="660f9-132">-InputObject</span></span>
<span data-ttu-id="660f9-133">Obiekt Key</span><span class="sxs-lookup"><span data-stu-id="660f9-133">Key Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="660f9-134">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="660f9-134">-InRemovedState</span></span>
<span data-ttu-id="660f9-135">Trwałe usunięcie wcześniej usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="660f9-135">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="660f9-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="660f9-136">-Name</span></span>
<span data-ttu-id="660f9-137">Nazwa klucza.</span><span class="sxs-lookup"><span data-stu-id="660f9-137">Key name.</span></span>
<span data-ttu-id="660f9-138">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie nazwa zarządzanego modułu HSM, obecnie wybranego środowiska i nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="660f9-138">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="660f9-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="660f9-139">-PassThru</span></span>
<span data-ttu-id="660f9-140">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="660f9-140">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="660f9-141">Jeśli ten przełącznik jest określony, polecenie cmdlet zwraca obiekt klucza, który został usunięty.</span><span class="sxs-lookup"><span data-stu-id="660f9-141">If this switch is specified, the cmdlet returns the key object that was deleted.</span></span>

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

### <span data-ttu-id="660f9-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="660f9-142">-Confirm</span></span>
<span data-ttu-id="660f9-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="660f9-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="660f9-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="660f9-144">-WhatIf</span></span>
<span data-ttu-id="660f9-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="660f9-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="660f9-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="660f9-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="660f9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="660f9-147">CommonParameters</span></span>
<span data-ttu-id="660f9-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="660f9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="660f9-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="660f9-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="660f9-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="660f9-150">INPUTS</span></span>

### <span data-ttu-id="660f9-151">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="660f9-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="660f9-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="660f9-152">OUTPUTS</span></span>

### <span data-ttu-id="660f9-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="660f9-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="660f9-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="660f9-154">NOTES</span></span>

## <span data-ttu-id="660f9-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="660f9-155">RELATED LINKS</span></span>

[<span data-ttu-id="660f9-156">Dodaj-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="660f9-156">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="660f9-157">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="660f9-157">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="660f9-158">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="660f9-158">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="660f9-159">Cofanie — AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="660f9-159">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="660f9-160">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="660f9-160">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="660f9-161">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="660f9-161">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)