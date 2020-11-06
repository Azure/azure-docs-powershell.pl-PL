---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
ms.openlocfilehash: 97bfd93babc75b09f87e53f62c60cd4fb08ea599
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546867"
---
# <span data-ttu-id="20b28-101">New-AzureRmSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="20b28-101">New-AzureRmSnapshotUpdateConfig</span></span>

## <span data-ttu-id="20b28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20b28-102">SYNOPSIS</span></span>
<span data-ttu-id="20b28-103">Umożliwia utworzenie obiektu aktualizacji migawki z możliwością konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="20b28-103">Creates a configurable snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20b28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20b28-104">SYNTAX</span></span>

```
New-AzureRmSnapshotUpdateConfig [-SkuName <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20b28-105">Opis</span><span class="sxs-lookup"><span data-stu-id="20b28-105">DESCRIPTION</span></span>
<span data-ttu-id="20b28-106">Polecenie cmdlet **New-AzureRmSnapshotUpdateConfig** umożliwia utworzenie obiektu aktualizacji migawki z możliwością konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="20b28-106">The **New-AzureRmSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="20b28-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20b28-107">EXAMPLES</span></span>

### <span data-ttu-id="20b28-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="20b28-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="20b28-109">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji migawki o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="20b28-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="20b28-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="20b28-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="20b28-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania klucza dla obiektu aktualizacji migawki.</span><span class="sxs-lookup"><span data-stu-id="20b28-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="20b28-112">Ostatnie polecenie pobiera obiekt Snapshot Update i aktualizuje istniejącą migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="20b28-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="20b28-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="20b28-113">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="20b28-114">To polecenie powoduje zaktualizowanie istniejącej migawki o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01" do rozmiaru dysku o rozmiarze 10 GB.</span><span class="sxs-lookup"><span data-stu-id="20b28-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="20b28-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20b28-115">PARAMETERS</span></span>

### <span data-ttu-id="20b28-116">-Opcja</span><span class="sxs-lookup"><span data-stu-id="20b28-116">-CreateOption</span></span>
<span data-ttu-id="20b28-117">Określa, czy to polecenie cmdlet tworzy migawkę na maszynie wirtualnej na platformie lub obrazie użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="20b28-117">Specifies whether this cmdlet creates a snapshot in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: DiskCreateOption
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy, Restore

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20b28-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="20b28-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="20b28-119">Określa obiekt klucza szyfrowania dysku na migawce.</span><span class="sxs-lookup"><span data-stu-id="20b28-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="20b28-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="20b28-120">-DiskSizeGB</span></span>
<span data-ttu-id="20b28-121">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="20b28-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="20b28-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="20b28-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="20b28-123">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="20b28-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="20b28-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="20b28-124">-ImageReference</span></span>
<span data-ttu-id="20b28-125">Określa odwołanie do obrazu w migawce.</span><span class="sxs-lookup"><span data-stu-id="20b28-125">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="20b28-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="20b28-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="20b28-127">Określa klucz szyfrowania klucza na migawce.</span><span class="sxs-lookup"><span data-stu-id="20b28-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="20b28-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="20b28-128">-OsType</span></span>
<span data-ttu-id="20b28-129">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="20b28-129">Specifies the OS type.</span></span>

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

### <span data-ttu-id="20b28-130">-SkuName</span><span class="sxs-lookup"><span data-stu-id="20b28-130">-SkuName</span></span>
<span data-ttu-id="20b28-131">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="20b28-131">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20b28-132">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="20b28-132">-SourceResourceId</span></span>
<span data-ttu-id="20b28-133">Określa identyfikator zasobu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="20b28-133">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="20b28-134">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="20b28-134">-SourceUri</span></span>
<span data-ttu-id="20b28-135">Określa źródłowy identyfikator URI.</span><span class="sxs-lookup"><span data-stu-id="20b28-135">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="20b28-136">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="20b28-136">-StorageAccountId</span></span>
<span data-ttu-id="20b28-137">Określa identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="20b28-137">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="20b28-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="20b28-138">-Tag</span></span>
<span data-ttu-id="20b28-139">Określa, że zasoby i grupy zasobów mogą być znakowane za pomocą zestawu par nazwa-wartość.</span><span class="sxs-lookup"><span data-stu-id="20b28-139">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20b28-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="20b28-140">-Confirm</span></span>
<span data-ttu-id="20b28-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20b28-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20b28-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20b28-142">-WhatIf</span></span>
<span data-ttu-id="20b28-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20b28-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20b28-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="20b28-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20b28-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b28-145">CommonParameters</span></span>
<span data-ttu-id="20b28-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20b28-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b28-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20b28-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b28-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20b28-148">INPUTS</span></span>

### <span data-ttu-id="20b28-149">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. StorageAccountTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="20b28-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="20b28-150">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] system. Collections. Hashtable. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] Microsoft. Azure. Management. COMPUTE. model.</span><span class="sxs-lookup"><span data-stu-id="20b28-150">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="20b28-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20b28-151">OUTPUTS</span></span>

### <span data-ttu-id="20b28-152">Microsoft. Azure. Management. COMPUTE. MODELES. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="20b28-152">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="20b28-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20b28-153">NOTES</span></span>

## <span data-ttu-id="20b28-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20b28-154">RELATED LINKS</span></span>

