---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
ms.openlocfilehash: c8a3ce4f0e21ac12f73fbcef6a4cb6c3b6b65bad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370377"
---
# <span data-ttu-id="46c20-101">Set-AzSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="46c20-101">Set-AzSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="46c20-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46c20-102">SYNOPSIS</span></span>
<span data-ttu-id="46c20-103">Ustawia właściwości klucza szyfrowania kluczy w obiekcie Snapshot.</span><span class="sxs-lookup"><span data-stu-id="46c20-103">Sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="46c20-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46c20-104">SYNTAX</span></span>

```
Set-AzSnapshotKeyEncryptionKey [-Snapshot] <PSSnapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46c20-105">Opis</span><span class="sxs-lookup"><span data-stu-id="46c20-105">DESCRIPTION</span></span>
<span data-ttu-id="46c20-106">Polecenie cmdlet **Set-AzSnapshotKeyEncryptionKey** ustawia właściwości klucza szyfrowania kluczy w obiekcie Snapshot.</span><span class="sxs-lookup"><span data-stu-id="46c20-106">The **Set-AzSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="46c20-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46c20-107">EXAMPLES</span></span>

### <span data-ttu-id="46c20-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="46c20-108">Example 1</span></span>
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

<span data-ttu-id="46c20-109">Pierwsze polecenie tworzy lokalny pusty obiekt migawki o rozmiarze 5GB w Standard_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="46c20-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="46c20-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="46c20-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="46c20-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania klucza dla obiektu Snapshot.</span><span class="sxs-lookup"><span data-stu-id="46c20-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="46c20-112">Ostatnie polecenie przyjmuje obiekt Snapshot i utworzy migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="46c20-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="46c20-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46c20-113">PARAMETERS</span></span>

### <span data-ttu-id="46c20-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46c20-114">-DefaultProfile</span></span>
<span data-ttu-id="46c20-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="46c20-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46c20-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="46c20-116">-KeyUrl</span></span>
<span data-ttu-id="46c20-117">Określa kluczowy adres URL.</span><span class="sxs-lookup"><span data-stu-id="46c20-117">Specifies the key Url.</span></span>

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

### <span data-ttu-id="46c20-118">-Migawka</span><span class="sxs-lookup"><span data-stu-id="46c20-118">-Snapshot</span></span>
<span data-ttu-id="46c20-119">Określa lokalny obiekt migawki.</span><span class="sxs-lookup"><span data-stu-id="46c20-119">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="46c20-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="46c20-120">-SourceVaultId</span></span>
<span data-ttu-id="46c20-121">Określa identyfikator magazynu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="46c20-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="46c20-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="46c20-122">-Confirm</span></span>
<span data-ttu-id="46c20-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46c20-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46c20-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46c20-124">-WhatIf</span></span>
<span data-ttu-id="46c20-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46c20-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46c20-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="46c20-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46c20-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46c20-127">CommonParameters</span></span>
<span data-ttu-id="46c20-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46c20-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46c20-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46c20-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46c20-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46c20-130">INPUTS</span></span>

### <span data-ttu-id="46c20-131">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="46c20-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="46c20-132">System. String</span><span class="sxs-lookup"><span data-stu-id="46c20-132">System.String</span></span>

## <span data-ttu-id="46c20-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46c20-133">OUTPUTS</span></span>

### <span data-ttu-id="46c20-134">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="46c20-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="46c20-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46c20-135">NOTES</span></span>

## <span data-ttu-id="46c20-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46c20-136">RELATED LINKS</span></span>
