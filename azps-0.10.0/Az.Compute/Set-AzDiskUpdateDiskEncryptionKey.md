---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 0f55058bc3419805bf7270e4d03c75db2208669e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893446"
---
# <span data-ttu-id="edb4a-101">Set-AzDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="edb4a-101">Set-AzDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="edb4a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="edb4a-102">SYNOPSIS</span></span>
<span data-ttu-id="edb4a-103">Ustawia właściwości klucza szyfrowania dysku w obiekcie aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="edb4a-103">Sets the disk encryption key properties on on a disk update object.</span></span>

## <span data-ttu-id="edb4a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="edb4a-104">SYNTAX</span></span>

```
Set-AzDiskUpdateDiskEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="edb4a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="edb4a-105">DESCRIPTION</span></span>
<span data-ttu-id="edb4a-106">Polecenie cmdlet **Set-AzDiskUpdateDiskEncryptionKey** ustawia właściwości klucza szyfrowania dysku w obiekcie aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="edb4a-106">The **Set-AzDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on on a disk update object.</span></span>

## <span data-ttu-id="edb4a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="edb4a-107">EXAMPLES</span></span>

### <span data-ttu-id="edb4a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="edb4a-108">Example 1</span></span>
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

<span data-ttu-id="edb4a-109">Pierwsze polecenie tworzy lokalny pusty obiekt aktualizacji dysku o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="edb4a-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="edb4a-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="edb4a-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="edb4a-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="edb4a-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="edb4a-112">Ostatnie polecenie pobiera obiekt aktualizacji dysku i aktualizuje istniejący dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="edb4a-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="edb4a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="edb4a-113">PARAMETERS</span></span>

### <span data-ttu-id="edb4a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb4a-114">-DefaultProfile</span></span>
<span data-ttu-id="edb4a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="edb4a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edb4a-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="edb4a-116">-DiskUpdate</span></span>
<span data-ttu-id="edb4a-117">Określa obiekt aktualizacji dysku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="edb4a-117">Specifies a local disk update object.</span></span>

```yaml
Type: PSDiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edb4a-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="edb4a-118">-SecretUrl</span></span>
<span data-ttu-id="edb4a-119">Określa tajny adres URL.</span><span class="sxs-lookup"><span data-stu-id="edb4a-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="edb4a-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="edb4a-120">-SourceVaultId</span></span>
<span data-ttu-id="edb4a-121">Określa identyfikator magazynu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="edb4a-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="edb4a-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="edb4a-122">-Confirm</span></span>
<span data-ttu-id="edb4a-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edb4a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edb4a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edb4a-124">-WhatIf</span></span>
<span data-ttu-id="edb4a-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edb4a-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="edb4a-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="edb4a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edb4a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb4a-127">CommonParameters</span></span>
<span data-ttu-id="edb4a-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edb4a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb4a-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edb4a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb4a-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="edb4a-130">INPUTS</span></span>

### <span data-ttu-id="edb4a-131">Microsoft. Azure. Management. COMPUTE. MODELES. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="edb4a-131">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="edb4a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="edb4a-132">System.String</span></span>

## <span data-ttu-id="edb4a-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="edb4a-133">OUTPUTS</span></span>

### <span data-ttu-id="edb4a-134">Microsoft. Azure. Management. COMPUTE. MODELES. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="edb4a-134">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="edb4a-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="edb4a-135">NOTES</span></span>

## <span data-ttu-id="edb4a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="edb4a-136">RELATED LINKS</span></span>

