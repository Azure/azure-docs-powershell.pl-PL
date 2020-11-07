---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
ms.openlocfilehash: 30a6ac1a3d74423302cc8b39e8b494e2f1ee2e22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716498"
---
# <span data-ttu-id="d6231-101">Update-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="d6231-101">Update-AzureRmDisk</span></span>

## <span data-ttu-id="d6231-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d6231-102">SYNOPSIS</span></span>
<span data-ttu-id="d6231-103">Aktualizuje dysk.</span><span class="sxs-lookup"><span data-stu-id="d6231-103">Updates a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6231-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d6231-104">SYNTAX</span></span>

### <span data-ttu-id="d6231-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d6231-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <DiskUpdate> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6231-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="d6231-106">FriendMethod</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <Disk> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6231-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d6231-107">DESCRIPTION</span></span>
<span data-ttu-id="d6231-108">Polecenie cmdlet **Update-AzureRmDisk** aktualizuje dysk.</span><span class="sxs-lookup"><span data-stu-id="d6231-108">The **Update-AzureRmDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="d6231-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d6231-109">EXAMPLES</span></span>

### <span data-ttu-id="d6231-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d6231-110">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="d6231-111">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji dysku o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d6231-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="d6231-112">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="d6231-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="d6231-113">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="d6231-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="d6231-114">Ostatnie polecenie pobiera obiekt aktualizacji dysku i aktualizuje istniejący dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="d6231-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="d6231-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d6231-115">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="d6231-116">To polecenie aktualizuje istniejący dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01" do rozmiaru dysku o rozmiarze 10 GB.</span><span class="sxs-lookup"><span data-stu-id="d6231-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="d6231-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d6231-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="d6231-118">Te polecenia również aktualizują istniejący dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01" do rozmiaru dysku o rozmiarze 10 GB.</span><span class="sxs-lookup"><span data-stu-id="d6231-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="d6231-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6231-119">PARAMETERS</span></span>

### <span data-ttu-id="d6231-120">— Dysk</span><span class="sxs-lookup"><span data-stu-id="d6231-120">-Disk</span></span>
<span data-ttu-id="d6231-121">Określa lokalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="d6231-121">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6231-122">-Diskname</span><span class="sxs-lookup"><span data-stu-id="d6231-122">-DiskName</span></span>
<span data-ttu-id="d6231-123">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="d6231-123">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6231-124">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="d6231-124">-DiskUpdate</span></span>
<span data-ttu-id="d6231-125">Określa obiekt aktualizacji dysku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="d6231-125">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6231-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6231-126">-ResourceGroupName</span></span>
<span data-ttu-id="d6231-127">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d6231-127">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6231-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d6231-128">-Confirm</span></span>
<span data-ttu-id="d6231-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6231-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6231-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6231-130">-WhatIf</span></span>
<span data-ttu-id="d6231-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6231-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6231-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d6231-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6231-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6231-133">CommonParameters</span></span>
<span data-ttu-id="d6231-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6231-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6231-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6231-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6231-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6231-136">INPUTS</span></span>

### <span data-ttu-id="d6231-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d6231-137">System.String</span></span>
<span data-ttu-id="d6231-138">Microsoft. Azure. Management. COMPUTE. models. DiskUpdate Microsoft. Azure. Management. COMPUTE. models. Disk</span><span class="sxs-lookup"><span data-stu-id="d6231-138">Microsoft.Azure.Management.Compute.Models.DiskUpdate Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="d6231-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d6231-139">OUTPUTS</span></span>

### <span data-ttu-id="d6231-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="d6231-140">System.Object</span></span>

## <span data-ttu-id="d6231-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d6231-141">NOTES</span></span>

## <span data-ttu-id="d6231-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6231-142">RELATED LINKS</span></span>

