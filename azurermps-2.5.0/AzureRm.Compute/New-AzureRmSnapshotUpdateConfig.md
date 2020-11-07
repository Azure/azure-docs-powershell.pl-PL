---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotupdateconfig
schema: 2.0.0
ms.openlocfilehash: 033b183c763be266b29aadf47a57e760e2432452
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898985"
---
# <span data-ttu-id="a0a12-101">New-AzureRmSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="a0a12-101">New-AzureRmSnapshotUpdateConfig</span></span>

## <span data-ttu-id="a0a12-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0a12-102">SYNOPSIS</span></span>
<span data-ttu-id="a0a12-103">Umożliwia utworzenie obiektu aktualizacji migawki z możliwością konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="a0a12-103">Creates a configurable snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0a12-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0a12-104">SYNTAX</span></span>

```
New-AzureRmSnapshotUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0a12-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a0a12-105">DESCRIPTION</span></span>
<span data-ttu-id="a0a12-106">Polecenie cmdlet **New-AzureRmSnapshotUpdateConfig** umożliwia utworzenie obiektu aktualizacji migawki z możliwością konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="a0a12-106">The **New-AzureRmSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="a0a12-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0a12-107">EXAMPLES</span></span>

### <span data-ttu-id="a0a12-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a0a12-108">Example 1</span></span>
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

<span data-ttu-id="a0a12-109">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji migawki o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a0a12-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="a0a12-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="a0a12-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="a0a12-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania klucza dla obiektu aktualizacji migawki.</span><span class="sxs-lookup"><span data-stu-id="a0a12-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="a0a12-112">Ostatnie polecenie pobiera obiekt Snapshot Update i aktualizuje istniejącą migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="a0a12-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="a0a12-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a0a12-113">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="a0a12-114">To polecenie powoduje zaktualizowanie istniejącej migawki o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01" do rozmiaru dysku o rozmiarze 10 GB.</span><span class="sxs-lookup"><span data-stu-id="a0a12-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="a0a12-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0a12-115">PARAMETERS</span></span>

### <span data-ttu-id="a0a12-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0a12-116">-DefaultProfile</span></span>
<span data-ttu-id="a0a12-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0a12-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0a12-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a0a12-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="a0a12-119">Określa obiekt klucza szyfrowania dysku na migawce.</span><span class="sxs-lookup"><span data-stu-id="a0a12-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="a0a12-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="a0a12-120">-DiskSizeGB</span></span>
<span data-ttu-id="a0a12-121">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="a0a12-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="a0a12-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="a0a12-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="a0a12-123">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="a0a12-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="a0a12-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a0a12-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="a0a12-125">Określa klucz szyfrowania klucza na migawce.</span><span class="sxs-lookup"><span data-stu-id="a0a12-125">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="a0a12-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="a0a12-126">-OsType</span></span>
<span data-ttu-id="a0a12-127">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="a0a12-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="a0a12-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a0a12-128">-SkuName</span></span>
<span data-ttu-id="a0a12-129">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a0a12-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="a0a12-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0a12-130">-Tag</span></span>
<span data-ttu-id="a0a12-131">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a0a12-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a0a12-132">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="a0a12-132">For example:</span></span>

<span data-ttu-id="a0a12-133">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="a0a12-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a0a12-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a0a12-134">-Confirm</span></span>
<span data-ttu-id="a0a12-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0a12-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0a12-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0a12-136">-WhatIf</span></span>
<span data-ttu-id="a0a12-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0a12-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0a12-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a0a12-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0a12-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a12-139">CommonParameters</span></span>
<span data-ttu-id="a0a12-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0a12-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a12-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0a12-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a12-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0a12-142">INPUTS</span></span>

### <span data-ttu-id="a0a12-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a0a12-143">None</span></span>
<span data-ttu-id="a0a12-144">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a0a12-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a0a12-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0a12-145">OUTPUTS</span></span>

### <span data-ttu-id="a0a12-146">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="a0a12-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="a0a12-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0a12-147">NOTES</span></span>

## <span data-ttu-id="a0a12-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0a12-148">RELATED LINKS</span></span>

