---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
ms.openlocfilehash: 04106c91e99372b985c0a10ac12a7944fdcb4e41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718941"
---
# <span data-ttu-id="737d2-101">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="737d2-101">New-AzureRmDisk</span></span>

## <span data-ttu-id="737d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="737d2-102">SYNOPSIS</span></span>
<span data-ttu-id="737d2-103">Tworzy dysk zarządzany.</span><span class="sxs-lookup"><span data-stu-id="737d2-103">Creates a managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="737d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="737d2-104">SYNTAX</span></span>

```
New-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <Disk> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="737d2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="737d2-105">DESCRIPTION</span></span>
<span data-ttu-id="737d2-106">Polecenie cmdlet **New-AzureRmDisk** tworzy dysk zarządzany.</span><span class="sxs-lookup"><span data-stu-id="737d2-106">The **New-AzureRmDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="737d2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="737d2-107">EXAMPLES</span></span>

### <span data-ttu-id="737d2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="737d2-108">Example 1</span></span>
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

<span data-ttu-id="737d2-109">Pierwsze polecenie tworzy lokalny pusty obiekt dyskowy o rozmiarze 5GB w Standard_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="737d2-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="737d2-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="737d2-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="737d2-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu dysk.</span><span class="sxs-lookup"><span data-stu-id="737d2-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="737d2-112">Ostatnie polecenie pobiera obiekt dysk i tworzy dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="737d2-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="737d2-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="737d2-113">PARAMETERS</span></span>

### <span data-ttu-id="737d2-114">— Dysk</span><span class="sxs-lookup"><span data-stu-id="737d2-114">-Disk</span></span>
<span data-ttu-id="737d2-115">Określa lokalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="737d2-115">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="737d2-116">-Diskname</span><span class="sxs-lookup"><span data-stu-id="737d2-116">-DiskName</span></span>
<span data-ttu-id="737d2-117">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="737d2-117">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737d2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="737d2-118">-ResourceGroupName</span></span>
<span data-ttu-id="737d2-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="737d2-119">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737d2-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="737d2-120">-Confirm</span></span>
<span data-ttu-id="737d2-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="737d2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="737d2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="737d2-122">-WhatIf</span></span>
<span data-ttu-id="737d2-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="737d2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="737d2-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="737d2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="737d2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737d2-125">CommonParameters</span></span>
<span data-ttu-id="737d2-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="737d2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737d2-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="737d2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737d2-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="737d2-128">INPUTS</span></span>

### <span data-ttu-id="737d2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="737d2-129">System.String</span></span>
<span data-ttu-id="737d2-130">Microsoft. Azure. Management. COMPUTE. modele. Disk</span><span class="sxs-lookup"><span data-stu-id="737d2-130">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="737d2-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="737d2-131">OUTPUTS</span></span>

### <span data-ttu-id="737d2-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="737d2-132">System.Object</span></span>

## <span data-ttu-id="737d2-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="737d2-133">NOTES</span></span>

## <span data-ttu-id="737d2-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="737d2-134">RELATED LINKS</span></span>

