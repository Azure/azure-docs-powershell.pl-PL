---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
ms.openlocfilehash: 8ef1bccc711b96eb4b06c0b1234a426f9752208d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238719"
---
# <span data-ttu-id="de43b-101">Set-AzDiskDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="de43b-101">Set-AzDiskDiskEncryptionKey</span></span>

## <span data-ttu-id="de43b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de43b-102">SYNOPSIS</span></span>
<span data-ttu-id="de43b-103">Ustawia właściwości klucza szyfrowania dysku obiektu dysku.</span><span class="sxs-lookup"><span data-stu-id="de43b-103">Sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="de43b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="de43b-104">SYNTAX</span></span>

```
Set-AzDiskDiskEncryptionKey [-Disk] <PSDisk> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de43b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="de43b-105">DESCRIPTION</span></span>
<span data-ttu-id="de43b-106">Polecenie **cmdlet Set-Az ZSzyfrujSzmianieKey** ustawia właściwości klucza szyfrowania dysku na obiekcie dysku.</span><span class="sxs-lookup"><span data-stu-id="de43b-106">The **Set-AzDiskDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="de43b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="de43b-107">EXAMPLES</span></span>

### <span data-ttu-id="de43b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="de43b-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> $diskConfig.EncryptionSettingsCollection.EncryptionSettingsVersion = '1.1'; 
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="de43b-109">Pierwsze polecenie tworzy lokalny pusty obiekt dysku o rozmiarze 5 GB w Standard_LRS typu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="de43b-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="de43b-110">Ustawia także typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="de43b-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="de43b-111">Drugie i trzecie polecenia ustawiają ustawienia klucza szyfrowania dysku i klucza klucza szyfrowania obiektu dysku.</span><span class="sxs-lookup"><span data-stu-id="de43b-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="de43b-112">Ostatnie polecenie pobiera obiekt dysku i tworzy dysk o nazwie "Dysk01" w grupie zasobów "Grupa Zasobów01".</span><span class="sxs-lookup"><span data-stu-id="de43b-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="de43b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de43b-113">PARAMETERS</span></span>

### <span data-ttu-id="de43b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de43b-114">-DefaultProfile</span></span>
<span data-ttu-id="de43b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="de43b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de43b-116">— Dysk</span><span class="sxs-lookup"><span data-stu-id="de43b-116">-Disk</span></span>
<span data-ttu-id="de43b-117">Określa obiekt dysku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="de43b-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="de43b-118">- SecretUrl</span><span class="sxs-lookup"><span data-stu-id="de43b-118">-SecretUrl</span></span>
<span data-ttu-id="de43b-119">Określa tajny adres URL.</span><span class="sxs-lookup"><span data-stu-id="de43b-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="de43b-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="de43b-120">-SourceVaultId</span></span>
<span data-ttu-id="de43b-121">Określa identyfikator magazynu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="de43b-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="de43b-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="de43b-122">-Confirm</span></span>
<span data-ttu-id="de43b-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="de43b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de43b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de43b-124">-WhatIf</span></span>
<span data-ttu-id="de43b-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de43b-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de43b-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="de43b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de43b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de43b-127">CommonParameters</span></span>
<span data-ttu-id="de43b-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de43b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de43b-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de43b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de43b-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de43b-130">INPUTS</span></span>

### <span data-ttu-id="de43b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="de43b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="de43b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="de43b-132">System.String</span></span>

## <span data-ttu-id="de43b-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de43b-133">OUTPUTS</span></span>

### <span data-ttu-id="de43b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="de43b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="de43b-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="de43b-135">NOTES</span></span>

## <span data-ttu-id="de43b-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de43b-136">RELATED LINKS</span></span>
