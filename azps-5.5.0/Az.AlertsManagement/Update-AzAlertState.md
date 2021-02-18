---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 4ba238f75fa1e39daf2309a1ceda1aed323ff47d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239954"
---
# <span data-ttu-id="2573d-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="2573d-101">Update-AzAlertState</span></span>

## <span data-ttu-id="2573d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2573d-102">SYNOPSIS</span></span>
<span data-ttu-id="2573d-103">Stan alertu aktualizacji</span><span class="sxs-lookup"><span data-stu-id="2573d-103">Updates alert state</span></span>

## <span data-ttu-id="2573d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2573d-104">SYNTAX</span></span>

### <span data-ttu-id="2573d-105">ByAlertId (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="2573d-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2573d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2573d-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2573d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="2573d-107">DESCRIPTION</span></span>
<span data-ttu-id="2573d-108">**Polecenie cmdlet Update-AzAlertState** aktualizuje stan alertu.</span><span class="sxs-lookup"><span data-stu-id="2573d-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="2573d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2573d-109">EXAMPLES</span></span>

### <span data-ttu-id="2573d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2573d-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="2573d-111">To polecenie cmdlet aktualizuje stan alertu na Zamknięty.</span><span class="sxs-lookup"><span data-stu-id="2573d-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="2573d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2573d-112">PARAMETERS</span></span>

### <span data-ttu-id="2573d-113">- AlertId</span><span class="sxs-lookup"><span data-stu-id="2573d-113">-AlertId</span></span>
<span data-ttu-id="2573d-114">Unikatowy identyfikator alertu/identyfikatora zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="2573d-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2573d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2573d-115">-DefaultProfile</span></span>
<span data-ttu-id="2573d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2573d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2573d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2573d-117">-InputObject</span></span>
<span data-ttu-id="2573d-118">Obiekt wejściowy z potoku.</span><span class="sxs-lookup"><span data-stu-id="2573d-118">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2573d-119">— województwo</span><span class="sxs-lookup"><span data-stu-id="2573d-119">-State</span></span>
<span data-ttu-id="2573d-120">Zaktualizowano stan alertu</span><span class="sxs-lookup"><span data-stu-id="2573d-120">Updated Alert State</span></span>

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

### <span data-ttu-id="2573d-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2573d-121">-Confirm</span></span>
<span data-ttu-id="2573d-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2573d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2573d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2573d-123">-WhatIf</span></span>
<span data-ttu-id="2573d-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2573d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2573d-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2573d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2573d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2573d-126">CommonParameters</span></span>
<span data-ttu-id="2573d-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2573d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2573d-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2573d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2573d-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2573d-129">INPUTS</span></span>

### <span data-ttu-id="2573d-130">Brak</span><span class="sxs-lookup"><span data-stu-id="2573d-130">None</span></span>

## <span data-ttu-id="2573d-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2573d-131">OUTPUTS</span></span>

### <span data-ttu-id="2573d-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="2573d-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="2573d-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2573d-133">NOTES</span></span>

## <span data-ttu-id="2573d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2573d-134">RELATED LINKS</span></span>
