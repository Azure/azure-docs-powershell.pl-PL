---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermsnapshotaccess
schema: 2.0.0
ms.openlocfilehash: b1957543c959a18c9fd0fe4fc12de02064ffdcf0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898800"
---
# <span data-ttu-id="fd5be-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="fd5be-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="fd5be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd5be-102">SYNOPSIS</span></span>
<span data-ttu-id="fd5be-103">Udziela dostępu do migawki.</span><span class="sxs-lookup"><span data-stu-id="fd5be-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd5be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd5be-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd5be-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fd5be-105">DESCRIPTION</span></span>
<span data-ttu-id="fd5be-106">Polecenie cmdlet **Grant-AzureRmSnapshotAccess** umożliwia uzyskanie dostępu do migawki.</span><span class="sxs-lookup"><span data-stu-id="fd5be-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="fd5be-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd5be-107">EXAMPLES</span></span>

### <span data-ttu-id="fd5be-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fd5be-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="fd5be-109">Udziel uprawnienia "Odczyt" do migawki o nazwie "Snapshot01" w grupie zasobów o nazwie "ResourceGroup01" przez 60 sekund.</span><span class="sxs-lookup"><span data-stu-id="fd5be-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="fd5be-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd5be-110">PARAMETERS</span></span>

### <span data-ttu-id="fd5be-111">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="fd5be-111">-Access</span></span>
<span data-ttu-id="fd5be-112">Określa poziom dostępu.</span><span class="sxs-lookup"><span data-stu-id="fd5be-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5be-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd5be-113">-AsJob</span></span>
<span data-ttu-id="fd5be-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fd5be-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd5be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd5be-115">-DefaultProfile</span></span>
<span data-ttu-id="fd5be-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd5be-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd5be-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="fd5be-117">-DurationInSecond</span></span>
<span data-ttu-id="fd5be-118">Określa czas trwania dostępu w sekundach.</span><span class="sxs-lookup"><span data-stu-id="fd5be-118">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="fd5be-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd5be-119">-ResourceGroupName</span></span>
<span data-ttu-id="fd5be-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fd5be-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fd5be-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="fd5be-121">-SnapshotName</span></span>
<span data-ttu-id="fd5be-122">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="fd5be-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="fd5be-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd5be-123">-Confirm</span></span>
<span data-ttu-id="fd5be-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd5be-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd5be-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd5be-125">-WhatIf</span></span>
<span data-ttu-id="fd5be-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd5be-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd5be-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fd5be-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd5be-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd5be-128">CommonParameters</span></span>
<span data-ttu-id="fd5be-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd5be-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd5be-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd5be-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd5be-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd5be-131">INPUTS</span></span>

### <span data-ttu-id="fd5be-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fd5be-132">System.String</span></span>

## <span data-ttu-id="fd5be-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd5be-133">OUTPUTS</span></span>

### <span data-ttu-id="fd5be-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="fd5be-134">System.Object</span></span>

## <span data-ttu-id="fd5be-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd5be-135">NOTES</span></span>

## <span data-ttu-id="fd5be-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd5be-136">RELATED LINKS</span></span>

