---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshot.md
ms.openlocfilehash: 6810aa032e6d822087c9951d23cb07c3850c67a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893642"
---
# <span data-ttu-id="3a490-101">New-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="3a490-101">New-AzSnapshot</span></span>

## <span data-ttu-id="3a490-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a490-102">SYNOPSIS</span></span>
<span data-ttu-id="3a490-103">Umożliwia utworzenie migawki.</span><span class="sxs-lookup"><span data-stu-id="3a490-103">Creates a snapshot.</span></span>

## <span data-ttu-id="3a490-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a490-104">SYNTAX</span></span>

```
New-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a490-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a490-105">DESCRIPTION</span></span>
<span data-ttu-id="3a490-106">Polecenie cmdlet **New-AzSnapshot** umożliwia utworzenie migawki.</span><span class="sxs-lookup"><span data-stu-id="3a490-106">The **New-AzSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="3a490-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a490-107">EXAMPLES</span></span>

### <span data-ttu-id="3a490-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3a490-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="3a490-109">Pierwsze polecenie tworzy lokalny pusty obiekt migawki o rozmiarze 5GB w Standard_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3a490-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="3a490-110">Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="3a490-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="3a490-111">Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania klucza dla obiektu Snapshot.</span><span class="sxs-lookup"><span data-stu-id="3a490-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="3a490-112">Ostatnie polecenie przyjmuje obiekt Snapshot i utworzy migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="3a490-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3a490-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a490-113">PARAMETERS</span></span>

### <span data-ttu-id="3a490-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a490-114">-AsJob</span></span>
<span data-ttu-id="3a490-115">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="3a490-115">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a490-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a490-116">-DefaultProfile</span></span>
<span data-ttu-id="3a490-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a490-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a490-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a490-118">-ResourceGroupName</span></span>
<span data-ttu-id="3a490-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a490-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3a490-120">-Migawka</span><span class="sxs-lookup"><span data-stu-id="3a490-120">-Snapshot</span></span>
<span data-ttu-id="3a490-121">Określa lokalny obiekt migawki.</span><span class="sxs-lookup"><span data-stu-id="3a490-121">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a490-122">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="3a490-122">-SnapshotName</span></span>
<span data-ttu-id="3a490-123">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="3a490-123">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="3a490-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a490-124">-Confirm</span></span>
<span data-ttu-id="3a490-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a490-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a490-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a490-126">-WhatIf</span></span>
<span data-ttu-id="3a490-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a490-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a490-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3a490-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a490-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a490-129">CommonParameters</span></span>
<span data-ttu-id="3a490-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a490-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a490-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a490-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a490-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a490-132">INPUTS</span></span>

### <span data-ttu-id="3a490-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3a490-133">System.String</span></span>
<span data-ttu-id="3a490-134">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="3a490-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="3a490-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a490-135">OUTPUTS</span></span>

### <span data-ttu-id="3a490-136">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="3a490-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="3a490-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="3a490-137">System.Object</span></span>

## <span data-ttu-id="3a490-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a490-138">NOTES</span></span>

## <span data-ttu-id="3a490-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a490-139">RELATED LINKS</span></span>

