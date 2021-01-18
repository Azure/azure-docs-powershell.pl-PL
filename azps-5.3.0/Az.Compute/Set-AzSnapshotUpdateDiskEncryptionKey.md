---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: b43593650e3eaed25e59526a067c4c569d19d28a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503971"
---
# <span data-ttu-id="dfb11-101">Set-AzSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="dfb11-101">Set-AzSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="dfb11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dfb11-102">SYNOPSIS</span></span>
<span data-ttu-id="dfb11-103">Ustawia właściwości klucza szyfrowania dysku w obiekcie aktualizacji migawki.</span><span class="sxs-lookup"><span data-stu-id="dfb11-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="dfb11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dfb11-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dfb11-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dfb11-105">DESCRIPTION</span></span>
<span data-ttu-id="dfb11-106">Polecenie cmdlet **Set-AzSnapshotUpdateDiskEncryptionKey** ustawia właściwości klucza szyfrowania dysku w obiekcie aktualizacji migawki.</span><span class="sxs-lookup"><span data-stu-id="dfb11-106">The **Set-AzSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="dfb11-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dfb11-107">EXAMPLES</span></span>

### <span data-ttu-id="dfb11-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dfb11-108">Example 1</span></span>
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

<span data-ttu-id="dfb11-109">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji migawki o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="dfb11-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="dfb11-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="dfb11-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="dfb11-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania klucza dla obiektu aktualizacji migawki.</span><span class="sxs-lookup"><span data-stu-id="dfb11-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="dfb11-112">Ostatnie polecenie pobiera obiekt Snapshot Update i aktualizuje istniejącą migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="dfb11-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="dfb11-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dfb11-113">PARAMETERS</span></span>

### <span data-ttu-id="dfb11-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfb11-114">-DefaultProfile</span></span>
<span data-ttu-id="dfb11-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dfb11-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfb11-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="dfb11-116">-SecretUrl</span></span>
<span data-ttu-id="dfb11-117">Określa tajny adres URL.</span><span class="sxs-lookup"><span data-stu-id="dfb11-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="dfb11-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="dfb11-118">-SnapshotUpdate</span></span>
<span data-ttu-id="dfb11-119">Określa obiekt aktualizacji migawki lokalnej.</span><span class="sxs-lookup"><span data-stu-id="dfb11-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfb11-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="dfb11-120">-SourceVaultId</span></span>
<span data-ttu-id="dfb11-121">Określa identyfikator magazynu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="dfb11-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="dfb11-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dfb11-122">-Confirm</span></span>
<span data-ttu-id="dfb11-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfb11-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfb11-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfb11-124">-WhatIf</span></span>
<span data-ttu-id="dfb11-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfb11-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfb11-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dfb11-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfb11-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfb11-127">CommonParameters</span></span>
<span data-ttu-id="dfb11-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfb11-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfb11-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfb11-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfb11-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dfb11-130">INPUTS</span></span>

### <span data-ttu-id="dfb11-131">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="dfb11-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="dfb11-132">System. String</span><span class="sxs-lookup"><span data-stu-id="dfb11-132">System.String</span></span>

## <span data-ttu-id="dfb11-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dfb11-133">OUTPUTS</span></span>

### <span data-ttu-id="dfb11-134">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="dfb11-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="dfb11-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dfb11-135">NOTES</span></span>

## <span data-ttu-id="dfb11-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dfb11-136">RELATED LINKS</span></span>
