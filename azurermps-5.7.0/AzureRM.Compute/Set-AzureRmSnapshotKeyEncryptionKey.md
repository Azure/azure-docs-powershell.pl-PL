---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotKeyEncryptionKey.md
ms.openlocfilehash: 9c6debcae0aa83dd08374c7e390e3a42c4e5233a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525286"
---
# <span data-ttu-id="36192-101">Set-AzureRmSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="36192-101">Set-AzureRmSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="36192-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36192-102">SYNOPSIS</span></span>
<span data-ttu-id="36192-103">Ustawia właściwości klucza szyfrowania kluczy w obiekcie Snapshot.</span><span class="sxs-lookup"><span data-stu-id="36192-103">Sets the key encryption key properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36192-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36192-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotKeyEncryptionKey [-Snapshot] <Snapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36192-105">Opis</span><span class="sxs-lookup"><span data-stu-id="36192-105">DESCRIPTION</span></span>
<span data-ttu-id="36192-106">Polecenie cmdlet **Set-AzureRmSnapshotKeyEncryptionKey** ustawia właściwości klucza szyfrowania kluczy w obiekcie Snapshot.</span><span class="sxs-lookup"><span data-stu-id="36192-106">The **Set-AzureRmSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="36192-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36192-107">EXAMPLES</span></span>

### <span data-ttu-id="36192-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="36192-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="36192-109">Pierwsze polecenie tworzy lokalny pusty obiekt migawki o rozmiarze 5GB w Standard_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="36192-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="36192-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="36192-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="36192-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania klucza dla obiektu Snapshot.</span><span class="sxs-lookup"><span data-stu-id="36192-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="36192-112">Ostatnie polecenie przyjmuje obiekt Snapshot i utworzy migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="36192-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="36192-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36192-113">PARAMETERS</span></span>

### <span data-ttu-id="36192-114">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="36192-114">-KeyUrl</span></span>
<span data-ttu-id="36192-115">Specifes kluczowy adres URL.</span><span class="sxs-lookup"><span data-stu-id="36192-115">Specifes the key Url.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36192-116">-Migawka</span><span class="sxs-lookup"><span data-stu-id="36192-116">-Snapshot</span></span>
<span data-ttu-id="36192-117">Określa lokalny obiekt migawki.</span><span class="sxs-lookup"><span data-stu-id="36192-117">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36192-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="36192-118">-SourceVaultId</span></span>
<span data-ttu-id="36192-119">Określa identyfikator magazynu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="36192-119">Specifies the source vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36192-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36192-120">-Confirm</span></span>
<span data-ttu-id="36192-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36192-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36192-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36192-122">-WhatIf</span></span>
<span data-ttu-id="36192-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36192-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36192-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="36192-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36192-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36192-125">CommonParameters</span></span>
<span data-ttu-id="36192-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36192-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36192-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36192-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36192-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36192-128">INPUTS</span></span>

### <span data-ttu-id="36192-129">Microsoft. Azure. Management. COMPUTE. models. snapshot</span><span class="sxs-lookup"><span data-stu-id="36192-129">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="36192-130">System. String</span><span class="sxs-lookup"><span data-stu-id="36192-130">System.String</span></span>

## <span data-ttu-id="36192-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36192-131">OUTPUTS</span></span>

### <span data-ttu-id="36192-132">Microsoft. Azure. Management. COMPUTE. models. snapshot</span><span class="sxs-lookup"><span data-stu-id="36192-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="36192-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36192-133">NOTES</span></span>

## <span data-ttu-id="36192-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36192-134">RELATED LINKS</span></span>

