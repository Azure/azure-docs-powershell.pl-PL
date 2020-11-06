---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
ms.openlocfilehash: 820406a3fe4bebfd0b2a972bb8676bbd483f7080
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527917"
---
# <span data-ttu-id="02d40-101">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="02d40-101">Set-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="02d40-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02d40-102">SYNOPSIS</span></span>
<span data-ttu-id="02d40-103">Tworzy lub aktualizuje klucz tajny w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="02d40-103">Creates or updates a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02d40-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02d40-104">SYNTAX</span></span>

### <span data-ttu-id="02d40-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="02d40-105">Default (Default)</span></span>
```
Set-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02d40-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="02d40-106">InputObject</span></span>
```
Set-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02d40-107">Opis</span><span class="sxs-lookup"><span data-stu-id="02d40-107">DESCRIPTION</span></span>
<span data-ttu-id="02d40-108">Polecenie cmdlet **Set-AzureKeyVaultSecret** umożliwia utworzenie lub zaktualizowanie klucza tajnego w magazynie kluczy usługi Azure Key.</span><span class="sxs-lookup"><span data-stu-id="02d40-108">The **Set-AzureKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="02d40-109">Jeśli klucz tajny nie istnieje, to polecenie cmdlet tworzy je.</span><span class="sxs-lookup"><span data-stu-id="02d40-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="02d40-110">Jeśli klucz tajny już istnieje, to polecenie cmdlet tworzy nową wersję tego klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="02d40-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="02d40-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02d40-111">EXAMPLES</span></span>

### <span data-ttu-id="02d40-112">Przykład 1: modyfikowanie wartości wpisu tajnego przy użyciu atrybutów domyślnych</span><span class="sxs-lookup"><span data-stu-id="02d40-112">Example 1: Modify the value of a secret using default attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret

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

<span data-ttu-id="02d40-113">Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Secret.</span><span class="sxs-lookup"><span data-stu-id="02d40-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="02d40-114">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="02d40-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="02d40-115">Drugie polecenie modyfikuje wartość wpisu tajnego o nazwie ITSecret w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="02d40-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="02d40-116">Wartość tajna stanie się wartością przechowywaną w $Secret.</span><span class="sxs-lookup"><span data-stu-id="02d40-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="02d40-117">Przykład 2: modyfikowanie wartości klucza tajnego przy użyciu atrybutów niestandardowych</span><span class="sxs-lookup"><span data-stu-id="02d40-117">Example 2: Modify the value of a secret using custom attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = 'true'}
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable -Tags $Tags

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

<span data-ttu-id="02d40-118">Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Secret.</span><span class="sxs-lookup"><span data-stu-id="02d40-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="02d40-119">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="02d40-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="02d40-120">Następne polecenia definiują atrybuty niestandardowe dla daty wygaśnięcia, znaczników i typu kontekstu oraz przechowują atrybuty w zmiennych.</span><span class="sxs-lookup"><span data-stu-id="02d40-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="02d40-121">W ostatnim poleceniu są modyfikowane wartości wpisu tajnego o nazwie ITSecret w magazynie kluczy o nazwie contoso, przy użyciu wartości określonych wcześniej jako zmienne.</span><span class="sxs-lookup"><span data-stu-id="02d40-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="02d40-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02d40-122">PARAMETERS</span></span>

### <span data-ttu-id="02d40-123">-Type</span><span class="sxs-lookup"><span data-stu-id="02d40-123">-ContentType</span></span>
<span data-ttu-id="02d40-124">Określa typ zawartości wpisu tajnego.</span><span class="sxs-lookup"><span data-stu-id="02d40-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="02d40-125">Aby usunąć istniejący typ zawartości, określ pusty ciąg.</span><span class="sxs-lookup"><span data-stu-id="02d40-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="02d40-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02d40-126">-DefaultProfile</span></span>
<span data-ttu-id="02d40-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="02d40-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02d40-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="02d40-128">-Disable</span></span>
<span data-ttu-id="02d40-129">Wskazuje, że to polecenie cmdlet wyłącza klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="02d40-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="02d40-130">-Wygasa</span><span class="sxs-lookup"><span data-stu-id="02d40-130">-Expires</span></span>
<span data-ttu-id="02d40-131">Określa czas wygaśnięcia jako obiekt **typu DateTime** dla wpisu tajnego, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02d40-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="02d40-132">W tym parametrze jest używany uniwersalny czas koordynowany (UTC).</span><span class="sxs-lookup"><span data-stu-id="02d40-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="02d40-133">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="02d40-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="02d40-134">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="02d40-134">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="02d40-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="02d40-135">-InputObject</span></span>
<span data-ttu-id="02d40-136">Obiekt tajny</span><span class="sxs-lookup"><span data-stu-id="02d40-136">Secret object</span></span>

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

### <span data-ttu-id="02d40-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="02d40-137">-Name</span></span>
<span data-ttu-id="02d40-138">Określa nazwę klucza tajnego do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="02d40-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="02d40-139">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza tajnego na podstawie nazwy, jaką ten parametr określa, nazwę magazynu kluczy i obecne środowisko.</span><span class="sxs-lookup"><span data-stu-id="02d40-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="02d40-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="02d40-140">-NotBefore</span></span>
<span data-ttu-id="02d40-141">Określa czas w postaci obiektu **DateTime** , przed którym nie można użyć klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="02d40-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="02d40-142">Ten parametr używa czasu UTC.</span><span class="sxs-lookup"><span data-stu-id="02d40-142">This parameter uses UTC.</span></span> <span data-ttu-id="02d40-143">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="02d40-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="02d40-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="02d40-144">-SecretValue</span></span>
<span data-ttu-id="02d40-145">Określa wartość wpisu tajnego jako obiekt **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="02d40-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="02d40-146">Aby uzyskać obiekt **SecureString** , użyj polecenia cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="02d40-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="02d40-147">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="02d40-147">For more information, type `Get-Help
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

### <span data-ttu-id="02d40-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="02d40-148">-Tag</span></span>
<span data-ttu-id="02d40-149">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="02d40-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="02d40-150">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="02d40-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="02d40-151">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="02d40-151">-VaultName</span></span>
<span data-ttu-id="02d40-152">Określa nazwę magazynu kluczy, do którego należy ten klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="02d40-152">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="02d40-153">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="02d40-153">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="02d40-154">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02d40-154">-Confirm</span></span>
<span data-ttu-id="02d40-155">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02d40-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02d40-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02d40-156">-WhatIf</span></span>
<span data-ttu-id="02d40-157">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02d40-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02d40-158">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="02d40-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02d40-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d40-159">CommonParameters</span></span>
<span data-ttu-id="02d40-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02d40-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d40-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02d40-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d40-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02d40-162">INPUTS</span></span>

### <span data-ttu-id="02d40-163">Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="02d40-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="02d40-164">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="02d40-164">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="02d40-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02d40-165">OUTPUTS</span></span>

### <span data-ttu-id="02d40-166">Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="02d40-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="02d40-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02d40-167">NOTES</span></span>

## <span data-ttu-id="02d40-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02d40-168">RELATED LINKS</span></span>

[<span data-ttu-id="02d40-169">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="02d40-169">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="02d40-170">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="02d40-170">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
