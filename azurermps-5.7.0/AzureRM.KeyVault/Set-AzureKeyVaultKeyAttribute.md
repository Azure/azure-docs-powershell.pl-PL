---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultkeyattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
ms.openlocfilehash: 4b9799a0d2433b513b801a95ffd5c408bf8bdbf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545668"
---
# <span data-ttu-id="3a91f-101">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="3a91f-101">Set-AzureKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="3a91f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a91f-102">SYNOPSIS</span></span>
<span data-ttu-id="3a91f-103">Aktualizuje atrybuty klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="3a91f-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a91f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a91f-104">SYNTAX</span></span>

### <span data-ttu-id="3a91f-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3a91f-105">Default (Default)</span></span>
```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a91f-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="3a91f-106">InputObject</span></span>
```
Set-AzureKeyVaultKeyAttribute [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a91f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3a91f-107">DESCRIPTION</span></span>
<span data-ttu-id="3a91f-108">Polecenie cmdlet **Set-AzureKeyVaultKeyAttribute** aktualizuje atrybuty edytowalne klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="3a91f-108">The **Set-AzureKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="3a91f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a91f-109">EXAMPLES</span></span>

### <span data-ttu-id="3a91f-110">Przykład 1: Zmodyfikuj klawisz, aby go włączyć, a następnie ustaw datę i Tagi wygasania.</span><span class="sxs-lookup"><span data-stu-id="3a91f-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="3a91f-111">Pierwsze polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="3a91f-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="3a91f-112">Ten obiekt Określa godzinę w przyszłości w dwóch latach.</span><span class="sxs-lookup"><span data-stu-id="3a91f-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="3a91f-113">Polecenie zapisuje tę datę w zmiennej $Expires.</span><span class="sxs-lookup"><span data-stu-id="3a91f-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="3a91f-114">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="3a91f-114">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="3a91f-115">Drugie polecenie tworzy zmienną do przechowywania wartości znaczników o wysokiej ważności i księgowaniu.</span><span class="sxs-lookup"><span data-stu-id="3a91f-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="3a91f-116">Polecenie ostatnie modyfikuje klucz o nazwie ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="3a91f-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="3a91f-117">Polecenie włącza klucz, ustawia czas wygaśnięcia w czasie przechowywanym w $Expires i ustawia Tagi przechowywane w $Tags.</span><span class="sxs-lookup"><span data-stu-id="3a91f-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="3a91f-118">Przykład 2: modyfikowanie klucza w celu usunięcia wszystkich znaczników</span><span class="sxs-lookup"><span data-stu-id="3a91f-118">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="3a91f-119">To polecenie usuwa wszystkie znaczniki dla określonej wersji klucza o nazwie ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="3a91f-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="3a91f-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a91f-120">PARAMETERS</span></span>

### <span data-ttu-id="3a91f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a91f-121">-DefaultProfile</span></span>
<span data-ttu-id="3a91f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3a91f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a91f-123">-Enable</span><span class="sxs-lookup"><span data-stu-id="3a91f-123">-Enable</span></span>
<span data-ttu-id="3a91f-124">Określa, czy należy włączyć lub wyłączyć klucz.</span><span class="sxs-lookup"><span data-stu-id="3a91f-124">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="3a91f-125">Wartość $True umożliwia włączenie klucza.</span><span class="sxs-lookup"><span data-stu-id="3a91f-125">A value of $True enables the key.</span></span> <span data-ttu-id="3a91f-126">Wartość $False wyłącza klucz.</span><span class="sxs-lookup"><span data-stu-id="3a91f-126">A value of $False disables the key.</span></span> <span data-ttu-id="3a91f-127">Jeśli nie podano tego parametru, to polecenie cmdlet nie powoduje zmiany stanu klucza.</span><span class="sxs-lookup"><span data-stu-id="3a91f-127">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a91f-128">-Wygasa</span><span class="sxs-lookup"><span data-stu-id="3a91f-128">-Expires</span></span>
<span data-ttu-id="3a91f-129">Określa czas wygaśnięcia jako obiekt **DateTime** dla klucza, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a91f-129">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="3a91f-130">W tym parametrze jest używany uniwersalny czas koordynowany (UTC).</span><span class="sxs-lookup"><span data-stu-id="3a91f-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="3a91f-131">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="3a91f-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="3a91f-132">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="3a91f-132">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="3a91f-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3a91f-133">-InputObject</span></span>
<span data-ttu-id="3a91f-134">Obiekt Key</span><span class="sxs-lookup"><span data-stu-id="3a91f-134">Key object</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a91f-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="3a91f-135">-KeyOps</span></span>
<span data-ttu-id="3a91f-136">Określa tablicę operacji, które można wykonać przy użyciu klucza, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a91f-136">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="3a91f-137">Jeśli nie podano tego parametru, można wykonać wszystkie operacje.</span><span class="sxs-lookup"><span data-stu-id="3a91f-137">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="3a91f-138">Dopuszczalne wartości tego parametru to rozdzielana przecinkami lista podstawowych operacji, które zdefiniowano w specyfikacji klucza internetowego JSON.</span><span class="sxs-lookup"><span data-stu-id="3a91f-138">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="3a91f-139">Wartości te (z uwzględnieniem wielkości liter) są następujące:</span><span class="sxs-lookup"><span data-stu-id="3a91f-139">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="3a91f-140">szyfrowane</span><span class="sxs-lookup"><span data-stu-id="3a91f-140">encrypt</span></span>
- <span data-ttu-id="3a91f-141">Szyfruj</span><span class="sxs-lookup"><span data-stu-id="3a91f-141">decrypt</span></span>
- <span data-ttu-id="3a91f-142">Pakuj</span><span class="sxs-lookup"><span data-stu-id="3a91f-142">wrap</span></span>
- <span data-ttu-id="3a91f-143">odwinięcie</span><span class="sxs-lookup"><span data-stu-id="3a91f-143">unwrap</span></span>
- <span data-ttu-id="3a91f-144">zapisywania</span><span class="sxs-lookup"><span data-stu-id="3a91f-144">sign</span></span>
- <span data-ttu-id="3a91f-145">sprawdzić</span><span class="sxs-lookup"><span data-stu-id="3a91f-145">verify</span></span>
- <span data-ttu-id="3a91f-146">wykonania</span><span class="sxs-lookup"><span data-stu-id="3a91f-146">backup</span></span>
- <span data-ttu-id="3a91f-147">przywrócenie</span><span class="sxs-lookup"><span data-stu-id="3a91f-147">restore</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a91f-148">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a91f-148">-Name</span></span>
<span data-ttu-id="3a91f-149">Określa nazwę klucza do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="3a91f-149">Specifies the name of the key to update.</span></span> <span data-ttu-id="3a91f-150">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza na podstawie nazwy, jaką określa ten parametr, nazwy magazynu kluczy i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="3a91f-150">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a91f-151">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="3a91f-151">-NotBefore</span></span>
<span data-ttu-id="3a91f-152">Określa czas (w postaci obiektu **DateTime** ), przed którym nie można użyć klucza.</span><span class="sxs-lookup"><span data-stu-id="3a91f-152">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="3a91f-153">Ten parametr używa czasu UTC.</span><span class="sxs-lookup"><span data-stu-id="3a91f-153">This parameter uses UTC.</span></span>
<span data-ttu-id="3a91f-154">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="3a91f-154">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="3a91f-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a91f-155">-PassThru</span></span>
<span data-ttu-id="3a91f-156">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="3a91f-156">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3a91f-157">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3a91f-157">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a91f-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="3a91f-158">-Tag</span></span>
<span data-ttu-id="3a91f-159">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3a91f-159">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3a91f-160">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="3a91f-160">For example:</span></span>

<span data-ttu-id="3a91f-161">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="3a91f-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3a91f-162">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="3a91f-162">-VaultName</span></span>
<span data-ttu-id="3a91f-163">Określa nazwę magazynu kluczy, w którym to polecenie cmdlet modyfikuje klucz.</span><span class="sxs-lookup"><span data-stu-id="3a91f-163">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="3a91f-164">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="3a91f-164">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a91f-165">-Version</span><span class="sxs-lookup"><span data-stu-id="3a91f-165">-Version</span></span>
<span data-ttu-id="3a91f-166">Określa wersję klucza.</span><span class="sxs-lookup"><span data-stu-id="3a91f-166">Specifies the key version.</span></span>
<span data-ttu-id="3a91f-167">To polecenie cmdlet konstruuje nazwę FQDN klucza na podstawie nazwy magazynu kluczy, obecnie wybranego środowiska, nazwy klucza i wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="3a91f-167">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a91f-168">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a91f-168">-Confirm</span></span>
<span data-ttu-id="3a91f-169">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a91f-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a91f-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a91f-170">-WhatIf</span></span>
<span data-ttu-id="3a91f-171">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a91f-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a91f-172">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3a91f-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a91f-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a91f-173">CommonParameters</span></span>
<span data-ttu-id="3a91f-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a91f-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a91f-175">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a91f-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a91f-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a91f-176">INPUTS</span></span>

### <span data-ttu-id="3a91f-177">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3a91f-177">None</span></span>
<span data-ttu-id="3a91f-178">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3a91f-178">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3a91f-179">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a91f-179">OUTPUTS</span></span>

### <span data-ttu-id="3a91f-180">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3a91f-180">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="3a91f-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a91f-181">NOTES</span></span>

## <span data-ttu-id="3a91f-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a91f-182">RELATED LINKS</span></span>

[<span data-ttu-id="3a91f-183">Dodaj-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3a91f-183">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="3a91f-184">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3a91f-184">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="3a91f-185">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3a91f-185">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)
