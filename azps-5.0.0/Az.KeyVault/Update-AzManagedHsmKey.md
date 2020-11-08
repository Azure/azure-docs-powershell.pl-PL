---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
ms.openlocfilehash: 79d01f96fe776432f650d827b16ba83f48b84ddd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233508"
---
# <span data-ttu-id="7b252-101">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="7b252-101">Update-AzManagedHsmKey</span></span>

## <span data-ttu-id="7b252-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b252-102">SYNOPSIS</span></span>
<span data-ttu-id="7b252-103">Aktualizuje atrybuty klucza w zarządzanym modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="7b252-103">Updates the attributes of a key in a managed HSM.</span></span>

## <span data-ttu-id="7b252-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b252-104">SYNTAX</span></span>

### <span data-ttu-id="7b252-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7b252-105">Default (Default)</span></span>
```
Update-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b252-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="7b252-106">InputObject</span></span>
```
Update-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b252-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7b252-107">DESCRIPTION</span></span>
<span data-ttu-id="7b252-108">Polecenie cmdlet **Update-AzManagedHsmKey** aktualizuje atrybuty edytowalne klucza w zarządzanym modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="7b252-108">The **Update-AzManagedHsmKey** cmdlet updates the editable attributes of a key in a managed HSM.</span></span>

## <span data-ttu-id="7b252-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b252-109">EXAMPLES</span></span>

### <span data-ttu-id="7b252-110">Przykład 1: Zmodyfikuj klawisz, aby go włączyć, a następnie ustaw datę i Tagi wygasania.</span><span class="sxs-lookup"><span data-stu-id="7b252-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzManagedHsmKey -HsmName testmhsm -Name testkey001 -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 49b74a39dab605bd336628dc094dc31b
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/49b74a39dab605bd336628dc094dc31b
Enabled        : True
Expires        : 10/14/2022 9:46:55 AM
Not Before     :
Created        : 10/14/2020 3:39:16 AM
Updated        : 10/14/2020 9:47:06 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="7b252-111">Pierwsze polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="7b252-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="7b252-112">Ten obiekt Określa godzinę w przyszłości w dwóch latach.</span><span class="sxs-lookup"><span data-stu-id="7b252-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="7b252-113">Polecenie zapisuje tę datę w zmiennej $Expires.</span><span class="sxs-lookup"><span data-stu-id="7b252-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="7b252-114">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="7b252-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="7b252-115">Drugie polecenie tworzy zmienną do przechowywania wartości znaczników o wysokiej ważności i księgowaniu.</span><span class="sxs-lookup"><span data-stu-id="7b252-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="7b252-116">Polecenie ostatnie modyfikuje klucz o nazwie testkey001.</span><span class="sxs-lookup"><span data-stu-id="7b252-116">The final command modifies a key named testkey001.</span></span> <span data-ttu-id="7b252-117">Polecenie włącza klucz, ustawia czas wygaśnięcia w czasie przechowywanym w $Expires i ustawia Tagi przechowywane w $Tags.</span><span class="sxs-lookup"><span data-stu-id="7b252-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

## <span data-ttu-id="7b252-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b252-118">PARAMETERS</span></span>

### <span data-ttu-id="7b252-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b252-119">-DefaultProfile</span></span>
<span data-ttu-id="7b252-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7b252-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b252-121">-Enable</span><span class="sxs-lookup"><span data-stu-id="7b252-121">-Enable</span></span>
<span data-ttu-id="7b252-122">Wartość True włącza klucz i wartość false Wyłącz klucz.</span><span class="sxs-lookup"><span data-stu-id="7b252-122">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="7b252-123">Jeśli nie określono tego parametru, istniejący stan włączony/wyłączony pozostaje bez zmian.</span><span class="sxs-lookup"><span data-stu-id="7b252-123">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b252-124">-Wygasa</span><span class="sxs-lookup"><span data-stu-id="7b252-124">-Expires</span></span>
<span data-ttu-id="7b252-125">Czas wygaśnięcia klucza w czasie UTC.</span><span class="sxs-lookup"><span data-stu-id="7b252-125">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="7b252-126">Jeśli nie podano tego parametru, dotychczasowy czas wygaśnięcia klucza pozostaje bez zmian.</span><span class="sxs-lookup"><span data-stu-id="7b252-126">If not specified, the existing expiration time of the key remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b252-127">-HsmName</span><span class="sxs-lookup"><span data-stu-id="7b252-127">-HsmName</span></span>
<span data-ttu-id="7b252-128">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="7b252-128">HSM name.</span></span> <span data-ttu-id="7b252-129">Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="7b252-129">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b252-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7b252-130">-InputObject</span></span>
<span data-ttu-id="7b252-131">Obiekt Key</span><span class="sxs-lookup"><span data-stu-id="7b252-131">Key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b252-132">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="7b252-132">-KeyOps</span></span>
<span data-ttu-id="7b252-133">Operacje, które można wykonać przy użyciu klucza.</span><span class="sxs-lookup"><span data-stu-id="7b252-133">The operations that can be performed with the key.</span></span>
<span data-ttu-id="7b252-134">Jeśli nie określono, istniejące kluczowe operacje klucza pozostaną niezmienione.</span><span class="sxs-lookup"><span data-stu-id="7b252-134">If not specified, the existing key operations of the key remain unchanged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b252-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7b252-135">-Name</span></span>
<span data-ttu-id="7b252-136">Nazwa klucza.</span><span class="sxs-lookup"><span data-stu-id="7b252-136">Key name.</span></span>
<span data-ttu-id="7b252-137">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie nazwa zarządzanego modułu HSM, obecnie wybranego środowiska i nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="7b252-137">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b252-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="7b252-138">-NotBefore</span></span>
<span data-ttu-id="7b252-139">Czas UTC, po upływie którego nie można użyć klucza.</span><span class="sxs-lookup"><span data-stu-id="7b252-139">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="7b252-140">Jeśli nie podano tego parametru, istniejący atrybut NotBefore klucza pozostaje niezmieniony.</span><span class="sxs-lookup"><span data-stu-id="7b252-140">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b252-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b252-141">-PassThru</span></span>
<span data-ttu-id="7b252-142">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="7b252-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7b252-143">Jeśli ten przełącznik jest określony, zwraca zaktualizowany obiekt pakietu kluczy.</span><span class="sxs-lookup"><span data-stu-id="7b252-143">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="7b252-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="7b252-144">-Tag</span></span>
<span data-ttu-id="7b252-145">Obiekt Hashtable reprezentuje Tagi kluczowe.</span><span class="sxs-lookup"><span data-stu-id="7b252-145">A hashtable represents key tags.</span></span>
<span data-ttu-id="7b252-146">Jeśli nie określono, znaczniki istniejące w kluczu pozostają niezmienione.</span><span class="sxs-lookup"><span data-stu-id="7b252-146">If not specified, the existings tags of the key remain unchanged.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b252-147">-Version</span><span class="sxs-lookup"><span data-stu-id="7b252-147">-Version</span></span>
<span data-ttu-id="7b252-148">Wersja klucza.</span><span class="sxs-lookup"><span data-stu-id="7b252-148">Key version.</span></span>
<span data-ttu-id="7b252-149">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie zarządzanej nazwy modułu HSM, obecnie wybranego środowiska, nazwy klucza i wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="7b252-149">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b252-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7b252-150">-Confirm</span></span>
<span data-ttu-id="7b252-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b252-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b252-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b252-152">-WhatIf</span></span>
<span data-ttu-id="7b252-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b252-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b252-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7b252-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b252-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b252-155">CommonParameters</span></span>
<span data-ttu-id="7b252-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b252-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b252-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b252-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b252-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b252-158">INPUTS</span></span>

### <span data-ttu-id="7b252-159">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7b252-159">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="7b252-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b252-160">OUTPUTS</span></span>

### <span data-ttu-id="7b252-161">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7b252-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="7b252-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b252-162">NOTES</span></span>

## <span data-ttu-id="7b252-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b252-163">RELATED LINKS</span></span>

[<span data-ttu-id="7b252-164">Dodaj-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="7b252-164">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="7b252-165">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="7b252-165">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="7b252-166">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="7b252-166">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="7b252-167">Cofanie — AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="7b252-167">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="7b252-168">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="7b252-168">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="7b252-169">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="7b252-169">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)