---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultKey.md
ms.openlocfilehash: e9e2401ab96da63c3fe6b5978916b96f98db9f54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545180"
---
# <span data-ttu-id="63ffa-101">Update-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="63ffa-101">Update-AzureKeyVaultKey</span></span>

## <span data-ttu-id="63ffa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63ffa-102">SYNOPSIS</span></span>
<span data-ttu-id="63ffa-103">Aktualizuje atrybuty klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="63ffa-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63ffa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63ffa-104">SYNTAX</span></span>

### <span data-ttu-id="63ffa-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="63ffa-105">Default (Default)</span></span>
```
Update-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63ffa-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="63ffa-106">InputObject</span></span>
```
Update-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63ffa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="63ffa-107">DESCRIPTION</span></span>
<span data-ttu-id="63ffa-108">Polecenie cmdlet **Update-AzureKeyVaultKey** aktualizuje atrybuty edytowalne klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="63ffa-108">The **Update-AzureKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="63ffa-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63ffa-109">EXAMPLES</span></span>

### <span data-ttu-id="63ffa-110">Przykład 1: Zmodyfikuj klawisz, aby go włączyć, a następnie ustaw datę i Tagi wygasania.</span><span class="sxs-lookup"><span data-stu-id="63ffa-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru

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

<span data-ttu-id="63ffa-111">Pierwsze polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="63ffa-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="63ffa-112">Ten obiekt Określa godzinę w przyszłości w dwóch latach.</span><span class="sxs-lookup"><span data-stu-id="63ffa-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="63ffa-113">Polecenie zapisuje tę datę w zmiennej $Expires.</span><span class="sxs-lookup"><span data-stu-id="63ffa-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="63ffa-114">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="63ffa-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="63ffa-115">Drugie polecenie tworzy zmienną do przechowywania wartości znaczników o wysokiej ważności i księgowaniu.</span><span class="sxs-lookup"><span data-stu-id="63ffa-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="63ffa-116">Polecenie ostatnie modyfikuje klucz o nazwie ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="63ffa-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="63ffa-117">Polecenie włącza klucz, ustawia czas wygaśnięcia w czasie przechowywanym w $Expires i ustawia Tagi przechowywane w $Tags.</span><span class="sxs-lookup"><span data-stu-id="63ffa-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="63ffa-118">Przykład 2: modyfikowanie klucza w celu usunięcia wszystkich znaczników</span><span class="sxs-lookup"><span data-stu-id="63ffa-118">Example 2: Modify a key to delete all tags</span></span>
```powershell
PS C:\> Update-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Version '394f9379a47a4e2086585468de6c7ae5' -Tag @{}

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

<span data-ttu-id="63ffa-119">To polecenie usuwa wszystkie znaczniki dla określonej wersji klucza o nazwie ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="63ffa-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="63ffa-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63ffa-120">PARAMETERS</span></span>

### <span data-ttu-id="63ffa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63ffa-121">-DefaultProfile</span></span>
<span data-ttu-id="63ffa-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63ffa-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63ffa-123">-Enable</span><span class="sxs-lookup"><span data-stu-id="63ffa-123">-Enable</span></span>
<span data-ttu-id="63ffa-124">Wartość True włącza klucz i wartość false Wyłącz klucz.</span><span class="sxs-lookup"><span data-stu-id="63ffa-124">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="63ffa-125">Jeśli nie określono tego parametru, istniejący stan włączony/wyłączony pozostaje bez zmian.</span><span class="sxs-lookup"><span data-stu-id="63ffa-125">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="63ffa-126">-Wygasa</span><span class="sxs-lookup"><span data-stu-id="63ffa-126">-Expires</span></span>
<span data-ttu-id="63ffa-127">Czas wygaśnięcia klucza w czasie UTC.</span><span class="sxs-lookup"><span data-stu-id="63ffa-127">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="63ffa-128">Jeśli nie podano tego parametru, dotychczasowy czas wygaśnięcia klucza pozostaje bez zmian.</span><span class="sxs-lookup"><span data-stu-id="63ffa-128">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="63ffa-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="63ffa-129">-InputObject</span></span>
<span data-ttu-id="63ffa-130">Obiekt Key</span><span class="sxs-lookup"><span data-stu-id="63ffa-130">Key object</span></span>

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

### <span data-ttu-id="63ffa-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="63ffa-131">-KeyOps</span></span>
<span data-ttu-id="63ffa-132">Operacje, które można wykonać przy użyciu klucza.</span><span class="sxs-lookup"><span data-stu-id="63ffa-132">The operations that can be performed with the key.</span></span>
<span data-ttu-id="63ffa-133">Jeśli nie określono, istniejące kluczowe operacje klucza pozostaną niezmienione.</span><span class="sxs-lookup"><span data-stu-id="63ffa-133">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="63ffa-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="63ffa-134">-Name</span></span>
<span data-ttu-id="63ffa-135">Nazwa klucza.</span><span class="sxs-lookup"><span data-stu-id="63ffa-135">Key name.</span></span>
<span data-ttu-id="63ffa-136">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie nazwy magazynu, obecnie wybranego środowiska i nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="63ffa-136">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="63ffa-137">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="63ffa-137">-NotBefore</span></span>
<span data-ttu-id="63ffa-138">Czas UTC, po upływie którego nie można użyć klucza.</span><span class="sxs-lookup"><span data-stu-id="63ffa-138">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="63ffa-139">Jeśli nie podano tego parametru, istniejący atrybut NotBefore klucza pozostaje niezmieniony.</span><span class="sxs-lookup"><span data-stu-id="63ffa-139">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="63ffa-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63ffa-140">-PassThru</span></span>
<span data-ttu-id="63ffa-141">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="63ffa-141">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="63ffa-142">Jeśli ten przełącznik jest określony, zwraca zaktualizowany obiekt pakietu kluczy.</span><span class="sxs-lookup"><span data-stu-id="63ffa-142">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="63ffa-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="63ffa-143">-Tag</span></span>
<span data-ttu-id="63ffa-144">Obiekt Hashtable reprezentuje Tagi kluczowe.</span><span class="sxs-lookup"><span data-stu-id="63ffa-144">A hashtable represents key tags.</span></span>
<span data-ttu-id="63ffa-145">Jeśli nie określono, znaczniki istniejące w kluczu pozostają niezmienione.</span><span class="sxs-lookup"><span data-stu-id="63ffa-145">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="63ffa-146">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="63ffa-146">-VaultName</span></span>
<span data-ttu-id="63ffa-147">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="63ffa-147">Vault name.</span></span>
<span data-ttu-id="63ffa-148">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="63ffa-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="63ffa-149">-Version</span><span class="sxs-lookup"><span data-stu-id="63ffa-149">-Version</span></span>
<span data-ttu-id="63ffa-150">Wersja klucza.</span><span class="sxs-lookup"><span data-stu-id="63ffa-150">Key version.</span></span>
<span data-ttu-id="63ffa-151">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie nazwy magazynu, obecnie wybranego środowiska, nazwy klucza i wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="63ffa-151">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="63ffa-152">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="63ffa-152">-Confirm</span></span>
<span data-ttu-id="63ffa-153">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63ffa-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63ffa-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63ffa-154">-WhatIf</span></span>
<span data-ttu-id="63ffa-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63ffa-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63ffa-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="63ffa-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63ffa-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63ffa-157">CommonParameters</span></span>
<span data-ttu-id="63ffa-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63ffa-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63ffa-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63ffa-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63ffa-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63ffa-160">INPUTS</span></span>

### <span data-ttu-id="63ffa-161">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="63ffa-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>
<span data-ttu-id="63ffa-162">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="63ffa-162">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="63ffa-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63ffa-163">OUTPUTS</span></span>

### <span data-ttu-id="63ffa-164">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="63ffa-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="63ffa-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63ffa-165">NOTES</span></span>

## <span data-ttu-id="63ffa-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63ffa-166">RELATED LINKS</span></span>
