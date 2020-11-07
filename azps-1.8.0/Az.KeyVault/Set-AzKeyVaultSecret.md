---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: 14b66299fb0321448b7e121cfced0a29f69518ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867868"
---
# <span data-ttu-id="55f98-101">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="55f98-101">Set-AzKeyVaultSecret</span></span>

## <span data-ttu-id="55f98-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="55f98-102">SYNOPSIS</span></span>
<span data-ttu-id="55f98-103">Tworzy lub aktualizuje klucz tajny w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="55f98-103">Creates or updates a secret in a key vault.</span></span>

## <span data-ttu-id="55f98-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="55f98-104">SYNTAX</span></span>

### <span data-ttu-id="55f98-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="55f98-105">Default (Default)</span></span>
```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55f98-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="55f98-106">InputObject</span></span>
```
Set-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55f98-107">Opis</span><span class="sxs-lookup"><span data-stu-id="55f98-107">DESCRIPTION</span></span>
<span data-ttu-id="55f98-108">Polecenie cmdlet **Set-AzKeyVaultSecret** umożliwia utworzenie lub zaktualizowanie klucza tajnego w magazynie kluczy usługi Azure Key.</span><span class="sxs-lookup"><span data-stu-id="55f98-108">The **Set-AzKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="55f98-109">Jeśli klucz tajny nie istnieje, to polecenie cmdlet tworzy je.</span><span class="sxs-lookup"><span data-stu-id="55f98-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="55f98-110">Jeśli klucz tajny już istnieje, to polecenie cmdlet tworzy nową wersję tego klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="55f98-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="55f98-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="55f98-111">EXAMPLES</span></span>

### <span data-ttu-id="55f98-112">Przykład 1: modyfikowanie wartości wpisu tajnego przy użyciu atrybutów domyślnych</span><span class="sxs-lookup"><span data-stu-id="55f98-112">Example 1: Modify the value of a secret using default attributes</span></span>
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

<span data-ttu-id="55f98-113">Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Secret.</span><span class="sxs-lookup"><span data-stu-id="55f98-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="55f98-114">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="55f98-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="55f98-115">Drugie polecenie modyfikuje wartość wpisu tajnego o nazwie ITSecret w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="55f98-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="55f98-116">Wartość tajna stanie się wartością przechowywaną w $Secret.</span><span class="sxs-lookup"><span data-stu-id="55f98-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="55f98-117">Przykład 2: modyfikowanie wartości klucza tajnego przy użyciu atrybutów niestandardowych</span><span class="sxs-lookup"><span data-stu-id="55f98-117">Example 2: Modify the value of a secret using custom attributes</span></span>
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

<span data-ttu-id="55f98-118">Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Secret.</span><span class="sxs-lookup"><span data-stu-id="55f98-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="55f98-119">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="55f98-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="55f98-120">Następne polecenia definiują atrybuty niestandardowe dla daty wygaśnięcia, znaczników i typu kontekstu oraz przechowują atrybuty w zmiennych.</span><span class="sxs-lookup"><span data-stu-id="55f98-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="55f98-121">W ostatnim poleceniu są modyfikowane wartości wpisu tajnego o nazwie ITSecret w magazynie kluczy o nazwie contoso, przy użyciu wartości określonych wcześniej jako zmienne.</span><span class="sxs-lookup"><span data-stu-id="55f98-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="55f98-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55f98-122">PARAMETERS</span></span>

### <span data-ttu-id="55f98-123">-Type</span><span class="sxs-lookup"><span data-stu-id="55f98-123">-ContentType</span></span>
<span data-ttu-id="55f98-124">Określa typ zawartości wpisu tajnego.</span><span class="sxs-lookup"><span data-stu-id="55f98-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="55f98-125">Aby usunąć istniejący typ zawartości, określ pusty ciąg.</span><span class="sxs-lookup"><span data-stu-id="55f98-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="55f98-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f98-126">-DefaultProfile</span></span>
<span data-ttu-id="55f98-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="55f98-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55f98-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="55f98-128">-Disable</span></span>
<span data-ttu-id="55f98-129">Wskazuje, że to polecenie cmdlet wyłącza klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="55f98-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="55f98-130">-Wygasa</span><span class="sxs-lookup"><span data-stu-id="55f98-130">-Expires</span></span>
<span data-ttu-id="55f98-131">Określa czas wygaśnięcia jako obiekt **typu DateTime** dla wpisu tajnego, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55f98-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="55f98-132">W tym parametrze jest używany uniwersalny czas koordynowany (UTC).</span><span class="sxs-lookup"><span data-stu-id="55f98-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="55f98-133">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="55f98-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="55f98-134">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="55f98-134">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="55f98-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="55f98-135">-InputObject</span></span>
<span data-ttu-id="55f98-136">Obiekt tajny</span><span class="sxs-lookup"><span data-stu-id="55f98-136">Secret object</span></span>

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

### <span data-ttu-id="55f98-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="55f98-137">-Name</span></span>
<span data-ttu-id="55f98-138">Określa nazwę klucza tajnego do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="55f98-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="55f98-139">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza tajnego na podstawie nazwy, jaką ten parametr określa, nazwę magazynu kluczy i obecne środowisko.</span><span class="sxs-lookup"><span data-stu-id="55f98-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="55f98-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="55f98-140">-NotBefore</span></span>
<span data-ttu-id="55f98-141">Określa czas w postaci obiektu **DateTime** , przed którym nie można użyć klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="55f98-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="55f98-142">Ten parametr używa czasu UTC.</span><span class="sxs-lookup"><span data-stu-id="55f98-142">This parameter uses UTC.</span></span> <span data-ttu-id="55f98-143">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="55f98-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="55f98-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="55f98-144">-SecretValue</span></span>
<span data-ttu-id="55f98-145">Określa wartość wpisu tajnego jako obiekt **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="55f98-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="55f98-146">Aby uzyskać obiekt **SecureString** , użyj polecenia cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="55f98-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="55f98-147">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="55f98-147">For more information, type `Get-Help
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

### <span data-ttu-id="55f98-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="55f98-148">-Tag</span></span>
<span data-ttu-id="55f98-149">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="55f98-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="55f98-150">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="55f98-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="55f98-151">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="55f98-151">-VaultName</span></span>
<span data-ttu-id="55f98-152">Określa nazwę magazynu kluczy, do którego należy ten klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="55f98-152">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="55f98-153">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="55f98-153">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="55f98-154">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="55f98-154">-Confirm</span></span>
<span data-ttu-id="55f98-155">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55f98-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55f98-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55f98-156">-WhatIf</span></span>
<span data-ttu-id="55f98-157">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55f98-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55f98-158">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="55f98-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55f98-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f98-159">CommonParameters</span></span>
<span data-ttu-id="55f98-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55f98-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f98-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55f98-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f98-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55f98-162">INPUTS</span></span>

### <span data-ttu-id="55f98-163">Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="55f98-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="55f98-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="55f98-164">OUTPUTS</span></span>

### <span data-ttu-id="55f98-165">Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="55f98-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="55f98-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="55f98-166">NOTES</span></span>

## <span data-ttu-id="55f98-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55f98-167">RELATED LINKS</span></span>

[<span data-ttu-id="55f98-168">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="55f98-168">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="55f98-169">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="55f98-169">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
