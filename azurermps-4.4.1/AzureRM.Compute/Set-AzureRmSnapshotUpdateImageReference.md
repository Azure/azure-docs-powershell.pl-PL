---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
ms.openlocfilehash: bbaa82500e06f426dd5b7496849507b91a599da6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716744"
---
# <span data-ttu-id="42606-101">Set-AzureRmSnapshotUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="42606-101">Set-AzureRmSnapshotUpdateImageReference</span></span>

## <span data-ttu-id="42606-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42606-102">SYNOPSIS</span></span>
<span data-ttu-id="42606-103">Ustawia właściwości odwołania obrazu w obiekcie aktualizacji migawki.</span><span class="sxs-lookup"><span data-stu-id="42606-103">Sets the image reference properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42606-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42606-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateImageReference [-SnapshotUpdate] <PSSnapshotUpdate> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42606-105">Opis</span><span class="sxs-lookup"><span data-stu-id="42606-105">DESCRIPTION</span></span>
<span data-ttu-id="42606-106">Polecenie cmdlet **Set-AzureRmSnapshotUpdateImageReference** ustawia właściwości odwołania obrazu w obiekcie aktualizacji migawki.</span><span class="sxs-lookup"><span data-stu-id="42606-106">The **Set-AzureRmSnapshotUpdateImageReference** cmdlet sets the image reference properties on a snapshot update object.</span></span>

## <span data-ttu-id="42606-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42606-107">EXAMPLES</span></span>

### <span data-ttu-id="42606-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="42606-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateImageReference -Snapshot $snapshotupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="42606-109">Pierwsze polecenie tworzy obiekt Local Snapshot Update ze zdjęciem o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="42606-109">The first command creates a local snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="42606-110">Ustawia również typ systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="42606-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="42606-111">Drugie polecenie ustawia identyfikator obrazu i numer jednostki logicznej 0 dla obiektu aktualizacji migawki.</span><span class="sxs-lookup"><span data-stu-id="42606-111">The second command sets the image id and the logical unit number 0 for the snapshot update object.</span></span>
<span data-ttu-id="42606-112">Ostatnie polecenie pobiera obiekt Snapshot Update i aktualizuje istniejącą migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="42606-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="42606-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42606-113">PARAMETERS</span></span>

### <span data-ttu-id="42606-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42606-114">-DefaultProfile</span></span>
<span data-ttu-id="42606-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="42606-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42606-116">-ID</span><span class="sxs-lookup"><span data-stu-id="42606-116">-Id</span></span>
<span data-ttu-id="42606-117">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="42606-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="42606-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="42606-118">-Lun</span></span>
<span data-ttu-id="42606-119">Określa numer jednostki logicznej (LUN).</span><span class="sxs-lookup"><span data-stu-id="42606-119">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42606-120">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="42606-120">-SnapshotUpdate</span></span>
<span data-ttu-id="42606-121">Określa obiekt aktualizacji migawki lokalnej.</span><span class="sxs-lookup"><span data-stu-id="42606-121">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42606-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42606-122">-Confirm</span></span>
<span data-ttu-id="42606-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42606-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42606-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42606-124">-WhatIf</span></span>
<span data-ttu-id="42606-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42606-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42606-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="42606-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42606-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42606-127">CommonParameters</span></span>
<span data-ttu-id="42606-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42606-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42606-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42606-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42606-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42606-130">INPUTS</span></span>

### <span data-ttu-id="42606-131">Microsoft. Azure. Management. COMPUTE. MODELES. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="42606-131">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="42606-132">System. String. Nullable. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="42606-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="42606-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42606-133">OUTPUTS</span></span>

### <span data-ttu-id="42606-134">Microsoft. Azure. Management. COMPUTE. MODELES. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="42606-134">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="42606-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42606-135">NOTES</span></span>

## <span data-ttu-id="42606-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42606-136">RELATED LINKS</span></span>

