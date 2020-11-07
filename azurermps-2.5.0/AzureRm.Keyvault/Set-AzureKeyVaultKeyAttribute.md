---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultkeyattribute
schema: 2.0.0
ms.openlocfilehash: e7daafc147775b128351a7fa9ffb7b4d807bfe17
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898740"
---
# <span data-ttu-id="e6766-101">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="e6766-101">Set-AzureKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="e6766-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6766-102">SYNOPSIS</span></span>
<span data-ttu-id="e6766-103">Aktualizuje atrybuty klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="e6766-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6766-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6766-104">SYNTAX</span></span>

```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6766-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e6766-105">DESCRIPTION</span></span>
<span data-ttu-id="e6766-106">Polecenie cmdlet **Set-AzureKeyVaultKeyAttribute** aktualizuje atrybuty edytowalne klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="e6766-106">The **Set-AzureKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="e6766-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6766-107">EXAMPLES</span></span>

### <span data-ttu-id="e6766-108">Przykład 1: Zmodyfikuj klawisz, aby go włączyć, a następnie ustaw datę i Tagi wygasania.</span><span class="sxs-lookup"><span data-stu-id="e6766-108">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="e6766-109">Pierwsze polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="e6766-109">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="e6766-110">Ten obiekt Określa godzinę w przyszłości w dwóch latach.</span><span class="sxs-lookup"><span data-stu-id="e6766-110">That object specifies a time two years in the future.</span></span> <span data-ttu-id="e6766-111">Polecenie zapisuje tę datę w zmiennej $Expires.</span><span class="sxs-lookup"><span data-stu-id="e6766-111">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="e6766-112">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="e6766-112">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="e6766-113">Drugie polecenie tworzy zmienną do przechowywania wartości znaczników o wysokiej ważności i księgowaniu.</span><span class="sxs-lookup"><span data-stu-id="e6766-113">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="e6766-114">Polecenie ostatnie modyfikuje klucz o nazwie ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="e6766-114">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="e6766-115">Polecenie włącza klucz, ustawia czas wygaśnięcia w czasie przechowywanym w $Expires i ustawia Tagi przechowywane w $Tags.</span><span class="sxs-lookup"><span data-stu-id="e6766-115">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="e6766-116">Przykład 2: modyfikowanie klucza w celu usunięcia wszystkich znaczników</span><span class="sxs-lookup"><span data-stu-id="e6766-116">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="e6766-117">To polecenie usuwa wszystkie znaczniki dla określonej wersji klucza o nazwie ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="e6766-117">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="e6766-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6766-118">PARAMETERS</span></span>

### <span data-ttu-id="e6766-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6766-119">-DefaultProfile</span></span>
<span data-ttu-id="e6766-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e6766-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6766-121">-Enable</span><span class="sxs-lookup"><span data-stu-id="e6766-121">-Enable</span></span>
<span data-ttu-id="e6766-122">Określa, czy należy włączyć lub wyłączyć klucz.</span><span class="sxs-lookup"><span data-stu-id="e6766-122">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="e6766-123">Wartość $True umożliwia włączenie klucza.</span><span class="sxs-lookup"><span data-stu-id="e6766-123">A value of $True enables the key.</span></span> <span data-ttu-id="e6766-124">Wartość $False wyłącza klucz.</span><span class="sxs-lookup"><span data-stu-id="e6766-124">A value of $False disables the key.</span></span> <span data-ttu-id="e6766-125">Jeśli nie podano tego parametru, to polecenie cmdlet nie powoduje zmiany stanu klucza.</span><span class="sxs-lookup"><span data-stu-id="e6766-125">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

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

### <span data-ttu-id="e6766-126">-Wygasa</span><span class="sxs-lookup"><span data-stu-id="e6766-126">-Expires</span></span>
<span data-ttu-id="e6766-127">Określa czas wygaśnięcia jako obiekt **DateTime** dla klucza, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6766-127">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="e6766-128">W tym parametrze jest używany uniwersalny czas koordynowany (UTC).</span><span class="sxs-lookup"><span data-stu-id="e6766-128">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="e6766-129">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="e6766-129">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="e6766-130">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="e6766-130">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="e6766-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="e6766-131">-KeyOps</span></span>
<span data-ttu-id="e6766-132">Określa tablicę operacji, które można wykonać przy użyciu klucza, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6766-132">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="e6766-133">Jeśli nie podano tego parametru, można wykonać wszystkie operacje.</span><span class="sxs-lookup"><span data-stu-id="e6766-133">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="e6766-134">Dopuszczalne wartości tego parametru to rozdzielana przecinkami lista podstawowych operacji, które zdefiniowano w specyfikacji klucza internetowego JSON.</span><span class="sxs-lookup"><span data-stu-id="e6766-134">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="e6766-135">Wartości te (z uwzględnieniem wielkości liter) są następujące:</span><span class="sxs-lookup"><span data-stu-id="e6766-135">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="e6766-136">szyfrowane</span><span class="sxs-lookup"><span data-stu-id="e6766-136">encrypt</span></span>
- <span data-ttu-id="e6766-137">Szyfruj</span><span class="sxs-lookup"><span data-stu-id="e6766-137">decrypt</span></span>
- <span data-ttu-id="e6766-138">Pakuj</span><span class="sxs-lookup"><span data-stu-id="e6766-138">wrap</span></span>
- <span data-ttu-id="e6766-139">odwinięcie</span><span class="sxs-lookup"><span data-stu-id="e6766-139">unwrap</span></span>
- <span data-ttu-id="e6766-140">zapisywania</span><span class="sxs-lookup"><span data-stu-id="e6766-140">sign</span></span>
- <span data-ttu-id="e6766-141">sprawdzić</span><span class="sxs-lookup"><span data-stu-id="e6766-141">verify</span></span>
- <span data-ttu-id="e6766-142">wykonania</span><span class="sxs-lookup"><span data-stu-id="e6766-142">backup</span></span>
- <span data-ttu-id="e6766-143">przywrócenie</span><span class="sxs-lookup"><span data-stu-id="e6766-143">restore</span></span>

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

### <span data-ttu-id="e6766-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e6766-144">-Name</span></span>
<span data-ttu-id="e6766-145">Określa nazwę klucza do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="e6766-145">Specifies the name of the key to update.</span></span> <span data-ttu-id="e6766-146">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza na podstawie nazwy, jaką określa ten parametr, nazwy magazynu kluczy i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="e6766-146">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6766-147">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="e6766-147">-NotBefore</span></span>
<span data-ttu-id="e6766-148">Określa czas (w postaci obiektu **DateTime** ), przed którym nie można użyć klucza.</span><span class="sxs-lookup"><span data-stu-id="e6766-148">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="e6766-149">Ten parametr używa czasu UTC.</span><span class="sxs-lookup"><span data-stu-id="e6766-149">This parameter uses UTC.</span></span>
<span data-ttu-id="e6766-150">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="e6766-150">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="e6766-151">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6766-151">-PassThru</span></span>
<span data-ttu-id="e6766-152">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="e6766-152">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e6766-153">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e6766-153">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e6766-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="e6766-154">-Tag</span></span>
<span data-ttu-id="e6766-155">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="e6766-155">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e6766-156">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="e6766-156">For example:</span></span>

<span data-ttu-id="e6766-157">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="e6766-157">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e6766-158">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="e6766-158">-VaultName</span></span>
<span data-ttu-id="e6766-159">Określa nazwę magazynu kluczy, w którym to polecenie cmdlet modyfikuje klucz.</span><span class="sxs-lookup"><span data-stu-id="e6766-159">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="e6766-160">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="e6766-160">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="e6766-161">-Version</span><span class="sxs-lookup"><span data-stu-id="e6766-161">-Version</span></span>
<span data-ttu-id="e6766-162">Określa wersję klucza.</span><span class="sxs-lookup"><span data-stu-id="e6766-162">Specifies the key version.</span></span>
<span data-ttu-id="e6766-163">To polecenie cmdlet konstruuje nazwę FQDN klucza na podstawie nazwy magazynu kluczy, obecnie wybranego środowiska, nazwy klucza i wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="e6766-163">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

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

### <span data-ttu-id="e6766-164">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e6766-164">-Confirm</span></span>
<span data-ttu-id="e6766-165">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6766-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6766-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6766-166">-WhatIf</span></span>
<span data-ttu-id="e6766-167">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6766-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6766-168">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e6766-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6766-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6766-169">CommonParameters</span></span>
<span data-ttu-id="e6766-170">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6766-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6766-171">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6766-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6766-172">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6766-172">INPUTS</span></span>

## <span data-ttu-id="e6766-173">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6766-173">OUTPUTS</span></span>

### <span data-ttu-id="e6766-174">Microsoft. Azure. Commands. platforming. MODELES.</span><span class="sxs-lookup"><span data-stu-id="e6766-174">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="e6766-175">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6766-175">NOTES</span></span>

## <span data-ttu-id="e6766-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6766-176">RELATED LINKS</span></span>

[<span data-ttu-id="e6766-177">Dodaj-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e6766-177">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="e6766-178">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e6766-178">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="e6766-179">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e6766-179">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)
