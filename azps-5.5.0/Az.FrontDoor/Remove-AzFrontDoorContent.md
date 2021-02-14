---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: b7b01ec1b301741c07a0667931a63287cc503434
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237809"
---
# <span data-ttu-id="7bcba-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="7bcba-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="7bcba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bcba-102">SYNOPSIS</span></span>
<span data-ttu-id="7bcba-103">Usuwanie zawartości z drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="7bcba-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="7bcba-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7bcba-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bcba-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7bcba-105">DESCRIPTION</span></span>
<span data-ttu-id="7bcba-106">Remove-AzFrontDoorContent zawartości przechowywanej w pamięci podręcznej w drzwiach frontowych</span><span class="sxs-lookup"><span data-stu-id="7bcba-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="7bcba-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7bcba-107">EXAMPLES</span></span>

### <span data-ttu-id="7bcba-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7bcba-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="7bcba-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bcba-109">PARAMETERS</span></span>

### <span data-ttu-id="7bcba-110">— ContentPath</span><span class="sxs-lookup"><span data-stu-id="7bcba-110">-ContentPath</span></span>
<span data-ttu-id="7bcba-111">Ścieżki do zawartości do przeczyszczania.</span><span class="sxs-lookup"><span data-stu-id="7bcba-111">The paths to the content to be purged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bcba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bcba-112">-DefaultProfile</span></span>
<span data-ttu-id="7bcba-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7bcba-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bcba-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7bcba-114">-Name</span></span>
<span data-ttu-id="7bcba-115">Nazwa drzwi przednich.</span><span class="sxs-lookup"><span data-stu-id="7bcba-115">Front Door name.</span></span>

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

### <span data-ttu-id="7bcba-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bcba-116">-PassThru</span></span>
<span data-ttu-id="7bcba-117">Zwracany obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="7bcba-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="7bcba-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bcba-118">-ResourceGroupName</span></span>
<span data-ttu-id="7bcba-119">Nazwa grupy zasobów drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="7bcba-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="7bcba-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7bcba-120">-Confirm</span></span>
<span data-ttu-id="7bcba-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7bcba-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bcba-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bcba-122">-WhatIf</span></span>
<span data-ttu-id="7bcba-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bcba-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bcba-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7bcba-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bcba-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bcba-125">CommonParameters</span></span>
<span data-ttu-id="7bcba-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bcba-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bcba-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bcba-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bcba-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7bcba-128">INPUTS</span></span>

### <span data-ttu-id="7bcba-129">Brak</span><span class="sxs-lookup"><span data-stu-id="7bcba-129">None</span></span>

## <span data-ttu-id="7bcba-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7bcba-130">OUTPUTS</span></span>

### <span data-ttu-id="7bcba-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7bcba-131">System.Boolean</span></span>

## <span data-ttu-id="7bcba-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7bcba-132">NOTES</span></span>

## <span data-ttu-id="7bcba-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7bcba-133">RELATED LINKS</span></span>
