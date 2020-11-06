---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
ms.openlocfilehash: b88802503247b1e753c9363558df30e57079f897
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552400"
---
# <span data-ttu-id="87d8f-101">Set-AzureRmSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="87d8f-101">Set-AzureRmSnapshotImageReference</span></span>

## <span data-ttu-id="87d8f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="87d8f-103">Ustawia właściwości odwołania obrazu dla obiektu typu migawka.</span><span class="sxs-lookup"><span data-stu-id="87d8f-103">Sets the image reference properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87d8f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87d8f-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87d8f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="87d8f-105">DESCRIPTION</span></span>
<span data-ttu-id="87d8f-106">Polecenie cmdlet **Set-AzureRmSnapshotImageReference** ustawia właściwości odwołania obrazu w obiekcie Snapshot.</span><span class="sxs-lookup"><span data-stu-id="87d8f-106">The **Set-AzureRmSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="87d8f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87d8f-107">EXAMPLES</span></span>

### <span data-ttu-id="87d8f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="87d8f-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzureRmSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="87d8f-109">Pierwsze polecenie tworzy obiekt Local Snapshot ze zdjęciem o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="87d8f-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="87d8f-110">Ustawia również typ systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="87d8f-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="87d8f-111">Drugie polecenie ustawia identyfikator obrazu i numer jednostki logicznej 0 dla obiektu Snapshot.</span><span class="sxs-lookup"><span data-stu-id="87d8f-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="87d8f-112">Ostatnie polecenie przyjmuje obiekt Snapshot i utworzy migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="87d8f-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="87d8f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87d8f-113">PARAMETERS</span></span>

### <span data-ttu-id="87d8f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d8f-114">-DefaultProfile</span></span>
<span data-ttu-id="87d8f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87d8f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87d8f-116">-ID</span><span class="sxs-lookup"><span data-stu-id="87d8f-116">-Id</span></span>
<span data-ttu-id="87d8f-117">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="87d8f-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="87d8f-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="87d8f-118">-Lun</span></span>
<span data-ttu-id="87d8f-119">Określa numer jednostki logicznej (LUN).</span><span class="sxs-lookup"><span data-stu-id="87d8f-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="87d8f-120">-Migawka</span><span class="sxs-lookup"><span data-stu-id="87d8f-120">-Snapshot</span></span>
<span data-ttu-id="87d8f-121">Określa lokalny obiekt migawki.</span><span class="sxs-lookup"><span data-stu-id="87d8f-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87d8f-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87d8f-122">-Confirm</span></span>
<span data-ttu-id="87d8f-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87d8f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87d8f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87d8f-124">-WhatIf</span></span>
<span data-ttu-id="87d8f-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87d8f-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87d8f-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="87d8f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87d8f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d8f-127">CommonParameters</span></span>
<span data-ttu-id="87d8f-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87d8f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d8f-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87d8f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d8f-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87d8f-130">INPUTS</span></span>

### <span data-ttu-id="87d8f-131">Microsoft. Azure. Management. COMPUTE. models. snapshot</span><span class="sxs-lookup"><span data-stu-id="87d8f-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="87d8f-132">System. String. Nullable. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="87d8f-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="87d8f-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87d8f-133">OUTPUTS</span></span>

### <span data-ttu-id="87d8f-134">Microsoft. Azure. Management. COMPUTE. models. snapshot</span><span class="sxs-lookup"><span data-stu-id="87d8f-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="87d8f-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87d8f-135">NOTES</span></span>

## <span data-ttu-id="87d8f-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87d8f-136">RELATED LINKS</span></span>

