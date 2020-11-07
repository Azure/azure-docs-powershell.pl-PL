---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmSnapshot.md
ms.openlocfilehash: fba3ec6f6ab78042a9e597a1c1074626afcddb25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717453"
---
# <span data-ttu-id="ae6b9-101">Update-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="ae6b9-101">Update-AzureRmSnapshot</span></span>

## <span data-ttu-id="ae6b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae6b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ae6b9-103">Umożliwia zaktualizowanie migawki.</span><span class="sxs-lookup"><span data-stu-id="ae6b9-103">Updates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae6b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae6b9-104">SYNTAX</span></span>

### <span data-ttu-id="ae6b9-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ae6b9-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-SnapshotUpdate] <PSSnapshotUpdate> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae6b9-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="ae6b9-106">FriendMethod</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae6b9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ae6b9-107">DESCRIPTION</span></span>
<span data-ttu-id="ae6b9-108">Polecenie cmdlet **Update-AzureRmSnapshot** umożliwia zaktualizowanie migawki.</span><span class="sxs-lookup"><span data-stu-id="ae6b9-108">The **Update-AzureRmSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="ae6b9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae6b9-109">EXAMPLES</span></span>

### <span data-ttu-id="ae6b9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae6b9-110">Example 1</span></span>
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

<span data-ttu-id="ae6b9-111">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji migawki o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ae6b9-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="ae6b9-112">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="ae6b9-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ae6b9-113">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania klucza dla obiektu aktualizacji migawki.</span><span class="sxs-lookup"><span data-stu-id="ae6b9-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="ae6b9-114">Ostatnie polecenie pobiera obiekt Snapshot Update i aktualizuje istniejącą migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ae6b9-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ae6b9-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ae6b9-115">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="ae6b9-116">To polecenie powoduje zaktualizowanie istniejącej migawki o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01" do rozmiaru dysku o rozmiarze 10 GB.</span><span class="sxs-lookup"><span data-stu-id="ae6b9-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="ae6b9-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="ae6b9-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="ae6b9-118">Te polecenia również aktualizują istniejącą migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01" do rozmiaru dysku o rozmiarze 10 GB.</span><span class="sxs-lookup"><span data-stu-id="ae6b9-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="ae6b9-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae6b9-119">PARAMETERS</span></span>

### <span data-ttu-id="ae6b9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae6b9-120">-AsJob</span></span>
<span data-ttu-id="ae6b9-121">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="ae6b9-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae6b9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae6b9-122">-DefaultProfile</span></span>
<span data-ttu-id="ae6b9-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae6b9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae6b9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae6b9-124">-ResourceGroupName</span></span>
<span data-ttu-id="ae6b9-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ae6b9-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6b9-126">-Migawka</span><span class="sxs-lookup"><span data-stu-id="ae6b9-126">-Snapshot</span></span>
<span data-ttu-id="ae6b9-127">Określa lokalny obiekt migawki.</span><span class="sxs-lookup"><span data-stu-id="ae6b9-127">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6b9-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="ae6b9-128">-SnapshotName</span></span>
<span data-ttu-id="ae6b9-129">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="ae6b9-129">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6b9-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="ae6b9-130">-SnapshotUpdate</span></span>
<span data-ttu-id="ae6b9-131">Określa obiekt aktualizacji migawki lokalnej.</span><span class="sxs-lookup"><span data-stu-id="ae6b9-131">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6b9-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae6b9-132">-Confirm</span></span>
<span data-ttu-id="ae6b9-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae6b9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae6b9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae6b9-134">-WhatIf</span></span>
<span data-ttu-id="ae6b9-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae6b9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae6b9-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ae6b9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae6b9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae6b9-137">CommonParameters</span></span>
<span data-ttu-id="ae6b9-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae6b9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae6b9-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae6b9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae6b9-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae6b9-140">INPUTS</span></span>

### <span data-ttu-id="ae6b9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ae6b9-141">System.String</span></span>

### <span data-ttu-id="ae6b9-142">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="ae6b9-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>
<span data-ttu-id="ae6b9-143">Parametry: SnapshotUpdate (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae6b9-143">Parameters: SnapshotUpdate (ByValue)</span></span>

### <span data-ttu-id="ae6b9-144">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="ae6b9-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>
<span data-ttu-id="ae6b9-145">Parametry: migawka (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae6b9-145">Parameters: Snapshot (ByValue)</span></span>

## <span data-ttu-id="ae6b9-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae6b9-146">OUTPUTS</span></span>

### <span data-ttu-id="ae6b9-147">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="ae6b9-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="ae6b9-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae6b9-148">NOTES</span></span>

## <span data-ttu-id="ae6b9-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae6b9-149">RELATED LINKS</span></span>