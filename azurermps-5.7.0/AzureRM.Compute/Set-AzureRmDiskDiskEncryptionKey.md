---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskDiskEncryptionKey.md
ms.openlocfilehash: e16b57c4fd674897192714c44620c6913838fc7e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548175"
---
# <span data-ttu-id="9f4cf-101">Set-AzureRmDiskDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="9f4cf-101">Set-AzureRmDiskDiskEncryptionKey</span></span>

## <span data-ttu-id="9f4cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9f4cf-102">SYNOPSIS</span></span>
<span data-ttu-id="9f4cf-103">Ustawia właściwości klucza szyfrowania dysku na obiekcie dysk.</span><span class="sxs-lookup"><span data-stu-id="9f4cf-103">Sets the disk encryption key properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f4cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9f4cf-104">SYNTAX</span></span>

```
Set-AzureRmDiskDiskEncryptionKey [-Disk] <Disk> [[-SecretUrl] <String>] [[-SourceVaultId] <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f4cf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9f4cf-105">DESCRIPTION</span></span>
<span data-ttu-id="9f4cf-106">Polecenie cmdlet **Set-AzureRmDiskDiskEncryptionKey** ustawia właściwości klucza szyfrowania dysku na obiekcie dysk.</span><span class="sxs-lookup"><span data-stu-id="9f4cf-106">The **Set-AzureRmDiskDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="9f4cf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9f4cf-107">EXAMPLES</span></span>

### <span data-ttu-id="9f4cf-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9f4cf-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="9f4cf-109">Pierwsze polecenie tworzy lokalny pusty obiekt dyskowy o rozmiarze 5GB w Standard_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="9f4cf-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="9f4cf-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="9f4cf-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="9f4cf-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu dysk.</span><span class="sxs-lookup"><span data-stu-id="9f4cf-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="9f4cf-112">Ostatnie polecenie pobiera obiekt dysk i tworzy dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="9f4cf-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="9f4cf-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9f4cf-113">PARAMETERS</span></span>

### <span data-ttu-id="9f4cf-114">— Dysk</span><span class="sxs-lookup"><span data-stu-id="9f4cf-114">-Disk</span></span>
<span data-ttu-id="9f4cf-115">Określa lokalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="9f4cf-115">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f4cf-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="9f4cf-116">-SecretUrl</span></span>
<span data-ttu-id="9f4cf-117">Określa tajny adres URL.</span><span class="sxs-lookup"><span data-stu-id="9f4cf-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="9f4cf-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="9f4cf-118">-SourceVaultId</span></span>
<span data-ttu-id="9f4cf-119">Określa identyfikator magazynu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="9f4cf-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="9f4cf-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9f4cf-120">-Confirm</span></span>
<span data-ttu-id="9f4cf-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f4cf-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f4cf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f4cf-122">-WhatIf</span></span>
<span data-ttu-id="9f4cf-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f4cf-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f4cf-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9f4cf-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f4cf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f4cf-125">CommonParameters</span></span>
<span data-ttu-id="9f4cf-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f4cf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f4cf-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f4cf-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f4cf-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f4cf-128">INPUTS</span></span>

### <span data-ttu-id="9f4cf-129">Microsoft. Azure. Management. COMPUTE. modele. Disk</span><span class="sxs-lookup"><span data-stu-id="9f4cf-129">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="9f4cf-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9f4cf-130">System.String</span></span>

## <span data-ttu-id="9f4cf-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9f4cf-131">OUTPUTS</span></span>

### <span data-ttu-id="9f4cf-132">Microsoft. Azure. Management. COMPUTE. modele. Disk</span><span class="sxs-lookup"><span data-stu-id="9f4cf-132">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="9f4cf-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9f4cf-133">NOTES</span></span>

## <span data-ttu-id="9f4cf-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f4cf-134">RELATED LINKS</span></span>

