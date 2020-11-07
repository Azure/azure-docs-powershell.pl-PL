---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotupdatediskencryptionkey
schema: 2.0.0
ms.openlocfilehash: b777c13abbbac7de79af09d61f660fcbc68aaeb8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897654"
---
# <span data-ttu-id="3796c-101">Set-AzureRmSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3796c-101">Set-AzureRmSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="3796c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3796c-102">SYNOPSIS</span></span>
<span data-ttu-id="3796c-103">Ustawia właściwości klucza szyfrowania dysku w obiekcie aktualizacji migawki.</span><span class="sxs-lookup"><span data-stu-id="3796c-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3796c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3796c-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3796c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3796c-105">DESCRIPTION</span></span>
<span data-ttu-id="3796c-106">Polecenie cmdlet **Set-AzureRmSnapshotUpdateDiskEncryptionKey** ustawia właściwości klucza szyfrowania dysku w obiekcie aktualizacji migawki.</span><span class="sxs-lookup"><span data-stu-id="3796c-106">The **Set-AzureRmSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="3796c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3796c-107">EXAMPLES</span></span>

### <span data-ttu-id="3796c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3796c-108">Example 1</span></span>
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

<span data-ttu-id="3796c-109">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji migawki o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3796c-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="3796c-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="3796c-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="3796c-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania klucza dla obiektu aktualizacji migawki.</span><span class="sxs-lookup"><span data-stu-id="3796c-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="3796c-112">Ostatnie polecenie pobiera obiekt Snapshot Update i aktualizuje istniejącą migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="3796c-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3796c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3796c-113">PARAMETERS</span></span>

### <span data-ttu-id="3796c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3796c-114">-DefaultProfile</span></span>
<span data-ttu-id="3796c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3796c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3796c-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="3796c-116">-SecretUrl</span></span>
<span data-ttu-id="3796c-117">Specifes tajny adres URL.</span><span class="sxs-lookup"><span data-stu-id="3796c-117">Specifes the secret Url.</span></span>

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

### <span data-ttu-id="3796c-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="3796c-118">-SnapshotUpdate</span></span>
<span data-ttu-id="3796c-119">Określa obiekt aktualizacji migawki lokalnej.</span><span class="sxs-lookup"><span data-stu-id="3796c-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: PSSnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3796c-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="3796c-120">-SourceVaultId</span></span>
<span data-ttu-id="3796c-121">Określa identyfikator magazynu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="3796c-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="3796c-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3796c-122">-Confirm</span></span>
<span data-ttu-id="3796c-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3796c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3796c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3796c-124">-WhatIf</span></span>
<span data-ttu-id="3796c-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3796c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3796c-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3796c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3796c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3796c-127">CommonParameters</span></span>
<span data-ttu-id="3796c-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3796c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3796c-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3796c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3796c-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3796c-130">INPUTS</span></span>

### <span data-ttu-id="3796c-131">Microsoft. Azure. Management. COMPUTE. MODELES. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="3796c-131">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="3796c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3796c-132">System.String</span></span>

## <span data-ttu-id="3796c-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3796c-133">OUTPUTS</span></span>

### <span data-ttu-id="3796c-134">Microsoft. Azure. Management. COMPUTE. MODELES. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="3796c-134">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="3796c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3796c-135">NOTES</span></span>

## <span data-ttu-id="3796c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3796c-136">RELATED LINKS</span></span>

