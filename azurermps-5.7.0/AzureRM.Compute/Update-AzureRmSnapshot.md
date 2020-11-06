---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
ms.openlocfilehash: ff70d3879685b0cdc9fcc42732a68e6b85bbd580
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525241"
---
# <span data-ttu-id="03bfd-101">Update-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="03bfd-101">Update-AzureRmSnapshot</span></span>

## <span data-ttu-id="03bfd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03bfd-102">SYNOPSIS</span></span>
<span data-ttu-id="03bfd-103">Umożliwia zaktualizowanie migawki.</span><span class="sxs-lookup"><span data-stu-id="03bfd-103">Updates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03bfd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03bfd-104">SYNTAX</span></span>

### <span data-ttu-id="03bfd-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="03bfd-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-SnapshotUpdate] <SnapshotUpdate> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03bfd-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="03bfd-106">FriendMethod</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <Snapshot> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03bfd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="03bfd-107">DESCRIPTION</span></span>
<span data-ttu-id="03bfd-108">Polecenie cmdlet **Update-AzureRmSnapshot** umożliwia zaktualizowanie migawki.</span><span class="sxs-lookup"><span data-stu-id="03bfd-108">The **Update-AzureRmSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="03bfd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03bfd-109">EXAMPLES</span></span>

### <span data-ttu-id="03bfd-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="03bfd-110">Example 1</span></span>
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

<span data-ttu-id="03bfd-111">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji migawki o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="03bfd-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="03bfd-112">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="03bfd-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="03bfd-113">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania klucza dla obiektu aktualizacji migawki.</span><span class="sxs-lookup"><span data-stu-id="03bfd-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="03bfd-114">Ostatnie polecenie pobiera obiekt Snapshot Update i aktualizuje istniejącą migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="03bfd-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="03bfd-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="03bfd-115">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="03bfd-116">To polecenie powoduje zaktualizowanie istniejącej migawki o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01" do rozmiaru dysku o rozmiarze 10 GB.</span><span class="sxs-lookup"><span data-stu-id="03bfd-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="03bfd-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="03bfd-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="03bfd-118">Te polecenia również aktualizują istniejącą migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01" do rozmiaru dysku o rozmiarze 10 GB.</span><span class="sxs-lookup"><span data-stu-id="03bfd-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="03bfd-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03bfd-119">PARAMETERS</span></span>

### <span data-ttu-id="03bfd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03bfd-120">-ResourceGroupName</span></span>
<span data-ttu-id="03bfd-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="03bfd-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="03bfd-122">-Migawka</span><span class="sxs-lookup"><span data-stu-id="03bfd-122">-Snapshot</span></span>
<span data-ttu-id="03bfd-123">Określa lokalny obiekt migawki.</span><span class="sxs-lookup"><span data-stu-id="03bfd-123">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03bfd-124">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="03bfd-124">-SnapshotName</span></span>
<span data-ttu-id="03bfd-125">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="03bfd-125">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="03bfd-126">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="03bfd-126">-SnapshotUpdate</span></span>
<span data-ttu-id="03bfd-127">Określa obiekt aktualizacji migawki lokalnej.</span><span class="sxs-lookup"><span data-stu-id="03bfd-127">Specifies a local snapshot update object.</span></span>

```yaml
Type: SnapshotUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03bfd-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03bfd-128">-Confirm</span></span>
<span data-ttu-id="03bfd-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03bfd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03bfd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03bfd-130">-WhatIf</span></span>
<span data-ttu-id="03bfd-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03bfd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03bfd-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="03bfd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03bfd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03bfd-133">CommonParameters</span></span>
<span data-ttu-id="03bfd-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03bfd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03bfd-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03bfd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03bfd-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03bfd-136">INPUTS</span></span>

### <span data-ttu-id="03bfd-137">System. String</span><span class="sxs-lookup"><span data-stu-id="03bfd-137">System.String</span></span>
<span data-ttu-id="03bfd-138">Microsoft. Azure. Management. COMPUTE. models. SnapshotUpdate Microsoft. Azure. Management. COMPUTE. models. snapshot</span><span class="sxs-lookup"><span data-stu-id="03bfd-138">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="03bfd-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03bfd-139">OUTPUTS</span></span>

### <span data-ttu-id="03bfd-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="03bfd-140">System.Object</span></span>

## <span data-ttu-id="03bfd-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03bfd-141">NOTES</span></span>

## <span data-ttu-id="03bfd-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03bfd-142">RELATED LINKS</span></span>

