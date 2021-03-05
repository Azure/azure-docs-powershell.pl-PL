---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azsnapshotkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
ms.openlocfilehash: c03056d9e563d9c96df54e1d3e37d4c9f86dc572
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007018"
---
# <span data-ttu-id="4851b-101">Set-AzSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="4851b-101">Set-AzSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="4851b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4851b-102">SYNOPSIS</span></span>
<span data-ttu-id="4851b-103">Ustawia właściwości klucza szyfrowania klucza klucza w obiekcie migawki.</span><span class="sxs-lookup"><span data-stu-id="4851b-103">Sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="4851b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4851b-104">SYNTAX</span></span>

```
Set-AzSnapshotKeyEncryptionKey [-Snapshot] <PSSnapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4851b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4851b-105">DESCRIPTION</span></span>
<span data-ttu-id="4851b-106">Polecenie **cmdlet Set-AzSnapshotKeyEncryptionKey** ustawia właściwości klucza szyfrowania klucza w obiekcie migawki.</span><span class="sxs-lookup"><span data-stu-id="4851b-106">The **Set-AzSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="4851b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4851b-107">EXAMPLES</span></span>

### <span data-ttu-id="4851b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4851b-108">Example 1</span></span>
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

<span data-ttu-id="4851b-109">Pierwsze polecenie tworzy lokalny pusty obiekt migawki o rozmiarze 5 GB Standard_LRS typu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="4851b-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="4851b-110">Ustawia także typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="4851b-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="4851b-111">Drugie i trzecie polecenie ustawia ustawienia klucza szyfrowania dysku i klucza klucza szyfrowania obiektu migawki.</span><span class="sxs-lookup"><span data-stu-id="4851b-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="4851b-112">Ostatnie polecenie pobiera obiekt migawki i tworzy migawkę o nazwie "Migawka01" w grupie zasobów "Grupa Zasobów01".</span><span class="sxs-lookup"><span data-stu-id="4851b-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4851b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4851b-113">PARAMETERS</span></span>

### <span data-ttu-id="4851b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4851b-114">-DefaultProfile</span></span>
<span data-ttu-id="4851b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4851b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4851b-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="4851b-116">-KeyUrl</span></span>
<span data-ttu-id="4851b-117">Określa adres URL klucza.</span><span class="sxs-lookup"><span data-stu-id="4851b-117">Specifies the key Url.</span></span>

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

### <span data-ttu-id="4851b-118">— Migawka</span><span class="sxs-lookup"><span data-stu-id="4851b-118">-Snapshot</span></span>
<span data-ttu-id="4851b-119">Określa lokalny obiekt migawki.</span><span class="sxs-lookup"><span data-stu-id="4851b-119">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="4851b-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="4851b-120">-SourceVaultId</span></span>
<span data-ttu-id="4851b-121">Określa identyfikator magazynu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="4851b-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="4851b-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4851b-122">-Confirm</span></span>
<span data-ttu-id="4851b-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4851b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4851b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4851b-124">-WhatIf</span></span>
<span data-ttu-id="4851b-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4851b-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4851b-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4851b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4851b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4851b-127">CommonParameters</span></span>
<span data-ttu-id="4851b-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4851b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4851b-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4851b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4851b-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4851b-130">INPUTS</span></span>

### <span data-ttu-id="4851b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="4851b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="4851b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4851b-132">System.String</span></span>

## <span data-ttu-id="4851b-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4851b-133">OUTPUTS</span></span>

### <span data-ttu-id="4851b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="4851b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="4851b-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4851b-135">NOTES</span></span>

## <span data-ttu-id="4851b-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4851b-136">RELATED LINKS</span></span>
