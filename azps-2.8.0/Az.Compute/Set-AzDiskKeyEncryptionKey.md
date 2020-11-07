---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
ms.openlocfilehash: c207ccf33b42cf0e7cf1fdb319d0ba17d040d3d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706219"
---
# <span data-ttu-id="180c2-101">Set-AzDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="180c2-101">Set-AzDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="180c2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="180c2-102">SYNOPSIS</span></span>
<span data-ttu-id="180c2-103">Ustawia właściwości klucza szyfrowania kluczy na obiekcie dysk.</span><span class="sxs-lookup"><span data-stu-id="180c2-103">Sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="180c2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="180c2-104">SYNTAX</span></span>

```
Set-AzDiskKeyEncryptionKey [-Disk] <PSDisk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="180c2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="180c2-105">DESCRIPTION</span></span>
<span data-ttu-id="180c2-106">Polecenie cmdlet **Set-AzDiskKeyEncryptionKey** ustawia właściwości klucza szyfrowania kluczy na obiekcie dysk.</span><span class="sxs-lookup"><span data-stu-id="180c2-106">The **Set-AzDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="180c2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="180c2-107">EXAMPLES</span></span>

### <span data-ttu-id="180c2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="180c2-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="180c2-109">Pierwsze polecenie tworzy lokalny pusty obiekt dyskowy o rozmiarze 5GB w Standard_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="180c2-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="180c2-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="180c2-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="180c2-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu dysk.</span><span class="sxs-lookup"><span data-stu-id="180c2-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="180c2-112">Ostatnie polecenie pobiera obiekt dysk i tworzy dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="180c2-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="180c2-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="180c2-113">PARAMETERS</span></span>

### <span data-ttu-id="180c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="180c2-114">-DefaultProfile</span></span>
<span data-ttu-id="180c2-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="180c2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="180c2-116">— Dysk</span><span class="sxs-lookup"><span data-stu-id="180c2-116">-Disk</span></span>
<span data-ttu-id="180c2-117">Określa lokalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="180c2-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="180c2-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="180c2-118">-KeyUrl</span></span>
<span data-ttu-id="180c2-119">Określa kluczowy adres URL.</span><span class="sxs-lookup"><span data-stu-id="180c2-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="180c2-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="180c2-120">-SourceVaultId</span></span>
<span data-ttu-id="180c2-121">Określa identyfikator magazynu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="180c2-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="180c2-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="180c2-122">-Confirm</span></span>
<span data-ttu-id="180c2-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="180c2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="180c2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="180c2-124">-WhatIf</span></span>
<span data-ttu-id="180c2-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="180c2-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="180c2-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="180c2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="180c2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="180c2-127">CommonParameters</span></span>
<span data-ttu-id="180c2-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="180c2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="180c2-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="180c2-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="180c2-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="180c2-130">INPUTS</span></span>

### <span data-ttu-id="180c2-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="180c2-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="180c2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="180c2-132">System.String</span></span>

## <span data-ttu-id="180c2-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="180c2-133">OUTPUTS</span></span>

### <span data-ttu-id="180c2-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="180c2-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="180c2-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="180c2-135">NOTES</span></span>

## <span data-ttu-id="180c2-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="180c2-136">RELATED LINKS</span></span>