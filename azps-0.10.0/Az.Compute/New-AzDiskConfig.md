---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 851687bdc00b25bd283433fbc00254380a8ef3a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893658"
---
# <span data-ttu-id="fcb5d-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="fcb5d-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="fcb5d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fcb5d-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb5d-103">Tworzy konfigurowalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="fcb5d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fcb5d-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>] [-Tag <Hashtable>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcb5d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fcb5d-105">DESCRIPTION</span></span>
<span data-ttu-id="fcb5d-106">Polecenie cmdlet **New-AzDiskConfig** tworzy konfigurowalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="fcb5d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fcb5d-107">EXAMPLES</span></span>

### <span data-ttu-id="fcb5d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fcb5d-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="fcb5d-109">Pierwsze polecenie tworzy lokalny pusty obiekt dyskowy o rozmiarze 5GB w Standard_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="fcb5d-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="fcb5d-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu dysk.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="fcb5d-112">Ostatnie polecenie pobiera obiekt dysk i tworzy dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="fcb5d-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="fcb5d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fcb5d-113">PARAMETERS</span></span>

### <span data-ttu-id="fcb5d-114">-Opcja</span><span class="sxs-lookup"><span data-stu-id="fcb5d-114">-CreateOption</span></span>
<span data-ttu-id="fcb5d-115">Określa, czy to polecenie cmdlet tworzy dysk na maszynie wirtualnej na platformie lub obrazie użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: DiskCreateOption
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcb5d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcb5d-116">-DefaultProfile</span></span>
<span data-ttu-id="fcb5d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcb5d-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="fcb5d-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="fcb5d-119">Określa obiekt klucza szyfrowania dysku na dysku.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-119">Specifies the disk encryption key object on a disk.</span></span>

```yaml
Type: KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcb5d-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="fcb5d-120">-DiskSizeGB</span></span>
<span data-ttu-id="fcb5d-121">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-121">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcb5d-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="fcb5d-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="fcb5d-123">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-123">Enable encryption settings.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcb5d-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="fcb5d-124">-ImageReference</span></span>
<span data-ttu-id="fcb5d-125">Określa odwołanie do obrazu na dysku.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-125">Specifies the image reference on a disk.</span></span>

```yaml
Type: ImageDiskReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcb5d-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="fcb5d-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="fcb5d-127">Określa klucz szyfrowania klucza na dysku.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-127">Specifies the Key encryption key on a disk.</span></span>

```yaml
Type: KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcb5d-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fcb5d-128">-Location</span></span>
<span data-ttu-id="fcb5d-129">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-129">Specifies a location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcb5d-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="fcb5d-130">-OsType</span></span>
<span data-ttu-id="fcb5d-131">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-131">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcb5d-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fcb5d-132">-SkuName</span></span>
<span data-ttu-id="fcb5d-133">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-133">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcb5d-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="fcb5d-134">-SourceResourceId</span></span>
<span data-ttu-id="fcb5d-135">Określa identyfikator zasobu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-135">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="fcb5d-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="fcb5d-136">-SourceUri</span></span>
<span data-ttu-id="fcb5d-137">Określa źródłowy identyfikator URI.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="fcb5d-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="fcb5d-138">-StorageAccountId</span></span>
<span data-ttu-id="fcb5d-139">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="fcb5d-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="fcb5d-140">-Tag</span></span>
<span data-ttu-id="fcb5d-141">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fcb5d-142">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="fcb5d-142">For example:</span></span>

<span data-ttu-id="fcb5d-143">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="fcb5d-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcb5d-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="fcb5d-144">-Zone</span></span>
<span data-ttu-id="fcb5d-145">Określa listę stref logicznych dla dysku.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-145">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="fcb5d-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fcb5d-146">-Confirm</span></span>
<span data-ttu-id="fcb5d-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcb5d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcb5d-148">-WhatIf</span></span>
<span data-ttu-id="fcb5d-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fcb5d-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcb5d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb5d-151">CommonParameters</span></span>
<span data-ttu-id="fcb5d-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcb5d-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcb5d-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb5d-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcb5d-154">INPUTS</span></span>

### <span data-ttu-id="fcb5d-155">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fcb5d-155">None</span></span>
<span data-ttu-id="fcb5d-156">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="fcb5d-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fcb5d-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fcb5d-157">OUTPUTS</span></span>

### <span data-ttu-id="fcb5d-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="fcb5d-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="fcb5d-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fcb5d-159">NOTES</span></span>

## <span data-ttu-id="fcb5d-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fcb5d-160">RELATED LINKS</span></span>

