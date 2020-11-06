---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 4d44bc014a3d38a89e6c9a6a6d755aa9353c052e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548163"
---
# <span data-ttu-id="5c259-101">Set-AzureRmDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5c259-101">Set-AzureRmDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="5c259-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c259-102">SYNOPSIS</span></span>
<span data-ttu-id="5c259-103">Ustawia właściwości klucza szyfrowania dysku w obiekcie aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="5c259-103">Sets the disk encryption key properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c259-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c259-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateDiskEncryptionKey [-DiskUpdate] <DiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c259-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5c259-105">DESCRIPTION</span></span>
<span data-ttu-id="5c259-106">Polecenie cmdlet **Set-AzureRmDiskUpdateDiskEncryptionKey** ustawia właściwości klucza szyfrowania dysku w obiekcie aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="5c259-106">The **Set-AzureRmDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="5c259-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c259-107">EXAMPLES</span></span>

### <span data-ttu-id="5c259-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5c259-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="5c259-109">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji dysku o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="5c259-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="5c259-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="5c259-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="5c259-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="5c259-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="5c259-112">Ostatnie polecenie pobiera obiekt aktualizacji dysku i aktualizuje istniejący dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="5c259-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="5c259-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c259-113">PARAMETERS</span></span>

### <span data-ttu-id="5c259-114">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="5c259-114">-DiskUpdate</span></span>
<span data-ttu-id="5c259-115">Określa obiekt aktualizacji dysku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="5c259-115">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c259-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="5c259-116">-SecretUrl</span></span>
<span data-ttu-id="5c259-117">Określa tajny adres URL.</span><span class="sxs-lookup"><span data-stu-id="5c259-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="5c259-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="5c259-118">-SourceVaultId</span></span>
<span data-ttu-id="5c259-119">Określa identyfikator magazynu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="5c259-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="5c259-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5c259-120">-Confirm</span></span>
<span data-ttu-id="5c259-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c259-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c259-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c259-122">-WhatIf</span></span>
<span data-ttu-id="5c259-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c259-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c259-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5c259-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c259-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c259-125">CommonParameters</span></span>
<span data-ttu-id="5c259-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c259-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c259-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c259-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c259-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c259-128">INPUTS</span></span>

### <span data-ttu-id="5c259-129">Microsoft. Azure. Management. COMPUTE. MODELES. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="5c259-129">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="5c259-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5c259-130">System.String</span></span>

## <span data-ttu-id="5c259-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c259-131">OUTPUTS</span></span>

### <span data-ttu-id="5c259-132">Microsoft. Azure. Management. COMPUTE. MODELES. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="5c259-132">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="5c259-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c259-133">NOTES</span></span>

## <span data-ttu-id="5c259-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c259-134">RELATED LINKS</span></span>

