---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: c2c17fe3329170d65d61e5439e614717a8119f26
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893634"
---
# <span data-ttu-id="4d998-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="4d998-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="4d998-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d998-102">SYNOPSIS</span></span>
<span data-ttu-id="4d998-103">Umożliwia utworzenie obiektu aktualizacji migawki z możliwością konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="4d998-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="4d998-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d998-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d998-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d998-105">DESCRIPTION</span></span>
<span data-ttu-id="4d998-106">Polecenie cmdlet **New-AzSnapshotUpdateConfig** umożliwia utworzenie obiektu aktualizacji migawki z możliwością konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="4d998-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="4d998-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d998-107">EXAMPLES</span></span>

### <span data-ttu-id="4d998-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4d998-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="4d998-109">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji migawki o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="4d998-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="4d998-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="4d998-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="4d998-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania klucza dla obiektu aktualizacji migawki.</span><span class="sxs-lookup"><span data-stu-id="4d998-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="4d998-112">Ostatnie polecenie pobiera obiekt Snapshot Update i aktualizuje istniejącą migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="4d998-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="4d998-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4d998-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="4d998-114">To polecenie powoduje zaktualizowanie istniejącej migawki o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01" do rozmiaru dysku o rozmiarze 10 GB.</span><span class="sxs-lookup"><span data-stu-id="4d998-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="4d998-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d998-115">PARAMETERS</span></span>

### <span data-ttu-id="4d998-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d998-116">-DefaultProfile</span></span>
<span data-ttu-id="4d998-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d998-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d998-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="4d998-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="4d998-119">Określa obiekt klucza szyfrowania dysku na migawce.</span><span class="sxs-lookup"><span data-stu-id="4d998-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="4d998-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="4d998-120">-DiskSizeGB</span></span>
<span data-ttu-id="4d998-121">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="4d998-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="4d998-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="4d998-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="4d998-123">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="4d998-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="4d998-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="4d998-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="4d998-125">Określa klucz szyfrowania klucza na migawce.</span><span class="sxs-lookup"><span data-stu-id="4d998-125">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="4d998-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="4d998-126">-OsType</span></span>
<span data-ttu-id="4d998-127">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="4d998-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="4d998-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4d998-128">-SkuName</span></span>
<span data-ttu-id="4d998-129">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="4d998-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="4d998-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="4d998-130">-Tag</span></span>
<span data-ttu-id="4d998-131">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4d998-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4d998-132">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="4d998-132">For example:</span></span>

<span data-ttu-id="4d998-133">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="4d998-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4d998-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d998-134">-Confirm</span></span>
<span data-ttu-id="4d998-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d998-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d998-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d998-136">-WhatIf</span></span>
<span data-ttu-id="4d998-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d998-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d998-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4d998-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d998-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d998-139">CommonParameters</span></span>
<span data-ttu-id="4d998-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d998-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d998-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d998-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d998-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d998-142">INPUTS</span></span>

### <span data-ttu-id="4d998-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4d998-143">None</span></span>
<span data-ttu-id="4d998-144">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4d998-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4d998-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d998-145">OUTPUTS</span></span>

### <span data-ttu-id="4d998-146">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="4d998-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="4d998-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d998-147">NOTES</span></span>

## <span data-ttu-id="4d998-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d998-148">RELATED LINKS</span></span>

