---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: 0733cf722e26cb52abdb84f7917a78d088f49fd4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185475"
---
# <span data-ttu-id="8abfb-101">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8abfb-101">Set-AzKeyVaultSecret</span></span>

## <span data-ttu-id="8abfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8abfb-102">SYNOPSIS</span></span>
<span data-ttu-id="8abfb-103">Tworzy lub aktualizuje klucz tajny w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="8abfb-103">Creates or updates a secret in a key vault.</span></span>

## <span data-ttu-id="8abfb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8abfb-104">SYNTAX</span></span>

### <span data-ttu-id="8abfb-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8abfb-105">Default (Default)</span></span>
```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8abfb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8abfb-106">InputObject</span></span>
```
Set-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8abfb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8abfb-107">DESCRIPTION</span></span>
<span data-ttu-id="8abfb-108">Polecenie **cmdlet Set-AzKeyVaultSecret** tworzy lub aktualizuje klucz tajny w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8abfb-108">The **Set-AzKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="8abfb-109">Jeśli klucz tajny nie istnieje, to polecenie cmdlet utworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8abfb-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="8abfb-110">Jeśli klucz tajny już istnieje, to polecenie cmdlet tworzy nową wersję tego tajnych.</span><span class="sxs-lookup"><span data-stu-id="8abfb-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="8abfb-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8abfb-111">EXAMPLES</span></span>

### <span data-ttu-id="8abfb-112">Przykład 1. Modyfikowanie wartości tajnych przy użyciu atrybutów domyślnych</span><span class="sxs-lookup"><span data-stu-id="8abfb-112">Example 1: Modify the value of a secret using default attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret

Vault Name   : Contoso
Name         : ITSecret
Version      : 8b5c0cb0326e4350bd78200fac932b51
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/8b5c0cb0326e4350bd78200fac932b51
Enabled      : True
Expires      :
Not Before   :
Created      : 5/25/2018 6:39:30 PM
Updated      : 5/25/2018 6:39:30 PM
Content Type :
Tags         :
```

<span data-ttu-id="8abfb-113">Pierwsze polecenie konwertuje ciąg na bezpieczny ciąg za pomocą polecenia cmdlet **ConvertTo-SecureString,** a następnie zapisuje ten ciąg w $Secret danych.</span><span class="sxs-lookup"><span data-stu-id="8abfb-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="8abfb-114">Aby uzyskać więcej informacji, wpisz `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="8abfb-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="8abfb-115">Drugie polecenie modyfikuje wartość klucza tajnego o nazwie ITSecret w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="8abfb-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="8abfb-116">Ta wartość staje się wartością przechowywaną w $Secret.</span><span class="sxs-lookup"><span data-stu-id="8abfb-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="8abfb-117">Przykład 2. Modyfikowanie wartości tajnych przy użyciu atrybutów niestandardowych</span><span class="sxs-lookup"><span data-stu-id="8abfb-117">Example 2: Modify the value of a secret using custom attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = 'true'}
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable -Tags $Tags

Vault Name   : Contoso
Name         : ITSecret
Version      : a2c150be3ea24dd6b8286986e6364851
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/a2c150be3ea24dd6b8286986e6364851
Enabled      : False
Expires      : 5/25/2020 6:40:00 PM
Not Before   : 5/25/2018 6:40:05 PM
Created      : 5/25/2018 6:41:22 PM
Updated      : 5/25/2018 6:41:22 PM
Content Type : txt
Tags         : Name      Value
               Severity  medium
               IT        true
```

<span data-ttu-id="8abfb-118">Pierwsze polecenie konwertuje ciąg na bezpieczny ciąg za pomocą polecenia cmdlet **ConvertTo-SecureString,** a następnie zapisuje ten ciąg w $Secret danych.</span><span class="sxs-lookup"><span data-stu-id="8abfb-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="8abfb-119">Aby uzyskać więcej informacji, wpisz `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="8abfb-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="8abfb-120">Następne polecenia definiują atrybuty niestandardowe dla daty wygaśnięcia, tagów i typu kontekstu oraz przechowują atrybuty w zmiennych.</span><span class="sxs-lookup"><span data-stu-id="8abfb-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="8abfb-121">Ostatnie polecenie modyfikuje wartości klucza tajnego o nazwie ITSecret w magazynie kluczy o nazwie Contoso, używając wartości określonych wcześniej jako zmienne.</span><span class="sxs-lookup"><span data-stu-id="8abfb-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="8abfb-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8abfb-122">PARAMETERS</span></span>

### <span data-ttu-id="8abfb-123">- ContentType</span><span class="sxs-lookup"><span data-stu-id="8abfb-123">-ContentType</span></span>
<span data-ttu-id="8abfb-124">Określa typ zawartości tajnej.</span><span class="sxs-lookup"><span data-stu-id="8abfb-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="8abfb-125">Aby usunąć istniejący typ zawartości, określ pusty ciąg.</span><span class="sxs-lookup"><span data-stu-id="8abfb-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="8abfb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8abfb-126">-DefaultProfile</span></span>
<span data-ttu-id="8abfb-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="8abfb-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8abfb-128">- Wyłącz</span><span class="sxs-lookup"><span data-stu-id="8abfb-128">-Disable</span></span>
<span data-ttu-id="8abfb-129">Wskazuje, że to polecenie cmdlet wyłącza klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="8abfb-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="8abfb-130">— Wygasa</span><span class="sxs-lookup"><span data-stu-id="8abfb-130">-Expires</span></span>
<span data-ttu-id="8abfb-131">Określa czas wygaśnięcia aktualizacji tego polecenia cmdlet jako obiektu **DateTime.**</span><span class="sxs-lookup"><span data-stu-id="8abfb-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="8abfb-132">W tym parametrze jest używany uniwersalny czas koordynowany (UTC).</span><span class="sxs-lookup"><span data-stu-id="8abfb-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="8abfb-133">Aby uzyskać obiekt **DateTime,** użyj polecenia cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="8abfb-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="8abfb-134">Aby uzyskać więcej informacji, wpisz `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="8abfb-134">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="8abfb-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8abfb-135">-InputObject</span></span>
<span data-ttu-id="8abfb-136">Tajny obiekt</span><span class="sxs-lookup"><span data-stu-id="8abfb-136">Secret object</span></span>

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

### <span data-ttu-id="8abfb-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8abfb-137">-Name</span></span>
<span data-ttu-id="8abfb-138">Określa nazwę tajnych danych do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="8abfb-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="8abfb-139">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza tajnego na podstawie nazwy, która jest określana przez ten parametr, nazwy magazynu kluczy i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="8abfb-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="8abfb-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="8abfb-140">-NotBefore</span></span>
<span data-ttu-id="8abfb-141">Określa czas jako obiekt **DateTime,** przed którym nie można użyć tajnych danych.</span><span class="sxs-lookup"><span data-stu-id="8abfb-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="8abfb-142">Ten parametr używa czasu UTC.</span><span class="sxs-lookup"><span data-stu-id="8abfb-142">This parameter uses UTC.</span></span> <span data-ttu-id="8abfb-143">Aby uzyskać obiekt **DateTime,** użyj polecenia cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="8abfb-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="8abfb-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="8abfb-144">-SecretValue</span></span>
<span data-ttu-id="8abfb-145">Określa wartość dla tajnego obiektu **jako obiekt SecureString.**</span><span class="sxs-lookup"><span data-stu-id="8abfb-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="8abfb-146">Aby uzyskać obiekt **SecureString,** użyj polecenia cmdlet **ConvertTo-SecureString.**</span><span class="sxs-lookup"><span data-stu-id="8abfb-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="8abfb-147">Aby uzyskać więcej informacji, wpisz `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="8abfb-147">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8abfb-148">— Tag</span><span class="sxs-lookup"><span data-stu-id="8abfb-148">-Tag</span></span>
<span data-ttu-id="8abfb-149">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="8abfb-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8abfb-150">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="8abfb-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8abfb-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8abfb-151">-VaultName</span></span>
<span data-ttu-id="8abfb-152">Określa nazwę magazynu kluczy, do którego należy ten klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="8abfb-152">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="8abfb-153">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, która jest określana przez ten parametr i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="8abfb-153">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="8abfb-154">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8abfb-154">-Confirm</span></span>
<span data-ttu-id="8abfb-155">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8abfb-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8abfb-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8abfb-156">-WhatIf</span></span>
<span data-ttu-id="8abfb-157">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8abfb-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8abfb-158">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8abfb-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8abfb-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8abfb-159">CommonParameters</span></span>
<span data-ttu-id="8abfb-160">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8abfb-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8abfb-161">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8abfb-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8abfb-162">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8abfb-162">INPUTS</span></span>

### <span data-ttu-id="8abfb-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8abfb-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="8abfb-164">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8abfb-164">OUTPUTS</span></span>

### <span data-ttu-id="8abfb-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8abfb-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="8abfb-166">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8abfb-166">NOTES</span></span>

## <span data-ttu-id="8abfb-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8abfb-167">RELATED LINKS</span></span>

[<span data-ttu-id="8abfb-168">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8abfb-168">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="8abfb-169">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8abfb-169">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
