---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: 235a315b56d7a99524d503bf992b770e31d01a25
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706205"
---
# <span data-ttu-id="3bdc3-101">Set-AzSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3bdc3-101">Set-AzSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="3bdc3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3bdc3-102">SYNOPSIS</span></span>
<span data-ttu-id="3bdc3-103">Ustawia właściwości klucza szyfrowania dysku w obiekcie aktualizacji migawki.</span><span class="sxs-lookup"><span data-stu-id="3bdc3-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="3bdc3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3bdc3-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3bdc3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3bdc3-105">DESCRIPTION</span></span>
<span data-ttu-id="3bdc3-106">Polecenie cmdlet **Set-AzSnapshotUpdateDiskEncryptionKey** ustawia właściwości klucza szyfrowania dysku w obiekcie aktualizacji migawki.</span><span class="sxs-lookup"><span data-stu-id="3bdc3-106">The **Set-AzSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="3bdc3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3bdc3-107">EXAMPLES</span></span>

### <span data-ttu-id="3bdc3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3bdc3-108">Example 1</span></span>
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

<span data-ttu-id="3bdc3-109">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji migawki o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3bdc3-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="3bdc3-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="3bdc3-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="3bdc3-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania klucza dla obiektu aktualizacji migawki.</span><span class="sxs-lookup"><span data-stu-id="3bdc3-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="3bdc3-112">Ostatnie polecenie pobiera obiekt Snapshot Update i aktualizuje istniejącą migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="3bdc3-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3bdc3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3bdc3-113">PARAMETERS</span></span>

### <span data-ttu-id="3bdc3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bdc3-114">-DefaultProfile</span></span>
<span data-ttu-id="3bdc3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3bdc3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bdc3-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="3bdc3-116">-SecretUrl</span></span>
<span data-ttu-id="3bdc3-117">Określa tajny adres URL.</span><span class="sxs-lookup"><span data-stu-id="3bdc3-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="3bdc3-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="3bdc3-118">-SnapshotUpdate</span></span>
<span data-ttu-id="3bdc3-119">Określa obiekt aktualizacji migawki lokalnej.</span><span class="sxs-lookup"><span data-stu-id="3bdc3-119">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="3bdc3-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="3bdc3-120">-SourceVaultId</span></span>
<span data-ttu-id="3bdc3-121">Określa identyfikator magazynu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="3bdc3-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="3bdc3-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3bdc3-122">-Confirm</span></span>
<span data-ttu-id="3bdc3-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bdc3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bdc3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bdc3-124">-WhatIf</span></span>
<span data-ttu-id="3bdc3-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bdc3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bdc3-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3bdc3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bdc3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bdc3-127">CommonParameters</span></span>
<span data-ttu-id="3bdc3-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bdc3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bdc3-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bdc3-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bdc3-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3bdc3-130">INPUTS</span></span>

### <span data-ttu-id="3bdc3-131">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="3bdc3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="3bdc3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3bdc3-132">System.String</span></span>

## <span data-ttu-id="3bdc3-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3bdc3-133">OUTPUTS</span></span>

### <span data-ttu-id="3bdc3-134">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="3bdc3-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="3bdc3-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3bdc3-135">NOTES</span></span>

## <span data-ttu-id="3bdc3-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3bdc3-136">RELATED LINKS</span></span>