---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
ms.openlocfilehash: cae763eedd98a98c7e09855a295791ddc96d5339
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220666"
---
# <span data-ttu-id="81e0a-101">Update-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="81e0a-101">Update-AzKeyVaultKey</span></span>

## <span data-ttu-id="81e0a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81e0a-102">SYNOPSIS</span></span>
<span data-ttu-id="81e0a-103">Aktualizuje atrybuty klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="81e0a-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="81e0a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81e0a-104">SYNTAX</span></span>

### <span data-ttu-id="81e0a-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="81e0a-105">Default (Default)</span></span>
```
Update-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81e0a-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="81e0a-106">InputObject</span></span>
```
Update-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81e0a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="81e0a-107">DESCRIPTION</span></span>
<span data-ttu-id="81e0a-108">Polecenie cmdlet **Update-AzKeyVaultKey** aktualizuje atrybuty edytowalne klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="81e0a-108">The **Update-AzKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="81e0a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81e0a-109">EXAMPLES</span></span>

### <span data-ttu-id="81e0a-110">Przykład 1: Zmodyfikuj klawisz, aby go włączyć, a następnie ustaw datę i Tagi wygasania.</span><span class="sxs-lookup"><span data-stu-id="81e0a-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
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

<span data-ttu-id="81e0a-111">Pierwsze polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="81e0a-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="81e0a-112">Ten obiekt Określa godzinę w przyszłości w dwóch latach.</span><span class="sxs-lookup"><span data-stu-id="81e0a-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="81e0a-113">Polecenie zapisuje tę datę w zmiennej $Expires.</span><span class="sxs-lookup"><span data-stu-id="81e0a-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="81e0a-114">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="81e0a-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="81e0a-115">Drugie polecenie tworzy zmienną do przechowywania wartości znaczników o wysokiej ważności i księgowaniu.</span><span class="sxs-lookup"><span data-stu-id="81e0a-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="81e0a-116">Polecenie ostatnie modyfikuje klucz o nazwie ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="81e0a-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="81e0a-117">Polecenie włącza klucz, ustawia czas wygaśnięcia w czasie przechowywanym w $Expires i ustawia Tagi przechowywane w $Tags.</span><span class="sxs-lookup"><span data-stu-id="81e0a-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="81e0a-118">Przykład 2: modyfikowanie klucza w celu usunięcia wszystkich znaczników</span><span class="sxs-lookup"><span data-stu-id="81e0a-118">Example 2: Modify a key to delete all tags</span></span>
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

<span data-ttu-id="81e0a-119">To polecenie usuwa wszystkie znaczniki dla określonej wersji klucza o nazwie ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="81e0a-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="81e0a-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81e0a-120">PARAMETERS</span></span>

### <span data-ttu-id="81e0a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81e0a-121">-DefaultProfile</span></span>
<span data-ttu-id="81e0a-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81e0a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81e0a-123">-Enable</span><span class="sxs-lookup"><span data-stu-id="81e0a-123">-Enable</span></span>
<span data-ttu-id="81e0a-124">Wartość True włącza klucz i wartość false Wyłącz klucz.</span><span class="sxs-lookup"><span data-stu-id="81e0a-124">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="81e0a-125">Jeśli nie określono tego parametru, istniejący stan włączony/wyłączony pozostaje bez zmian.</span><span class="sxs-lookup"><span data-stu-id="81e0a-125">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="81e0a-126">-Wygasa</span><span class="sxs-lookup"><span data-stu-id="81e0a-126">-Expires</span></span>
<span data-ttu-id="81e0a-127">Czas wygaśnięcia klucza w czasie UTC.</span><span class="sxs-lookup"><span data-stu-id="81e0a-127">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="81e0a-128">Jeśli nie podano tego parametru, dotychczasowy czas wygaśnięcia klucza pozostaje bez zmian.</span><span class="sxs-lookup"><span data-stu-id="81e0a-128">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="81e0a-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="81e0a-129">-InputObject</span></span>
<span data-ttu-id="81e0a-130">Obiekt Key</span><span class="sxs-lookup"><span data-stu-id="81e0a-130">Key object</span></span>

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

### <span data-ttu-id="81e0a-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="81e0a-131">-KeyOps</span></span>
<span data-ttu-id="81e0a-132">Operacje, które można wykonać przy użyciu klucza.</span><span class="sxs-lookup"><span data-stu-id="81e0a-132">The operations that can be performed with the key.</span></span>
<span data-ttu-id="81e0a-133">Jeśli nie określono, istniejące kluczowe operacje klucza pozostaną niezmienione.</span><span class="sxs-lookup"><span data-stu-id="81e0a-133">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="81e0a-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="81e0a-134">-Name</span></span>
<span data-ttu-id="81e0a-135">Nazwa klucza.</span><span class="sxs-lookup"><span data-stu-id="81e0a-135">Key name.</span></span>
<span data-ttu-id="81e0a-136">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie nazwy magazynu, obecnie wybranego środowiska i nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="81e0a-136">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="81e0a-137">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="81e0a-137">-NotBefore</span></span>
<span data-ttu-id="81e0a-138">Czas UTC, po upływie którego nie można użyć klucza.</span><span class="sxs-lookup"><span data-stu-id="81e0a-138">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="81e0a-139">Jeśli nie podano tego parametru, istniejący atrybut NotBefore klucza pozostaje niezmieniony.</span><span class="sxs-lookup"><span data-stu-id="81e0a-139">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="81e0a-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81e0a-140">-PassThru</span></span>
<span data-ttu-id="81e0a-141">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="81e0a-141">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="81e0a-142">Jeśli ten przełącznik jest określony, zwraca zaktualizowany obiekt pakietu kluczy.</span><span class="sxs-lookup"><span data-stu-id="81e0a-142">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="81e0a-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="81e0a-143">-Tag</span></span>
<span data-ttu-id="81e0a-144">Obiekt Hashtable reprezentuje Tagi kluczowe.</span><span class="sxs-lookup"><span data-stu-id="81e0a-144">A hashtable represents key tags.</span></span>
<span data-ttu-id="81e0a-145">Jeśli nie określono, znaczniki istniejące w kluczu pozostają niezmienione.</span><span class="sxs-lookup"><span data-stu-id="81e0a-145">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="81e0a-146">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="81e0a-146">-VaultName</span></span>
<span data-ttu-id="81e0a-147">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="81e0a-147">Vault name.</span></span>
<span data-ttu-id="81e0a-148">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="81e0a-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="81e0a-149">-Version</span><span class="sxs-lookup"><span data-stu-id="81e0a-149">-Version</span></span>
<span data-ttu-id="81e0a-150">Wersja klucza.</span><span class="sxs-lookup"><span data-stu-id="81e0a-150">Key version.</span></span>
<span data-ttu-id="81e0a-151">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie nazwy magazynu, obecnie wybranego środowiska, nazwy klucza i wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="81e0a-151">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="81e0a-152">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81e0a-152">-Confirm</span></span>
<span data-ttu-id="81e0a-153">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81e0a-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81e0a-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81e0a-154">-WhatIf</span></span>
<span data-ttu-id="81e0a-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81e0a-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81e0a-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="81e0a-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81e0a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81e0a-157">CommonParameters</span></span>
<span data-ttu-id="81e0a-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81e0a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81e0a-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81e0a-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81e0a-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81e0a-160">INPUTS</span></span>

### <span data-ttu-id="81e0a-161">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="81e0a-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="81e0a-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81e0a-162">OUTPUTS</span></span>

### <span data-ttu-id="81e0a-163">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="81e0a-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="81e0a-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81e0a-164">NOTES</span></span>

## <span data-ttu-id="81e0a-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81e0a-165">RELATED LINKS</span></span>
