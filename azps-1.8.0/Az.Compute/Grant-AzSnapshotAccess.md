---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: 85954c0364ef264e24d045b50526345e444b2b39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710292"
---
# <span data-ttu-id="0c9f2-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="0c9f2-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="0c9f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c9f2-102">SYNOPSIS</span></span>
<span data-ttu-id="0c9f2-103">Udziela dostępu do migawki.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="0c9f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c9f2-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c9f2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0c9f2-105">DESCRIPTION</span></span>
<span data-ttu-id="0c9f2-106">Polecenie cmdlet **Grant-AzSnapshotAccess** umożliwia uzyskanie dostępu do migawki.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="0c9f2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c9f2-107">EXAMPLES</span></span>

### <span data-ttu-id="0c9f2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0c9f2-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="0c9f2-109">Udziel uprawnienia "Odczyt" do migawki o nazwie "Snapshot01" w grupie zasobów o nazwie "ResourceGroup01" przez 60 sekund.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="0c9f2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c9f2-110">PARAMETERS</span></span>

### <span data-ttu-id="0c9f2-111">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="0c9f2-111">-Access</span></span>
<span data-ttu-id="0c9f2-112">Określa poziom dostępu.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c9f2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c9f2-113">-AsJob</span></span>
<span data-ttu-id="0c9f2-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0c9f2-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c9f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c9f2-115">-DefaultProfile</span></span>
<span data-ttu-id="0c9f2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c9f2-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="0c9f2-117">-DurationInSecond</span></span>
<span data-ttu-id="0c9f2-118">Określa czas trwania dostępu w sekundach.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c9f2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c9f2-119">-ResourceGroupName</span></span>
<span data-ttu-id="0c9f2-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c9f2-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="0c9f2-121">-SnapshotName</span></span>
<span data-ttu-id="0c9f2-122">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-122">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c9f2-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c9f2-123">-Confirm</span></span>
<span data-ttu-id="0c9f2-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c9f2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c9f2-125">-WhatIf</span></span>
<span data-ttu-id="0c9f2-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c9f2-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c9f2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c9f2-128">CommonParameters</span></span>
<span data-ttu-id="0c9f2-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c9f2-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c9f2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c9f2-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c9f2-131">INPUTS</span></span>

### <span data-ttu-id="0c9f2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0c9f2-132">System.String</span></span>

## <span data-ttu-id="0c9f2-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c9f2-133">OUTPUTS</span></span>

### <span data-ttu-id="0c9f2-134">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="0c9f2-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="0c9f2-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c9f2-135">NOTES</span></span>

## <span data-ttu-id="0c9f2-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c9f2-136">RELATED LINKS</span></span>
