---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
ms.openlocfilehash: de8e542079cdeebdb6513c8e0febf8cfe0952889
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500889"
---
# <span data-ttu-id="5f601-101">Update-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5f601-101">Update-AzKeyVaultKey</span></span>

## <span data-ttu-id="5f601-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f601-102">SYNOPSIS</span></span>
<span data-ttu-id="5f601-103">Aktualizuje atrybuty klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="5f601-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="5f601-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f601-104">SYNTAX</span></span>

### <span data-ttu-id="5f601-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="5f601-105">Default (Default)</span></span>
```
Update-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f601-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="5f601-106">HsmInteractive</span></span>
```
Update-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f601-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="5f601-107">InputObject</span></span>
```
Update-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f601-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5f601-108">DESCRIPTION</span></span>
<span data-ttu-id="5f601-109">Polecenie cmdlet **Update-AzKeyVaultKey** aktualizuje atrybuty edytowalne klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="5f601-109">The **Update-AzKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="5f601-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f601-110">EXAMPLES</span></span>

### <span data-ttu-id="5f601-111">Przykład 1: Zmodyfikuj klawisz, aby go włączyć, a następnie ustaw datę i Tagi wygasania.</span><span class="sxs-lookup"><span data-stu-id="5f601-111">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
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

<span data-ttu-id="5f601-112">Pierwsze polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="5f601-112">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="5f601-113">Ten obiekt Określa godzinę w przyszłości w dwóch latach.</span><span class="sxs-lookup"><span data-stu-id="5f601-113">That object specifies a time two years in the future.</span></span> <span data-ttu-id="5f601-114">Polecenie zapisuje tę datę w zmiennej $Expires.</span><span class="sxs-lookup"><span data-stu-id="5f601-114">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="5f601-115">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="5f601-115">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="5f601-116">Drugie polecenie tworzy zmienną do przechowywania wartości znaczników o wysokiej ważności i księgowaniu.</span><span class="sxs-lookup"><span data-stu-id="5f601-116">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="5f601-117">Polecenie ostatnie modyfikuje klucz o nazwie ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="5f601-117">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="5f601-118">Polecenie włącza klucz, ustawia czas wygaśnięcia w czasie przechowywanym w $Expires i ustawia Tagi przechowywane w $Tags.</span><span class="sxs-lookup"><span data-stu-id="5f601-118">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="5f601-119">Przykład 2: modyfikowanie klucza w celu usunięcia wszystkich znaczników</span><span class="sxs-lookup"><span data-stu-id="5f601-119">Example 2: Modify a key to delete all tags</span></span>
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

<span data-ttu-id="5f601-120">To polecenie usuwa wszystkie znaczniki dla określonej wersji klucza o nazwie ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="5f601-120">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="5f601-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f601-121">PARAMETERS</span></span>

### <span data-ttu-id="5f601-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f601-122">-DefaultProfile</span></span>
<span data-ttu-id="5f601-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f601-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f601-124">-Enable</span><span class="sxs-lookup"><span data-stu-id="5f601-124">-Enable</span></span>
<span data-ttu-id="5f601-125">Wartość True włącza klucz i wartość false Wyłącz klucz.</span><span class="sxs-lookup"><span data-stu-id="5f601-125">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="5f601-126">Jeśli nie określono tego parametru, istniejący stan włączony/wyłączony pozostaje bez zmian.</span><span class="sxs-lookup"><span data-stu-id="5f601-126">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="5f601-127">-Wygasa</span><span class="sxs-lookup"><span data-stu-id="5f601-127">-Expires</span></span>
<span data-ttu-id="5f601-128">Czas wygaśnięcia klucza w czasie UTC.</span><span class="sxs-lookup"><span data-stu-id="5f601-128">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="5f601-129">Jeśli nie podano tego parametru, dotychczasowy czas wygaśnięcia klucza pozostaje bez zmian.</span><span class="sxs-lookup"><span data-stu-id="5f601-129">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="5f601-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="5f601-130">-HsmName</span></span>
<span data-ttu-id="5f601-131">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="5f601-131">HSM name.</span></span> <span data-ttu-id="5f601-132">Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="5f601-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="5f601-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5f601-133">-InputObject</span></span>
<span data-ttu-id="5f601-134">Obiekt Key</span><span class="sxs-lookup"><span data-stu-id="5f601-134">Key object</span></span>

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

### <span data-ttu-id="5f601-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="5f601-135">-KeyOps</span></span>
<span data-ttu-id="5f601-136">Operacje, które można wykonać przy użyciu klucza.</span><span class="sxs-lookup"><span data-stu-id="5f601-136">The operations that can be performed with the key.</span></span>
<span data-ttu-id="5f601-137">Jeśli nie określono, istniejące kluczowe operacje klucza pozostaną niezmienione.</span><span class="sxs-lookup"><span data-stu-id="5f601-137">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="5f601-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5f601-138">-Name</span></span>
<span data-ttu-id="5f601-139">Nazwa klucza.</span><span class="sxs-lookup"><span data-stu-id="5f601-139">Key name.</span></span>
<span data-ttu-id="5f601-140">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie nazwy magazynu, obecnie wybranego środowiska i nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="5f601-140">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="5f601-141">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="5f601-141">-NotBefore</span></span>
<span data-ttu-id="5f601-142">Czas UTC, po upływie którego nie można użyć klucza.</span><span class="sxs-lookup"><span data-stu-id="5f601-142">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="5f601-143">Jeśli nie podano tego parametru, istniejący atrybut NotBefore klucza pozostaje niezmieniony.</span><span class="sxs-lookup"><span data-stu-id="5f601-143">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="5f601-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f601-144">-PassThru</span></span>
<span data-ttu-id="5f601-145">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="5f601-145">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="5f601-146">Jeśli ten przełącznik jest określony, zwraca zaktualizowany obiekt pakietu kluczy.</span><span class="sxs-lookup"><span data-stu-id="5f601-146">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="5f601-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="5f601-147">-Tag</span></span>
<span data-ttu-id="5f601-148">Obiekt Hashtable reprezentuje Tagi kluczowe.</span><span class="sxs-lookup"><span data-stu-id="5f601-148">A hashtable represents key tags.</span></span>
<span data-ttu-id="5f601-149">Jeśli nie określono, znaczniki istniejące w kluczu pozostają niezmienione.</span><span class="sxs-lookup"><span data-stu-id="5f601-149">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="5f601-150">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="5f601-150">-VaultName</span></span>
<span data-ttu-id="5f601-151">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="5f601-151">Vault name.</span></span>
<span data-ttu-id="5f601-152">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="5f601-152">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="5f601-153">-Version</span><span class="sxs-lookup"><span data-stu-id="5f601-153">-Version</span></span>
<span data-ttu-id="5f601-154">Wersja klucza.</span><span class="sxs-lookup"><span data-stu-id="5f601-154">Key version.</span></span>
<span data-ttu-id="5f601-155">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie nazwy magazynu, obecnie wybranego środowiska, nazwy klucza i wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="5f601-155">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="5f601-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5f601-156">-Confirm</span></span>
<span data-ttu-id="5f601-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f601-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f601-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f601-158">-WhatIf</span></span>
<span data-ttu-id="5f601-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f601-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f601-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5f601-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f601-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f601-161">CommonParameters</span></span>
<span data-ttu-id="5f601-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f601-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f601-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f601-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f601-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f601-164">INPUTS</span></span>

### <span data-ttu-id="5f601-165">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="5f601-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="5f601-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f601-166">OUTPUTS</span></span>

### <span data-ttu-id="5f601-167">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5f601-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="5f601-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f601-168">NOTES</span></span>

## <span data-ttu-id="5f601-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f601-169">RELATED LINKS</span></span>
