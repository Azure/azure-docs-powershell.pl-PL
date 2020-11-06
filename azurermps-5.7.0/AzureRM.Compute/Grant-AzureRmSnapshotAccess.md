---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
ms.openlocfilehash: 8f68957020d8e4607477bd78cc42b05c29e321c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525325"
---
# <span data-ttu-id="c1b8c-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="c1b8c-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="c1b8c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c1b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b8c-103">Udziela dostępu do migawki.</span><span class="sxs-lookup"><span data-stu-id="c1b8c-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1b8c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c1b8c-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1b8c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c1b8c-105">DESCRIPTION</span></span>
<span data-ttu-id="c1b8c-106">Polecenie cmdlet **Grant-AzureRmSnapshotAccess** umożliwia uzyskanie dostępu do migawki.</span><span class="sxs-lookup"><span data-stu-id="c1b8c-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="c1b8c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c1b8c-107">EXAMPLES</span></span>

### <span data-ttu-id="c1b8c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c1b8c-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="c1b8c-109">Udziel uprawnienia "Odczyt" do migawki o nazwie "Snapshot01" w grupie zasobów o nazwie "ResourceGroup01" przez 60 sekund.</span><span class="sxs-lookup"><span data-stu-id="c1b8c-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="c1b8c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c1b8c-110">PARAMETERS</span></span>

### <span data-ttu-id="c1b8c-111">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="c1b8c-111">-Access</span></span>
<span data-ttu-id="c1b8c-112">Określa poziom dostępu.</span><span class="sxs-lookup"><span data-stu-id="c1b8c-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b8c-113">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="c1b8c-113">-DurationInSecond</span></span>
<span data-ttu-id="c1b8c-114">Określa czas trwania dostępu w sekundach.</span><span class="sxs-lookup"><span data-stu-id="c1b8c-114">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b8c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1b8c-115">-ResourceGroupName</span></span>
<span data-ttu-id="c1b8c-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c1b8c-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c1b8c-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="c1b8c-117">-SnapshotName</span></span>
<span data-ttu-id="c1b8c-118">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="c1b8c-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="c1b8c-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c1b8c-119">-Confirm</span></span>
<span data-ttu-id="c1b8c-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1b8c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1b8c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1b8c-121">-WhatIf</span></span>
<span data-ttu-id="c1b8c-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1b8c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1b8c-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c1b8c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1b8c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b8c-124">CommonParameters</span></span>
<span data-ttu-id="c1b8c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1b8c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b8c-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1b8c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b8c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1b8c-127">INPUTS</span></span>

### <span data-ttu-id="c1b8c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c1b8c-128">System.String</span></span>

## <span data-ttu-id="c1b8c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c1b8c-129">OUTPUTS</span></span>

### <span data-ttu-id="c1b8c-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="c1b8c-130">System.Object</span></span>

## <span data-ttu-id="c1b8c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c1b8c-131">NOTES</span></span>

## <span data-ttu-id="c1b8c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1b8c-132">RELATED LINKS</span></span>

