---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotconfig
schema: 2.0.0
ms.openlocfilehash: a18eb8513e419d174efac9179cb65fe175d12dd1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899145"
---
# <span data-ttu-id="30bec-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="30bec-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="30bec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30bec-102">SYNOPSIS</span></span>
<span data-ttu-id="30bec-103">Umożliwia utworzenie obiektu migawki z możliwością konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="30bec-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30bec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30bec-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30bec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="30bec-105">DESCRIPTION</span></span>
<span data-ttu-id="30bec-106">Polecenie cmdlet **New-AzureRmSnapshotConfig** tworzy obiekt o konfigurowalnej migawce.</span><span class="sxs-lookup"><span data-stu-id="30bec-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="30bec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30bec-107">EXAMPLES</span></span>

### <span data-ttu-id="30bec-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="30bec-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="30bec-109">Pierwsze polecenie tworzy lokalny pusty obiekt migawki o rozmiarze 5GB w Standard_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="30bec-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="30bec-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="30bec-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="30bec-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania klucza dla obiektu Snapshot.</span><span class="sxs-lookup"><span data-stu-id="30bec-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="30bec-112">Ostatnie polecenie przyjmuje obiekt Snapshot i utworzy migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="30bec-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="30bec-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30bec-113">PARAMETERS</span></span>

### <span data-ttu-id="30bec-114">-Opcja</span><span class="sxs-lookup"><span data-stu-id="30bec-114">-CreateOption</span></span>
<span data-ttu-id="30bec-115">Określa, czy to polecenie cmdlet tworzy dysk na maszynie wirtualnej na platformie lub obrazie użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="30bec-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="30bec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30bec-116">-DefaultProfile</span></span>
<span data-ttu-id="30bec-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="30bec-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30bec-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="30bec-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="30bec-119">Określa obiekt klucza szyfrowania dysku na migawce.</span><span class="sxs-lookup"><span data-stu-id="30bec-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="30bec-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="30bec-120">-DiskSizeGB</span></span>
<span data-ttu-id="30bec-121">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="30bec-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="30bec-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="30bec-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="30bec-123">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="30bec-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="30bec-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="30bec-124">-ImageReference</span></span>
<span data-ttu-id="30bec-125">Określa odwołanie do obrazu w migawce.</span><span class="sxs-lookup"><span data-stu-id="30bec-125">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="30bec-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="30bec-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="30bec-127">Określa klucz szyfrowania klucza na migawce.</span><span class="sxs-lookup"><span data-stu-id="30bec-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="30bec-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="30bec-128">-Location</span></span>
<span data-ttu-id="30bec-129">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="30bec-129">Specifies a location.</span></span>

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

### <span data-ttu-id="30bec-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="30bec-130">-OsType</span></span>
<span data-ttu-id="30bec-131">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="30bec-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="30bec-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="30bec-132">-SkuName</span></span>
<span data-ttu-id="30bec-133">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="30bec-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="30bec-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="30bec-134">-SourceResourceId</span></span>
<span data-ttu-id="30bec-135">Określa identyfikator zasobu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="30bec-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="30bec-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="30bec-136">-SourceUri</span></span>
<span data-ttu-id="30bec-137">Określa źródłowy identyfikator URI.</span><span class="sxs-lookup"><span data-stu-id="30bec-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="30bec-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="30bec-138">-StorageAccountId</span></span>
<span data-ttu-id="30bec-139">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="30bec-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="30bec-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="30bec-140">-Tag</span></span>
<span data-ttu-id="30bec-141">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="30bec-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="30bec-142">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="30bec-142">For example:</span></span>

<span data-ttu-id="30bec-143">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="30bec-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="30bec-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="30bec-144">-Confirm</span></span>
<span data-ttu-id="30bec-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30bec-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30bec-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30bec-146">-WhatIf</span></span>
<span data-ttu-id="30bec-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30bec-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30bec-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="30bec-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30bec-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30bec-149">CommonParameters</span></span>
<span data-ttu-id="30bec-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30bec-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30bec-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30bec-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30bec-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30bec-152">INPUTS</span></span>

### <span data-ttu-id="30bec-153">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="30bec-153">None</span></span>
<span data-ttu-id="30bec-154">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="30bec-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30bec-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30bec-155">OUTPUTS</span></span>

### <span data-ttu-id="30bec-156">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="30bec-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="30bec-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30bec-157">NOTES</span></span>

## <span data-ttu-id="30bec-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30bec-158">RELATED LINKS</span></span>

