---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 5f7e0f26461780b30dbe2b80c79bad8231590e7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015578"
---
# <span data-ttu-id="7420c-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="7420c-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="7420c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7420c-102">SYNOPSIS</span></span>
<span data-ttu-id="7420c-103">Aktualizacja stanu grupy inteligentnej</span><span class="sxs-lookup"><span data-stu-id="7420c-103">Updates smart group state</span></span>

## <span data-ttu-id="7420c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7420c-104">SYNTAX</span></span>

### <span data-ttu-id="7420c-105">BySmartGroupId (domyślna)</span><span class="sxs-lookup"><span data-stu-id="7420c-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7420c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7420c-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7420c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7420c-107">DESCRIPTION</span></span>
<span data-ttu-id="7420c-108">**Polecenie cmdlet Update-AzSmartGroupState** aktualizuje stan grupy inteligentnej.</span><span class="sxs-lookup"><span data-stu-id="7420c-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="7420c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7420c-109">EXAMPLES</span></span>

### <span data-ttu-id="7420c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7420c-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="7420c-111">To polecenie cmdlet aktualizuje stan grupy inteligentnej na Acknowleged.</span><span class="sxs-lookup"><span data-stu-id="7420c-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="7420c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7420c-112">PARAMETERS</span></span>

### <span data-ttu-id="7420c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7420c-113">-DefaultProfile</span></span>
<span data-ttu-id="7420c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7420c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7420c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7420c-115">-InputObject</span></span>
<span data-ttu-id="7420c-116">Obiekt wejściowy z potoku.</span><span class="sxs-lookup"><span data-stu-id="7420c-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7420c-117">- SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="7420c-117">-SmartGroupId</span></span>
<span data-ttu-id="7420c-118">Unikatowy identyfikator grupy inteligentnej/identyfikatora zasobu grupy inteligentnej.</span><span class="sxs-lookup"><span data-stu-id="7420c-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7420c-119">— województwo</span><span class="sxs-lookup"><span data-stu-id="7420c-119">-State</span></span>
<span data-ttu-id="7420c-120">Zaktualizowany stan grupy inteligentnej</span><span class="sxs-lookup"><span data-stu-id="7420c-120">Updated Smart group State</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7420c-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7420c-121">-Confirm</span></span>
<span data-ttu-id="7420c-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7420c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7420c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7420c-123">-WhatIf</span></span>
<span data-ttu-id="7420c-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7420c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7420c-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7420c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7420c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7420c-126">CommonParameters</span></span>
<span data-ttu-id="7420c-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7420c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7420c-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7420c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7420c-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7420c-129">INPUTS</span></span>

### <span data-ttu-id="7420c-130">Brak</span><span class="sxs-lookup"><span data-stu-id="7420c-130">None</span></span>

## <span data-ttu-id="7420c-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7420c-131">OUTPUTS</span></span>

### <span data-ttu-id="7420c-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="7420c-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="7420c-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7420c-133">NOTES</span></span>

## <span data-ttu-id="7420c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7420c-134">RELATED LINKS</span></span>
