---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultSecret.md
ms.openlocfilehash: d895485354c33daa4eac57b699358ee0335905be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719118"
---
# <span data-ttu-id="36cc3-101">Update-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="36cc3-101">Update-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="36cc3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="36cc3-103">Aktualizuje atrybuty klucza tajnego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="36cc3-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36cc3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36cc3-104">SYNTAX</span></span>

### <span data-ttu-id="36cc3-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="36cc3-105">Default (Default)</span></span>
```
Update-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36cc3-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="36cc3-106">InputObject</span></span>
```
Update-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36cc3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="36cc3-107">DESCRIPTION</span></span>
<span data-ttu-id="36cc3-108">Polecenie cmdlet **Update-AzureKeyVaultSecret** umożliwia aktualizowanie edytowalnych atrybutów klucza tajnego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="36cc3-108">The **Update-AzureKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="36cc3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36cc3-109">EXAMPLES</span></span>

### <span data-ttu-id="36cc3-110">Przykład 1: modyfikowanie atrybutów tajności</span><span class="sxs-lookup"><span data-stu-id="36cc3-110">Example 1: Modify the attributes of a secret</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzureKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

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

<span data-ttu-id="36cc3-111">Pierwsze cztery polecenia definiują atrybuty daty wygaśnięcia, NotBefore Data, Tagi i typ kontekstu oraz przechowują atrybuty w zmiennych.</span><span class="sxs-lookup"><span data-stu-id="36cc3-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="36cc3-112">Polecenie ostatnie modyfikuje atrybuty wpisu tajnego o nazwie HR w magazynie kluczy o nazwie ContosoVault, korzystając z przechowywanych zmiennych.</span><span class="sxs-lookup"><span data-stu-id="36cc3-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="36cc3-113">Przykład 2: usuwanie znaczników i typu zawartości dla wpisu tajnego</span><span class="sxs-lookup"><span data-stu-id="36cc3-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzureKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="36cc3-114">To polecenie usuwa znaczniki i typ zawartości określonej wersji sekretu o nazwie HR w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="36cc3-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="36cc3-115">Przykład 3: wyłączanie bieżącej wersji kluczy tajnych, których imiona i nazwiska zaczynają się od niej</span><span class="sxs-lookup"><span data-stu-id="36cc3-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzureKeyVaultSecret -Enable $False
```

<span data-ttu-id="36cc3-116">Pierwsze polecenie zapisuje wartość ciągu contoso w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="36cc3-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="36cc3-117">Drugie polecenie zapisuje wartość ciągu w zmiennej $Prefix.</span><span class="sxs-lookup"><span data-stu-id="36cc3-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="36cc3-118">W trzecim poleceniu jest używane polecenie cmdlet Get-AzureKeyVaultSecret w celu uzyskania kluczy tajnych w określonym magazynie kluczy, a następnie przekazanie tych kluczy tajnych do polecenia cmdlet **WHERE-Object** .</span><span class="sxs-lookup"><span data-stu-id="36cc3-118">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="36cc3-119">Polecenie cmdlet **WHERE-Object** filtruje klucze tajne dla nazw, które zaczynają się od znaków.</span><span class="sxs-lookup"><span data-stu-id="36cc3-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="36cc3-120">Polecenie przełączy klucze tajne, które pasują do filtru Update-AzureKeyVaultSecret polecenia cmdlet, co powoduje wyłączenie ich.</span><span class="sxs-lookup"><span data-stu-id="36cc3-120">The command pipes the secrets that match the filter to the Update-AzureKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="36cc3-121">Przykład 4: Ustawianie typu zawartości dla wszystkich wersji klucza tajnego</span><span class="sxs-lookup"><span data-stu-id="36cc3-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzureKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="36cc3-122">Pierwsze trzy polecenia definiują zmienne tekstowe, które mają być używane dla parametrów *magazynname* , *name* i *ContentType* .</span><span class="sxs-lookup"><span data-stu-id="36cc3-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="36cc3-123">W czwartym poleceniu jest używane polecenie cmdlet Get-AzureKeyVaultKey w celu uzyskania określonych kluczy i przeprzewody klawiszy do polecenia cmdlet Update-AzureKeyVaultSecret w celu ustawienia typu zawartości na wartość XML.</span><span class="sxs-lookup"><span data-stu-id="36cc3-123">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzureKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="36cc3-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36cc3-124">PARAMETERS</span></span>

### <span data-ttu-id="36cc3-125">-Type</span><span class="sxs-lookup"><span data-stu-id="36cc3-125">-ContentType</span></span>
<span data-ttu-id="36cc3-126">Typ zawartości klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="36cc3-126">Secret's content type.</span></span>
<span data-ttu-id="36cc3-127">Jeśli nie zostanie określona, istniejąca wartość typu zawartości sekretu pozostanie niezmieniona.</span><span class="sxs-lookup"><span data-stu-id="36cc3-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="36cc3-128">Usuń istniejącą wartość typu zawartości, określając pusty ciąg.</span><span class="sxs-lookup"><span data-stu-id="36cc3-128">Remove the existing content type value by specifying an empty string.</span></span>

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

### <span data-ttu-id="36cc3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36cc3-129">-DefaultProfile</span></span>
<span data-ttu-id="36cc3-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="36cc3-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36cc3-131">-Enable</span><span class="sxs-lookup"><span data-stu-id="36cc3-131">-Enable</span></span>
<span data-ttu-id="36cc3-132">Jeśli jest obecny, włącz klucz tajny, jeśli wartość jest równa prawda.</span><span class="sxs-lookup"><span data-stu-id="36cc3-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="36cc3-133">Wyłącz klucz tajny, jeśli wartość jest równa FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="36cc3-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="36cc3-134">Jeśli nie określono tej wartości, istniejąca wartość stanu włączenia/wyłączenia klucza tajnego pozostaje bez zmian.</span><span class="sxs-lookup"><span data-stu-id="36cc3-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="36cc3-135">-Wygasa</span><span class="sxs-lookup"><span data-stu-id="36cc3-135">-Expires</span></span>
<span data-ttu-id="36cc3-136">Czas wygaśnięcia klucza tajnego w czasie UTC.</span><span class="sxs-lookup"><span data-stu-id="36cc3-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="36cc3-137">Jeśli nie podano tego parametru, istniejąca wartość czasu wygaśnięcia klucza tajnego pozostanie niezmieniona.</span><span class="sxs-lookup"><span data-stu-id="36cc3-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

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

### <span data-ttu-id="36cc3-138">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="36cc3-138">-InputObject</span></span>
<span data-ttu-id="36cc3-139">Obiekt tajny</span><span class="sxs-lookup"><span data-stu-id="36cc3-139">Secret object</span></span>

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

### <span data-ttu-id="36cc3-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36cc3-140">-Name</span></span>
<span data-ttu-id="36cc3-141">Nazwa tajna.</span><span class="sxs-lookup"><span data-stu-id="36cc3-141">Secret name.</span></span>
<span data-ttu-id="36cc3-142">Polecenie cmdlet tworzy nazwę FQDN wpisu tajnego na podstawie nazwy magazynu, obecnie wybranej nazwy środowiska i sekretu.</span><span class="sxs-lookup"><span data-stu-id="36cc3-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="36cc3-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="36cc3-143">-NotBefore</span></span>
<span data-ttu-id="36cc3-144">Czas UTC, przed upływem którego nie można użyć klucza.</span><span class="sxs-lookup"><span data-stu-id="36cc3-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="36cc3-145">Jeśli nie podano tego parametru, istniejąca wartość atrybutu NotBefore tajnego wpisu pozostaje niezmieniona.</span><span class="sxs-lookup"><span data-stu-id="36cc3-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

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

### <span data-ttu-id="36cc3-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36cc3-146">-PassThru</span></span>
<span data-ttu-id="36cc3-147">Polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="36cc3-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="36cc3-148">Jeśli ten przełącznik jest określony, zwraca tajny obiekt.</span><span class="sxs-lookup"><span data-stu-id="36cc3-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="36cc3-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="36cc3-149">-Tag</span></span>
<span data-ttu-id="36cc3-150">Obiekt Hashtable reprezentujący Tagi tajne.</span><span class="sxs-lookup"><span data-stu-id="36cc3-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="36cc3-151">Jeśli nie określono, istniejące znaczniki sekretu pozostaną niezmienione.</span><span class="sxs-lookup"><span data-stu-id="36cc3-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="36cc3-152">Usuń znacznik, określając pustą tablicę.</span><span class="sxs-lookup"><span data-stu-id="36cc3-152">Remove a tag by specifying an empty Hashtable.</span></span>

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

### <span data-ttu-id="36cc3-153">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="36cc3-153">-VaultName</span></span>
<span data-ttu-id="36cc3-154">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="36cc3-154">Vault name.</span></span>
<span data-ttu-id="36cc3-155">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="36cc3-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="36cc3-156">-Version</span><span class="sxs-lookup"><span data-stu-id="36cc3-156">-Version</span></span>
<span data-ttu-id="36cc3-157">Wersja tajna.</span><span class="sxs-lookup"><span data-stu-id="36cc3-157">Secret version.</span></span>
<span data-ttu-id="36cc3-158">Polecenie cmdlet tworzy nazwę FQDN wpisu tajnego na podstawie nazwy magazynu, obecnie wybranego środowiska, tajnej nazwy i tajnej wersji.</span><span class="sxs-lookup"><span data-stu-id="36cc3-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

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

### <span data-ttu-id="36cc3-159">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36cc3-159">-Confirm</span></span>
<span data-ttu-id="36cc3-160">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36cc3-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36cc3-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36cc3-161">-WhatIf</span></span>
<span data-ttu-id="36cc3-162">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36cc3-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36cc3-163">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="36cc3-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36cc3-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36cc3-164">CommonParameters</span></span>
<span data-ttu-id="36cc3-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36cc3-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36cc3-166">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36cc3-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36cc3-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36cc3-167">INPUTS</span></span>

### <span data-ttu-id="36cc3-168">Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="36cc3-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="36cc3-169">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="36cc3-169">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="36cc3-170">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36cc3-170">OUTPUTS</span></span>

### <span data-ttu-id="36cc3-171">Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="36cc3-171">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="36cc3-172">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36cc3-172">NOTES</span></span>

## <span data-ttu-id="36cc3-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36cc3-173">RELATED LINKS</span></span>
