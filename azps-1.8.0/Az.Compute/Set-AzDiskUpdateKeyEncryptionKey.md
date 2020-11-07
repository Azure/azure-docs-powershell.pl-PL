---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
ms.openlocfilehash: d9e92c9669ac63ce4e727a92e001406e3bb4c5f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710216"
---
# <span data-ttu-id="c35e4-101">Set-AzDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="c35e4-101">Set-AzDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="c35e4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c35e4-102">SYNOPSIS</span></span>
<span data-ttu-id="c35e4-103">Ustawia właściwości klucza szyfrowania kluczy w obiekcie aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="c35e4-103">Sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="c35e4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c35e4-104">SYNTAX</span></span>

```
Set-AzDiskUpdateKeyEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c35e4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c35e4-105">DESCRIPTION</span></span>
<span data-ttu-id="c35e4-106">Polecenie cmdlet **Set-AzDiskUpdateKeyEncryptionKey** ustawia właściwości klucza szyfrowania kluczy w obiekcie aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="c35e4-106">The **Set-AzDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="c35e4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c35e4-107">EXAMPLES</span></span>

### <span data-ttu-id="c35e4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c35e4-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="c35e4-109">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji dysku o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c35e4-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="c35e4-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="c35e4-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="c35e4-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="c35e4-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="c35e4-112">Ostatnie polecenie pobiera obiekt aktualizacji dysku i aktualizuje istniejący dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c35e4-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c35e4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c35e4-113">PARAMETERS</span></span>

### <span data-ttu-id="c35e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c35e4-114">-DefaultProfile</span></span>
<span data-ttu-id="c35e4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c35e4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c35e4-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="c35e4-116">-DiskUpdate</span></span>
<span data-ttu-id="c35e4-117">Określa obiekt aktualizacji dysku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="c35e4-117">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c35e4-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="c35e4-118">-KeyUrl</span></span>
<span data-ttu-id="c35e4-119">Specifes kluczowy adres URL.</span><span class="sxs-lookup"><span data-stu-id="c35e4-119">Specifes the key Url.</span></span>

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

### <span data-ttu-id="c35e4-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="c35e4-120">-SourceVaultId</span></span>
<span data-ttu-id="c35e4-121">Określa identyfikator magazynu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="c35e4-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="c35e4-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c35e4-122">-Confirm</span></span>
<span data-ttu-id="c35e4-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c35e4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c35e4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c35e4-124">-WhatIf</span></span>
<span data-ttu-id="c35e4-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c35e4-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c35e4-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c35e4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c35e4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c35e4-127">CommonParameters</span></span>
<span data-ttu-id="c35e4-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c35e4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c35e4-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c35e4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c35e4-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c35e4-130">INPUTS</span></span>

### <span data-ttu-id="c35e4-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="c35e4-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="c35e4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c35e4-132">System.String</span></span>

## <span data-ttu-id="c35e4-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c35e4-133">OUTPUTS</span></span>

### <span data-ttu-id="c35e4-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="c35e4-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="c35e4-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c35e4-135">NOTES</span></span>

## <span data-ttu-id="c35e4-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c35e4-136">RELATED LINKS</span></span>
