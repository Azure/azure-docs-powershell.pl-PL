---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://go.microsoft.com/fwlink/?LinkId=690303
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
ms.openlocfilehash: 737a99fa59530ca37d32e2ca1c2c7d7e609ed225
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719022"
---
# <span data-ttu-id="b6edb-101">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b6edb-101">Set-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="b6edb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6edb-102">SYNOPSIS</span></span>
<span data-ttu-id="b6edb-103">Tworzy lub aktualizuje klucz tajny w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="b6edb-103">Creates or updates a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6edb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6edb-104">SYNTAX</span></span>

```
Set-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6edb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6edb-105">DESCRIPTION</span></span>
<span data-ttu-id="b6edb-106">Polecenie cmdlet **Set-AzureKeyVaultSecret** umożliwia utworzenie lub zaktualizowanie klucza tajnego w magazynie kluczy usługi Azure Key.</span><span class="sxs-lookup"><span data-stu-id="b6edb-106">The **Set-AzureKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="b6edb-107">Jeśli klucz tajny nie istnieje, to polecenie cmdlet tworzy je.</span><span class="sxs-lookup"><span data-stu-id="b6edb-107">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="b6edb-108">Jeśli klucz tajny już istnieje, to polecenie cmdlet tworzy nową wersję tego klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="b6edb-108">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="b6edb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6edb-109">EXAMPLES</span></span>

### <span data-ttu-id="b6edb-110">Przykład 1: modyfikowanie wartości wpisu tajnego przy użyciu atrybutów domyślnych</span><span class="sxs-lookup"><span data-stu-id="b6edb-110">Example 1: Modify the value of a secret using default attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret
```

<span data-ttu-id="b6edb-111">Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Secret.</span><span class="sxs-lookup"><span data-stu-id="b6edb-111">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="b6edb-112">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="b6edb-112">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="b6edb-113">Drugie polecenie modyfikuje wartość wpisu tajnego o nazwie ITSecret w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="b6edb-113">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="b6edb-114">Wartość tajna stanie się wartością przechowywaną w $Secret.</span><span class="sxs-lookup"><span data-stu-id="b6edb-114">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="b6edb-115">Przykład 2: modyfikowanie wartości klucza tajnego przy użyciu atrybutów niestandardowych</span><span class="sxs-lookup"><span data-stu-id="b6edb-115">Example 2: Modify the value of a secret using custom attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = null }
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable $False -Tags $Tags
```

<span data-ttu-id="b6edb-116">Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Secret.</span><span class="sxs-lookup"><span data-stu-id="b6edb-116">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="b6edb-117">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="b6edb-117">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="b6edb-118">Następne polecenia definiują atrybuty niestandardowe dla daty wygaśnięcia, znaczników i typu kontekstu oraz przechowują atrybuty w zmiennych.</span><span class="sxs-lookup"><span data-stu-id="b6edb-118">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="b6edb-119">W ostatnim poleceniu są modyfikowane wartości wpisu tajnego o nazwie ITSecret w magazynie kluczy o nazwie contoso, przy użyciu wartości określonych wcześniej jako zmienne.</span><span class="sxs-lookup"><span data-stu-id="b6edb-119">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="b6edb-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6edb-120">PARAMETERS</span></span>

### <span data-ttu-id="b6edb-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6edb-121">-Confirm</span></span>
<span data-ttu-id="b6edb-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6edb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6edb-123">-Type</span><span class="sxs-lookup"><span data-stu-id="b6edb-123">-ContentType</span></span>
<span data-ttu-id="b6edb-124">Określa typ zawartości wpisu tajnego.</span><span class="sxs-lookup"><span data-stu-id="b6edb-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="b6edb-125">Aby usunąć istniejący typ zawartości, określ pusty ciąg.</span><span class="sxs-lookup"><span data-stu-id="b6edb-125">To delete the existing content type, specify an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6edb-126">-Disable</span><span class="sxs-lookup"><span data-stu-id="b6edb-126">-Disable</span></span>
<span data-ttu-id="b6edb-127">Wskazuje, że to polecenie cmdlet wyłącza klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="b6edb-127">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="b6edb-128">-Wygasa</span><span class="sxs-lookup"><span data-stu-id="b6edb-128">-Expires</span></span>
<span data-ttu-id="b6edb-129">Określa czas wygaśnięcia jako obiekt **typu DateTime** dla wpisu tajnego, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6edb-129">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="b6edb-130">W tym parametrze jest używany uniwersalny czas koordynowany (UTC).</span><span class="sxs-lookup"><span data-stu-id="b6edb-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="b6edb-131">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="b6edb-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="b6edb-132">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="b6edb-132">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6edb-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6edb-133">-Name</span></span>
<span data-ttu-id="b6edb-134">Określa nazwę klucza tajnego do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="b6edb-134">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="b6edb-135">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza tajnego na podstawie nazwy, jaką ten parametr określa, nazwę magazynu kluczy i obecne środowisko.</span><span class="sxs-lookup"><span data-stu-id="b6edb-135">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6edb-136">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="b6edb-136">-NotBefore</span></span>
<span data-ttu-id="b6edb-137">Określa czas w postaci obiektu **DateTime** , przed którym nie można użyć klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="b6edb-137">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="b6edb-138">Ten parametr używa czasu UTC.</span><span class="sxs-lookup"><span data-stu-id="b6edb-138">This parameter uses UTC.</span></span> <span data-ttu-id="b6edb-139">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="b6edb-139">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6edb-140">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="b6edb-140">-SecretValue</span></span>
<span data-ttu-id="b6edb-141">Określa wartość wpisu tajnego jako obiekt **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="b6edb-141">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="b6edb-142">Aby uzyskać obiekt **SecureString** , użyj polecenia cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="b6edb-142">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="b6edb-143">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="b6edb-143">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6edb-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6edb-144">-Tag</span></span>
<span data-ttu-id="b6edb-145">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="b6edb-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b6edb-146">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="b6edb-146">For example:</span></span>

<span data-ttu-id="b6edb-147">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="b6edb-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6edb-148">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="b6edb-148">-VaultName</span></span>
<span data-ttu-id="b6edb-149">Określa nazwę magazynu kluczy, do którego należy ten klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="b6edb-149">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="b6edb-150">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="b6edb-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6edb-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6edb-151">-WhatIf</span></span>
<span data-ttu-id="b6edb-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6edb-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6edb-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b6edb-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6edb-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6edb-154">-DefaultProfile</span></span>
<span data-ttu-id="b6edb-155">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6edb-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6edb-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6edb-156">CommonParameters</span></span>
<span data-ttu-id="b6edb-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6edb-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6edb-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6edb-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6edb-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6edb-159">INPUTS</span></span>

## <span data-ttu-id="b6edb-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6edb-160">OUTPUTS</span></span>

### <span data-ttu-id="b6edb-161">Microsoft. Azure. Commands. model. modeli. Secret</span><span class="sxs-lookup"><span data-stu-id="b6edb-161">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="b6edb-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6edb-162">NOTES</span></span>

## <span data-ttu-id="b6edb-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6edb-163">RELATED LINKS</span></span>

[<span data-ttu-id="b6edb-164">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b6edb-164">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="b6edb-165">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b6edb-165">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)