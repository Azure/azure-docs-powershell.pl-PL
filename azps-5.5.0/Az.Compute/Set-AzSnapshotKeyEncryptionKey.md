---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
ms.openlocfilehash: c8a3ce4f0e21ac12f73fbcef6a4cb6c3b6b65bad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199187"
---
# <span data-ttu-id="458f6-101">Set-AzSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="458f6-101">Set-AzSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="458f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="458f6-102">SYNOPSIS</span></span>
<span data-ttu-id="458f6-103">Ustawia właściwości klucza szyfrowania dla obiektu migawki.</span><span class="sxs-lookup"><span data-stu-id="458f6-103">Sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="458f6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="458f6-104">SYNTAX</span></span>

```
Set-AzSnapshotKeyEncryptionKey [-Snapshot] <PSSnapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="458f6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="458f6-105">DESCRIPTION</span></span>
<span data-ttu-id="458f6-106">Polecenie **cmdlet Set-AzSnapshotKeyEncryptionKey** ustawia właściwości klucza szyfrowania klucza w obiekcie migawki.</span><span class="sxs-lookup"><span data-stu-id="458f6-106">The **Set-AzSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="458f6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="458f6-107">EXAMPLES</span></span>

### <span data-ttu-id="458f6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="458f6-108">Example 1</span></span>
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

<span data-ttu-id="458f6-109">Pierwsze polecenie tworzy lokalny pusty obiekt migawki o rozmiarze 5 GB Standard_LRS typu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="458f6-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="458f6-110">Ustawia także typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="458f6-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="458f6-111">Drugie i trzecie polecenia ustawiają ustawienia klucza szyfrowania dysku i klucza klucza szyfrowania obiektu migawki.</span><span class="sxs-lookup"><span data-stu-id="458f6-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="458f6-112">Ostatnie polecenie pobiera obiekt migawki i tworzy migawkę o nazwie "Migawka01" w grupie zasobów "Grupa Zasobów01".</span><span class="sxs-lookup"><span data-stu-id="458f6-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="458f6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="458f6-113">PARAMETERS</span></span>

### <span data-ttu-id="458f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="458f6-114">-DefaultProfile</span></span>
<span data-ttu-id="458f6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="458f6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="458f6-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="458f6-116">-KeyUrl</span></span>
<span data-ttu-id="458f6-117">Określa klucz adresu URL.</span><span class="sxs-lookup"><span data-stu-id="458f6-117">Specifies the key Url.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="458f6-118">— Migawka</span><span class="sxs-lookup"><span data-stu-id="458f6-118">-Snapshot</span></span>
<span data-ttu-id="458f6-119">Określa lokalny obiekt migawki.</span><span class="sxs-lookup"><span data-stu-id="458f6-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="458f6-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="458f6-120">-SourceVaultId</span></span>
<span data-ttu-id="458f6-121">Określa identyfikator magazynu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="458f6-121">Specifies the source vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="458f6-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="458f6-122">-Confirm</span></span>
<span data-ttu-id="458f6-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="458f6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="458f6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="458f6-124">-WhatIf</span></span>
<span data-ttu-id="458f6-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="458f6-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="458f6-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="458f6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="458f6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="458f6-127">CommonParameters</span></span>
<span data-ttu-id="458f6-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="458f6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="458f6-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="458f6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="458f6-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="458f6-130">INPUTS</span></span>

### <span data-ttu-id="458f6-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="458f6-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="458f6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="458f6-132">System.String</span></span>

## <span data-ttu-id="458f6-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="458f6-133">OUTPUTS</span></span>

### <span data-ttu-id="458f6-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="458f6-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="458f6-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="458f6-135">NOTES</span></span>

## <span data-ttu-id="458f6-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="458f6-136">RELATED LINKS</span></span>
