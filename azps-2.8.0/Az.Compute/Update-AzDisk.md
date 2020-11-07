---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
ms.openlocfilehash: 382bbb84a12834ea35bf42d2a1cce95afa5d93de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706128"
---
# <span data-ttu-id="14eab-101">Update-AzDisk</span><span class="sxs-lookup"><span data-stu-id="14eab-101">Update-AzDisk</span></span>

## <span data-ttu-id="14eab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="14eab-102">SYNOPSIS</span></span>
<span data-ttu-id="14eab-103">Aktualizuje dysk.</span><span class="sxs-lookup"><span data-stu-id="14eab-103">Updates a disk.</span></span>

## <span data-ttu-id="14eab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="14eab-104">SYNTAX</span></span>

### <span data-ttu-id="14eab-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="14eab-105">DefaultParameter (Default)</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14eab-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="14eab-106">FriendMethod</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14eab-107">Opis</span><span class="sxs-lookup"><span data-stu-id="14eab-107">DESCRIPTION</span></span>
<span data-ttu-id="14eab-108">Polecenie cmdlet **Update-AzDisk** aktualizuje dysk.</span><span class="sxs-lookup"><span data-stu-id="14eab-108">The **Update-AzDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="14eab-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="14eab-109">EXAMPLES</span></span>

### <span data-ttu-id="14eab-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="14eab-110">Example 1</span></span>
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

<span data-ttu-id="14eab-111">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji dysku o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="14eab-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="14eab-112">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="14eab-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="14eab-113">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="14eab-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="14eab-114">Ostatnie polecenie pobiera obiekt aktualizacji dysku i aktualizuje istniejący dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="14eab-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="14eab-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="14eab-115">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="14eab-116">To polecenie aktualizuje istniejący dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01" do rozmiaru dysku o rozmiarze 10 GB.</span><span class="sxs-lookup"><span data-stu-id="14eab-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="14eab-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="14eab-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="14eab-118">Te polecenia również aktualizują istniejący dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01" do rozmiaru dysku o rozmiarze 10 GB.</span><span class="sxs-lookup"><span data-stu-id="14eab-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="14eab-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="14eab-119">PARAMETERS</span></span>

### <span data-ttu-id="14eab-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14eab-120">-AsJob</span></span>
<span data-ttu-id="14eab-121">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="14eab-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="14eab-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14eab-122">-DefaultProfile</span></span>
<span data-ttu-id="14eab-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="14eab-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14eab-124">— Dysk</span><span class="sxs-lookup"><span data-stu-id="14eab-124">-Disk</span></span>
<span data-ttu-id="14eab-125">Określa lokalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="14eab-125">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14eab-126">-Diskname</span><span class="sxs-lookup"><span data-stu-id="14eab-126">-DiskName</span></span>
<span data-ttu-id="14eab-127">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="14eab-127">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14eab-128">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="14eab-128">-DiskUpdate</span></span>
<span data-ttu-id="14eab-129">Określa obiekt aktualizacji dysku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="14eab-129">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14eab-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14eab-130">-ResourceGroupName</span></span>
<span data-ttu-id="14eab-131">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="14eab-131">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14eab-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="14eab-132">-Confirm</span></span>
<span data-ttu-id="14eab-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14eab-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14eab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14eab-134">-WhatIf</span></span>
<span data-ttu-id="14eab-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14eab-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14eab-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="14eab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14eab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14eab-137">CommonParameters</span></span>
<span data-ttu-id="14eab-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14eab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14eab-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14eab-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14eab-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14eab-140">INPUTS</span></span>

### <span data-ttu-id="14eab-141">System. String</span><span class="sxs-lookup"><span data-stu-id="14eab-141">System.String</span></span>

### <span data-ttu-id="14eab-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="14eab-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="14eab-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="14eab-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="14eab-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="14eab-144">OUTPUTS</span></span>

### <span data-ttu-id="14eab-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="14eab-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="14eab-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="14eab-146">NOTES</span></span>

## <span data-ttu-id="14eab-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14eab-147">RELATED LINKS</span></span>