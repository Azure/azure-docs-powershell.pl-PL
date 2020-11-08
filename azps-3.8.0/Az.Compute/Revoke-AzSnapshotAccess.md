---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: 35e767c340d5418ae500c4cc87a4b40741d8ba6a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051058"
---
# <span data-ttu-id="b5b46-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="b5b46-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="b5b46-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5b46-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b46-103">Odwołuje dostęp do migawki.</span><span class="sxs-lookup"><span data-stu-id="b5b46-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="b5b46-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5b46-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5b46-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b5b46-105">DESCRIPTION</span></span>
<span data-ttu-id="b5b46-106">Polecenie cmdlet **REVOKE-AzSnapshotAccess** odwołuje dostęp do migawki.</span><span class="sxs-lookup"><span data-stu-id="b5b46-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="b5b46-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5b46-107">EXAMPLES</span></span>

### <span data-ttu-id="b5b46-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b5b46-108">Example 1</span></span>
```
PS C:\> Revoke-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="b5b46-109">Odwoływanie dostępu do migawki o nazwie "Snapshot01" w grupie zasobów o nazwie "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="b5b46-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="b5b46-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5b46-110">PARAMETERS</span></span>

### <span data-ttu-id="b5b46-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5b46-111">-AsJob</span></span>
<span data-ttu-id="b5b46-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b5b46-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5b46-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b46-113">-DefaultProfile</span></span>
<span data-ttu-id="b5b46-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5b46-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5b46-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5b46-115">-ResourceGroupName</span></span>
<span data-ttu-id="b5b46-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b5b46-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b5b46-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="b5b46-117">-SnapshotName</span></span>
<span data-ttu-id="b5b46-118">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="b5b46-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="b5b46-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b5b46-119">-Confirm</span></span>
<span data-ttu-id="b5b46-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b46-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5b46-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5b46-121">-WhatIf</span></span>
<span data-ttu-id="b5b46-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b46-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5b46-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b5b46-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5b46-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b46-124">CommonParameters</span></span>
<span data-ttu-id="b5b46-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5b46-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b46-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5b46-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b46-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5b46-127">INPUTS</span></span>

### <span data-ttu-id="b5b46-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b5b46-128">System.String</span></span>

## <span data-ttu-id="b5b46-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5b46-129">OUTPUTS</span></span>

### <span data-ttu-id="b5b46-130">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b5b46-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b5b46-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5b46-131">NOTES</span></span>

## <span data-ttu-id="b5b46-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5b46-132">RELATED LINKS</span></span>
