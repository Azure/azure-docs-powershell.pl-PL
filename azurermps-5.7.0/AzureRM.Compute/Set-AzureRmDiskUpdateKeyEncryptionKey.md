---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateKeyEncryptionKey.md
ms.openlocfilehash: 3e1667cb7a8e8bd078e03d2ddafab559ca7b143f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548155"
---
# <span data-ttu-id="88934-101">Set-AzureRmDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="88934-101">Set-AzureRmDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="88934-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88934-102">SYNOPSIS</span></span>
<span data-ttu-id="88934-103">Ustawia właściwości klucza szyfrowania kluczy w obiekcie aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="88934-103">Sets the key encryption key properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88934-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88934-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateKeyEncryptionKey [-DiskUpdate] <DiskUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88934-105">Opis</span><span class="sxs-lookup"><span data-stu-id="88934-105">DESCRIPTION</span></span>
<span data-ttu-id="88934-106">Polecenie cmdlet **Set-AzureRmDiskUpdateKeyEncryptionKey** ustawia właściwości klucza szyfrowania kluczy w obiekcie aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="88934-106">The **Set-AzureRmDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="88934-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88934-107">EXAMPLES</span></span>

### <span data-ttu-id="88934-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="88934-108">Example 1</span></span>
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

<span data-ttu-id="88934-109">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji dysku o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="88934-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="88934-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="88934-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="88934-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="88934-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="88934-112">Ostatnie polecenie pobiera obiekt aktualizacji dysku i aktualizuje istniejący dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="88934-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="88934-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88934-113">PARAMETERS</span></span>

### <span data-ttu-id="88934-114">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="88934-114">-DiskUpdate</span></span>
<span data-ttu-id="88934-115">Określa obiekt aktualizacji dysku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="88934-115">Specifies a local disk update object.</span></span>

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

### <span data-ttu-id="88934-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="88934-116">-KeyUrl</span></span>
<span data-ttu-id="88934-117">Specifes kluczowy adres URL.</span><span class="sxs-lookup"><span data-stu-id="88934-117">Specifes the key Url.</span></span>

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

### <span data-ttu-id="88934-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="88934-118">-SourceVaultId</span></span>
<span data-ttu-id="88934-119">Określa identyfikator magazynu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="88934-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="88934-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88934-120">-Confirm</span></span>
<span data-ttu-id="88934-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88934-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88934-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88934-122">-WhatIf</span></span>
<span data-ttu-id="88934-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88934-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88934-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="88934-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88934-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88934-125">CommonParameters</span></span>
<span data-ttu-id="88934-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88934-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88934-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88934-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88934-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88934-128">INPUTS</span></span>

### <span data-ttu-id="88934-129">Microsoft. Azure. Management. COMPUTE. MODELES. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="88934-129">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="88934-130">System. String</span><span class="sxs-lookup"><span data-stu-id="88934-130">System.String</span></span>

## <span data-ttu-id="88934-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88934-131">OUTPUTS</span></span>

### <span data-ttu-id="88934-132">Microsoft. Azure. Management. COMPUTE. MODELES. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="88934-132">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="88934-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88934-133">NOTES</span></span>

## <span data-ttu-id="88934-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88934-134">RELATED LINKS</span></span>

