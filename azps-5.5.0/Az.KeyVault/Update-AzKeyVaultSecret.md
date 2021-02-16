---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 5efc920d4dd6e8e83c0a2ee5f61768ac7373f864
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185363"
---
# <span data-ttu-id="f4cca-101">Update-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f4cca-101">Update-AzKeyVaultSecret</span></span>

## <span data-ttu-id="f4cca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4cca-102">SYNOPSIS</span></span>
<span data-ttu-id="f4cca-103">Aktualizuje atrybuty klucza tajnego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="f4cca-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="f4cca-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f4cca-104">SYNTAX</span></span>

### <span data-ttu-id="f4cca-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f4cca-105">Default (Default)</span></span>
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4cca-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f4cca-106">InputObject</span></span>
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4cca-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f4cca-107">DESCRIPTION</span></span>
<span data-ttu-id="f4cca-108">Polecenie **cmdlet Update-AzKeyVaultSecret** aktualizuje edytowalne atrybuty klucza tajnego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="f4cca-108">The **Update-AzKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="f4cca-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f4cca-109">EXAMPLES</span></span>

### <span data-ttu-id="f4cca-110">Przykład 1. Modyfikowanie atrybutów tajnych</span><span class="sxs-lookup"><span data-stu-id="f4cca-110">Example 1: Modify the attributes of a secret</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

<span data-ttu-id="f4cca-111">Pierwsze cztery polecenia definiują atrybuty daty wygaśnięcia, daty, tagów i typu kontekstowego NotBefore oraz przechowują atrybuty w zmiennych.</span><span class="sxs-lookup"><span data-stu-id="f4cca-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="f4cca-112">Ostatnie polecenie modyfikuje atrybuty klucza tajnego o nazwie HR w magazynie kluczy o nazwie ContosoVault przy użyciu zmiennych przechowywanych.</span><span class="sxs-lookup"><span data-stu-id="f4cca-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="f4cca-113">Przykład 2. Usuwanie tagów i typu zawartości dla tajnych</span><span class="sxs-lookup"><span data-stu-id="f4cca-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="f4cca-114">To polecenie usuwa tagi i typ zawartości dla określonej wersji klucza tajnego o nazwie KADR w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="f4cca-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="f4cca-115">Przykład 3. Wyłączenie bieżącej wersji tajemnic, których nazwa zaczyna się od it</span><span class="sxs-lookup"><span data-stu-id="f4cca-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

<span data-ttu-id="f4cca-116">Pierwsze polecenie przechowuje wartość ciągu Contoso w $Vault zmienną.</span><span class="sxs-lookup"><span data-stu-id="f4cca-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="f4cca-117">Drugie polecenie przechowuje wartość ciągu IT w $Prefix zmienną.</span><span class="sxs-lookup"><span data-stu-id="f4cca-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="f4cca-118">Trzecie polecenie używa Get-AzKeyVaultSecret cmdlet w celu uzyskania sekretów określonego magazynu kluczy, a następnie przekazuje te tajemnice do polecenia cmdlet **Where-Object.**</span><span class="sxs-lookup"><span data-stu-id="f4cca-118">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="f4cca-119">Polecenie **cmdlet Where-Object** odfiltrowuje sekrety nazw zaczynanych od znaków IT.</span><span class="sxs-lookup"><span data-stu-id="f4cca-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="f4cca-120">Polecenie potokuje tajemnice, które pasują do filtru Update-AzKeyVaultSecret polecenie cmdlet, co spowoduje ich wyłączenie.</span><span class="sxs-lookup"><span data-stu-id="f4cca-120">The command pipes the secrets that match the filter to the Update-AzKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="f4cca-121">Przykład 4. Ustawianie typu Zawartości dla wszystkich wersji tajnych</span><span class="sxs-lookup"><span data-stu-id="f4cca-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="f4cca-122">Pierwsze trzy polecenia definiują zmienne ciągu, które mają być używane dla parametrów *Nazwa* magazynu, *Nazwa* i *ContentType.*</span><span class="sxs-lookup"><span data-stu-id="f4cca-122">The first three commands define string variables to use for the *VaultName*, *Name*, and *ContentType* parameters.</span></span> <span data-ttu-id="f4cca-123">Czwarte polecenie używa polecenia cmdlet Get-AzKeyVaultKey do uzyskania określonych kluczy i potokuje klawisze do polecenia cmdlet programu Update-AzKeyVaultSecret, aby ustawić typ zawartości na XML.</span><span class="sxs-lookup"><span data-stu-id="f4cca-123">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="f4cca-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4cca-124">PARAMETERS</span></span>

### <span data-ttu-id="f4cca-125">- ContentType</span><span class="sxs-lookup"><span data-stu-id="f4cca-125">-ContentType</span></span>
<span data-ttu-id="f4cca-126">Typ zawartości tajny.</span><span class="sxs-lookup"><span data-stu-id="f4cca-126">Secret's content type.</span></span>
<span data-ttu-id="f4cca-127">Jeśli nie zostanie określona, istniejąca wartość typu zawartości tajnych pozostanie niezmieniona.</span><span class="sxs-lookup"><span data-stu-id="f4cca-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="f4cca-128">Usuń istniejącą wartość typu zawartości, określając pusty ciąg.</span><span class="sxs-lookup"><span data-stu-id="f4cca-128">Remove the existing content type value by specifying an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4cca-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4cca-129">-DefaultProfile</span></span>
<span data-ttu-id="f4cca-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4cca-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4cca-131">— Włącz</span><span class="sxs-lookup"><span data-stu-id="f4cca-131">-Enable</span></span>
<span data-ttu-id="f4cca-132">Jeśli istnieje, włącz klucz tajny, jeśli wartość jest prawdziwa.</span><span class="sxs-lookup"><span data-stu-id="f4cca-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="f4cca-133">Wyłącz klucz tajny, jeśli wartość jest fałszywa.</span><span class="sxs-lookup"><span data-stu-id="f4cca-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="f4cca-134">Jeśli nie zostanie określona, istniejąca wartość stanu włączone/wyłączonego tajnych pozostanie niezmieniona.</span><span class="sxs-lookup"><span data-stu-id="f4cca-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="f4cca-135">— Wygasa</span><span class="sxs-lookup"><span data-stu-id="f4cca-135">-Expires</span></span>
<span data-ttu-id="f4cca-136">Czas wygaśnięcia tajnego pliku w czasie UTC.</span><span class="sxs-lookup"><span data-stu-id="f4cca-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="f4cca-137">Jeśli nie zostanie określona, istniejąca wartość czasu wygaśnięcia tajemnicy pozostanie niezmieniona.</span><span class="sxs-lookup"><span data-stu-id="f4cca-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

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

### <span data-ttu-id="f4cca-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4cca-138">-InputObject</span></span>
<span data-ttu-id="f4cca-139">Tajny obiekt</span><span class="sxs-lookup"><span data-stu-id="f4cca-139">Secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4cca-140">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f4cca-140">-Name</span></span>
<span data-ttu-id="f4cca-141">Tajna nazwa.</span><span class="sxs-lookup"><span data-stu-id="f4cca-141">Secret name.</span></span>
<span data-ttu-id="f4cca-142">Polecenie cmdlet konstruuje nazwę FQDN tajnych nazw magazynów, obecnie wybranego środowiska i nazwy tajnej.</span><span class="sxs-lookup"><span data-stu-id="f4cca-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4cca-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="f4cca-143">-NotBefore</span></span>
<span data-ttu-id="f4cca-144">Czas UTC, przed którym nie można użyć tajnych danych.</span><span class="sxs-lookup"><span data-stu-id="f4cca-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="f4cca-145">Jeśli nie zostanie określona, istniejąca wartość atrybutu NotBefore sekretu pozostanie niezmieniona.</span><span class="sxs-lookup"><span data-stu-id="f4cca-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

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

### <span data-ttu-id="f4cca-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4cca-146">-PassThru</span></span>
<span data-ttu-id="f4cca-147">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="f4cca-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="f4cca-148">Jeśli ten przełącznik jest określony, zwróć tajny obiekt.</span><span class="sxs-lookup"><span data-stu-id="f4cca-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="f4cca-149">— Tag</span><span class="sxs-lookup"><span data-stu-id="f4cca-149">-Tag</span></span>
<span data-ttu-id="f4cca-150">Hashtable representing secret tags.</span><span class="sxs-lookup"><span data-stu-id="f4cca-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="f4cca-151">Jeśli nie zostanie określona, istniejące tagi tajnych pozostaną niezmienione.</span><span class="sxs-lookup"><span data-stu-id="f4cca-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="f4cca-152">Usuń tag, określając pustą tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="f4cca-152">Remove a tag by specifying an empty Hashtable.</span></span>

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

### <span data-ttu-id="f4cca-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f4cca-153">-VaultName</span></span>
<span data-ttu-id="f4cca-154">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="f4cca-154">Vault name.</span></span>
<span data-ttu-id="f4cca-155">Polecenie cmdlet konstruuje nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="f4cca-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f4cca-156">— Wersja</span><span class="sxs-lookup"><span data-stu-id="f4cca-156">-Version</span></span>
<span data-ttu-id="f4cca-157">Wersja tajna.</span><span class="sxs-lookup"><span data-stu-id="f4cca-157">Secret version.</span></span>
<span data-ttu-id="f4cca-158">Polecenie cmdlet konstruuje nazwę FQDN tajnych nazw magazynów, obecnie wybrane środowisko, nazwę tajną i wersję tajną.</span><span class="sxs-lookup"><span data-stu-id="f4cca-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4cca-159">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f4cca-159">-Confirm</span></span>
<span data-ttu-id="f4cca-160">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f4cca-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4cca-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4cca-161">-WhatIf</span></span>
<span data-ttu-id="f4cca-162">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4cca-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4cca-163">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f4cca-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4cca-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4cca-164">CommonParameters</span></span>
<span data-ttu-id="f4cca-165">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4cca-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4cca-166">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4cca-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4cca-167">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4cca-167">INPUTS</span></span>

### <span data-ttu-id="f4cca-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f4cca-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="f4cca-169">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4cca-169">OUTPUTS</span></span>

### <span data-ttu-id="f4cca-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f4cca-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="f4cca-171">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f4cca-171">NOTES</span></span>

## <span data-ttu-id="f4cca-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4cca-172">RELATED LINKS</span></span>
