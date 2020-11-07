---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: 59f01cd55083c1dcda811c8362a27ce1af69e6e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869019"
---
# <span data-ttu-id="6938e-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="6938e-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="6938e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6938e-102">SYNOPSIS</span></span>
<span data-ttu-id="6938e-103">Umożliwia utworzenie obiektu aktualizacji migawki z możliwością konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="6938e-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="6938e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6938e-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6938e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6938e-105">DESCRIPTION</span></span>
<span data-ttu-id="6938e-106">Polecenie cmdlet **New-AzSnapshotUpdateConfig** umożliwia utworzenie obiektu aktualizacji migawki z możliwością konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="6938e-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="6938e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6938e-107">EXAMPLES</span></span>

### <span data-ttu-id="6938e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6938e-108">Example 1</span></span>
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

<span data-ttu-id="6938e-109">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji migawki o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6938e-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="6938e-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="6938e-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="6938e-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania klucza dla obiektu aktualizacji migawki.</span><span class="sxs-lookup"><span data-stu-id="6938e-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="6938e-112">Ostatnie polecenie pobiera obiekt Snapshot Update i aktualizuje istniejącą migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6938e-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="6938e-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6938e-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="6938e-114">To polecenie powoduje zaktualizowanie istniejącej migawki o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01" do rozmiaru dysku o rozmiarze 10 GB.</span><span class="sxs-lookup"><span data-stu-id="6938e-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="6938e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6938e-115">PARAMETERS</span></span>

### <span data-ttu-id="6938e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6938e-116">-DefaultProfile</span></span>
<span data-ttu-id="6938e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6938e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6938e-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6938e-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="6938e-119">Określa obiekt klucza szyfrowania dysku na migawce.</span><span class="sxs-lookup"><span data-stu-id="6938e-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="6938e-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="6938e-120">-DiskSizeGB</span></span>
<span data-ttu-id="6938e-121">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="6938e-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="6938e-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="6938e-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="6938e-123">Włącz ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="6938e-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="6938e-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6938e-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="6938e-125">Określa klucz szyfrowania klucza na migawce.</span><span class="sxs-lookup"><span data-stu-id="6938e-125">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="6938e-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="6938e-126">-OsType</span></span>
<span data-ttu-id="6938e-127">Określa typ OS.</span><span class="sxs-lookup"><span data-stu-id="6938e-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="6938e-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6938e-128">-SkuName</span></span>
<span data-ttu-id="6938e-129">Określa nazwę SKU konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6938e-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="6938e-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="6938e-130">-Tag</span></span>
<span data-ttu-id="6938e-131">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="6938e-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6938e-132">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="6938e-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6938e-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6938e-133">-Confirm</span></span>
<span data-ttu-id="6938e-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6938e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6938e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6938e-135">-WhatIf</span></span>
<span data-ttu-id="6938e-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6938e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6938e-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6938e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6938e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6938e-138">CommonParameters</span></span>
<span data-ttu-id="6938e-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6938e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6938e-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6938e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6938e-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6938e-141">INPUTS</span></span>

### <span data-ttu-id="6938e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6938e-142">System.String</span></span>

### <span data-ttu-id="6938e-143">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. OperatingSystemTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="6938e-143">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="6938e-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6938e-144">System.Int32</span></span>

### <span data-ttu-id="6938e-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6938e-145">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6938e-146">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6938e-146">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6938e-147">Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="6938e-147">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="6938e-148">Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="6938e-148">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="6938e-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6938e-149">OUTPUTS</span></span>

### <span data-ttu-id="6938e-150">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="6938e-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="6938e-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6938e-151">NOTES</span></span>

## <span data-ttu-id="6938e-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6938e-152">RELATED LINKS</span></span>
