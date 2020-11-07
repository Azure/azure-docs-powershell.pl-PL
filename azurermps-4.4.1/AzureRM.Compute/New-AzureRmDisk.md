---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
ms.openlocfilehash: 4392c1ccf19474e1a8f73c5bccca2c09f53cbea8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719531"
---
# <span data-ttu-id="c2078-101">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="c2078-101">New-AzureRmDisk</span></span>

## <span data-ttu-id="c2078-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2078-102">SYNOPSIS</span></span>
<span data-ttu-id="c2078-103">Tworzy dysk zarządzany.</span><span class="sxs-lookup"><span data-stu-id="c2078-103">Creates a managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2078-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2078-104">SYNTAX</span></span>

```
New-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2078-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c2078-105">DESCRIPTION</span></span>
<span data-ttu-id="c2078-106">Polecenie cmdlet **New-AzureRmDisk** tworzy dysk zarządzany.</span><span class="sxs-lookup"><span data-stu-id="c2078-106">The **New-AzureRmDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="c2078-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2078-107">EXAMPLES</span></span>

### <span data-ttu-id="c2078-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c2078-108">Example 1</span></span>
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

<span data-ttu-id="c2078-109">Pierwsze polecenie tworzy lokalny pusty obiekt dyskowy o rozmiarze 5GB w Standard_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c2078-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="c2078-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="c2078-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="c2078-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu dysk.</span><span class="sxs-lookup"><span data-stu-id="c2078-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="c2078-112">Ostatnie polecenie pobiera obiekt dysk i tworzy dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c2078-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c2078-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2078-113">PARAMETERS</span></span>

### <span data-ttu-id="c2078-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2078-114">-DefaultProfile</span></span>
<span data-ttu-id="c2078-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2078-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2078-116">— Dysk</span><span class="sxs-lookup"><span data-stu-id="c2078-116">-Disk</span></span>
<span data-ttu-id="c2078-117">Określa lokalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="c2078-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2078-118">-Diskname</span><span class="sxs-lookup"><span data-stu-id="c2078-118">-DiskName</span></span>
<span data-ttu-id="c2078-119">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="c2078-119">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2078-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2078-120">-ResourceGroupName</span></span>
<span data-ttu-id="c2078-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2078-121">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2078-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2078-122">-Confirm</span></span>
<span data-ttu-id="c2078-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2078-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2078-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2078-124">-WhatIf</span></span>
<span data-ttu-id="c2078-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2078-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2078-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c2078-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2078-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2078-127">CommonParameters</span></span>
<span data-ttu-id="c2078-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2078-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2078-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2078-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2078-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2078-130">INPUTS</span></span>

### <span data-ttu-id="c2078-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c2078-131">System.String</span></span>
<span data-ttu-id="c2078-132">Microsoft. Azure. Management. COMPUTE. modele. Disk</span><span class="sxs-lookup"><span data-stu-id="c2078-132">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="c2078-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2078-133">OUTPUTS</span></span>

### <span data-ttu-id="c2078-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="c2078-134">System.Object</span></span>

## <span data-ttu-id="c2078-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2078-135">NOTES</span></span>

## <span data-ttu-id="c2078-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2078-136">RELATED LINKS</span></span>

