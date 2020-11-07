---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecretattribute
schema: 2.0.0
ms.openlocfilehash: f8463533f8a153b74df1863ba251950f16f9e19a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897333"
---
# <span data-ttu-id="0d26a-101">Set-AzureKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="0d26a-101">Set-AzureKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="0d26a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d26a-102">SYNOPSIS</span></span>
<span data-ttu-id="0d26a-103">Aktualizuje atrybuty klucza tajnego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="0d26a-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d26a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d26a-104">SYNTAX</span></span>

```
Set-AzureKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d26a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0d26a-105">DESCRIPTION</span></span>
<span data-ttu-id="0d26a-106">Polecenie cmdlet **Set-AzureKeyVaultSecretAttribute** aktualizuje atrybuty edytowalne klucza tajnego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="0d26a-106">The **Set-AzureKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="0d26a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d26a-107">EXAMPLES</span></span>

### <span data-ttu-id="0d26a-108">Przykład 1: modyfikowanie atrybutów tajności</span><span class="sxs-lookup"><span data-stu-id="0d26a-108">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="0d26a-109">Pierwsze cztery polecenia definiują atrybuty daty wygaśnięcia, NotBefore Data, Tagi i typ kontekstu oraz przechowują atrybuty w zmiennych.</span><span class="sxs-lookup"><span data-stu-id="0d26a-109">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="0d26a-110">Polecenie ostatnie modyfikuje atrybuty wpisu tajnego o nazwie HR w magazynie kluczy o nazwie ContosoVault, korzystając z przechowywanych zmiennych.</span><span class="sxs-lookup"><span data-stu-id="0d26a-110">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="0d26a-111">Przykład 2: usuwanie znaczników i typu zawartości dla wpisu tajnego</span><span class="sxs-lookup"><span data-stu-id="0d26a-111">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="0d26a-112">To polecenie usuwa znaczniki i typ zawartości określonej wersji sekretu o nazwie HR w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="0d26a-112">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="0d26a-113">Przykład 3: wyłączanie bieżącej wersji kluczy tajnych, których imiona i nazwiska zaczynają się od niej</span><span class="sxs-lookup"><span data-stu-id="0d26a-113">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzureKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="0d26a-114">Pierwsze polecenie zapisuje wartość ciągu contoso w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="0d26a-114">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="0d26a-115">Drugie polecenie zapisuje wartość ciągu w zmiennej $Prefix.</span><span class="sxs-lookup"><span data-stu-id="0d26a-115">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="0d26a-116">W trzecim poleceniu jest używane polecenie cmdlet Get-AzureKeyVaultSecret w celu uzyskania kluczy tajnych w określonym magazynie kluczy, a następnie przekazanie tych kluczy tajnych do polecenia cmdlet **WHERE-Object** .</span><span class="sxs-lookup"><span data-stu-id="0d26a-116">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="0d26a-117">Polecenie cmdlet **WHERE-Object** filtruje klucze tajne dla nazw, które zaczynają się od znaków.</span><span class="sxs-lookup"><span data-stu-id="0d26a-117">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="0d26a-118">Polecenie przełączy klucze tajne, które pasują do filtru Set-AzureKeyVaultSecretAttribute polecenia cmdlet, co powoduje wyłączenie ich.</span><span class="sxs-lookup"><span data-stu-id="0d26a-118">The command pipes the secrets that match the filter to the Set-AzureKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="0d26a-119">Przykład 4: Ustawianie typu zawartości dla wszystkich wersji klucza tajnego</span><span class="sxs-lookup"><span data-stu-id="0d26a-119">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzureKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="0d26a-120">Pierwsze trzy polecenia definiują zmienne tekstowe, które mają być używane dla parametrów *magazynname* , *name* i *ContentType* .</span><span class="sxs-lookup"><span data-stu-id="0d26a-120">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="0d26a-121">W czwartym poleceniu jest używane polecenie cmdlet Get-AzureKeyVaultKey w celu uzyskania określonych kluczy i przeprzewody klawiszy do polecenia cmdlet Set-AzureKeyVaultSecretAttribute w celu ustawienia typu zawartości na wartość XML.</span><span class="sxs-lookup"><span data-stu-id="0d26a-121">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzureKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="0d26a-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d26a-122">PARAMETERS</span></span>

### <span data-ttu-id="0d26a-123">-Type</span><span class="sxs-lookup"><span data-stu-id="0d26a-123">-ContentType</span></span>
<span data-ttu-id="0d26a-124">Określa typ zawartości wpisu tajnego.</span><span class="sxs-lookup"><span data-stu-id="0d26a-124">Specifies the content type of a secret.</span></span> <span data-ttu-id="0d26a-125">Jeśli nie określisz tego parametru, nie zmienisz typu zawartości bieżącego klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="0d26a-125">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="0d26a-126">Aby usunąć istniejący typ zawartości, określ pusty ciąg.</span><span class="sxs-lookup"><span data-stu-id="0d26a-126">To remove the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="0d26a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d26a-127">-DefaultProfile</span></span>
<span data-ttu-id="0d26a-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0d26a-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d26a-129">-Enable</span><span class="sxs-lookup"><span data-stu-id="0d26a-129">-Enable</span></span>
<span data-ttu-id="0d26a-130">Wskazuje, czy włączyć klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="0d26a-130">Indicates whether to enable a secret.</span></span> <span data-ttu-id="0d26a-131">Określ $False, aby wyłączyć klucz tajny lub $True w celu włączenia klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="0d26a-131">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="0d26a-132">Jeśli ten parametr nie jest określony, nie ma żadnej zmiany w stanie włączenia lub wyłączenia bieżącego klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="0d26a-132">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

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

### <span data-ttu-id="0d26a-133">-Wygasa</span><span class="sxs-lookup"><span data-stu-id="0d26a-133">-Expires</span></span>
<span data-ttu-id="0d26a-134">Określa datę i godzinę unieważnienia klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="0d26a-134">Specifies the date and time that a secret expires.</span></span>

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

### <span data-ttu-id="0d26a-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0d26a-135">-Name</span></span>
<span data-ttu-id="0d26a-136">Określa nazwę wpisu tajnego.</span><span class="sxs-lookup"><span data-stu-id="0d26a-136">Specifies the name of a secret.</span></span> <span data-ttu-id="0d26a-137">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza tajnego na podstawie nazwy, jaką ten parametr określa, nazwę magazynu kluczy i obecne środowisko.</span><span class="sxs-lookup"><span data-stu-id="0d26a-137">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="0d26a-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="0d26a-138">-NotBefore</span></span>
<span data-ttu-id="0d26a-139">Określa uniwersalny czas koordynowany (UTC), przed którym nie można użyć klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="0d26a-139">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="0d26a-140">Jeśli nie określisz tego parametru, nie zmienisz atrybutu NotBefore bieżącego klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="0d26a-140">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

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

### <span data-ttu-id="0d26a-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d26a-141">-PassThru</span></span>
<span data-ttu-id="0d26a-142">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="0d26a-142">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0d26a-143">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="0d26a-143">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0d26a-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="0d26a-144">-Tag</span></span>
<span data-ttu-id="0d26a-145">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="0d26a-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0d26a-146">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="0d26a-146">For example:</span></span>

<span data-ttu-id="0d26a-147">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="0d26a-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0d26a-148">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="0d26a-148">-VaultName</span></span>
<span data-ttu-id="0d26a-149">Określa nazwę magazynu kluczy do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="0d26a-149">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="0d26a-150">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, którą ten parametr określa, oraz obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="0d26a-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

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

### <span data-ttu-id="0d26a-151">-Version</span><span class="sxs-lookup"><span data-stu-id="0d26a-151">-Version</span></span>
<span data-ttu-id="0d26a-152">Określa wersję wpisu tajnego.</span><span class="sxs-lookup"><span data-stu-id="0d26a-152">Specifies the version of a secret.</span></span>
<span data-ttu-id="0d26a-153">To polecenie cmdlet konstruuje nazwę FQDN wpisu tajnego na podstawie nazwy magazynu kluczy, obecnie wybranego środowiska, tajnej nazwy i tajnej wersji.</span><span class="sxs-lookup"><span data-stu-id="0d26a-153">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d26a-154">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0d26a-154">-Confirm</span></span>
<span data-ttu-id="0d26a-155">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d26a-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d26a-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d26a-156">-WhatIf</span></span>
<span data-ttu-id="0d26a-157">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d26a-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d26a-158">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0d26a-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d26a-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d26a-159">CommonParameters</span></span>
<span data-ttu-id="0d26a-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d26a-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d26a-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d26a-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d26a-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d26a-162">INPUTS</span></span>

## <span data-ttu-id="0d26a-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d26a-163">OUTPUTS</span></span>

### <span data-ttu-id="0d26a-164">Microsoft. Azure. Commands. model. modeli. Secret</span><span class="sxs-lookup"><span data-stu-id="0d26a-164">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>
<span data-ttu-id="0d26a-165">Zwraca wartość Microsoft. Azure. Commands. Stream. models. Secret, jeśli jest określony PassThru.</span><span class="sxs-lookup"><span data-stu-id="0d26a-165">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="0d26a-166">W przeciwnym razie zwraca wartość Nothing.</span><span class="sxs-lookup"><span data-stu-id="0d26a-166">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="0d26a-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d26a-167">NOTES</span></span>

## <span data-ttu-id="0d26a-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d26a-168">RELATED LINKS</span></span>

[<span data-ttu-id="0d26a-169">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0d26a-169">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="0d26a-170">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0d26a-170">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="0d26a-171">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0d26a-171">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
