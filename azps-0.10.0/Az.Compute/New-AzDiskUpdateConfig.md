---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: c346cebbc14a25b2afa8047deea3578ab8330d87
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893653"
---
# <span data-ttu-id="a682d-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="a682d-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="a682d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a682d-102">SYNOPSIS</span></span>
<span data-ttu-id="a682d-103">Tworzy obiekt konfigurowalnej aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="a682d-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="a682d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a682d-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a682d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a682d-105">DESCRIPTION</span></span>
<span data-ttu-id="a682d-106">Polecenie cmdlet **New-AzDiskUpdateConfig** tworzy konfigurowalny obiekt aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="a682d-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="a682d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a682d-107">EXAMPLES</span></span>

### <span data-ttu-id="a682d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a682d-108">Example 1</span></span>
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

<span data-ttu-id="a682d-109">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji dysku o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a682d-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="a682d-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="a682d-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="a682d-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="a682d-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="a682d-112">Ostatnie polecenie pobiera obiekt aktualizacji dysku i aktualizuje istniejący dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="a682d-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="a682d-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a682d-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="a682d-114">To polecenie aktualizuje istniejący dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01" do rozmiaru dysku o rozmiarze 10 GB.</span><span class="sxs-lookup"><span data-stu-id="a682d-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="a682d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a682d-115">PARAMETERS</span></span>

### <span data-ttu-id="a682d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a682d-116">-DefaultProfile</span></span>
<span data-ttu-id="a682d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a682d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a682d-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a682d-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="a682d-119">Określa obiekt klucza szyfrowania dysku na dysku.</span><span class="sxs-lookup"><span data-stu-id="a682d-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="a682d-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="a682d-120">-DiskSizeGB</span></span>
<span data-ttu-id="a682d-121">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="a682d-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="a682d-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="a682d-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="a682d-123">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="a682d-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="a682d-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a682d-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="a682d-125">Określa klucz szyfrowania klucza na dysku.</span><span class="sxs-lookup"><span data-stu-id="a682d-125">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="a682d-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="a682d-126">-OsType</span></span>
<span data-ttu-id="a682d-127">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="a682d-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="a682d-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a682d-128">-SkuName</span></span>
<span data-ttu-id="a682d-129">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a682d-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="a682d-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="a682d-130">-Tag</span></span>
<span data-ttu-id="a682d-131">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a682d-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a682d-132">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="a682d-132">For example:</span></span>

<span data-ttu-id="a682d-133">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="a682d-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a682d-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a682d-134">-Confirm</span></span>
<span data-ttu-id="a682d-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a682d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a682d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a682d-136">-WhatIf</span></span>
<span data-ttu-id="a682d-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a682d-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a682d-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a682d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a682d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a682d-139">CommonParameters</span></span>
<span data-ttu-id="a682d-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a682d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a682d-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a682d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a682d-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a682d-142">INPUTS</span></span>

### <span data-ttu-id="a682d-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a682d-143">None</span></span>
<span data-ttu-id="a682d-144">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a682d-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a682d-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a682d-145">OUTPUTS</span></span>

### <span data-ttu-id="a682d-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="a682d-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="a682d-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a682d-147">NOTES</span></span>

## <span data-ttu-id="a682d-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a682d-148">RELATED LINKS</span></span>

