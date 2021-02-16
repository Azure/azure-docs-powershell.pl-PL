---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
ms.openlocfilehash: de8e542079cdeebdb6513c8e0febf8cfe0952889
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185402"
---
# <span data-ttu-id="f029d-101">Update-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f029d-101">Update-AzKeyVaultKey</span></span>

## <span data-ttu-id="f029d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f029d-102">SYNOPSIS</span></span>
<span data-ttu-id="f029d-103">Aktualizuje atrybuty klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="f029d-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="f029d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f029d-104">SYNTAX</span></span>

### <span data-ttu-id="f029d-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f029d-105">Default (Default)</span></span>
```
Update-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f029d-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="f029d-106">HsmInteractive</span></span>
```
Update-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f029d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f029d-107">InputObject</span></span>
```
Update-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f029d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f029d-108">DESCRIPTION</span></span>
<span data-ttu-id="f029d-109">Polecenie **cmdlet Update-AzKeyVaultKey** aktualizuje edytowalne atrybuty klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="f029d-109">The **Update-AzKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="f029d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f029d-110">EXAMPLES</span></span>

### <span data-ttu-id="f029d-111">Przykład 1. Modyfikowanie klucza w celu jego włączenia oraz ustawianie daty wygaśnięcia i tagów</span><span class="sxs-lookup"><span data-stu-id="f029d-111">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 7:59:02 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="f029d-112">Pierwsze polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="f029d-112">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="f029d-113">Ten obiekt określa czas za dwa lata.</span><span class="sxs-lookup"><span data-stu-id="f029d-113">That object specifies a time two years in the future.</span></span> <span data-ttu-id="f029d-114">Polecenie przechowuje datę w $Expires zmienną.</span><span class="sxs-lookup"><span data-stu-id="f029d-114">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="f029d-115">Aby uzyskać więcej informacji, wpisz `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="f029d-115">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="f029d-116">Drugie polecenie tworzy zmienną do przechowywania wartości tagów o wysokim poziomie ważności i księgowości.</span><span class="sxs-lookup"><span data-stu-id="f029d-116">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="f029d-117">Ostatnie polecenie modyfikuje klucz o nazwie ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="f029d-117">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="f029d-118">To polecenie włącza klawisz, ustawia czas wygaśnięcia na czas przechowywany w $Expires i ustawia tagi, które są przechowywane w $Tags.</span><span class="sxs-lookup"><span data-stu-id="f029d-118">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="f029d-119">Przykład 2. Modyfikowanie klawisza w celu usunięcia wszystkich tagów</span><span class="sxs-lookup"><span data-stu-id="f029d-119">Example 2: Modify a key to delete all tags</span></span>
```powershell
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Version '394f9379a47a4e2086585468de6c7ae5' -Tag @{}

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 8:00:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="f029d-120">To polecenia usuwają wszystkie tagi dla określonej wersji klucza o nazwie ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="f029d-120">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="f029d-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f029d-121">PARAMETERS</span></span>

### <span data-ttu-id="f029d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f029d-122">-DefaultProfile</span></span>
<span data-ttu-id="f029d-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f029d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f029d-124">— Włącz</span><span class="sxs-lookup"><span data-stu-id="f029d-124">-Enable</span></span>
<span data-ttu-id="f029d-125">Wartość prawda włącza klucz, a wartość fałsz wyłącza ten klucz.</span><span class="sxs-lookup"><span data-stu-id="f029d-125">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="f029d-126">Jeśli nie zostanie określone, istniejący stan włączony/wyłączony pozostanie bez zmian.</span><span class="sxs-lookup"><span data-stu-id="f029d-126">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="f029d-127">— Wygasa</span><span class="sxs-lookup"><span data-stu-id="f029d-127">-Expires</span></span>
<span data-ttu-id="f029d-128">Czas wygaśnięcia klucza w czasie UTC.</span><span class="sxs-lookup"><span data-stu-id="f029d-128">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="f029d-129">Jeśli nie zostanie określona, istniejący czas wygaśnięcia klucza pozostanie bez zmian.</span><span class="sxs-lookup"><span data-stu-id="f029d-129">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="f029d-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="f029d-130">-HsmName</span></span>
<span data-ttu-id="f029d-131">Nazwa HSM.</span><span class="sxs-lookup"><span data-stu-id="f029d-131">HSM name.</span></span> <span data-ttu-id="f029d-132">Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="f029d-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractive
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f029d-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f029d-133">-InputObject</span></span>
<span data-ttu-id="f029d-134">Obiekt Key</span><span class="sxs-lookup"><span data-stu-id="f029d-134">Key object</span></span>

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

### <span data-ttu-id="f029d-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="f029d-135">-KeyOps</span></span>
<span data-ttu-id="f029d-136">Operacje, które można wykonać za pomocą klucza.</span><span class="sxs-lookup"><span data-stu-id="f029d-136">The operations that can be performed with the key.</span></span>
<span data-ttu-id="f029d-137">Jeśli nie zostanie określona, istniejące operacje klucza pozostaną niezmienione.</span><span class="sxs-lookup"><span data-stu-id="f029d-137">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="f029d-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f029d-138">-Name</span></span>
<span data-ttu-id="f029d-139">Nazwa klucza.</span><span class="sxs-lookup"><span data-stu-id="f029d-139">Key name.</span></span>
<span data-ttu-id="f029d-140">Polecenie cmdlet konstruuje nazwę FQDN klucza z nazwy magazynu, obecnie wybranego środowiska i nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="f029d-140">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HsmInteractive
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f029d-141">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="f029d-141">-NotBefore</span></span>
<span data-ttu-id="f029d-142">Czas UTC, przed którym nie można użyć klucza.</span><span class="sxs-lookup"><span data-stu-id="f029d-142">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="f029d-143">Jeśli nie zostanie określona, istniejący atrybut NotBefore klucza pozostanie niezmieniony.</span><span class="sxs-lookup"><span data-stu-id="f029d-143">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="f029d-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f029d-144">-PassThru</span></span>
<span data-ttu-id="f029d-145">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="f029d-145">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f029d-146">Jeśli ten przełącznik jest określony, zwraca zaktualizowany obiekt pakietu klucza.</span><span class="sxs-lookup"><span data-stu-id="f029d-146">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="f029d-147">— Tag</span><span class="sxs-lookup"><span data-stu-id="f029d-147">-Tag</span></span>
<span data-ttu-id="f029d-148">Skróty reprezentują tagi klucza.</span><span class="sxs-lookup"><span data-stu-id="f029d-148">A hashtable represents key tags.</span></span>
<span data-ttu-id="f029d-149">Jeśli nie zostanie określona, istniejące tagi klucza pozostaną niezmienione.</span><span class="sxs-lookup"><span data-stu-id="f029d-149">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="f029d-150">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f029d-150">-VaultName</span></span>
<span data-ttu-id="f029d-151">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="f029d-151">Vault name.</span></span>
<span data-ttu-id="f029d-152">Polecenie cmdlet konstruuje nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="f029d-152">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f029d-153">— Wersja</span><span class="sxs-lookup"><span data-stu-id="f029d-153">-Version</span></span>
<span data-ttu-id="f029d-154">Wersja klucza.</span><span class="sxs-lookup"><span data-stu-id="f029d-154">Key version.</span></span>
<span data-ttu-id="f029d-155">Polecenie cmdlet konstruuje nazwę FQDN klucza z nazwy magazynu, obecnie wybranego środowiska, nazwy klucza i wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="f029d-155">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="f029d-156">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f029d-156">-Confirm</span></span>
<span data-ttu-id="f029d-157">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f029d-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f029d-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f029d-158">-WhatIf</span></span>
<span data-ttu-id="f029d-159">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f029d-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f029d-160">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f029d-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f029d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f029d-161">CommonParameters</span></span>
<span data-ttu-id="f029d-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f029d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f029d-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f029d-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f029d-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f029d-164">INPUTS</span></span>

### <span data-ttu-id="f029d-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f029d-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="f029d-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f029d-166">OUTPUTS</span></span>

### <span data-ttu-id="f029d-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f029d-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="f029d-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f029d-168">NOTES</span></span>

## <span data-ttu-id="f029d-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f029d-169">RELATED LINKS</span></span>
