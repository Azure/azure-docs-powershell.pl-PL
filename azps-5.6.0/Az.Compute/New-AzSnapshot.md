---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshot.md
ms.openlocfilehash: f73132550eceb092c8c869e7a555173c11d7d226
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980881"
---
# <span data-ttu-id="271b4-101">New-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="271b4-101">New-AzSnapshot</span></span>

## <span data-ttu-id="271b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="271b4-102">SYNOPSIS</span></span>
<span data-ttu-id="271b4-103">Tworzy migawkę.</span><span class="sxs-lookup"><span data-stu-id="271b4-103">Creates a snapshot.</span></span>

## <span data-ttu-id="271b4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="271b4-104">SYNTAX</span></span>

```
New-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="271b4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="271b4-105">DESCRIPTION</span></span>
<span data-ttu-id="271b4-106">Polecenie **cmdlet New-AzSnapshot** tworzy migawkę.</span><span class="sxs-lookup"><span data-stu-id="271b4-106">The **New-AzSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="271b4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="271b4-107">EXAMPLES</span></span>

### <span data-ttu-id="271b4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="271b4-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="271b4-109">Pierwsze polecenie tworzy lokalny pusty obiekt migawki o rozmiarze 5 GB Standard_LRS typu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="271b4-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="271b4-110">Ustawia także typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="271b4-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="271b4-111">Drugie i trzecie polecenie ustawia ustawienia klucza szyfrowania dysku i klucza klucza szyfrowania obiektu migawki.</span><span class="sxs-lookup"><span data-stu-id="271b4-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="271b4-112">Ostatnie polecenie pobiera obiekt migawki i tworzy migawkę o nazwie "Migawka01" w grupie zasobów "Grupa Zasobów01".</span><span class="sxs-lookup"><span data-stu-id="271b4-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="271b4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="271b4-113">PARAMETERS</span></span>

### <span data-ttu-id="271b4-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="271b4-114">-AsJob</span></span>
<span data-ttu-id="271b4-115">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="271b4-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="271b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="271b4-116">-DefaultProfile</span></span>
<span data-ttu-id="271b4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="271b4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="271b4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="271b4-118">-ResourceGroupName</span></span>
<span data-ttu-id="271b4-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="271b4-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="271b4-120">— Migawka</span><span class="sxs-lookup"><span data-stu-id="271b4-120">-Snapshot</span></span>
<span data-ttu-id="271b4-121">Określa lokalny obiekt migawki.</span><span class="sxs-lookup"><span data-stu-id="271b4-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="271b4-122">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="271b4-122">-SnapshotName</span></span>
<span data-ttu-id="271b4-123">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="271b4-123">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="271b4-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="271b4-124">-Confirm</span></span>
<span data-ttu-id="271b4-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="271b4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="271b4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="271b4-126">-WhatIf</span></span>
<span data-ttu-id="271b4-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="271b4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="271b4-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="271b4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="271b4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="271b4-129">CommonParameters</span></span>
<span data-ttu-id="271b4-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="271b4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="271b4-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="271b4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="271b4-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="271b4-132">INPUTS</span></span>

### <span data-ttu-id="271b4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="271b4-133">System.String</span></span>

### <span data-ttu-id="271b4-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="271b4-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="271b4-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="271b4-135">OUTPUTS</span></span>

### <span data-ttu-id="271b4-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="271b4-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="271b4-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="271b4-137">NOTES</span></span>

## <span data-ttu-id="271b4-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="271b4-138">RELATED LINKS</span></span>
