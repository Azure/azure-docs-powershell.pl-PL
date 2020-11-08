---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
ms.openlocfilehash: 53a8ef8455fe95647b7b51473828f7684495aab7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064261"
---
# <span data-ttu-id="76135-101">Set-AzDiskDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="76135-101">Set-AzDiskDiskEncryptionKey</span></span>

## <span data-ttu-id="76135-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76135-102">SYNOPSIS</span></span>
<span data-ttu-id="76135-103">Ustawia właściwości klucza szyfrowania dysku na obiekcie dysk.</span><span class="sxs-lookup"><span data-stu-id="76135-103">Sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="76135-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76135-104">SYNTAX</span></span>

```
Set-AzDiskDiskEncryptionKey [-Disk] <PSDisk> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76135-105">Opis</span><span class="sxs-lookup"><span data-stu-id="76135-105">DESCRIPTION</span></span>
<span data-ttu-id="76135-106">Polecenie cmdlet **Set-AzDiskDiskEncryptionKey** ustawia właściwości klucza szyfrowania dysku na obiekcie dysk.</span><span class="sxs-lookup"><span data-stu-id="76135-106">The **Set-AzDiskDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="76135-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76135-107">EXAMPLES</span></span>

### <span data-ttu-id="76135-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="76135-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> $diskConfig.EncryptionSettingsCollection.EncryptionSettingsVersion = '1.1'; 
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="76135-109">Pierwsze polecenie tworzy lokalny pusty obiekt dyskowy o rozmiarze 5GB w Standard_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="76135-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="76135-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="76135-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="76135-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu dysk.</span><span class="sxs-lookup"><span data-stu-id="76135-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="76135-112">Ostatnie polecenie pobiera obiekt dysk i tworzy dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="76135-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="76135-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76135-113">PARAMETERS</span></span>

### <span data-ttu-id="76135-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76135-114">-DefaultProfile</span></span>
<span data-ttu-id="76135-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76135-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76135-116">— Dysk</span><span class="sxs-lookup"><span data-stu-id="76135-116">-Disk</span></span>
<span data-ttu-id="76135-117">Określa lokalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="76135-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="76135-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="76135-118">-SecretUrl</span></span>
<span data-ttu-id="76135-119">Określa tajny adres URL.</span><span class="sxs-lookup"><span data-stu-id="76135-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="76135-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="76135-120">-SourceVaultId</span></span>
<span data-ttu-id="76135-121">Określa identyfikator magazynu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="76135-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="76135-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76135-122">-Confirm</span></span>
<span data-ttu-id="76135-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76135-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76135-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76135-124">-WhatIf</span></span>
<span data-ttu-id="76135-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76135-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76135-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="76135-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76135-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76135-127">CommonParameters</span></span>
<span data-ttu-id="76135-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76135-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76135-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76135-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76135-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76135-130">INPUTS</span></span>

### <span data-ttu-id="76135-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="76135-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="76135-132">System. String</span><span class="sxs-lookup"><span data-stu-id="76135-132">System.String</span></span>

## <span data-ttu-id="76135-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76135-133">OUTPUTS</span></span>

### <span data-ttu-id="76135-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="76135-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="76135-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76135-135">NOTES</span></span>

## <span data-ttu-id="76135-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76135-136">RELATED LINKS</span></span>
