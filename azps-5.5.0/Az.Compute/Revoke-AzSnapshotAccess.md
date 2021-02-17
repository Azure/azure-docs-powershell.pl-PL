---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: 35e767c340d5418ae500c4cc87a4b40741d8ba6a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238740"
---
# <span data-ttu-id="9cd2b-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="9cd2b-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="9cd2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cd2b-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd2b-103">Cofa dostęp do migawki.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="9cd2b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9cd2b-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cd2b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9cd2b-105">DESCRIPTION</span></span>
<span data-ttu-id="9cd2b-106">Polecenie cmdlet **Revoke-AzSnapshotAccess** odwołuje dostęp do migawki.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="9cd2b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9cd2b-107">EXAMPLES</span></span>

### <span data-ttu-id="9cd2b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9cd2b-108">Example 1</span></span>
```
PS C:\> Revoke-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="9cd2b-109">Odwoływanie dostępu do migawki o nazwie "Migawka01" w grupie zasobów o nazwie "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="9cd2b-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="9cd2b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cd2b-110">PARAMETERS</span></span>

### <span data-ttu-id="9cd2b-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9cd2b-111">-AsJob</span></span>
<span data-ttu-id="9cd2b-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9cd2b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9cd2b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cd2b-113">-DefaultProfile</span></span>
<span data-ttu-id="9cd2b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cd2b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cd2b-115">-ResourceGroupName</span></span>
<span data-ttu-id="9cd2b-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9cd2b-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="9cd2b-117">-SnapshotName</span></span>
<span data-ttu-id="9cd2b-118">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="9cd2b-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9cd2b-119">-Confirm</span></span>
<span data-ttu-id="9cd2b-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cd2b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cd2b-121">-WhatIf</span></span>
<span data-ttu-id="9cd2b-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9cd2b-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cd2b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd2b-124">CommonParameters</span></span>
<span data-ttu-id="9cd2b-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cd2b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd2b-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9cd2b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd2b-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cd2b-127">INPUTS</span></span>

### <span data-ttu-id="9cd2b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9cd2b-128">System.String</span></span>

## <span data-ttu-id="9cd2b-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cd2b-129">OUTPUTS</span></span>

### <span data-ttu-id="9cd2b-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="9cd2b-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="9cd2b-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9cd2b-131">NOTES</span></span>

## <span data-ttu-id="9cd2b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cd2b-132">RELATED LINKS</span></span>
