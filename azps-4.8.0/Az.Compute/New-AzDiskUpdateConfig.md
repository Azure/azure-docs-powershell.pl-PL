---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: 9c267a01629922408f25669ab93aa9a20a01b02b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063606"
---
# <span data-ttu-id="fa9d9-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="fa9d9-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="fa9d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa9d9-102">SYNOPSIS</span></span>
<span data-ttu-id="fa9d9-103">Tworzy obiekt konfigurowalnej aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="fa9d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa9d9-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa9d9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fa9d9-105">DESCRIPTION</span></span>
<span data-ttu-id="fa9d9-106">Polecenie cmdlet **New-AzDiskUpdateConfig** tworzy konfigurowalny obiekt aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="fa9d9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa9d9-107">EXAMPLES</span></span>

### <span data-ttu-id="fa9d9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fa9d9-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="fa9d9-109">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji dysku o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="fa9d9-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="fa9d9-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="fa9d9-112">Ostatnie polecenie pobiera obiekt aktualizacji dysku i aktualizuje istniejący dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="fa9d9-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="fa9d9-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fa9d9-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="fa9d9-114">To polecenie aktualizuje istniejący dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01" do rozmiaru dysku o rozmiarze 10 GB.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="fa9d9-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa9d9-115">PARAMETERS</span></span>

### <span data-ttu-id="fa9d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa9d9-116">-DefaultProfile</span></span>
<span data-ttu-id="fa9d9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa9d9-118">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="fa9d9-118">-DiskAccessId</span></span>
<span data-ttu-id="fa9d9-119">{{Fill DiskAccessId Description}}</span><span class="sxs-lookup"><span data-stu-id="fa9d9-119">{{ Fill DiskAccessId Description }}</span></span>

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

### <span data-ttu-id="fa9d9-120">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="fa9d9-120">-DiskEncryptionKey</span></span>
<span data-ttu-id="fa9d9-121">Określa obiekt klucza szyfrowania dysku na dysku.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-121">Specifies the disk encryption key object on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9d9-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="fa9d9-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="fa9d9-123">Określa identyfikator zasobu zestawu ustawień szyfrowania dysku, który ma być używany do włączania szyfrowania w stanie spoczynku.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-123">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="fa9d9-124">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="fa9d9-124">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="fa9d9-125">Liczba IOPS dozwolonych dla tego dysku; tylko dla dysków UltraSSD można tylko settablecie.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-125">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="fa9d9-126">Jedna operacja może przekazywać między 4K a 256k bajtami.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-126">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9d9-127">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="fa9d9-127">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="fa9d9-128">Przepustowość dozwolona dla tego dysku; tylko dla dysków UltraSSD można tylko settablecie.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-128">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="fa9d9-129">MB/s oznacza, że miliony bajtów na sekundę-MB używa notacji ISO o uprawnieniach 10.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-129">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9d9-130">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="fa9d9-130">-DiskSizeGB</span></span>
<span data-ttu-id="fa9d9-131">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-131">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9d9-132">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="fa9d9-132">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="fa9d9-133">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-133">Enable encryption settings.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9d9-134">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="fa9d9-134">-EncryptionType</span></span>
<span data-ttu-id="fa9d9-135">Typ klucza służący do szyfrowania danych dysku.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-135">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="fa9d9-136">Dostępne wartości: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="fa9d9-136">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="fa9d9-137">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="fa9d9-137">-KeyEncryptionKey</span></span>
<span data-ttu-id="fa9d9-138">Określa klucz szyfrowania klucza na dysku.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-138">Specifies the Key encryption key on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9d9-139">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fa9d9-139">-NetworkAccessPolicy</span></span>
<span data-ttu-id="fa9d9-140">{{Fill NetworkAccessPolicy Description}}</span><span class="sxs-lookup"><span data-stu-id="fa9d9-140">{{ Fill NetworkAccessPolicy Description }}</span></span>

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

### <span data-ttu-id="fa9d9-141">-OsType</span><span class="sxs-lookup"><span data-stu-id="fa9d9-141">-OsType</span></span>
<span data-ttu-id="fa9d9-142">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-142">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9d9-143">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fa9d9-143">-SkuName</span></span>
<span data-ttu-id="fa9d9-144">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-144">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="fa9d9-145">Dostępne wartości to Standard_LRS, Premium_LRS, StandardSSD_LRS i UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-145">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="fa9d9-146">UltraSSD_LRS można użyć tylko z wartością pustą dla parametru usługi.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-146">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9d9-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="fa9d9-147">-Tag</span></span>
<span data-ttu-id="fa9d9-148">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fa9d9-149">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="fa9d9-149">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9d9-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fa9d9-150">-Confirm</span></span>
<span data-ttu-id="fa9d9-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa9d9-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa9d9-152">-WhatIf</span></span>
<span data-ttu-id="fa9d9-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa9d9-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa9d9-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa9d9-155">CommonParameters</span></span>
<span data-ttu-id="fa9d9-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa9d9-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa9d9-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa9d9-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa9d9-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa9d9-158">INPUTS</span></span>

### <span data-ttu-id="fa9d9-159">System. String</span><span class="sxs-lookup"><span data-stu-id="fa9d9-159">System.String</span></span>

### <span data-ttu-id="fa9d9-160">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. OperatingSystemTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="fa9d9-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="fa9d9-161">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fa9d9-161">System.Int32</span></span>

### <span data-ttu-id="fa9d9-162">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fa9d9-162">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fa9d9-163">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fa9d9-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fa9d9-164">Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="fa9d9-164">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="fa9d9-165">Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="fa9d9-165">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="fa9d9-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa9d9-166">OUTPUTS</span></span>

### <span data-ttu-id="fa9d9-167">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="fa9d9-167">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="fa9d9-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa9d9-168">NOTES</span></span>

## <span data-ttu-id="fa9d9-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa9d9-169">RELATED LINKS</span></span>
