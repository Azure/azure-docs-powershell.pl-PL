---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 5efc920d4dd6e8e83c0a2ee5f61768ac7373f864
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220836"
---
# <span data-ttu-id="9cd72-101">Update-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9cd72-101">Update-AzKeyVaultSecret</span></span>

## <span data-ttu-id="9cd72-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9cd72-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd72-103">Aktualizuje atrybuty klucza tajnego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="9cd72-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="9cd72-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9cd72-104">SYNTAX</span></span>

### <span data-ttu-id="9cd72-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9cd72-105">Default (Default)</span></span>
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cd72-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="9cd72-106">InputObject</span></span>
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cd72-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9cd72-107">DESCRIPTION</span></span>
<span data-ttu-id="9cd72-108">Polecenie cmdlet **Update-AzKeyVaultSecret** umożliwia aktualizowanie edytowalnych atrybutów klucza tajnego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="9cd72-108">The **Update-AzKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="9cd72-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9cd72-109">EXAMPLES</span></span>

### <span data-ttu-id="9cd72-110">Przykład 1: modyfikowanie atrybutów tajności</span><span class="sxs-lookup"><span data-stu-id="9cd72-110">Example 1: Modify the attributes of a secret</span></span>
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

<span data-ttu-id="9cd72-111">Pierwsze cztery polecenia definiują atrybuty daty wygaśnięcia, NotBefore Data, Tagi i typ kontekstu oraz przechowują atrybuty w zmiennych.</span><span class="sxs-lookup"><span data-stu-id="9cd72-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="9cd72-112">Polecenie ostatnie modyfikuje atrybuty wpisu tajnego o nazwie HR w magazynie kluczy o nazwie ContosoVault, korzystając z przechowywanych zmiennych.</span><span class="sxs-lookup"><span data-stu-id="9cd72-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="9cd72-113">Przykład 2: usuwanie znaczników i typu zawartości dla wpisu tajnego</span><span class="sxs-lookup"><span data-stu-id="9cd72-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="9cd72-114">To polecenie usuwa znaczniki i typ zawartości określonej wersji sekretu o nazwie HR w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="9cd72-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="9cd72-115">Przykład 3: wyłączanie bieżącej wersji kluczy tajnych, których imiona i nazwiska zaczynają się od niej</span><span class="sxs-lookup"><span data-stu-id="9cd72-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

<span data-ttu-id="9cd72-116">Pierwsze polecenie zapisuje wartość ciągu contoso w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="9cd72-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="9cd72-117">Drugie polecenie zapisuje wartość ciągu w zmiennej $Prefix.</span><span class="sxs-lookup"><span data-stu-id="9cd72-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="9cd72-118">W trzecim poleceniu jest używane polecenie cmdlet Get-AzKeyVaultSecret w celu uzyskania kluczy tajnych w określonym magazynie kluczy, a następnie przekazanie tych kluczy tajnych do polecenia cmdlet **WHERE-Object** .</span><span class="sxs-lookup"><span data-stu-id="9cd72-118">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="9cd72-119">Polecenie cmdlet **WHERE-Object** filtruje klucze tajne dla nazw, które zaczynają się od znaków.</span><span class="sxs-lookup"><span data-stu-id="9cd72-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="9cd72-120">Polecenie przełączy klucze tajne, które pasują do filtru Update-AzKeyVaultSecret polecenia cmdlet, co powoduje wyłączenie ich.</span><span class="sxs-lookup"><span data-stu-id="9cd72-120">The command pipes the secrets that match the filter to the Update-AzKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="9cd72-121">Przykład 4: Ustawianie typu zawartości dla wszystkich wersji klucza tajnego</span><span class="sxs-lookup"><span data-stu-id="9cd72-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="9cd72-122">Pierwsze trzy polecenia definiują zmienne tekstowe, które mają być używane dla parametrów *magazynname* , *name* i *ContentType* .</span><span class="sxs-lookup"><span data-stu-id="9cd72-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="9cd72-123">W czwartym poleceniu jest używane polecenie cmdlet Get-AzKeyVaultKey w celu uzyskania określonych kluczy i przeprzewody klawiszy do polecenia cmdlet Update-AzKeyVaultSecret w celu ustawienia typu zawartości na wartość XML.</span><span class="sxs-lookup"><span data-stu-id="9cd72-123">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="9cd72-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9cd72-124">PARAMETERS</span></span>

### <span data-ttu-id="9cd72-125">-Type</span><span class="sxs-lookup"><span data-stu-id="9cd72-125">-ContentType</span></span>
<span data-ttu-id="9cd72-126">Typ zawartości klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="9cd72-126">Secret's content type.</span></span>
<span data-ttu-id="9cd72-127">Jeśli nie zostanie określona, istniejąca wartość typu zawartości sekretu pozostanie niezmieniona.</span><span class="sxs-lookup"><span data-stu-id="9cd72-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="9cd72-128">Usuń istniejącą wartość typu zawartości, określając pusty ciąg.</span><span class="sxs-lookup"><span data-stu-id="9cd72-128">Remove the existing content type value by specifying an empty string.</span></span>

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

### <span data-ttu-id="9cd72-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cd72-129">-DefaultProfile</span></span>
<span data-ttu-id="9cd72-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9cd72-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cd72-131">-Enable</span><span class="sxs-lookup"><span data-stu-id="9cd72-131">-Enable</span></span>
<span data-ttu-id="9cd72-132">Jeśli jest obecny, włącz klucz tajny, jeśli wartość jest równa prawda.</span><span class="sxs-lookup"><span data-stu-id="9cd72-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="9cd72-133">Wyłącz klucz tajny, jeśli wartość jest równa FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="9cd72-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="9cd72-134">Jeśli nie określono tej wartości, istniejąca wartość stanu włączenia/wyłączenia klucza tajnego pozostaje bez zmian.</span><span class="sxs-lookup"><span data-stu-id="9cd72-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="9cd72-135">-Wygasa</span><span class="sxs-lookup"><span data-stu-id="9cd72-135">-Expires</span></span>
<span data-ttu-id="9cd72-136">Czas wygaśnięcia klucza tajnego w czasie UTC.</span><span class="sxs-lookup"><span data-stu-id="9cd72-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="9cd72-137">Jeśli nie podano tego parametru, istniejąca wartość czasu wygaśnięcia klucza tajnego pozostanie niezmieniona.</span><span class="sxs-lookup"><span data-stu-id="9cd72-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

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

### <span data-ttu-id="9cd72-138">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9cd72-138">-InputObject</span></span>
<span data-ttu-id="9cd72-139">Obiekt tajny</span><span class="sxs-lookup"><span data-stu-id="9cd72-139">Secret object</span></span>

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

### <span data-ttu-id="9cd72-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9cd72-140">-Name</span></span>
<span data-ttu-id="9cd72-141">Nazwa tajna.</span><span class="sxs-lookup"><span data-stu-id="9cd72-141">Secret name.</span></span>
<span data-ttu-id="9cd72-142">Polecenie cmdlet tworzy nazwę FQDN wpisu tajnego na podstawie nazwy magazynu, obecnie wybranej nazwy środowiska i sekretu.</span><span class="sxs-lookup"><span data-stu-id="9cd72-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="9cd72-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="9cd72-143">-NotBefore</span></span>
<span data-ttu-id="9cd72-144">Czas UTC, przed upływem którego nie można użyć klucza.</span><span class="sxs-lookup"><span data-stu-id="9cd72-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="9cd72-145">Jeśli nie podano tego parametru, istniejąca wartość atrybutu NotBefore tajnego wpisu pozostaje niezmieniona.</span><span class="sxs-lookup"><span data-stu-id="9cd72-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

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

### <span data-ttu-id="9cd72-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cd72-146">-PassThru</span></span>
<span data-ttu-id="9cd72-147">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="9cd72-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="9cd72-148">Jeśli ten przełącznik jest określony, zwraca tajny obiekt.</span><span class="sxs-lookup"><span data-stu-id="9cd72-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="9cd72-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="9cd72-149">-Tag</span></span>
<span data-ttu-id="9cd72-150">Obiekt Hashtable reprezentujący Tagi tajne.</span><span class="sxs-lookup"><span data-stu-id="9cd72-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="9cd72-151">Jeśli nie określono, istniejące znaczniki sekretu pozostaną niezmienione.</span><span class="sxs-lookup"><span data-stu-id="9cd72-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="9cd72-152">Usuń znacznik, określając pustą tablicę.</span><span class="sxs-lookup"><span data-stu-id="9cd72-152">Remove a tag by specifying an empty Hashtable.</span></span>

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

### <span data-ttu-id="9cd72-153">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="9cd72-153">-VaultName</span></span>
<span data-ttu-id="9cd72-154">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="9cd72-154">Vault name.</span></span>
<span data-ttu-id="9cd72-155">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="9cd72-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="9cd72-156">-Version</span><span class="sxs-lookup"><span data-stu-id="9cd72-156">-Version</span></span>
<span data-ttu-id="9cd72-157">Wersja tajna.</span><span class="sxs-lookup"><span data-stu-id="9cd72-157">Secret version.</span></span>
<span data-ttu-id="9cd72-158">Polecenie cmdlet tworzy nazwę FQDN wpisu tajnego na podstawie nazwy magazynu, obecnie wybranego środowiska, tajnej nazwy i tajnej wersji.</span><span class="sxs-lookup"><span data-stu-id="9cd72-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

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

### <span data-ttu-id="9cd72-159">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9cd72-159">-Confirm</span></span>
<span data-ttu-id="9cd72-160">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cd72-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cd72-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cd72-161">-WhatIf</span></span>
<span data-ttu-id="9cd72-162">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cd72-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cd72-163">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9cd72-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cd72-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd72-164">CommonParameters</span></span>
<span data-ttu-id="9cd72-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cd72-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd72-166">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cd72-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd72-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cd72-167">INPUTS</span></span>

### <span data-ttu-id="9cd72-168">Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9cd72-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="9cd72-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9cd72-169">OUTPUTS</span></span>

### <span data-ttu-id="9cd72-170">Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9cd72-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="9cd72-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9cd72-171">NOTES</span></span>

## <span data-ttu-id="9cd72-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cd72-172">RELATED LINKS</span></span>
