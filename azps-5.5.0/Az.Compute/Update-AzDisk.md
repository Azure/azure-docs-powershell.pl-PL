---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
ms.openlocfilehash: 18f013643ad65bd4f7c70f3181e5950e10aa08ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177410"
---
# <span data-ttu-id="623d9-101">Update-AzDisk</span><span class="sxs-lookup"><span data-stu-id="623d9-101">Update-AzDisk</span></span>

## <span data-ttu-id="623d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="623d9-102">SYNOPSIS</span></span>
<span data-ttu-id="623d9-103">Aktualizuje dysk.</span><span class="sxs-lookup"><span data-stu-id="623d9-103">Updates a disk.</span></span>

## <span data-ttu-id="623d9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="623d9-104">SYNTAX</span></span>

### <span data-ttu-id="623d9-105">DefaultParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="623d9-105">DefaultParameter (Default)</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="623d9-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="623d9-106">FriendMethod</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="623d9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="623d9-107">DESCRIPTION</span></span>
<span data-ttu-id="623d9-108">Polecenie cmdlet **Update-AzCm** aktualizuje dysk.</span><span class="sxs-lookup"><span data-stu-id="623d9-108">The **Update-AzDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="623d9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="623d9-109">EXAMPLES</span></span>

### <span data-ttu-id="623d9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="623d9-110">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="623d9-111">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji dysku o rozmiarze 10 GB Premium_LRS typu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="623d9-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="623d9-112">Ustawia także typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="623d9-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="623d9-113">Drugie i trzecie polecenia ustawiają ustawienia klucza szyfrowania dysku i klucza klucza szyfrowania dla obiektu aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="623d9-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="623d9-114">Ostatnie polecenie pobiera obiekt aktualizacji dysku i aktualizuje istniejący dysk nazwą "Dysk01" w grupie zasobów "Grupa Zasobów01".</span><span class="sxs-lookup"><span data-stu-id="623d9-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="623d9-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="623d9-115">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="623d9-116">To polecenie aktualizuje istniejący dysk o nazwie "Dysk01" w grupie zasobów "Grupa Zasobów001" do rozmiaru dysku 10 GB.</span><span class="sxs-lookup"><span data-stu-id="623d9-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="623d9-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="623d9-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="623d9-118">Te polecenia aktualizują również istniejący dysk o nazwie "Dysk01" w grupie zasobów "Grupa Zasobów001" do rozmiaru dysku 10 GB.</span><span class="sxs-lookup"><span data-stu-id="623d9-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="623d9-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="623d9-119">PARAMETERS</span></span>

### <span data-ttu-id="623d9-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="623d9-120">-AsJob</span></span>
<span data-ttu-id="623d9-121">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="623d9-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="623d9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="623d9-122">-DefaultProfile</span></span>
<span data-ttu-id="623d9-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="623d9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="623d9-124">— Dysk</span><span class="sxs-lookup"><span data-stu-id="623d9-124">-Disk</span></span>
<span data-ttu-id="623d9-125">Określa obiekt dysku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="623d9-125">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="623d9-126">-DiskName</span><span class="sxs-lookup"><span data-stu-id="623d9-126">-DiskName</span></span>
<span data-ttu-id="623d9-127">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="623d9-127">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="623d9-128">- DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="623d9-128">-DiskUpdate</span></span>
<span data-ttu-id="623d9-129">Określa obiekt aktualizacji dysku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="623d9-129">Specifies a local disk update object.</span></span>

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

### <span data-ttu-id="623d9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="623d9-130">-ResourceGroupName</span></span>
<span data-ttu-id="623d9-131">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="623d9-131">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="623d9-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="623d9-132">-Confirm</span></span>
<span data-ttu-id="623d9-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="623d9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="623d9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="623d9-134">-WhatIf</span></span>
<span data-ttu-id="623d9-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="623d9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="623d9-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="623d9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="623d9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="623d9-137">CommonParameters</span></span>
<span data-ttu-id="623d9-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="623d9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="623d9-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="623d9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="623d9-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="623d9-140">INPUTS</span></span>

### <span data-ttu-id="623d9-141">System.String</span><span class="sxs-lookup"><span data-stu-id="623d9-141">System.String</span></span>

### <span data-ttu-id="623d9-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="623d9-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="623d9-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="623d9-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="623d9-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="623d9-144">OUTPUTS</span></span>

### <span data-ttu-id="623d9-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="623d9-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="623d9-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="623d9-146">NOTES</span></span>

## <span data-ttu-id="623d9-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="623d9-147">RELATED LINKS</span></span>
