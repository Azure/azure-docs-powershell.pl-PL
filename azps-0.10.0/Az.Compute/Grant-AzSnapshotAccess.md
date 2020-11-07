---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: e4283b23fb4a82c17f35354d854c30c3ec1b2329
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893674"
---
# <span data-ttu-id="696c5-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="696c5-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="696c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="696c5-102">SYNOPSIS</span></span>
<span data-ttu-id="696c5-103">Udziela dostępu do migawki.</span><span class="sxs-lookup"><span data-stu-id="696c5-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="696c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="696c5-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="696c5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="696c5-105">DESCRIPTION</span></span>
<span data-ttu-id="696c5-106">Polecenie cmdlet **Grant-AzSnapshotAccess** umożliwia uzyskanie dostępu do migawki.</span><span class="sxs-lookup"><span data-stu-id="696c5-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="696c5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="696c5-107">EXAMPLES</span></span>

### <span data-ttu-id="696c5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="696c5-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="696c5-109">Udziel uprawnienia "Odczyt" do migawki o nazwie "Snapshot01" w grupie zasobów o nazwie "ResourceGroup01" przez 60 sekund.</span><span class="sxs-lookup"><span data-stu-id="696c5-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="696c5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="696c5-110">PARAMETERS</span></span>

### <span data-ttu-id="696c5-111">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="696c5-111">-Access</span></span>
<span data-ttu-id="696c5-112">Określa poziom dostępu.</span><span class="sxs-lookup"><span data-stu-id="696c5-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="696c5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="696c5-113">-AsJob</span></span>
<span data-ttu-id="696c5-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="696c5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="696c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="696c5-115">-DefaultProfile</span></span>
<span data-ttu-id="696c5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="696c5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="696c5-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="696c5-117">-DurationInSecond</span></span>
<span data-ttu-id="696c5-118">Określa czas trwania dostępu w sekundach.</span><span class="sxs-lookup"><span data-stu-id="696c5-118">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="696c5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="696c5-119">-ResourceGroupName</span></span>
<span data-ttu-id="696c5-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="696c5-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="696c5-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="696c5-121">-SnapshotName</span></span>
<span data-ttu-id="696c5-122">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="696c5-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="696c5-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="696c5-123">-Confirm</span></span>
<span data-ttu-id="696c5-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="696c5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="696c5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="696c5-125">-WhatIf</span></span>
<span data-ttu-id="696c5-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="696c5-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="696c5-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="696c5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="696c5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696c5-128">CommonParameters</span></span>
<span data-ttu-id="696c5-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="696c5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696c5-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="696c5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696c5-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="696c5-131">INPUTS</span></span>

### <span data-ttu-id="696c5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="696c5-132">System.String</span></span>

## <span data-ttu-id="696c5-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="696c5-133">OUTPUTS</span></span>

### <span data-ttu-id="696c5-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="696c5-134">System.Object</span></span>

## <span data-ttu-id="696c5-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="696c5-135">NOTES</span></span>

## <span data-ttu-id="696c5-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="696c5-136">RELATED LINKS</span></span>

