---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: 56a3fb2d31e4f80b15c027945437ffdc78aa131a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892997"
---
# <span data-ttu-id="381ba-101">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="381ba-101">Set-AzKeyVaultSecret</span></span>

## <span data-ttu-id="381ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="381ba-102">SYNOPSIS</span></span>
<span data-ttu-id="381ba-103">Tworzy lub aktualizuje klucz tajny w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="381ba-103">Creates or updates a secret in a key vault.</span></span>

## <span data-ttu-id="381ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="381ba-104">SYNTAX</span></span>

```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="381ba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="381ba-105">DESCRIPTION</span></span>
<span data-ttu-id="381ba-106">Polecenie cmdlet **Set-AzKeyVaultSecret** umożliwia utworzenie lub zaktualizowanie klucza tajnego w magazynie kluczy usługi Azure Key.</span><span class="sxs-lookup"><span data-stu-id="381ba-106">The **Set-AzKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="381ba-107">Jeśli klucz tajny nie istnieje, to polecenie cmdlet tworzy je.</span><span class="sxs-lookup"><span data-stu-id="381ba-107">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="381ba-108">Jeśli klucz tajny już istnieje, to polecenie cmdlet tworzy nową wersję tego klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="381ba-108">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="381ba-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="381ba-109">EXAMPLES</span></span>

### <span data-ttu-id="381ba-110">Przykład 1: modyfikowanie wartości wpisu tajnego przy użyciu atrybutów domyślnych</span><span class="sxs-lookup"><span data-stu-id="381ba-110">Example 1: Modify the value of a secret using default attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret
```

<span data-ttu-id="381ba-111">Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Secret.</span><span class="sxs-lookup"><span data-stu-id="381ba-111">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="381ba-112">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="381ba-112">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="381ba-113">Drugie polecenie modyfikuje wartość wpisu tajnego o nazwie ITSecret w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="381ba-113">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="381ba-114">Wartość tajna stanie się wartością przechowywaną w $Secret.</span><span class="sxs-lookup"><span data-stu-id="381ba-114">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="381ba-115">Przykład 2: modyfikowanie wartości klucza tajnego przy użyciu atrybutów niestandardowych</span><span class="sxs-lookup"><span data-stu-id="381ba-115">Example 2: Modify the value of a secret using custom attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = null }
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable $False -Tags $Tags
```

<span data-ttu-id="381ba-116">Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Secret.</span><span class="sxs-lookup"><span data-stu-id="381ba-116">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="381ba-117">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="381ba-117">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="381ba-118">Następne polecenia definiują atrybuty niestandardowe dla daty wygaśnięcia, znaczników i typu kontekstu oraz przechowują atrybuty w zmiennych.</span><span class="sxs-lookup"><span data-stu-id="381ba-118">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="381ba-119">W ostatnim poleceniu są modyfikowane wartości wpisu tajnego o nazwie ITSecret w magazynie kluczy o nazwie contoso, przy użyciu wartości określonych wcześniej jako zmienne.</span><span class="sxs-lookup"><span data-stu-id="381ba-119">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="381ba-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="381ba-120">PARAMETERS</span></span>

### <span data-ttu-id="381ba-121">-Type</span><span class="sxs-lookup"><span data-stu-id="381ba-121">-ContentType</span></span>
<span data-ttu-id="381ba-122">Określa typ zawartości wpisu tajnego.</span><span class="sxs-lookup"><span data-stu-id="381ba-122">Specifies the content type of a secret.</span></span>
<span data-ttu-id="381ba-123">Aby usunąć istniejący typ zawartości, określ pusty ciąg.</span><span class="sxs-lookup"><span data-stu-id="381ba-123">To delete the existing content type, specify an empty string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381ba-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="381ba-124">-DefaultProfile</span></span>
<span data-ttu-id="381ba-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="381ba-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381ba-126">-Disable</span><span class="sxs-lookup"><span data-stu-id="381ba-126">-Disable</span></span>
<span data-ttu-id="381ba-127">Wskazuje, że to polecenie cmdlet wyłącza klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="381ba-127">Indicates that this cmdlet disables a secret.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381ba-128">-Wygasa</span><span class="sxs-lookup"><span data-stu-id="381ba-128">-Expires</span></span>
<span data-ttu-id="381ba-129">Określa czas wygaśnięcia jako obiekt **typu DateTime** dla wpisu tajnego, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="381ba-129">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="381ba-130">W tym parametrze jest używany uniwersalny czas koordynowany (UTC).</span><span class="sxs-lookup"><span data-stu-id="381ba-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="381ba-131">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="381ba-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="381ba-132">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="381ba-132">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381ba-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="381ba-133">-Name</span></span>
<span data-ttu-id="381ba-134">Określa nazwę klucza tajnego do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="381ba-134">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="381ba-135">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza tajnego na podstawie nazwy, jaką ten parametr określa, nazwę magazynu kluczy i obecne środowisko.</span><span class="sxs-lookup"><span data-stu-id="381ba-135">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381ba-136">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="381ba-136">-NotBefore</span></span>
<span data-ttu-id="381ba-137">Określa czas w postaci obiektu **DateTime** , przed którym nie można użyć klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="381ba-137">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="381ba-138">Ten parametr używa czasu UTC.</span><span class="sxs-lookup"><span data-stu-id="381ba-138">This parameter uses UTC.</span></span> <span data-ttu-id="381ba-139">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="381ba-139">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381ba-140">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="381ba-140">-SecretValue</span></span>
<span data-ttu-id="381ba-141">Określa wartość wpisu tajnego jako obiekt **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="381ba-141">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="381ba-142">Aby uzyskać obiekt **SecureString** , użyj polecenia cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="381ba-142">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="381ba-143">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="381ba-143">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381ba-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="381ba-144">-Tag</span></span>
<span data-ttu-id="381ba-145">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="381ba-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="381ba-146">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="381ba-146">For example:</span></span>

<span data-ttu-id="381ba-147">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="381ba-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381ba-148">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="381ba-148">-VaultName</span></span>
<span data-ttu-id="381ba-149">Określa nazwę magazynu kluczy, do którego należy ten klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="381ba-149">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="381ba-150">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="381ba-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="381ba-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="381ba-151">-Confirm</span></span>
<span data-ttu-id="381ba-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="381ba-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381ba-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="381ba-153">-WhatIf</span></span>
<span data-ttu-id="381ba-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="381ba-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="381ba-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="381ba-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381ba-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="381ba-156">CommonParameters</span></span>
<span data-ttu-id="381ba-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="381ba-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="381ba-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="381ba-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="381ba-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="381ba-159">INPUTS</span></span>

### <span data-ttu-id="381ba-160">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="381ba-160">None</span></span>
<span data-ttu-id="381ba-161">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="381ba-161">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="381ba-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="381ba-162">OUTPUTS</span></span>

### <span data-ttu-id="381ba-163">Microsoft. Azure. Commands. model. modeli. Secret</span><span class="sxs-lookup"><span data-stu-id="381ba-163">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="381ba-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="381ba-164">NOTES</span></span>

## <span data-ttu-id="381ba-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="381ba-165">RELATED LINKS</span></span>

[<span data-ttu-id="381ba-166">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="381ba-166">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="381ba-167">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="381ba-167">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
